<template>
  <v-container class="dash">
    <v-row>
      <v-col md=1></v-col>
      <v-col md="3" style="width:10px !important">
        <v-card class="mainCard" style="width:240px !important">
          <v-card class="mainCardData"><br>
            <div class="avatar">
              <v-img src="../../images/image-jeremy.png"></v-img>
            </div>
            <p class="rep">Report for</p>
            <p class="name">Jeremy Robson</p>
          </v-card>
          <div class="btns">
            <br>
            <button @click="daily()" class="btnsC active">Daily</button>
            <button @click="weekly()" class="btnsC">Weekly</button>
            <button @click="monthly()" class="btnsC">Monthly</button>
          </div>
        </v-card>
      </v-col>

      <v-col md="7">
        <v-row>
          <v-col md="3.5" class="infoCard">
            <v-card class="imgCard" style="background-color:hsl(15, 100%, 70%)">
              <v-img class="iconImgs" src="../../images/icon-work.svg"></v-img>
              <v-card class="infoCardData">
                <p class="type">Work</p>
                <p class="mainHrs">{{hrsWork}}hrs</p>
                <p class="lastHrs">{{phrase}} - {{lHrsWork}}hrs</p>
              </v-card>
            </v-card>
          </v-col>
          <v-col md="3.5" class="infoCard">
            <v-card class="imgCard" style="background-color:hsl(195, 74%, 62%)">
              <v-img class="iconImgs" src="../../images/icon-play.svg"></v-img>
              <v-card class="infoCardData">
                <p class="type">Play</p>
                <p class="mainHrs">{{hrsPlay}}hrs</p>
                <p class="lastHrs">{{phrase}} - {{lHrsPlay}}hrs</p>
              </v-card>
            </v-card>
            </v-col>
          <v-col md="3.5" class="infoCard">
            <v-card class="imgCard" style="background-color:hsl(348, 100%, 68%)">
              <v-img class="iconImgs" src="../../images/icon-study.svg"></v-img>
              <v-card class="infoCardData">
                <p class="type">Study</p>
                <p class="mainHrs">{{hrsStudy}}hrs</p>
                <p class="lastHrs">{{phrase}} - {{lHrsStudy}}hrs</p>
              </v-card>
            </v-card>
            </v-col>
        </v-row>
        
        <v-row>
          <v-col md="3.5" class="infoCard">
            <v-card class="imgCard" style="background-color:hsl(145, 58%, 55%)">
              <v-img class="iconImgs" src="../../images/icon-exercise.svg"></v-img>
              <v-card class="infoCardData">
                <p class="type">Exercise</p>
                <p class="mainHrs">{{hrsExercise}}hrs</p>
                <p class="lastHrs">{{phrase}} - {{lHrsExercise}}hrs</p>
              </v-card>
            </v-card>
            </v-col>
          <v-col md="3.5" class="infoCard">
            <v-card class="imgCard" style="background-color:hsl(264, 64%, 52%)">
              <v-img class="iconImgs" src="../../images/icon-social.svg"></v-img>
              <v-card class="infoCardData">
                <p class="type">Social</p>
                <p class="mainHrs">{{hrsSocial}}hrs</p>
                <p class="lastHrs">{{phrase}} - {{lHrsSocial}}hrs</p>
              </v-card>
            </v-card>
            </v-col>
          <v-col md="3.5" class="infoCard">
            <v-card class="imgCard" style="background-color:hsl(43, 84%, 65%)">
              <v-img class="iconImgs" src="../../images/icon-self-care.svg"></v-img>
              <v-card class="infoCardData">
                <p class="type">Self Care</p>
                <p class="mainHrs">{{hrsSelfCare}}hrs</p>
                <p class="lastHrs">{{phrase}} - {{lHrsSelfCare}}hrs</p>
              </v-card>
            </v-card>
            </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>

  export default {
    name: 'HelloWorld',
    data(){
      return{
        hrsWork:'8',
        hrsPlay:'4',
        hrsStudy:'6',
        hrsExercise:'2',
        hrsSocial:'2',
        hrsSelfCare:'2',
        lHrsWork:'11',
        lHrsPlay:'12',
        lHrsStudy:'13',
        lHrsExercise:'14',
        lHrsSocial:'15',
        lHrsSelfCare:'16',
        phrase:'yesterday'
      }
    },
    mounted(){
      this.daily();
const btns = document.querySelectorAll(".btnsC");
for (var i = 0; i < btns.length; i++) {
  btns[i].addEventListener("click", function() {
    var current = document.getElementsByClassName("active");
    if (current.length > 0) {
      current[0].className = current[0].className.replace(" active", "");
    }
    this.className += " active";
  });
}
    },

    methods:{
      daily(){
        this.hrsWork = 8
        this.hrsPlay = 4
        this.hrsStudy = 6
        this.hrsExercise = 2
        this.hrsSocial = 2
        this.hrsSelfCare = 2
        this.lHrsWork = 7
        this.lHrsPlay = 5
        this.lHrsStudy = 5
        this.lHrsExercise = 3
        this.lHrsSocial = 2
        this.lHrsSelfCare = 2
        this.phrase = "Yesterday"
      },
      weekly(){
        this.hrsWork = 56
        this.hrsPlay = 28
        this.hrsStudy = 42
        this.hrsExercise = 14
        this.hrsSocial = 14
        this.hrsSelfCare = 14
        this.lHrsWork = 49
        this.lHrsPlay = 35
        this.lHrsStudy = 35
        this.lHrsExercise = 21
        this.lHrsSocial = 14
        this.lHrsSelfCare = 14
        this.phrase = "Last Week"
      },
      monthly(){
        this.hrsWork = 240
        this.hrsPlay = 120
        this.hrsStudy = 180
        this.hrsExercise = 60
        this.hrsSocial = 60
        this.hrsSelfCare = 60
        this.lHrsWork = 210
        this.lHrsPlay = 150
        this.lHrsStudy = 150
        this.lHrsExercise = 90
        this.lHrsSocial = 60
        this.lHrsSelfCare = 60
        this.phrase = "Last Month"
      },
      activate(){
      }
    }
  }
