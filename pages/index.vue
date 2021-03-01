<template>
  <div id="body">
        <div id="mobile-body">
            <div id="mobile-header" style="padding-top: 15px;font-size: 12px;">
                <h2 class="text-center text-white" style="font-family: Aclonica, sans-serif;">MUSIC</h2>
            </div>
            <p class="text-white">Want lastest music, you can now find your favorite musicians and stay up to date with their latest songs here.</p>
            <div class="row">
                <div class="col-md-10 offset-md-1">
                    <div class="card m-auto" style="max-width:850px">
                        <div class="card-body" style="padding: 0px;">
                            <form @submit.prevent="submit" class="d-flex align-items-center"><i class="fas fa-search d-none d-sm-block h4 text-body m-0"></i><input class="form-control flex-shrink-1 form-control-borderless" type="search" placeholder="Search for songs..." name="searchbar" required=""><button class="btn btn-success"
                                    type="submit">Search</button></form>
                        </div>
                    </div>
                </div>
            </div>
            <div class="section">
                <div id="category" style="padding-top: 20px;">
                    <h4 class="text-left text-white" id="category-header" style="font-family: Aclonica, sans-serif;">New release</h4><span><i class="fas fa-fire"></i></span></div>
                <div id="chips" class="chips"><span class="badge badge-pill badge-primary shadow chip-item" id="chip-item" style="font-size: 15px;background-color: #383a3d;">Hello&nbsp;<i class="icon ion-close-round" style="font-size: 13px;font-weight: 100;"></i></span><span class="badge badge-pill badge-primary shadow chip-item"
                        id="chip-item-3" style="font-size: 15px;background-color: #383a3d;">Hello&nbsp;<i class="icon ion-close-round" style="font-size: 13px;font-weight: 100;"></i></span><span class="badge badge-pill badge-primary shadow chip-item" id="chip-item-2"
                        style="font-size: 15px;background-color: #383a3d;">Hello&nbsp;<i class="icon ion-close-round" style="font-size: 13px;font-weight: 100;"></i></span><span class="badge badge-pill badge-primary shadow chip-item" id="chip-item-1" style="font-size: 15px;background-color: #383a3d;">Hello&nbsp;<i class="icon ion-close-round" style="font-size: 13px;font-weight: 100;"></i></span></div>
                <div
                    id="category-item" class="category-item">
                    <div class="card item-card">
                        <div class="card-body" style="padding-top: 0px;padding-right: 0px;padding-bottom: 0px;padding-left: 0px;">
                            <div class="row no-gutters row-cols-3" style="margin-right: 0px;margin-left: 0px;">
                                <div class="col-3 card-image"><img class="rounded img-fluid" :src="require('@/assets/avatar.png')" width="60px"></div>
                                <div class="col-7">
                                    <div class="card-title"></div>
                                    <h1 style="color: #ffffff;font-size: 18px;padding-top: 15px;">Lingus</h1>
                                    <p class="card-subtitle-artist" style="color: #e1e7eb;font-size: 13px;margin-top: -6px;">Snarky Puppy</p>
                                </div>
                                <div class="col-2">
                                    <div class="text-center" style="padding-top: 50%;"></div><i class="fas fa-location-arrow" style="color: #ffffff;font-size: 20px;padding-left: 16px;"></i></div>
                            </div>
                        </div>
                    </div>
            </div>
            <div id="category-item-2" class="category-item">
                <div class="card item-card">
                    <div class="card-body" style="padding-top: 0px;padding-right: 0px;padding-bottom: 0px;padding-left: 0px;">
                        <div class="row no-gutters row-cols-3" style="margin-right: 0px;margin-left: 0px;">
                            <div class="col-3 card-image"><img class="rounded img-fluid" :src="require('@/assets/avatar.png')" width="60px"></div>
                            <div class="col-7">
                                <div class="card-title"></div>
                                <h1 style="color: #ffffff;font-size: 18px;padding-top: 15px;">Lingus</h1>
                                <p class="card-subtitle-artist" style="color: #e1e7eb;font-size: 13px;margin-top: -6px;">Snarky Puppy</p>
                            </div>
                            <div class="col-2">
                                <div class="text-center" style="padding-top: 50%;"></div><i class="fas fa-location-arrow" style="color: #ffffff;font-size: 20px;padding-left: 16px;"></i></div>
                        </div>
                    </div>
                </div>
            </div>
            <div id="category-item-1" class="category-item">
                <div class="card item-card">
                    <div class="card-body" style="padding-top: 0px;padding-right: 0px;padding-bottom: 0px;padding-left: 0px;">
                        <div class="row no-gutters row-cols-3" style="margin-right: 0px;margin-left: 0px;">
                            <div class="col-3 card-image"><img class="rounded img-fluid" :src="require('@/assets/avatar.png')" width="60px"></div>
                            <div class="col-7">
                                <div class="card-title"></div>
                                <h1 style="color: #ffffff;font-size: 18px;padding-top: 15px;">Lingus</h1>
                                <p class="card-subtitle-artist" style="color: #e1e7eb;font-size: 13px;margin-top: -6px;">Snarky Puppy</p>
                            </div>
                            <div class="col-2">
                                <div class="text-center" style="padding-top: 50%;"></div><i class="fas fa-location-arrow" style="color: #ffffff;font-size: 20px;padding-left: 16px;"></i></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="section">
            <div id="category" style="padding-top: 20px;">
                <h4 class="text-left text-white" id="category-header" style="font-family: Aclonica, sans-serif;">Top Albums</h4><span><i class="fas fa-fire"></i></span></div>
            <div id="chips" class="chips"><span class="badge badge-pill badge-primary shadow chip-item" id="chip-item" style="font-size: 15px;background-color: #383a3d;">Hello&nbsp;<i class="icon ion-close-round" style="font-size: 13px;font-weight: 100;"></i></span><span class="badge badge-pill badge-primary shadow chip-item"
                    id="chip-item-3" style="font-size: 15px;background-color: #383a3d;">Hello&nbsp;<i class="icon ion-close-round" style="font-size: 13px;font-weight: 100;"></i></span><span class="badge badge-pill badge-primary shadow chip-item" id="chip-item-2"
                    style="font-size: 15px;background-color: #383a3d;">Hello&nbsp;<i class="icon ion-close-round" style="font-size: 13px;font-weight: 100;"></i></span><span class="badge badge-pill badge-primary shadow chip-item" id="chip-item-1" style="font-size: 15px;background-color: #383a3d;">Hello&nbsp;<i class="icon ion-close-round" style="font-size: 13px;font-weight: 100;"></i></span></div>
            <div
                id="category-item" class="category-item">
                <div class="card item-card">
                    <div class="card-body" style="padding-top: 0px;padding-right: 0px;padding-bottom: 0px;padding-left: 0px;">
                        <div class="row no-gutters row-cols-3" style="margin-right: 0px;margin-left: 0px;">
                            <div class="col-3 card-image"><img class="rounded img-fluid" :src="require('@/assets/avatar.png')" width="60px"></div>
                            <div class="col-7">
                                <div class="card-title"></div>
                                <h1 style="color: #ffffff;font-size: 18px;padding-top: 15px;">Lingus</h1>
                                <p class="card-subtitle-artist" style="color: #e1e7eb;font-size: 13px;margin-top: -6px;">Snarky Puppy</p>
                            </div>
                            <div class="col-2">
                                <div class="text-center" style="padding-top: 50%;"></div><i class="fas fa-location-arrow" style="color: #ffffff;font-size: 20px;padding-left: 16px;"></i></div>
                        </div>
                    </div>
                </div>
        </div>
        <div id="category-item-2" class="category-item">
            <div class="card item-card">
                <div class="card-body" style="padding-top: 0px;padding-right: 0px;padding-bottom: 0px;padding-left: 0px;">
                    <div class="row no-gutters row-cols-3" style="margin-right: 0px;margin-left: 0px;">
                        <div class="col-3 card-image"><img class="rounded img-fluid" :src="require('@/assets/avatar.png')" width="60px"></div>
                        <div class="col-7">
                            <div class="card-title"></div>
                            <h1 style="color: #ffffff;font-size: 18px;padding-top: 15px;">Lingus</h1>
                            <p class="card-subtitle-artist" style="color: #e1e7eb;font-size: 13px;margin-top: -6px;">Snarky Puppy</p>
                        </div>
                        <div class="col-2">
                            <div class="text-center" style="padding-top: 50%;"></div><i class="fas fa-location-arrow" style="color: #ffffff;font-size: 20px;padding-left: 16px;"></i></div>
                    </div>
                </div>
            </div>
        </div>
        <div id="category-item-1" class="category-item">
            <div class="card item-card">
                <div class="card-body" style="padding-top: 0px;padding-right: 0px;padding-bottom: 0px;padding-left: 0px;">
                    <div class="row no-gutters row-cols-3" style="margin-right: 0px;margin-left: 0px;">
                        <div class="col-3 card-image"><img class="rounded img-fluid" :src="require('@/assets/avatar.png')" width="60px"></div>
                        <div class="col-7">
                            <div class="card-title"></div>
                            <h1 style="color: #ffffff;font-size: 18px;padding-top: 15px;">Lingus</h1>
                            <p class="card-subtitle-artist" style="color: #e1e7eb;font-size: 13px;margin-top: -6px;">Snarky Puppy</p>
                        </div>
                        <div class="col-2">
                            <div class="text-center" style="padding-top: 50%;"></div><i class="fas fa-location-arrow" style="color: #ffffff;font-size: 20px;padding-left: 16px;"></i></div>
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
methods: {
  async submit(){
    let {data} = this.$axios.get("https://api.discogs.com/database/search?artist=Eminem", {
      headers: {
        'Authorization': "Discogs key=pVgcPLxEMfaZLZrnrFzK, secret=QsPkJunoMtkOBcIfEsAWYsvqbVsDBKAB"
      }
    })
    console.log(data)
  }
}
}
</script>

<style>

</style>
