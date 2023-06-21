const VueAPlayer = window['VueAPlayer'];
Vue.component('aplayer', VueAPlayer);

new Vue({
  el: '#app',
  data: {
    music: {
      title: 'ON Popラジオ',
      artist: '不明',
      src: 'https://0n-pop.radionetz.de/0n-pop.mp3',
      pic: ''
    },
    list: [
      {
        title: "ON Popラジオ",
        artist: "不明",
        src: "https://0n-pop.radionetz.de/0n-pop.mp3",
        pic: "",
        lrc: ""
      },
      {
        title: "The Metalラジオ",
        artist: "不明",
        src: "https://ais-sa2.cdnstream1.com/1987_128.mp3",
        pic: "",
        lrc: ""
      },
      {
        title: "90s90s BEATラジオ",
        artist: "不明",
        src: "https://regiocast.streamabc.net/regc-90s90smain4920117-mp3-192-6232809",
        pic: "",
        lrc: ""
      },
      {
        title: "Wave Anime Radioラジオ",
        artist: "不明",
        src: "https://otsu.s04.radio-tochka.com:5475/mount",
        pic: "",
        lrc: ""
      },
      {
        title: "J-Pop Powerplayラジオ",
        artist: "不明",
        src: "https://kathy.torontocast.com:3560/;",
        pic: "",
        lrc: ""
      },
      {
        title: "J-Pop Sakura Natuskasiiラジオ",
        artist: "不明",
        src: "https://cast1.torontocast.com:2170/;",
        pic: "",
        lrc: ""
      }
    ]
  },
  components: {
    'nested-component': {
      template: `
        <div>
          <h2>Nested Component</h2>
          <aplayer :music="music" :list="list"></aplayer>
        </div>
      `,
      data() {
        return {
          music: this.$parent.music,
          list: this.$parent.list
        };
      }
    }
  }
});
