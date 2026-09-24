<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Ride Fuel</title>
<style>
body{font-family:-apple-system,BlinkMacSystemFont,sans-serif;background:#f5f5f5;margin:0;padding:16px;color:#111}
main{max-width:600px;margin:auto}
h1{margin:5px 0}.sub{color:#777;margin-bottom:18px}
.card{background:white;border-radius:16px;padding:16px;margin-bottom:12px}
h2{font-size:18px;margin:0 0 12px}
.item{display:flex;align-items:center;justify-content:space-between;border-bottom:1px solid #eee;padding:10px 0;gap:10px}
.item:last-child{border-bottom:0}
.name{font-weight:600}.info{font-size:12px;color:#777;margin-top:3px}
.buttons{display:flex;align-items:center;gap:8px}
button{width:42px;height:42px;border:0;border-radius:12px;background:#111;color:white;font-size:22px}
.qty{width:25px;text-align:center;font-weight:bold}
input,select,textarea{font:inherit;width:100%;box-sizing:border-box;border:1px solid #ddd;border-radius:10px;padding:11px;background:white}
.duration{display:flex;gap:8px}.duration input{width:50%}
.stats{display:flex;gap:8px}.stat{flex:1;background:#eee;border-radius:12px;text-align:center;padding:10px}
.stat b{display:block;font-size:20px}.stat span{font-size:11px;color:#666}
textarea{height:145px;resize:none}.copy{width:100%;height:48px;font-size:16px;margin-top:10px}
</style>
</head>
<body>
<main>
<h1>Ride Fuel 🚴</h1>
<div class="sub">Nutrition pour tes sorties vélo</div>

<div class="card">
<h2>⏱️ Durée</h2>
<div class="duration">
<input id="hours" type="number" min="0" value="0" placeholder="Heures">
<input id="minutes" type="number" min="0" max="59" value="0" placeholder="Minutes">
</div>
</div>

<div class="card"><h2>🍯 BAAM</h2><div id="baam"></div></div>
<div class="card"><h2>🧃 Gels</h2><div id="gels"></div></div>
<div class="card"><h2>🍬 Autres</h2><div id="other"></div></div>

<div class="card">
<h2>⚡ Athletic Fuel</h2>
<select id="fuel"></select>
<div class="info">30 g = 1 scoop · 15 g = ½ scoop · 94 g glucides / 100 g</div>
</div>

<div class="card">
<h2>📊 Total</h2>
<div class="stats">
<div class="stat"><b id="totalCarbs">0</b><span>g glucides</span></div>
<div class="stat"><b id="totalKcal">0</b><span>kcal</span></div>
<div class="stat"><b id="carbsHour">0</b><span>g/h</span></div>
</div>
</div>

<div class="card">
<h2>📝 Strava</h2>
<textarea id="description" readonly></textarea>
<button class="copy" id="copy">Copier</button>
</div>
</main>

<script>
var foods = [
 {cat:"baam",name:"BAAM Miel Banane Agrumes",kcal:174,carbs:17},
 {cat:"baam",name:"BAAM Miel Cacao Café Gingembre",kcal:174,carbs:16},
 {cat:"baam",name:"BAAM Miel Sésame Citron",kcal:192,carbs:16},
 {cat:"baam",name:"BAAM Miel Tomate Piment Curcuma",kcal:170,carbs:19},
 {cat:"baam",name:"BAAM Protéinée Miel Figues",kcal:180,carbs:15},
 {cat:"gels",name:"Nduranz Fraise NRGY Gel",kcal:180,carbs:45},
 {cat:"other",name:"Krema Régal'ad",kcal:25,carbs:5.2},
 {cat:"other",name:"Banane",kcal:105,carbs:27}
];

var quantities = [];
for(var i=0;i<foods.length;i++) quantities[i]=0;

function draw(cat,id){
 var box=document.getElementById(id);
 for(let i=0;i<foods.length;i++){
  if(foods[i].cat!==cat) continue;
  let f=foods[i];
  let row=document.createElement("div");
  row.className="item";
  row.innerHTML='<div><div class="name">'+f.name+'</div><div class="info">'+f.carbs+' g glucides · '+f.kcal+' kcal</div></div>'+
    '<div class="buttons"><button class="minus">−</button><div class="qty">0</div><button class="plus">+</button></div>';
  let q=row.querySelector(".qty");
  row.querySelector(".minus").onclick=function(){
    if(quantities[i]>0) quantities[i]--;
    q.textContent=quantities[i];
    calculate();
  };
  row.querySelector(".plus").onclick=function(){
    quantities[i]++;
    q.textContent=quantities[i];
    calculate();
  };
  box.appendChild(row);
 }
}

draw("baam","baam");
draw("gels","gels");
draw("other","other");

var other=document.getElementById("other");
var coke=document.createElement("div");
coke.className="item";
coke.innerHTML='<div><div class="name">🥤 Coca-Cola</div><div class="info">10,6 g glucides · 42 kcal / 100 ml</div></div><input id="cokeMl" type="number" min="0" step="10" value="0" placeholder="ml" style="width:100px">';
other.appendChild(coke);

var fuel=document.getElementById("fuel");
for(var g=0;g<=300;g+=15){
 var option=document.createElement("option");
 option.value=g;
 option.textContent=g+" g ("+(g/30)+" scoop"+(g/30===1?"":"s")+")";
 fuel.appendChild(option);
}

function calculate(){
 var carbs=0,kcal=0,lines=[];
 for(var i=0;i<foods.length;i++){
  var n=quantities[i];
  if(n>0){
   carbs+=n*foods[i].carbs;
   kcal+=n*foods[i].kcal;
   lines.push(n+"× "+foods[i].name);
  }
 }
 var ml=Number(document.getElementById("cokeMl").value)||0;
 if(ml>0){
  carbs+=ml*0.106;
  kcal+=ml*0.42;
  lines.push(ml+" ml Coca-Cola");
 }
 var grams=Number(fuel.value)||0;
 if(grams>0){
  carbs+=grams*0.94;
  lines.push(grams+" g Athletic Fuel ("+(grams/30)+" scoop"+(grams/30===1?"":"s")+")");
 }
 var minutes=(Number(document.getElementById("hours").value)||0)*60+(Number(document.getElementById("minutes").value)||0);
 var perHour=minutes>0?carbs/(minutes/60):0;
 document.getElementById("totalCarbs").textContent=carbs.toFixed(1);
 document.getElementById("totalKcal").textContent=Math.round(kcal);
 document.getElementById("carbsHour").textContent=perHour.toFixed(1);
 var duration=Math.floor(minutes/60)+"h"+String(minutes%60).padStart(2,"0");
 document.getElementById("description").value=
  "🍽️ Nutrition — "+duration+"\\n"+
  (lines.length?lines.join("\\n"):"Aucune nutrition renseignée")+
  "\\n\\n"+carbs.toFixed(1)+" g glucides · "+Math.round(kcal)+" kcal · "+perHour.toFixed(1)+" g/h";
}

document.getElementById("hours").oninput=calculate;
document.getElementById("minutes").oninput=calculate;
document.getElementById("cokeMl").oninput=calculate;
fuel.onchange=calculate;

document.getElementById("copy").onclick=function(){
 var text=document.getElementById("description").value;
 if(navigator.clipboard && window.isSecureContext){
  navigator.clipboard.writeText(text);
 }else{
  var area=document.getElementById("description");
  area.removeAttribute("readonly");area.select();document.execCommand("copy");area.setAttribute("readonly","");
 }
};

calculate();
</script>
</body>
</html>
