    new Vue({
      el: '#app',
      data() {
        return {
          videos: [
            {
              title: "Video 1",
              src: "https://21emon.wjg.jp/AndroidApp/index.html"
            },
            {
              title: "Video 2",
              src: "https://21emon.wjg.jp/ClockWithTimeSignal/index.html"
            },
            {
              title: "Video 3",
              src: "https://chat.openai.com"
            }
          ]
        };
      },
      methods: {
        changeVideo(index) {
          // ビデオのURLを切り替える処理
          // 例えば、別のビデオを再生する場合は以下のようにします
          this.videos[index].src = "http://21emon.wjg.jp";
        }
      }
    });