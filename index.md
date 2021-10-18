<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <script src="vue.js"></script>

    <title>Vue</title>
  </head>
  <body>
    <div id="app">
      <input type="text" v-model="age" />
      <p>Javascript : {{age >= 18 ? "Reşittir" : "Değildir"}}</p>
      <p>Method : {{ageWriter()}}</p>
      <p>Computed : {{ageWriteComp}}</p>
      <p>{{sayi}}</p>
      <button @click="sayi++">Arttır</button>
    </div>

    <script>
      new Vue({
        el: "#app",
        data: {
          age: 0,
          sayi: 0,
        },
        methods: {
          ageWriter() {
            console.log("method çalıştı...");
            return this.age >= 18 ? "Reşittir" : "Değildir";
          },
        },
        computed: {
          ageWriteComp() {
            console.log("computed çalıştı");
            return this.age >= 18 ? "Reşittir" : "Değildir";
          },
        },
      });
    </script>
        <script src="vue.js"></script>

  </body>
</html>
