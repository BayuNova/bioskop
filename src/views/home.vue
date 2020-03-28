<template>
<div id="home">
    <div class="container">
            <div class="row row-cols-4">
            <div class="col" v-for="(data, index) in movies" :key="index">
                <div class="image-area">
                    <img :src="data.image" class="image">
                </div>
                <div class="content-area">
                    <h4>{{ data.title}} ({{data.release}})</h4>
                    <span class="badge badge-pill badge-success margin-pill">{{ data.duration }}</span>
                    <p class="font-text">Dircted by : <b>{{ data.director }}</b></p>
                </div>
                <div class="button-area">
                    <button class="btn btn-info" @click="goToDetail(data.id)">Info</button>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      title: 'Home',
      movies: [
        {
          title: 'One Piece Stampade',
          image: require('../assets/3.jpg'),
          duration: '113 min',
          director: 'Samehada',
          release: 2019,
          desc: 'Mengisahkan Kelompok Topi Jerami yang diundang untuk hadir pada acara Pirates Expo. Semua bajak laut terhebat datang pada acara itu. Tentu Luffy sangat bersemangat untuk datang. Acara berlangsung meriah. Banyak makanan, permainan, dan pertunjukan. Semua orang tampak bersenang-senang. Namun, tiba-tiba tentara angkatan laut ikut campur dalam acara tersebut. Keadaan juga semakin tidak jelas saat Usopp terluka oleh seseorang. Kini Luffy dan anggota bajak lautnya mulai waspada dan mencari tahu yang sebenarnya terjadi. Keadaan awal yang tadinya aman, bukan tidak mungkin menjadi berantakan dan juga berbahaya.',
          id: 1
        },
        {
          title: 'City Hunter',
          image: require('../assets/1.jpg'),
          duration: '130 min',
          director: 'Anime Indo',
          release: 2019,
          desc: 'Film baru yang ber-setting di Shinjuku pada masa kini. Ryo Saeba, seorang sniper dan private eye (“sweeper“) yang bermarkas di Shinjuku Ward Tokyo dengan keahlian menembak yang tak tertandingi dan obsesi berlebihan untuk lawan jenis. Dia memberi jasa sebagai pengawal dan tugas lain untuk kliennya.',
          id: 2
        },
        {
          title: 'Doraemon the Movie ',
          image: require('../assets/2.jpg'),
          duration: '142 min',
          director: 'Animeku',
          release: 2019,
          desc: 'Menceritakan Nobita dan kawan-kawannya yang berpetualang di bulan, dan juga hadirnya murid baru di kelas Nobita yang misterius bernama Luka. Cerita dari film ini sendiri berkaitan dengan dongeng kuno Jepang yang menyebutkan bahwa bulan dihuni oleh kelinci.',
          id: 3
        },
        {
         title: 'Black Fox Movie',
          image: require('../assets/4.jpg'),
          duration: '102 min',
          director: 'Anoboy',
          release: 2019,
          desc: 'Tinggal di kediaman ninja yang terselip di sudut kota futuristik adalah Rikka, anak perempuan tertua dari klan Ninja, yang sangat menghormati ayahnya — seorang peneliti — sangat banyak. Melanjutkan hidupnya dengan normal, rumah Rikka tiba-tiba diserang suatu hari. Didorong ke sudut, apa yang akan dia lakukan untuk mengatasi krisis ini? Potong kegelapan menjadi potongan-potongan dan menjadi “HITAM”!',
          id: 4
        }
      ]
    }
  },
  methods: {
    goToDetail (proId) {
      this.$router.push({ name: 'detail', params: { Pid: proId } })
    }
  }
}

</script>

<style>
.container
{
    margin-top: 2%;
}
.font-text
{
    font-size: 9pt;
    margin: 10px 0;
}
.image-area
{
    width: 200px;
    height: 300px;
    text-align: center;
}
.image{
    width: 200px;
    height: 300px;
}
.content-area
{
    margin: 10px 0;
    height: 30%;
}
</style>
