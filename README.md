[Лисья тропа_ Крылов и фольклор (5 класс).html](https://github.com/user-attachments/files/33210778/_.5.html)
# viktorinapo
Викторина по литературе 5 класс после прочтений басен Крылова И.А.
<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Лисья тропа: Крылов и фольклор</title>
<style>
:root{box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px);--bg:#fdf3e1;--card:#fff;--ink:#3b2a1a;--mut:#8a6f55;--acc:#e07a1f;--ok:#2e9e5b;--bad:#d9453d;--line:#ecd8b8}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#1f1710;--card:#2c2118;--ink:#f6e8d3;--mut:#b99d7e;--line:#4a3826}}
:root[data-theme="dark"]{--bg:#1f1710;--card:#2c2118;--ink:#f6e8d3;--mut:#b99d7e;--line:#4a3826}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--ink);font-family:Georgia,"Times New Roman",serif;min-height:100vh}
.wrap{max-width:680px;margin:0 auto;padding:16px}
.card{background:var(--card);border:2px solid var(--line);border-radius:18px;padding:20px;margin-bottom:14px}
h1{font-size:28px;margin:0 0 6px}
.big{font-size:64px;text-align:center}
.mut{color:var(--mut)}
button{font:inherit;cursor:pointer}
.btn{background:var(--acc);color:#fff;border:0;border-radius:14px;padding:12px 22px;font-size:18px;font-weight:bold}
.btn:active{transform:scale(.97)}
.top{display:flex;justify-content:space-between;align-items:center;gap:8px;font-weight:bold}
.timer{font-size:22px;font-variant-numeric:tabular-nums}
.timer.low{color:var(--bad)}
.path{display:flex;align-items:center;margin:12px 0;overflow:hidden}
.dot{flex:1;height:8px;background:var(--line);border-radius:4px;margin:0 1px;position:relative}
.dot.done{background:var(--ok)}.dot.miss{background:var(--bad)}
.fox{position:absolute;top:-22px;right:-10px;font-size:20px}
.q{font-size:21px;margin:8px 0 14px;line-height:1.35}
.tag{display:inline-block;font-size:13px;background:var(--line);padding:3px 10px;border-radius:20px}
.opt{display:block;width:100%;text-align:left;background:var(--bg);color:var(--ink);border:2px solid var(--line);border-radius:12px;padding:12px 14px;margin:8px 0;font-size:17px}
.opt:hover:not(:disabled){border-color:var(--acc)}
.opt.ok{background:var(--ok);color:#fff;border-color:var(--ok)}
.opt.bad{background:var(--bad);color:#fff;border-color:var(--bad)}
.exp{margin-top:10px;padding:10px 12px;border-left:5px solid var(--acc);background:var(--bg);border-radius:8px}
.grade{font-size:120px;font-weight:bold;text-align:center;line-height:1}
.g5{color:var(--ok)}.g4{color:#6aa84f}.g3{color:var(--acc)}.g2{color:var(--bad)}
.mini{background:none;border:2px solid var(--line);color:var(--ink);border-radius:10px;padding:4px 10px}
ul{padding-left:20px}
.info{background:var(--bg);border:2px dashed var(--acc);border-radius:12px;padding:10px 14px;margin:10px 0;font-size:16px;line-height:1.4}
.row{display:flex;flex-wrap:wrap;align-items:center;gap:8px;margin:10px 0}
.row span{flex:1 1 200px;font-size:17px}
select,input{font:inherit;font-size:16px;padding:8px;border:2px solid var(--line);border-radius:10px;background:var(--bg);color:var(--ink);max-width:100%}
input{width:100%;margin:8px 0}
select.ok{border-color:var(--ok);background:var(--ok);color:#fff}
select.bad{border-color:var(--bad);background:var(--bad);color:#fff}
table{width:100%;border-collapse:collapse}td,th{padding:8px 6px;border-bottom:1px solid var(--line);text-align:left}
</style>
</head>
<body>
<div class="wrap" id="app"></div>
<script>
// [вопрос, верный ответ, ошибка1, ошибка2, ошибка3, пояснение, тема]
const Q=[
["Кто такой Иван Андреевич Крылов?","Русский баснописец","Автор волшебных сказок","Автор былин","Составитель народных загадок","Крылов (1769–1844) — великий русский баснописец.","Крылов"],
["Что такое басня?","Короткий рассказ в стихах с нравоучением","Песня для малышей","Загадка с отгадкой","Народное изречение","В басне есть иносказание и мораль — вывод-нравоучение.","Крылов"],
["Как называется иносказание, когда за животными скрыты люди и их недостатки?","Аллегория","Рифма","Загадка","Потешка","Аллегория — иносказание: звери в баснях изображают людей.","Крылов"],
["Что называют моралью басни?","Нравоучение, вывод","Первую строчку","Имя автора","Описание природы","Мораль — главный вывод басни, чему она учит.","Крылов"],
["Что послал Ворона «Бог» в басне «Ворона и Лисица»?","Кусочек сыру","Кусочек мяса","Орех","Рыбку","«Вороне где-то Бог послал кусочек сыру».","Ворона и Лисица"],
["Чем Лисица заставила Ворону каркнуть и выронить сыр?","Лестью","Угрозами","Просьбой поделиться","Силой","Лисица льстила: хвалила голос и красоту Вороны.","Ворона и Лисица"],
["Чему учит басня «Ворона и Лисица»?","Не верь льстецам","Нужно делиться","Надо рано вставать","Береги дерево","«Как много в мире лести гнусной, вредной!» — льстец ищет выгоду.","Ворона и Лисица"],
["Куда ночью забрался Волк в басне «Волк на псарне»?","На псарню","В овчарню","В курятник","В деревню","Волк забрался на псарню, но попал в беду.","Волк на псарне"],
["Что предложил Волк, когда оказался в западне?","Заключить мир","Отдать добычу","Уйти в лес навсегда","Стать охранником","Волк хитрил: «К чему друзья вражда? Я сам готов мириться».","Волк на псарне"],
["Что ответил Ловчий Волку?","«Ты сер, а я, приятель, сед»","«Прощаю тебя»","«Будь нам другом»","«Иди с миром»","Ловчий знал волчью натуру и не поверил Волку.","Волк на псарне"],
["Кого в басне «Волк на псарне» изображает Ловчий?","Кутузова","Наполеона","Пушкина","Царя Петра","Басня написана после 1812 года: Волк — Наполеон, Ловчий — Кутузов.","Волк на псарне"],
["Кто хвастался в басне «Листы и Корни»?","Листы","Корни","Ветки","Птицы","Листы гордились красотой и тенью, а Корни молчали.","Листы и Корни"],
["Что ответили Корни Листам?","Что питают дерево и без них не будет листвы","Что им нет дела до красоты","Что уйдут в землю глубже","Что листья им не нужны","Основа жизни — то, что скрыто. Не презирай тех, на ком всё держится.","Листы и Корни"],
["Что делала Свинья под Дубом?","Подрывала корни дуба","Ела жёлуди и хвалила дуб","Спала под дубом","Сажала жёлуди","Она наелась желудей и стала подрывать корни дерева.","Свинья под Дубом"],
["О ком басня «Свинья под Дубом»?","О невеждах, не ценящих науку","О трудолюбивых людях","О лентяях","О друзьях","Невежда хулит науку и учёность, не зная их пользы.","Свинья под Дубом"],
["Сколько героев-музыкантов в басне «Квартет»?","Четыре","Три","Пять","Два","Квартет — четверо: Мартышка, Осёл, Козёл и Косолапый Мишка.","Квартет"],
["Что ответил Соловей музыкантам в басне «Квартет»?","Надо иметь уменье, а не просто пересаживаться","Нужно сыграть громче","Нужен хороший дирижёр","Надо репетировать ночью","«Чтоб музыкантом быть, так надобно уменье».","Квартет"],
["Кого попросил спеть Осёл в басне «Осёл и Соловей»?","Соловья","Петуха","Ворону","Жаворонка","Осёл просит Соловья показать своё искусство.","Осёл и Соловей"],
["Что посоветовал Осёл Соловью после его пения?","Поучиться у Петуха","Спеть громче","Петь днём","Больше отдыхать","Осёл судит о том, чего не понимает: невежда не ценит искусство.","Осёл и Соловей"],
["Как называется короткое мудрое изречение с законченной мыслью: «Без труда не вытащишь и рыбку из пруда»?","Пословица","Поговорка","Считалка","Загадка","Пословица — законченная мысль и поучение.","Фольклор"],
["Какое выражение — поговорка?","Бить баклуши","Старый друг лучше новых двух","Не в деньгах счастье","Тише едешь — дальше будешь","Поговорка — образное выражение без законченного поучения.","Фольклор"],
["К какому жанру относится: «Раз, два, три, четыре, пять — вышел зайчик погулять»?","Считалка","Потешка","Загадка","Небылица","Считалками распределяют роли в игре.","Фольклор"],
["Какой жанр: «Карл у Клары украл кораллы»?","Скороговорка","Колыбельная","Закличка","Пословица","Скороговорка трудна для произношения и развивает речь.","Фольклор"],
["Какой жанр: «Ладушки, ладушки, где были? — У бабушки»?","Потешка","Загадка","Пословица","Былина","Потешки — игры с малышами, пальчиковые и ладошки.","Фольклор"],
["Что такое загадка?","Иносказательное описание предмета, который надо отгадать","Песня для засыпания","Нелепая выдумка","Обращение к природе","«Зимой и летом одним цветом» — ёлка.","Фольклор"],
["Как называется песня, которую поют малышу, чтобы он уснул?","Колыбельная","Закличка","Прибаутка","Считалка","«Баю-баюшки-баю…» — колыбельная.","Фольклор"],
["Что такое небылица?","Весёлая выдумка, где всё наоборот","Мудрое изречение","Песня для сна","Объяснение природы","«Ехала деревня мимо мужика» — небылица-перевёртыш.","Фольклор"]
];
const I=[
["Иван Крылов родился в Москве в 1769 году. Первая книга его басен вышла в 1809 году. Басни так полюбились читателям, что многие строки стали пословицами и поговорками.","Как называют строки из басен, которые стали общеупотребительными выражениями?","Крылатые выражения","Колыбельные","Считалки","Былины","Строки вроде «А Васька слушает да ест» живут в нашей речи как крылатые выражения.","Крылов"],
["Лесть — это чрезмерная, неискренняя похвала. Ею пользуются, чтобы добиться выгоды. Сюжет басни «Ворона и Лисица» известен со времён Эзопа и Лафонтена, но Крылов пересказал его по-своему.","Чего добивалась Лисица своей лестью?","Получить сыр","Подружиться с Вороной","Научиться петь","Прогнать Ворону с ветки","Лисица хвалила Ворону, чтобы та каркнула и выронила сыр.","Ворона и Лисица"],
["Басня «Волк на псарне» написана в 1812 году, во время войны с Наполеоном. Волк в ней — Наполеон, который просил мира, чтобы спасти армию, а Ловчий — полководец Кутузов.","Почему Ловчий не поверил Волку?","Знал, что волки хитрят и не меняются","Волк говорил очень тихо","Хотел мира с волками","Не заметил Волка","«Ты сер, а я, приятель, сед» — Ловчий опытен и не верит хитрецу.","Волк на псарне"],
["Листья дерева видны всем: они шелестят на ветру и дают тень. А корни спрятаны под землёй, но именно они добывают воду и питание для всего дерева.","Какой вывод делает басня «Листы и Корни»?","Нельзя презирать тех, на ком всё держится","Листья важнее корней","Корни должны выйти на свет","Дереву не нужна вода","Не гордись тем, что на виду: без скрытого труда других не обойтись.","Листы и Корни"],
["Дуб в басне «Свинья под Дубом» — символ науки и знаний. Невежда — это человек, который многого не знает и не хочет узнавать.","Кого олицетворяет Свинья в басне?","Невежду","Мудреца","Трудолюбивого человека","Хитреца","Свинья пользуется плодами дуба, но подрывает его корни.","Свинья под Дубом"],
["Слово «квартет» значит «четвёрка»: так называют музыкальное произведение для четырёх исполнителей. Герои басни Крылова тоже решили сыграть квартет, но играть не умели.","Над кем смеётся Крылов в басне «Квартет»?","Над теми, кто берётся за дело без умения","Над настоящими музыкантами","Над Соловьём","Над любителями природы","Соловей сказал: чтобы быть музыкантом, нужно уменье.","Квартет"],
["Соловья в народе считают лучшим певцом леса. А Осёл в баснях Крылова — олицетворение упрямства и глупости: он судит о том, в чём не разбирается.","Почему Осёл посоветовал Соловью поучиться у Петуха?","Не понимал настоящего искусства","Был хорошим знатоком музыки","Хотел помочь Соловью","Любил Петуха больше всех","Невежда не умеет оценить талант.","Осёл и Соловей"],
["Фольклор — это устное народное творчество. Малые жанры фольклора короткие: пословицы, поговорки, загадки, считалки, скороговорки, потешки. Их передавали из уст в уста.","Почему у малых жанров фольклора нет автора?","Их создавал и передавал народ","Они появились только в книгах","Их придумал один древний писатель","Их написал неизвестный иностранец","Фольклор — творчество всего народа.","Фольклор"],
["Колыбельные пели матери и няни, чтобы убаюкать малыша. В них часто повторяются слова «баю-баю» и ласковые обращения.","Для чего нужны колыбельные песни?","Чтобы убаюкать ребёнка","Чтобы развеселить гостей","Чтобы разделить игроков на команды","Чтобы загадать загадку","Спокойный ритм и повторы помогают малышу уснуть.","Фольклор"]
];
const M=[
["Соедини басню и то, что в ней важно:",[["Ворона и Лисица","Сыр"],["Свинья под Дубом","Жёлуди"],["Волк на псарне","Ловчий"],["Листы и Корни","Дерево"]],"Крылов"],
["Соедини жанр фольклора и пример:",[["Пословица","Семь раз отмерь, один раз отрежь"],["Загадка","Сидит дед, во сто шуб одет"],["Считалка","Аты-баты, шли солдаты"],["Скороговорка","Тридцать три корабля лавировали"]],"Фольклор"],
["Соедини жанр и его определение:",[["Пословица","Законченная мудрая мысль с поучением"],["Поговорка","Образное выражение без поучения"],["Загадка","Иносказание, которое нужно отгадать"],["Считалка","Нужна, чтобы распределить роли в игре"]],"Фольклор"],
["Соедини басню и её мораль:",[["Ворона и Лисица","Не верь льстивым речам"],["Листы и Корни","Цени тех, на ком всё держится"],["Волк на псарне","Хитрецу нельзя верить на слово"],["Осёл и Соловей","Невежда не умеет ценить талант"]],"Крылов"]
];
let player='';
const esc=s=>String(s).replace(/[&<>"]/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;'}[c]));
function loadR(){try{return JSON.parse(localStorage.getItem('kr')||'[]')}catch(e){return[]}}
function saveR(r){try{const a=loadR();a.push(r);localStorage.setItem('kr',JSON.stringify(a))}catch(e){}}
function rating(){
 fx.click();
 const a=loadR().sort((x,y)=>y.g-x.g||y.p-x.p||x.t-y.t).slice(0,30);
 app.innerHTML=`<div class="card"><h1>🏆 Рейтинг класса</h1>${a.length?`<table><tr><th>#</th><th>Ученик</th><th>Оценка</th><th>%</th><th>Время</th></tr>${a.map((r,i)=>`<tr><td>${i+1}${['🥇','🥈','🥉'][i]||''}</td><td>${esc(r.n)}</td><td><b>${r.g}</b></td><td>${r.p}%</td><td>${fmt(r.t)}</td></tr>`).join('')}</table>`:'<p class="mut">Пока никого нет. Введи имя и сыграй!</p>'}<p><button class="btn" id="bk">Назад</button> <button class="mini" id="clr">Очистить</button></p></div>`;
 $('#bk').onclick=menu;
 $('#clr').onclick=e=>{if(e.target.dataset.s){try{localStorage.removeItem('kr')}catch(x){}rating()}else{e.target.dataset.s=1;e.target.textContent='Точно очистить?'}};
}
function matchHTML(q){q.rs=shuffle(q.match.map(p=>p[1]));return `<div id="mt">${q.match.map((p,i)=>`<div class="row"><span>${p[0]}</span><select><option value="">— выбери —</option>${q.rs.map(r=>`<option>${r}</option>`).join('')}</select></div>`).join('')}</div><p><button class="btn" id="chk">Проверить</button></p>`}
function checkMatch(){
 if(st.locked)return;
 const q=st.pick[st.i],sel=[...document.querySelectorAll('#mt select')];
 if(sel.some(x=>!x.value)){$('#fb').innerHTML='<div class="exp">Выбери пару в каждой строке.</div>';return}
 st.locked=true;let n=0;
 sel.forEach((x,i)=>{const r=x.value===q.match[i][1];if(r)n++;x.disabled=true;x.classList.add(r?'ok':'bad');if(!r)x.insertAdjacentHTML('afterend',`<small class="mut">верно: ${q.match[i][1]}</small>`)});
 const all=n===sel.length;st.ok+=n/sel.length;st.res[st.i]=all?1:0;all?fx.ok():fx.bad();
 $('#chk').style.display='none';
 const last=st.i===TOTAL-1;
 $('#fb').innerHTML=`<div class="exp">${all?'✅ Все пары верны!':'❌ Верных пар: '+n+' из '+sel.length+'.'}</div><p><button class="btn" id="nx">${last?'Узнать оценку':'Дальше →'}</button></p>`;
 $('#nx').onclick=()=>{fx.click();if(last)finish();else{st.i++;draw()}};
}
const TOTAL=20,TIME=30*60;
let st,tick,muted=false,ac;
const $=s=>document.querySelector(s);
const app=$('#app');
const shuffle=a=>{a=a.slice();for(let i=a.length-1;i>0;i--){const j=Math.floor(Math.random()*(i+1));[a[i],a[j]]=[a[j],a[i]]}return a};
function snd(f,d,t='sine',v=.15,when=0){if(muted)return;try{ac=ac||new (window.AudioContext||window.webkitAudioContext)();const o=ac.createOscillator(),g=ac.createGain();o.type=t;o.frequency.value=f;g.gain.setValueAtTime(v,ac.currentTime+when);g.gain.exponentialRampToValueAtTime(.001,ac.currentTime+when+d);o.connect(g);g.connect(ac.destination);o.start(ac.currentTime+when);o.stop(ac.currentTime+when+d)}catch(e){}}
const fx={ok(){snd(660,.12,'triangle');snd(880,.18,'triangle',.15,.1)},bad(){snd(220,.25,'sawtooth',.1);snd(160,.3,'sawtooth',.1,.15)},click(){snd(500,.05,'square',.05)},tick(){snd(900,.04,'square',.04)},win(){[523,659,784,1047].forEach((f,i)=>snd(f,.25,'triangle',.15,i*.15))},lose(){[400,330,260].forEach((f,i)=>snd(f,.3,'sine',.15,i*.2))}};
function start(){
 const pick=shuffle([...shuffle(Q).slice(0,10).map(q=>({q:q[0],ans:q[1],opts:shuffle(q.slice(1,5)),exp:q[5],tag:q[6]})),...shuffle(I).slice(0,7).map(q=>({info:q[0],q:q[1],ans:q[2],opts:shuffle(q.slice(2,6)),exp:q[6],tag:q[7]})),...shuffle(M).slice(0,3).map(m=>({q:m[0],match:m[1],tag:m[2]}))]);
 st={pick,i:0,ok:0,left:TIME,res:[],done:false,locked:false};
 clearInterval(tick);
 tick=setInterval(()=>{st.left--;if(st.left<=0){st.left=0;finish()}else{if(st.left<=60)fx.tick();upd()}},1000);
 fx.click();draw();
}
function fmt(s){return String(Math.floor(s/60)).padStart(2,'0')+':'+String(s%60).padStart(2,'0')}
function upd(){const t=$('#t');if(t){t.textContent='⏱ '+fmt(st.left);t.className='timer'+(st.left<=300?' low':'')}}
function menu(){
 app.innerHTML=`<div class="card"><div class="big">🦊📜</div><h1>Лисья тропа</h1>
 <p>Помоги Лисе пройти тропу из ${TOTAL} вопросов: басни И.А. Крылова («Волк на псарне», «Листы и Корни», «Свинья под Дубом», «Квартет», «Осёл и Соловей», «Ворона и Лисица») и малые жанры фольклора.</p>
 <ul><li>⏱ На всё — 30 минут</li><li>🔊 Есть звуковые эффекты</li><li>🏆 В конце — оценка от «2» до «5»</li><li>📖 Вопросы со справкой и на соответствие</li><li>👥 Режим класса: введи имя — результат попадёт в рейтинг</li></ul>
 <input id="nm" placeholder="Имя ученика (для рейтинга класса)" maxlength="30" value="${esc(player)}"><button class="btn" id="go">Начать игру</button> <button class="mini" id="rt">🏆 Рейтинг класса</button> <button class="mini" id="mu">🔊 Звук вкл.</button></div>`;
 $('#go').onclick=()=>{player=$('#nm').value.trim();start()};$('#rt').onclick=rating;
 $('#mu').onclick=e=>{muted=!muted;e.target.textContent=muted?'🔇 Звук выкл.':'🔊 Звук вкл.';fx.click()};
}
function draw(){
 const q=st.pick[st.i];
 const dots=st.pick.map((_,k)=>`<div class="dot ${st.res[k]===1?'done':st.res[k]===0?'miss':''}">${k===st.i?'<span class="fox">🦊</span>':''}</div>`).join('');
 app.innerHTML=`<div class="top"><span>⭐ ${+st.ok.toFixed(1)}</span><span class="timer" id="t">⏱ ${fmt(st.left)}</span><button class="mini" id="mu">${muted?'🔇':'🔊'}</button></div>
 <div class="path">${dots}</div>
 <div class="card"><span class="tag">${q.tag} · вопрос ${st.i+1} из ${TOTAL}</span>${q.info?`<div class="info">📖 <b>Знаешь ли ты?</b> ${q.info}</div>`:''}<div class="q">${q.q}</div>
 ${q.match?matchHTML(q):''}<div id="o">${(q.opts||[]).map((o,k)=>`<button class="opt" data-k="${k}">${o}</button>`).join('')}</div>
 <div id="fb"></div></div>`;
 st.locked=false;upd();
 $('#mu').onclick=e=>{muted=!muted;e.target.textContent=muted?'🔇':'🔊';fx.click()};
 document.querySelectorAll('.opt').forEach(b=>b.onclick=()=>answer(b));
 if(q.match)$('#chk').onclick=checkMatch;
}
function answer(b){
 if(st.locked)return;st.locked=true;
 const q=st.pick[st.i],right=b.textContent===q.ans;
 document.querySelectorAll('.opt').forEach(o=>{o.disabled=true;if(o.textContent===q.ans)o.classList.add('ok')});
 if(right){st.ok++;fx.ok()}else{b.classList.add('bad');fx.bad()}
 st.res[st.i]=right?1:0;
 const last=st.i===TOTAL-1;
 $('#fb').innerHTML=`<div class="exp">${right?'✅ Верно! ':'❌ Не совсем. '}${q.exp}</div><p><button class="btn" id="nx">${last?'Узнать оценку':'Дальше →'}</button></p>`;
 $('#nx').onclick=()=>{fx.click();if(last)finish();else{st.i++;draw()}};
}
function finish(){
 if(st.done)return;st.done=true;clearInterval(tick);
 const p=Math.round(st.ok/TOTAL*100),g=p>=90?5:p>=75?4:p>=50?3:2;
 const txt={5:'Отлично!',4:'Хорошо!',3:'Пойдёт',2:'Плохо'}[g];
 const msg={5:'Ты настоящий знаток басен и фольклора! 🎉',4:'Хороший результат, ещё немного — и будет «5».',3:'Неплохо, но стоит повторить басни и жанры.',2:'Перечитай басни и жанры фольклора и попробуй снова.'}[g];
 g>=4?fx.win():fx.lose();
 const spent=TIME-st.left;if(player)saveR({n:player,g,p,t:spent});
 app.innerHTML=`<div class="card"><div class="big">${g>=4?'🏆':g==3?'🦊':'📚'}</div>
 <div class="grade g${g}">${g}</div><h1 style="text-align:center">${txt}</h1>
 <p style="text-align:center">${msg}</p>
 <p style="text-align:center" class="mut">Баллов: ${+st.ok.toFixed(1)} из ${TOTAL} (${p}%) · Время: ${fmt(spent)}${st.left===0?' · время вышло':''}</p>
 <p style="text-align:center"><button class="btn" id="again">Играть снова</button> <button class="mini" id="rt">🏆 Рейтинг</button> <button class="mini" id="mn">Новый ученик</button></p>
 <p class="mut" style="font-size:14px">Шкала: «5» — от 90%, «4» — от 75%, «3» — от 50%, «2» — меньше 50%.</p></div>`;
 $('#again').onclick=start;$('#rt').onclick=rating;$('#mn').onclick=menu;
}
menu();
</script>
</body>
</html>