</script>

<style>

.btn {
  background-color: #f1f1f1;
  margin: 2px;
  height: 35px;
  width: 15px;
  cursor: pointer;
}
.infoCardData{
  background-color: hsl(235, 46%, 20%)  !important;
  height: 160px;
  width: 200px;
  border-radius: 10px !important;
  color: white !important;
  transition: 1s;
}
.infoCardData:hover{
  background-color: hsl(235, 29%, 51%) !important;
  transition: 1s;
  cursor: pointer;
}
.dash{
  height: 100vh;
  justify-content: center;
  align-items: center;
  display: flex;  
}
.mainCard{
  margin-top: 10px;
  height: 430px;
  background-color: hsl(235, 46%, 20%) !important;
  border-radius: 20px !important;
}
.mainCardData{
  background-color: hsl(246, 80%, 60%) !important;
  height: 300px;
  border-radius: 15px !important;
  color: white !important;
}
.btns{
display: flex;
flex-direction: column;
}
.btnsC{
  color: rgba(255, 255, 255, .7);
  text-align: left;
  margin: 3px;
  margin-left: 35px;
}
.active, .btnsC:hover {
  color: white;
}
.infoCard{
  height: 200px;
  margin-top: 15px !important;
}
.iconImgs{
  margin-left:145px; 
  width:50px;
  height: 35px;
}
.imgCard{
  border-radius:11px !important; 
  width: 200px;
}
.mainHrs{
  font-size: 45px;
  font-weight: 300;
  margin-left: 15px;
}
.lastHrs{
  color: rgba(255, 255, 255, .7);
  font-size: 12px;
  font-weight: 200;
  margin-left: 17px;
  margin-top: -13px;
}
.rep{
  color: rgba(255, 255, 255, .7);
  font-size: 12px;
  font-weight: 200;
  margin-left: 40px;
  margin-top: 20px;
  margin-bottom: -10px !important;
}
.name{
  font-size: 40px;
  font-weight: 300;
  margin-left: 40px;
  margin-top: -10px;
}
.type{
  margin-left: 17px;
  padding-top: 15px;
}
.avatar{
  width: 80px;
  border: 3px solid white;
  border-radius: 100% !important;
  margin-left: 25px;
}
</style>
