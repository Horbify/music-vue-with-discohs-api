<template>
  <div id="body">
    <div id="mobile-body">
      <div id="mobile-header" style="padding-top: 15px; font-size: 12px">
        <h2
          class="text-center text-white"
          style="font-family: Aclonica, sans-serif"
        >
          MUSIC
        </h2>
      </div>
      <p class="text-white">
        Want lastest music, you can now find your favorite musicians and stay up
        to date with their latest songs here.
      </p>
      <div class="row">
        <div class="col-md-10 offset-md-1">
          <div class="card m-auto" style="max-width: 850px">
            <div class="card-body" style="padding: 0px">
              <form @submit.prevent="submit" class="d-flex align-items-center">
                <i class="fas fa-search d-none d-sm-block h4 text-body m-0"></i
                ><input
                  class="form-control flex-shrink-1 form-control-borderless"
                  type="search"
                  placeholder="Search for songs..."
                  name="searchbar"
                  v-model="searchValue"
                  required=""
                /><button class="btn btn-success" type="submit">Search</button>
              </form>
            </div>
          </div>
        </div>
      </div>
      <div class="section">
        <div id="category" style="padding-top: 20px">
          <h4
            class="text-left text-white"
            id="category-header"
            style="font-family: Aclonica, sans-serif"
          >
            New release
          </h4>
          <span><i class="fas fa-fire"></i></span>
        </div>
        <!-- <div id="chips" class="chips">
          <span
            class="badge badge-pill badge-primary shadow chip-item"
            id="chip-item"
            style="font-size: 15px; background-color: #383a3d"
            >Hello&nbsp;<i
              class="icon ion-close-round"
              style="font-size: 13px; font-weight: 100"
            ></i></span
          ><span
            class="badge badge-pill badge-primary shadow chip-item"
            id="chip-item-3"
            style="font-size: 15px; background-color: #383a3d"
            >Hello&nbsp;<i
              class="icon ion-close-round"
              style="font-size: 13px; font-weight: 100"
            ></i></span
          >
        </div> -->
        <div id="category-item" class="category-item" v-for="(item, i) in result" :key="i">
          <div class="card item-card">
            <div
              class="card-body"
              style="
                padding-top: 0px;
                padding-right: 0px;
                padding-bottom: 0px;
                padding-left: 0px;
              "
            >
              <div
                class="row no-gutters row-cols-3"
                style="margin-right: 0px; margin-left: 0px"
              >
                <div class="col-3 card-image">
                  <img
                    class="rounded img-fluid"
                    :src="item.images.background"
                    width="60px"
                  />
                </div>
                <div class="col-7">
                  <div class="card-title"></div>
                  <h1
                    style="color: #ffffff; font-size: 18px; padding-top: 15px"
                  >
                    {{item.title}}
                  </h1>
                  <p
                    class="card-subtitle-artist"
                    style="color: #e1e7eb; font-size: 13px; margin-top: -6px"
                  >
                    {{item.subtitle}}
                  </p>
                </div>
                <div class="col-2">
                  <div class="text-center" style="padding-top: 50%"></div>
                  <a :href="item.url">
                                    <i
                    class="fas fa-location-arrow"
                    style="color: #ffffff; font-size: 20px; padding-left: 16px"
                  ></i>
                  </a>

                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="section">
        <div id="category" style="padding-top: 20px">
          <h4
            class="text-left text-white"
            id="category-header"
            style="font-family: Aclonica, sans-serif"
          >
            Top Generes
          </h4>
          <span><i class="fas fa-fire"></i></span>
        </div>
        <!-- <div id="chips" class="chips">
          <span
            class="badge badge-pill badge-primary shadow chip-item"
            id="chip-item"
            style="font-size: 15px; background-color: #383a3d"
            >Hello&nbsp;<i
              class="icon ion-close-round"
              style="font-size: 13px; font-weight: 100"
            ></i></span
          ><span
            class="badge badge-pill badge-primary shadow chip-item"
            id="chip-item-3"
            style="font-size: 15px; background-color: #383a3d"
            >Hello&nbsp;<i
              class="icon ion-close-round"
              style="font-size: 13px; font-weight: 100"
            ></i></span
          >
        </div> -->
        <div id="category-item" class="category-item" v-for="(item, i) in generes" :key="i">
          <div class="card item-card">
            <div
              class="card-body"
              style="
                padding-top: 0px;
                padding-right: 0px;
                padding-bottom: 0px;
                padding-left: 0px;
              "
            >
              <div
                class="row no-gutters row-cols-3"
                style="margin-right: 0px; margin-left: 0px"
              >
                <div class="col-3 card-image">
                  <img
                    class="rounded img-fluid"
                    :src="require('@/assets/avatar.png')"
                    width="60px"
                  />
                </div>
                <div class="col-7">
                  <div class="card-title"></div>
                  <h1
                    style="color: #ffffff; font-size: 18px; padding-top: 15px"
                  >
                    {{item.name}}
                  </h1>
                  <p
                    class="card-subtitle-artist"
                    style="color: #e1e7eb; font-size: 13px; margin-top: -6px"
                  >
                    Snarky Puppy
                  </p>
                </div>
                <div class="col-2">
                  <div class="text-center" style="padding-top: 50%"></div>
                  <i
                    class="fas fa-location-arrow"
                    style="color: #ffffff; font-size: 20px; padding-left: 16px"
                  ></i>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  async fetch() {
    let params = new URLSearchParams();
    params.append("pageSize", "5");
    params.append("startFrom", "0");
    params.append("locale", "en-US");
    let { data } = await this.$axios.get("https://shazam.p.rapidapi.com/charts/track", {
      headers: {
        "x-rapidapi-key": "80cae7e366msh3612a2d667aac92p16071djsn90096a385475",
        "x-rapidapi-host": "shazam.p.rapidapi.com",
        useQueryString: true,
      },
      params: params,
    });

    let result = await this.$axios.get("https://shazam.p.rapidapi.com/charts/list", {
      headers: {
        "x-rapidapi-key": "80cae7e366msh3612a2d667aac92p16071djsn90096a385475",
        "x-rapidapi-host": "shazam.p.rapidapi.com",
        useQueryString: true,
      }
    });
    let ok = result.data.global.genres.slice(0, 4)
    this.generes = ok

    this.result = data.tracks
  },
  data() {
    return {
      searchValue: "",
      result: [],
      generes: []
    };
  },
  methods: {
    async submit() {
      let params = new URLSearchParams();
      params.append("term", `${this.searchValue}`);
      params.append("offset", "0");
      params.append("locale", "en-US");
      let { data } = this.$axios.get("https://shazam.p.rapidapi.com/search", {
        headers: {
          "x-rapidapi-key":
            "80cae7e366msh3612a2d667aac92p16071djsn90096a385475",
          "x-rapidapi-host": "shazam.p.rapidapi.com",
          useQueryString: true,
        },
        params: params,
      });
      console.log(data);
    },
  },
};
</script>

<style>

#body {
  background-color: #211f1f;
  padding: 15px;
}

#mobile-header {
  height: 10vh;
}

#category {
  display: flex;
}

#category-header {
  flex-grow: 1;
}

.fas.fa-fire {
  color: #E25822;
  font-size: 25px;
}

#chips {
  overflow-x: scroll;
  overflow-y: hidden;
  white-space: nowrap;
}

chip-item {
  margin-right: 10px;
  display: inline-block;
}

#chips::-webkit-scrollbar {
  display: hidden;
}

.chips::-webkit-scrollbar {
  display: grid;
}

.badge.badge-primary {
  padding-right: 6px;
}

.chip-item {
  margin-right: 10px;
}

.card-body{
    padding: 0px;
}

.card.item-card {
  background-color: #383a3d;
  height: 80px;
}

.col {
  max-height: 80px;
}

.col-3.card-image {
  padding: 10px;
}


.category-item {
  margin-top: 10px;
}

.section {
  margin-top: 20px;
}



</style>
