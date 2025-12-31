<script setup>
  import {ref} from 'vue'
  const file_name=ref('')
  const handlefile=(e)=>{
    if (e.target.files && e.target.files.length > 0) {
    file_name.value = e.target.files[0].name
  } else {
    file_name.value = ''
  }
  }
</script>
<template>
  <div class="box">
    <div class="div-text">
      <div class="text">
        <span class="text-span1">Finish!</span>
        <br>
        <span class="text-span1">Upload your resume</span>
        <br>
        <span class="text-span2">
          Upload your resume,the platform will help you parse and optimize, you can also skip this step
        </span>
      </div>
    </div>
    <div class="div-img">
      <img src="../public/f3b98a45b95147719af263d1e992460c384c379e.png" alt="">
    </div>
    <div class="div-box">
      <input type="file" id="file-input" :style="{display:'none'}" @change="handlefile">
      <div class="div-form">
        <span class="form-text">Upload file</span>
        <label for="file-input">
          <div class="file-div" ref="file_req">
            <svg :style="{width:'58px',height:'39px'}" t="1767079948480" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="10903" width="256" height="256"><path d="M554.666667 550.4V768h192c85.333333-8.533333 149.333333-81.066667 149.333333-170.666667 0-93.866667-76.8-170.666667-170.666667-170.666666h-4.266666c-21.333333-98.133333-106.666667-170.666667-209.066667-170.666667-119.466667 0-213.333333 93.866667-213.333333 213.333333-72.533333 8.533333-128 72.533333-128 149.333334C170.666667 699.733333 238.933333 768 320 768H512v-217.6l-98.133333 98.133333-29.866667-29.866666 149.333333-149.333334 149.333334 149.333334-29.866667 29.866666-98.133333-98.133333z m0 217.6v42.666667h-42.666667v-42.666667h-64v42.666667h-128C213.333333 810.666667 128 725.333333 128 618.666667c0-85.333333 55.466667-157.866667 128-183.466667C273.066667 311.466667 379.733333 213.333333 512 213.333333c110.933333 0 209.066667 72.533333 243.2 170.666667 102.4 12.8 183.466667 102.4 183.466667 213.333333s-85.333333 200.533333-192 213.333334h-128v-42.666667H554.666667z" fill="#1849D6" p-id="10904"></path></svg>
            <span v-if="file_name.length==0">Drag your resume file to this area, or click on the area to select the appropriate file to upload</span>
            <span v-else>{{ file_name }}</span>
          </div>
        </label>
        <div class="div-button">
          <div><span>Last step</span></div>
          <div><span>Finish</span></div>
        </div>
        <div class="progress">
          <div>
            <svg t="1767080227467" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="5575" width="16" height="16"><path d="M392.533333 806.4L85.333333 503.466667l59.733334-59.733334 247.466666 247.466667L866.133333 213.333333l59.733334 59.733334L392.533333 806.4z" fill="#2A4CFE" p-id="5576"></path></svg>
          </div>
          <div>
            <svg t="1767080227467" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="5575" width="16" height="16"><path d="M392.533333 806.4L85.333333 503.466667l59.733334-59.733334 247.466666 247.466667L866.133333 213.333333l59.733334 59.733334L392.533333 806.4z" fill="#2A4CFE" p-id="5576"></path></svg>
          </div>
          <div><span>3</span></div>
        </div>
        <div class="progress-box">
          <div class="progress1"></div>
          <div class="progress2"></div>
        </div>
        
      </div>
    </div>
  </div>
</template>

<style scoped>
  .box{
    display: grid;
    height: 1080px;
    width:99vw;
    grid-template-columns: 875px 1fr;
    grid-template-rows: 511px 1fr;
    grid-template-areas:
    "text box"
    "img box"
    ;
  }
  .div-text{
    grid-area: text;
  }
  .div-img{
    grid-area: img;
    img{
      width: 763px;
      height: 569px;
    }
  }
  .div-box{
    grid-area: box;
  }
  .div-form{
    margin-top: 103px;
    padding-left: 129px;
    padding-top: 30px;
    border-radius: 32px;
    height: 922px;
    width: 943px;
    box-shadow: 0 2px 20px 0 rgba(19, 67, 112, 0.15);
  }
  .text{
    margin-top: 124px;
    margin-left: 102px;
    .text-span1{
      font-family: 'Inter';
      line-height: 55px;
      font-size: 40px;
    }
    .text-span2{ 
      display: inline-block;
      color:#A5A5A5;
      font-family: 'Inter';
      line-height: 35px;
      width:696px;
      font-size: 20px;
      font-weight: 400;
      letter-spacing:0;
    }
  }
  .form-text{
    font-family: "Inter";
    font-weight: 500;
    font-size: 36px;
    line-height: 35px;
    Letter-spacing:8%;
  }
  .file-div{
    box-sizing:content-box;
    margin-top: 53px;
    width: 685px;
    height: 420px;
    background-color: rgba(242,250,255,1);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    background-image: url("../public/Rectangle 34624658.png");
    span{
      width: 400px;
      text-align: center;
      font-size: 16px;
      font-weight: 400;
      font-family: 'Inter';
      line-height: 32px;
      letter-spacing: 0%;
      color: #A5A5A5;
    }
  }
  .div-button{
    /* margin-left: 56px; */
    margin-top: 98px;
    width: 685px;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 29px;
    div{
      width: 272px;
      height: 67px;
      border-radius: 8px;
      background-color: rgba(117,172,255,1);
      line-height: 67px;
      font-weight: 400;
      font-size: 24px;
      letter-spacing: 8%;
      text-align: center;
      color: rgba(255, 255, 255, 1);
      cursor: pointer;
      
    }
    div:active{
      background-color:#1B5AFF;
      
    }
  }
  .progress{
    display: flex;
    justify-content: center;
    width: 685px;
    margin-top: 101px;
    gap: 93px;
    span{
        cursor: default;
      }
    div{
      box-sizing: content-box;
      border: #2A4CFE 3px solid;
      height: 26px;
      width: 26px;
      border-radius: 50%;
      background-color: #85A7FF;
      line-height: 26px;
      text-align: center;
      font-size: 11px;
      color: #FFFFFF;
      box-shadow: 0 7px 64px 0 rgba(0, 0, 0, 0.07);
      z-index: 3;
      .icon{
        width: 10px;
        height: 10px;
      }
    }
  }
  .progress-box{
    position: relative;
    bottom: 20px;
    margin-left: 167px;
  }
  .progress1{
    background-color: #DDE0E7;
    width: 343px;
    height: 4px;
    z-index: 2;
  }
  .progress2{
    background-color: #85A7FF;
    width: 299px;
    height: 4px;
    position: relative;
    bottom: 4px;
    z-index: 1;
  }
  @media (max-width: 900px) {
    .box {
      display: grid;
      grid-template-columns:1fr;
      grid-template-rows:repeat(3,1fr);
      grid-template-areas:
      "text"
      "img"
      "box";
      width: 100vw;
      margin: 0;
    }
    .div-text{ grid-area: text; }
    .div-img{ grid-area: img; }
    .div-box{ grid-area: box; }
  }
</style>
<style>
   *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Inter';
    letter-spacing: 0px;
  }
  span{
    user-select: none;
  }
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap');
 
</style>