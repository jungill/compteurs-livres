<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Compteurs de plateau</title>
<style>
  :root{
    --table:#17262A;
    --mat-dot:rgba(233,227,212,.07);
    --chit:#E9E3D4;
    --chit-art:#F3EFE4;
    --chit-edge:#C7BFA9;
    --ink:#14201E;
    --ink-soft:#5F6E68;
    --brass:#D6A93B;
    --jade:#7FB8A4;
    --danger:#B04A34;
    --font:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Helvetica,Arial,sans-serif;
    --mono:ui-monospace,"SF Mono","Cascadia Mono","Roboto Mono",Menlo,Consolas,monospace;
  }

  *{box-sizing:border-box}

  html,body{height:100%}

  body{
    margin:0;
    padding:0;
    font-family:var(--font);
    color:var(--chit);
    background-color:var(--table);
    background-image:radial-gradient(var(--mat-dot) 1px, transparent 1px);
    background-size:22px 22px;
    display:flex;
    flex-direction:column;
    min-height:100%;
  }

  /* ---------- barre du haut ---------- */
  .bar{
    display:flex;
    flex-wrap:wrap;
    align-items:center;
    gap:14px 18px;
    padding:18px 22px;
    border-bottom:1px solid rgba(233,227,212,.13);
  }
  .brand{display:flex;align-items:baseline;gap:10px;margin-right:auto}
  .brand h1{
    margin:0;
    font-size:15px;
    font-weight:600;
    letter-spacing:.16em;
    text-transform:uppercase;
  }
  .brand .mark{font-family:var(--mono);font-size:15px;color:var(--brass)}
  .tools{display:flex;flex-wrap:wrap;gap:8px}

  .btn{
    font-family:inherit;
    font-size:13px;
    letter-spacing:.02em;
    color:var(--chit);
    background:transparent;
    border:1px solid rgba(233,227,212,.28);
    border-radius:2px;
    padding:8px 13px;
    cursor:pointer;
  }
  .btn:hover{border-color:var(--chit);background:rgba(233,227,212,.06)}
  .btn-primary{background:var(--brass);border-color:var(--brass);color:var(--ink);font-weight:600}
  .btn-primary:hover{background:#E2B848;border-color:#E2B848}
  .btn-quiet{border-color:transparent;color:var(--ink-soft)}
  .btn-quiet:hover{color:var(--chit);border-color:rgba(233,227,212,.28)}

  :focus-visible{outline:2px solid var(--brass);outline-offset:2px}

  /* ---------- plateau ---------- */
  .board{
    flex:1;
    display:grid;
    grid-template-columns:repeat(auto-fill,minmax(176px,1fr));
    gap:16px;
    align-content:start;
    padding:22px;
  }
  .board:empty{display:none}

  .chit{
    position:relative;
    background:var(--chit);
    border:1px solid var(--chit-edge);
    border-radius:3px;
    overflow:hidden;
    display:flex;
    flex-direction:column;
  }

  .art{
    aspect-ratio:1/1;
    background:var(--chit-art);
    display:grid;
    place-items:center;
    padding:12px;
    border-bottom:1px solid var(--chit-edge);
  }
  .art img{max-width:100%;max-height:100%;object-fit:contain;display:block}

  .label{
    font-family:inherit;
    font-size:11px;
    font-weight:600;
    letter-spacing:.1em;
    text-transform:uppercase;
    text-align:center;
    color:var(--ink-soft);
    background:transparent;
    border:0;
    border-bottom:1px solid transparent;
    padding:9px 8px;
    margin:0 8px;
    width:calc(100% - 16px);
  }
  .label:hover{border-bottom-color:var(--chit-edge)}
  .label:focus{color:var(--ink);border-bottom-color:var(--brass);outline:none}

  /* ---------- les deux pistes de comptage ---------- */
  .tracks{margin-top:auto;background:var(--ink)}

  .track{
    display:grid;
    grid-template-columns:46px 1fr 46px;
    align-items:stretch;
  }
  .track + .track{border-top:1px solid rgba(233,227,212,.14)}

  .step{
    font-family:var(--mono);
    font-size:20px;
    line-height:1;
    color:var(--accent);
    background:transparent;
    border:0;
    padding:0;
    cursor:pointer;
    -webkit-user-select:none;
    user-select:none;
  }
  .step:hover{background:rgba(233,227,212,.09)}
  .step:active{background:rgba(233,227,212,.17)}

  .readout{display:flex;flex-direction:column;align-items:center;padding:8px 0 10px;min-width:0}

  .tag{
    font-size:9px;
    font-weight:700;
    letter-spacing:.16em;
    text-transform:uppercase;
    color:var(--accent);
    white-space:nowrap;
    overflow:hidden;
    text-overflow:ellipsis;
    max-width:100%;
  }

  .count{
    font-family:var(--mono);
    font-size:27px;
    font-weight:600;
    font-variant-numeric:tabular-nums;
    letter-spacing:-.03em;
    text-align:center;
    color:var(--chit);
    background:transparent;
    border:0;
    padding:1px 0 0;
    width:100%;
    min-width:0;
    transition:transform .12s ease-out;
  }
  .count:focus{outline:none;color:var(--accent)}
  .count.bump{transform:scale(1.16)}
  @media (prefers-reduced-motion:reduce){.count{transition:none}.count.bump{transform:none}}

  .remove{
    position:absolute;
    top:6px;
    right:6px;
    width:24px;
    height:24px;
    font-size:15px;
    line-height:1;
    color:var(--ink-soft);
    background:var(--chit-art);
    border:1px solid var(--chit-edge);
    border-radius:50%;
    cursor:pointer;
    opacity:0;
  }
  .chit:hover .remove,.chit:focus-within .remove{opacity:1}
  .remove:hover{color:#fff;background:var(--danger);border-color:var(--danger)}

  /* ---------- écran vide ---------- */
  .empty{
    flex:1;
    margin:22px;
    display:grid;
    place-content:center;
    justify-items:center;
    gap:14px;
    text-align:center;
    border:2px dashed rgba(233,227,212,.22);
    border-radius:4px;
    padding:40px 24px;
  }
  .empty[hidden]{display:none}
  .empty p{margin:0;max-width:34ch;font-size:14px;line-height:1.6;color:var(--ink-soft)}
  .empty strong{
    display:block;
    font-size:19px;
    font-weight:600;
    letter-spacing:.02em;
    color:var(--chit);
    margin-bottom:6px;
  }

  .hint{
    padding:14px 22px 20px;
    font-size:12px;
    line-height:1.7;
    color:var(--ink-soft);
    border-top:1px solid rgba(233,227,212,.13);
  }
  .hint code{font-family:var(--mono);color:var(--brass)}

  /* ---------- voile de dépôt ---------- */
  .veil{
    position:fixed;
    inset:0;
    display:grid;
    place-items:center;
    font-size:20px;
    letter-spacing:.08em;
    text-transform:uppercase;
    background:rgba(23,38,42,.9);
    border:3px solid var(--brass);
    z-index:10;
  }
  .veil[hidden]{display:none}

  @media (max-width:520px){
    .board{grid-template-columns:repeat(auto-fill,minmax(150px,1fr));gap:12px;padding:14px}
    .track{grid-template-columns:40px 1fr 40px}
    .count{font-size:24px}
  }
</style>
</head>
<body>

<header class="bar">
  <div class="brand"><span class="mark">&#9672;</span><h1>Compteurs de plateau</h1></div>
  <div class="tools">
    <button class="btn btn-primary" id="add">Ajouter des images</button>
    <button class="btn" id="zero">Tout remettre à zéro</button>
    <button class="btn btn-quiet" id="export">Exporter</button>
    <button class="btn btn-quiet" id="import">Importer</button>
  </div>
</header>

<main class="board" id="board"></main>

<section class="empty" id="empty">
  <p><strong>Le plateau est vide</strong>Dépose ici les images de tes ressources et de tes unités, ou utilise le bouton « Ajouter des images ». Chaque image reçoit deux compteurs, Dubail et Oratoire.</p>
</section>

<footer class="hint">
  Clique sur un nombre pour le saisir directement, ou utilise <code>&uarr;</code> <code>&darr;</code> · Maintiens <code>Maj</code> en cliquant sur <code>&minus;</code> ou <code>+</code> pour avancer de 5 · Le titre sous chaque image est modifiable.
</footer>

<div class="veil" id="veil" hidden>Dépose les images</div>

<input type="file" id="picker" accept="image/*" multiple hidden>
<input type="file" id="jsonPicker" accept=".json,application/json" hidden>

<script>
(function(){
  "use strict";

  /* Les deux pistes. Pour les renommer ou en ajouter une troisième,
     il suffit de modifier cette liste : le reste du code s'adapte. */
  var TRACKS = [
    { name: "Dubail",   color: "var(--brass)" },
    { name: "Oratoire", color: "var(--jade)"  }
  ];

  var KEY = "compteurs-plateau-v1";
  var MAX_SIDE = 320;          // les images sont réduites : plateau léger et sauvegarde compacte
  var board = document.getElementById("board");
  var empty = document.getElementById("empty");
  var veil  = document.getElementById("veil");
  var picker = document.getElementById("picker");
  var jsonPicker = document.getElementById("jsonPicker");

  /* Stockage : localStorage si disponible, sinon mémoire de session. */
  var store = (function(){
    try {
      localStorage.setItem("__test__","1");
      localStorage.removeItem("__test__");
      return {
        get: function(){ return localStorage.getItem(KEY); },
        set: function(v){ localStorage.setItem(KEY, v); }
      };
    } catch (e) {
      var mem = null;
      return { get:function(){ return mem; }, set:function(v){ mem = v; } };
    }
  })();

  /* Remet une tuile au format attendu, y compris les plateaux
     enregistrés quand il n'y avait qu'un seul compteur. */
  function normalize(t){
    if (!t || !t.src) return null;
    var counts = Array.isArray(t.counts) ? t.counts : [parseInt(t.count, 10) || 0];
    return {
      id: t.id || uid(),
      src: t.src,
      label: typeof t.label === "string" ? t.label : "",
      counts: TRACKS.map(function(_, i){ return parseInt(counts[i], 10) || 0; })
    };
  }

  var tiles = [];
  try {
    var parsed = JSON.parse(store.get());
    if (Array.isArray(parsed)) tiles = parsed.map(normalize).filter(Boolean);
  } catch (e) { tiles = []; }

  function save(){
    try {
      store.set(JSON.stringify(tiles));
    } catch (e) {
      alert("La sauvegarde automatique a atteint sa limite. Utilise « Exporter » pour conserver ce plateau dans un fichier.");
    }
  }

  function uid(){
    return Date.now().toString(36) + Math.random().toString(36).slice(2,7);
  }

  /* ---------- import des images ---------- */

  function shrink(file){
    return new Promise(function(resolve, reject){
      var reader = new FileReader();
      reader.onerror = function(){ reject(new Error("lecture")); };
      reader.onload = function(){
        var img = new Image();
        img.onerror = function(){ reject(new Error("décodage")); };
        img.onload = function(){
          var ratio = Math.min(1, MAX_SIDE / Math.max(img.width, img.height));
          var w = Math.max(1, Math.round(img.width * ratio));
          var h = Math.max(1, Math.round(img.height * ratio));
          var canvas = document.createElement("canvas");
          canvas.width = w; canvas.height = h;
          canvas.getContext("2d").drawImage(img, 0, 0, w, h);
          // WebP conserve la transparence des icônes ; JPEG suffit pour les photos.
          var keepAlpha = /png|webp|gif|svg/.test(file.type);
          var out = canvas.toDataURL(keepAlpha ? "image/webp" : "image/jpeg", 0.85);
          if (keepAlpha && out.indexOf("data:image/webp") !== 0) {
            out = canvas.toDataURL("image/png");   // repli si WebP n'est pas encodé
          }
          resolve(out);
        };
        img.src = reader.result;
      };
      reader.readAsDataURL(file);
    });
  }

  function cleanName(name){
    return name.replace(/\.[^.]+$/, "").replace(/[_-]+/g, " ").trim().slice(0, 24);
  }

  function addFiles(fileList){
    var files = Array.prototype.slice.call(fileList).filter(function(f){
      return f.type.indexOf("image/") === 0;
    });
    if (!files.length) return;

    var jobs = files.map(function(file){
      return shrink(file).then(function(src){
        return normalize({ src: src, label: cleanName(file.name) });
      }, function(){ return null; });
    });

    Promise.all(jobs).then(function(made){
      var ok = made.filter(Boolean);
      if (ok.length < files.length) {
        alert((files.length - ok.length) + " image(s) n'ont pas pu être lues.");
      }
      ok.forEach(function(t){ tiles.push(t); });
      save();
      render();
    });
  }

  /* ---------- rendu ---------- */

  function bump(input){
    input.classList.remove("bump");
    void input.offsetWidth;
    input.classList.add("bump");
  }

  function makeTrack(tile, index){
    var track = TRACKS[index];

    var row = document.createElement("div");
    row.className = "track";
    row.style.setProperty("--accent", track.color);

    var readout = document.createElement("div");
    readout.className = "readout";

    var tag = document.createElement("span");
    tag.className = "tag";
    tag.textContent = track.name;

    var count = document.createElement("input");
    count.className = "count";
    count.type = "text";
    count.inputMode = "numeric";
    count.value = tile.counts[index];
    count.setAttribute("aria-label", track.name + " · " + (tile.label || "cet élément"));

    readout.appendChild(tag);
    readout.appendChild(count);

    function step(direction, event){
      var amount = (event && event.shiftKey) ? 5 : 1;
      tile.counts[index] = tile.counts[index] + direction * amount;
      count.value = tile.counts[index];
      save();
      bump(count);
    }

    var minus = document.createElement("button");
    minus.className = "step";
    minus.type = "button";
    minus.textContent = "\u2212";
    minus.setAttribute("aria-label", "Retirer 1 à " + track.name);
    minus.addEventListener("click", function(e){ step(-1, e); });

    var plus = document.createElement("button");
    plus.className = "step";
    plus.type = "button";
    plus.textContent = "+";
    plus.setAttribute("aria-label", "Ajouter 1 à " + track.name);
    plus.addEventListener("click", function(e){ step(1, e); });

    count.addEventListener("focus", function(){ count.select(); });
    count.addEventListener("input", function(){
      var kept = count.value.replace(/[^\d-]/g, "");
      if (kept !== count.value) count.value = kept;
      tile.counts[index] = parseInt(kept, 10) || 0;
      save();
    });
    count.addEventListener("blur", function(){ count.value = tile.counts[index]; });
    count.addEventListener("keydown", function(e){
      if (e.key === "ArrowUp")   { e.preventDefault(); step(1, e); }
      if (e.key === "ArrowDown") { e.preventDefault(); step(-1, e); }
      if (e.key === "Enter")     { count.blur(); }
    });

    row.appendChild(minus);
    row.appendChild(readout);
    row.appendChild(plus);
    return row;
  }

  function makeChit(tile){
    var chit = document.createElement("article");
    chit.className = "chit";

    var art = document.createElement("div");
    art.className = "art";
    var img = document.createElement("img");
    img.src = tile.src;
    img.alt = tile.label || "";
    img.draggable = false;
    art.appendChild(img);

    var label = document.createElement("input");
    label.className = "label";
    label.value = tile.label || "";
    label.placeholder = "Sans nom";
    label.maxLength = 24;
    label.setAttribute("aria-label", "Nom de cet élément");
    label.addEventListener("input", function(){
      tile.label = label.value;
      img.alt = label.value;
      save();
    });

    var tracks = document.createElement("div");
    tracks.className = "tracks";
    TRACKS.forEach(function(_, i){ tracks.appendChild(makeTrack(tile, i)); });

    var remove = document.createElement("button");
    remove.className = "remove";
    remove.type = "button";
    remove.textContent = "\u00D7";
    remove.setAttribute("aria-label", "Retirer " + (tile.label || "cet élément") + " du plateau");
    remove.addEventListener("click", function(){
      if (!confirm("Retirer « " + (tile.label || "cet élément") + " » du plateau ?")) return;
      tiles = tiles.filter(function(t){ return t.id !== tile.id; });
      save();
      render();
    });

    chit.appendChild(remove);
    chit.appendChild(art);
    chit.appendChild(label);
    chit.appendChild(tracks);
    return chit;
  }

  function render(){
    board.textContent = "";
    tiles.forEach(function(tile){ board.appendChild(makeChit(tile)); });
    empty.hidden = tiles.length > 0;
  }

  /* ---------- barre d'outils ---------- */

  document.getElementById("add").addEventListener("click", function(){ picker.click(); });
  picker.addEventListener("change", function(){
    addFiles(picker.files);
    picker.value = "";
  });

  document.getElementById("zero").addEventListener("click", function(){
    if (!tiles.length) return;
    if (!confirm("Remettre tous les compteurs à zéro ? Les images restent en place.")) return;
    tiles.forEach(function(t){ t.counts = t.counts.map(function(){ return 0; }); });
    save();
    render();
  });

  document.getElementById("export").addEventListener("click", function(){
    if (!tiles.length) { alert("Le plateau est vide, il n'y a rien à exporter."); return; }
    var blob = new Blob([JSON.stringify(tiles)], { type: "application/json" });
    var url = URL.createObjectURL(blob);
    var a = document.createElement("a");
    a.href = url;
    a.download = "plateau.json";
    a.click();
    setTimeout(function(){ URL.revokeObjectURL(url); }, 1000);
  });

  document.getElementById("import").addEventListener("click", function(){ jsonPicker.click(); });
  jsonPicker.addEventListener("change", function(){
    var file = jsonPicker.files[0];
    jsonPicker.value = "";
    if (!file) return;
    var reader = new FileReader();
    reader.onload = function(){
      var data;
      try { data = JSON.parse(reader.result); } catch (e) { data = null; }
      var loaded = Array.isArray(data) ? data.map(normalize).filter(Boolean) : [];
      if (!loaded.length) {
        alert("Ce fichier n'est pas un plateau exporté depuis cette page.");
        return;
      }
      if (tiles.length && !confirm("Remplacer le plateau actuel par celui du fichier ?")) return;
      tiles = loaded;
      save();
      render();
    };
    reader.readAsText(file);
  });

  /* ---------- glisser-déposer ---------- */

  var depth = 0;
  window.addEventListener("dragenter", function(e){
    if (e.dataTransfer && Array.prototype.indexOf.call(e.dataTransfer.types, "Files") === -1) return;
    depth++;
    veil.hidden = false;
  });
  window.addEventListener("dragover", function(e){ e.preventDefault(); });
  window.addEventListener("dragleave", function(){
    depth = Math.max(0, depth - 1);
    if (!depth) veil.hidden = true;
  });
  window.addEventListener("drop", function(e){
    e.preventDefault();
    depth = 0;
    veil.hidden = true;
    if (e.dataTransfer && e.dataTransfer.files) addFiles(e.dataTransfer.files);
  });

  render();
})();
</script>
</body>
</html>
