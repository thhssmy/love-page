<template>
    <header>
      <div class="navbar bg-base-100">
        <div class="flex-1">
          <a class="btn btn-ghost text-xl">💗SENİ ÇOK SEVİYORUM SEWGİLİM💗</a>
        </div>
      </div>
  
      <div class="flex flex-col md:flex-row">
        <!-- First Card -->
        <div class="card w-full md:w-96 bg-primary text-primary-content mb-4 md:mr-4">
          <div class="card-body">
            <h2 class="card-title">Seni nekadar sevdiğimi öğren;</h2>
            <input @change="(event) => {this.sayiSevgiVeri = event.target.value}" type="text" placeholder="Beni nekadar seviyorsun bir sayı yaz" class="input input-bordered w-full max-w-xs text-black" />
            <div class="card-actions justify-end">
              <button class="btn" @click="() => {this.sevgiOgrenClicked = true;}">Öğren</button>
            </div>
            <div role="alert" class="alert alert-success" v-if="sevgiOgrenClicked">
              <svg xmlns="http://www.w3.org/2000/svg" class="stroke-current shrink-0 h-6 w-6" fill="none" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>
              <span>Ben seni {{ sayiSevgiVeri }} + 9999999 kez seviyorum yani senden daha çok. Aslında sonsuz kez sewiyorum ama kudur diye senden çok yaptım :D</span>
            </div>
          </div>
        </div>
  
        <!-- Second Card -->
        <div class="card w-full md:w-96 bg-primary text-primary-content">
          <div class="card-body">
            <h2 class="card-title">Senden önce ve seninleyken;</h2>
            <div class="carousel w-full">
              <div id="slide1" class="carousel-item relative w-full">
                <img src="/images/sad-spongebob.jpg"  class="w-full" />
                <div class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2">
                  <a href="#slide2" class="btn btn-circle">❮</a> 
                  <a href="#slide2" class="btn btn-circle">❯</a>
                </div>
              </div> 
              <div id="slide2" class="carousel-item relative w-full">
                <img src="/images/happy-spongebob.jpg"  class="w-full" />
                <div class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2">
                  <a href="#slide1" class="btn btn-circle">❮</a> 
                  <a href="#slide1" class="btn btn-circle">❯</a>
                </div>
              </div> 
            </div>
          </div>
        </div>
      </div>
    </header>
  </template>
  
  <script>
  export default {
    data() {
      return {
        sevgiOgrenClicked: false,
        sayiSevgiVeri: 0 // You can set the initial value as needed
      };
    }
  };
  </script>
  
  <style>
  </style>
  