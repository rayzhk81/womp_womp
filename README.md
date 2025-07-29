# womp_womp
hck
<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<title>Systemzugriff</title>
<style>
  body { background: black; color: lime; font-family: monospace; padding: 20px; }
  h1 { font-size: 20px; }
</style>
</head>
<body>
<h1>Verbindung mit Zielsystem wird hergestellt...</h1>
<pre id="terminal"></pre>
<script>
const msg = new SpeechSynthesisUtterance("System wird überwacht. Zugriff protokolliert.");
msg.lang = "de-DE"; msg.rate = 0.9; speechSynthesis.speak(msg);
const lines = [
  "Authentifizierung erfolgreich.",
  "Zugriff auf Kamera...",
  "Zugriff gewährt.",
  "Standortdaten analysiert...",
  "Gebäudetyp: Einrichtung erkannt.",
  "Verdacht: 3. Etage, Zimmer mit Blick zur Straße.",
  "Hautton: Analyse abgeschlossen.",
  "Alter geschätzt: ~14.",
  "Subjekt eindeutig identifiziert.",
  "Verbindung zu Rahaman hergestellt...",
  "Bericht wird übertragen..."
];
let i = 0;
function typeLine(){
  if(i < lines.length){
    document.getElementById("terminal").innerHTML += lines[i] + "\n";
    i++;
    setTimeout(typeLine, 1200);
  }
}
typeLine();
</script>
</body>
</html>
