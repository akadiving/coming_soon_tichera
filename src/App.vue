<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style>
.container{
  display: grid;
}

@keyframes tipsy {
  0% {
    transform: translateX(-50%) translateY(-50%) rotate(0deg);
  }
  100% {
    transform: translateX(-50%) translateY(-50%) rotate(360deg);
  }
}

body {
  font-family: helvetica, arial, sans-serif;
  background-color: #2e2e31;
}

p {
  color: #f5b921;
  text-shadow: 0 20px 25px #2e2e31, 0 40px 60px #2e2e31;
  font-size: 80px;
  font-weight: bold;
  text-decoration: none;
  letter-spacing: -3px;
  margin: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translateX(-50%) translateY(-50%);
}

p:before,
p:after {
  content: '';
  padding: .9em .4em;
  position: absolute;
  left: 50%;
  width: 100%;
  top: 50%;
  display: block;
  border: 15px solid red;
  transform: translateX(-50%) translateY(-50%) rotate(0deg);
  animation: 10s infinite alternate ease-in-out tipsy;
}

p:before {
  border-color: #d9524a #d9524a rgba(0, 0, 0, 0) rgba(0, 0, 0, 0);
  z-index: -1;
}

p:after {
  border-color: rgba(0, 0, 0, 0) rgba(0, 0, 0, 0) #d9524a #d9524a;
  box-shadow: 25px 25px 25px rgba(46, 46, 49, .8);
}

h2 {
  display: block;
  margin: 0;
  position: absolute;
  top: 78%;
  left: 45%;
  text-align: center;
  color: #f5b921;
  font-size: 60px;
  -webkit-box-reflect: below 1px linear-gradient(transparent, #0008);
  line-height: 0.70em;
  outline: none;
  animation: glow 5s linear infinite;
}

@keyframes glow {
  0%, 18%, 20%, 50.1%, 60%, 65.1%, 80%, 90.1%, 92% {
    color: #f5b921;
    text-shadow: none;
  }
  18.1%, 20.1%, 30%, 50%, 60.1%, 65%, 80.1%, 90%, 92.1%, 100% {
  color: #fff;
  text-shadow: 0 0 10px #03bcf4,
  0 0 20px #03bcf4,
  0 0 40px #03bcf4,
  0 0 80px #03bcf4,
  0 0 160px #03bcf4,
  }
}
</style>
