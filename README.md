<!DOCTYPE html>
<html lang="uz">
<head>
<meta charset="UTF-8">
<title>Habit Tracker</title>

<style>
body{
  background:#0f172a;
  color:white;
  font-family:Arial;
  display:flex;
  justify-content:center;
  align-items:center;
  min-height:100vh;
  margin:0;
}

.container{
  background:#1e293b;
  padding:25px;
  border-radius:15px;
  width:400px;
  text-align:center;
}

input{
  width:100%;
  padding:10px;
  border:none;
  border-radius:8px;
  margin-top:10px;
}

button{
  margin-top:15px;
  padding:10px 15px;
  border:none;
  border-radius:8px;
  background:#38bdf8;
  cursor:pointer;
}

.item{
  background:#334155;
  margin-top:10px;
  padding:10px;
  border-radius:10px;
  text-align:left;
  display:flex;
  justify-content:space-between;
  align-items:center;
}

.done{
  text-decoration:line-through;
  color:#22c55e;
}
</style>
</head>

<body>

<div class="container">

<h1>🧭 Habit Tracker</h1>

<input id="habit" placeholder="New habit...">

<button onclick="addHabit()">➕ Add</button>

<div id="list"></div>

</div>

<script>
let habits = JSON.parse(localStorage.getItem("habits")) || [];

function save(){
  localStorage.setItem("habits", JSON.stringify(habits));
}

function addHabit(){

  const habit =
    document.getElementById("habit").value;

  if(!habit) return;

  habits.push({text:habit,done:false});

  save();
  render();

  document.getElementById("habit").value = "";
}

function toggle(i){
  habits[i].done = !habits[i].done;
  save();
  render();
}

function remove(i){
  habits.splice(i,1);
  save();
  render();
}

function render(){

  const list =
    document.getElementById("list");

  list.innerHTML = "";

  habits.forEach((h,i)=>{

    list.innerHTML += `
      <div class="item">

        <span class="${h.done ? "done" : ""}">
          ${h.text}
        </span>

        <div>

          <button onclick="toggle(${i})">
            ✔
          </button>

          <button onclick="remove(${i})">
            ❌
          </button>

        </div>

      </div>
    `;
  });
}

render();
</script>

</body>
</html>
