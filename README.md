<h1>SVG-Glitch Doku</h1>

## **Aufgabenstellung**

In diesem Projekt sollten wir uns mit der Struktur von SVG - Vektorgrafiken auseinandersetzen und diese systematisch verändern bzw. glitchen. Wir haben uns dazu entschieden SVG Emojis zusammenzufügen und dadurch neue Emojis zu erstellen. 
Die geglitchten Emojis haben wir durch das editieren verschiedener oder durch das hinzufügen neuer Parameter im Source Code der Emojis erstellt.



### **Viewport**

Der Viewport eines SVGs wird durch die `width` und `height` Attribute im &lt;svg&gt; tag definiert. Ein SVG Viewport hat den Koordinaten Nullpunkt oben links.
Die `viewBox` eines SVGs braucht vier Parameter und gibt an welcher Bereich des SVG Viewports gezeigt wird. Die ersten beiden bestimmen die Verschiebung vom Nullpunkt, die letzten beiden die Größe des Fensters. Dadurch lassen sich SVGs auch skalieren, da sich die gezeichneten Elemente an dem umschließenden Element ausrichten, das heisst je größer die `viewBox` desto kleiner das angezeigte SVG.

In diesem Beispiel ist die `viewBox` um 100 Einheiten nach rechts verschoben, so wird der negative Bereich der x-Achse gezeigt, während die Sonne sich noch immer am Nullpunkt befindet. Daher wird auch der Rote Kreis mit einem negativen x-Wert sichtbar, der sich bei einer `viewBox` an den Koordinaten 0, 0 ausserhalb des Sichtfelds befinden würde.

<svg id="emoji" xmlns="http://www.w3.org/2000/svg" width="1000" heigth="10" viewBox="-100 00 250 70">

 <circle cx="-80.8456" cy="34.789" r="3" fill="#ff0000" stroke="none"/>
 <g>
  <g id="color">
    <polygon fill="#FCEA2B" points="36,10 31.4483,4.3216 28.6708,11.0465 22.7014,6.8864 21.9435,14.1231 15.0427,11.817 16.3488,18.9749 9.0779,18.6961 12.3422,25.1984 5.2887,26.9833 10.2616,32.295 4,36 10.2616,39.7051 5.2889,45.0172 12.3426,46.8026 9.0787,53.3052 16.3497,53.0261 15.044,60.1842 21.9445,57.8775 22.7026,65.1141 28.6713,60.9536 31.4484,67.6784 36,62 40.5517,67.6784 43.3292,60.9535 49.2986,65.1135 50.0565,57.8769 56.9573,60.183 55.6512,53.0251 62.9221,53.3039 59.6578,46.8016 66.7113,45.0167 61.7384,39.705 68,36 61.7384,32.2949 66.7111,26.9828 59.6573,25.1974 62.9213,18.6948 55.6503,18.9739 56.956,11.8158 50.0555,14.1225 49.2974,6.8859 43.3287,11.0464 40.5516,4.3216" stroke="none"/>
  </g>
  <g id="hair"/>
  <g id="skin"/>
  <g id="skin-shadow"/>
  <g id="line">
    <polygon fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" points="36,10 31.4483,4.3216 28.6708,11.0465 22.7014,6.8864 21.9435,14.1231 15.0427,11.817 16.3488,18.9749 9.0779,18.6961 12.3422,25.1984 5.2887,26.9833 10.2616,32.295 4,36 10.2616,39.7051 5.2889,45.0172 12.3426,46.8026 9.0787,53.3052 16.3497,53.0261 15.044,60.1842 21.9445,57.8775 22.7026,65.1141 28.6713,60.9536 31.4484,67.6784 36,62 40.5517,67.6784 43.3292,60.9535 49.2986,65.1135 50.0565,57.8769 56.9573,60.183 55.6512,53.0251 62.9221,53.3039 59.6578,46.8016 66.7113,45.0167 61.7384,39.705 68,36 61.7384,32.2949 66.7111,26.9828 59.6573,25.1974 62.9213,18.6948 55.6503,18.9739 56.956,11.8158 50.0555,14.1225 49.2974,6.8859 43.3287,11.0464 40.5516,4.3216"/>
    <circle cx="27.8456" cy="33.789" r="3" fill="#000000" stroke="none"/>
    <circle cx="44.1544" cy="33.789" r="3" fill="#000000" stroke="none"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M43.6763,46.3816c-2.1347,1.5846-4.8139,2.5518-7.6766,2.5518c-2.9019,0-5.5262-0.9282-7.6759-2.5523"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M31.7748,23.0042c0,0-4.7748-2.6003-9.5496,1.6523"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M40.2252,23.0042c0,0,4.7748-2.6003,9.5496,1.6523"/>
  </g>
  </g>
</svg>


### **Path**

Das Attribut `d` des &lt;path&gt; tags beinhaltet die Koordinaten und Richtungsanweisungen nach denen sich der Pfad bewegt. Die Anweisungen werden mit M, L, H, V, C, S, Q, T und Z, wobei jede Anweisung als Groß oder Kleinbuchstabe angegeben werden kann. Versalien bedeuten dabei stets, dass die angegebenen Koordinaten absolute Koordinaten sind, während Kleinbuchstaben immer Koordinatenverschiebungen relativ zur aktuellen Position angeben. M bewegt z.B. einen imaginären Cursor zu den angegeben Koordinaten, L zieht eine Linie zu von einem Start zu einem Endpunkt. Auf diesem Wege lassen sich sowohl leicht grobe Umrisse skizzieren, als auch komplexe Muster und Formen erstellen.


<svg width="1000" height="250">
  <path fill="none" stroke="#ffffff" stroke-width="2" d="M200, 120 h50 l20, -60 l20, 120 l20, -60 h50">
</svg>




### **Animate**

Das Tag &lt;animate&gt; bzw. &lt;animateTransform&gt;, &lt;animateMotion&gt; und einige weitere Variationen erlauben das animieren von Elementen über verschiedene Parameter. `attributeName` gibt dabei an welches Attribut im Laufe der Animation verändert wird. &lt;animateTransform&gt; erlaubt Transformationsbasierte Animation wie wie z.B. das rotieren mit `rotate` oder skalieren mit `scale`, ausserdem sind einfache bewegungen mit `translate` möglich. Die Parameter `from` und `to` geben eine Start und Endposition des Animierten Elements an, `dur` die Dauer der Animation und `repeatCount` gibt an wie oft die Animation wiederholt werden soll.

<img src="example_1.svg">

Mit  &lt;animateMotion&gt; lassen sich Elemente an einem Pfad entlang bewegen und so komplexere Bewegungen animieren.

<svg width="1000" heigth="300" viewBox="0 0 1000 300">
  <path fill="none" stroke="#ffffff" stroke-width="2" d="M200, 120 h50 l20, -60 l20, 120 l20, -60 h50 ">
  <animateMotion dur="5s" repeatCount="indefinite"
      path="M20,50 C20,-50 180,150 180,50 C180-50 20,150 20,50 z" />
  </path>
</svg>

##  **Ergebnisse**

Die nun erlernten Fähigkeiten haben wir an einigen Emojis von der HfG - Openmoji Bibliothek ausprobiert.

### **Remix**

Die Emojis dieser Kategorie wurden durch das mixen einzelner Emojis entstanden bzw. durch das ersetzen bestimmter Teile eines Emojis mit anderen Emojis. Dafür haben wir den gewünschten Bereich eines Emojis entfernt und stattdessen als verschachteltes SVG das zweite Emoji eingesetzt. Anschließend haben wir die viewBoxen der einzelnen SVGs aufeinander abgestimmt.

## **Schneemann**
Die Grundlage für diese Kreation war ein Surfer-Emoji, dessen Körper mit einem Schneemann ersetzt wurde, dessen Kopf wiederrum mit dem Weltkugel Emoji ersetzt wurde, ausserdem hält er in der rechten Hand einen Krug Mango-Maracujaschorle mit Schlagsahne.

<svg id="emoji" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 70.636 86.636">
  <svg id="emoji" xmlns="http://www.w3.org/2000/svg" viewBox="0 10 72 72">
    <g id="color">
      <path d="M45.0931,43.8251c3.3559,6.6281,2.72,14.78-4.1425,18.2551" fill="none" stroke="#d0cfce" stroke-linecap="round" stroke-miterlimit="10" stroke-width="4"/>
      <path d="M43,21c1.7484,4.4914.4947,9.8429-4.7506,11.8847" fill="none" stroke="#d0cfce" stroke-linecap="round" stroke-miterlimit="10" stroke-width="3"/>  
    </g>
    <g id="line">
      <line x1="13.677" y1="9.9536" x2="19.0703" y2="15.3469" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <line x1="19.8939" y1="11.196" x2="12.7703" y2="13.9501" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <line x1="15.3315" y1="16.2584" x2="17.3327" y2="8.8878" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <path d="M47,43c3.7422,7.3909,3.0334,16.4814-4.6193,20.3561A15.2726,15.2726,0,0,1,21.7485,56.99C19.7516,53.0455,20.9967,46.6853,23,43" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <path d="M32,28s3,4,7,0" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <line x1="25" y1="38" x2="11" y2="30" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <line x1="46.0179" y1="38.0311" x2="60" y2="31" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <circle cx="35.5" cy="44.5" r="0.5" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <circle cx="35.5" cy="56.5" r="0.5" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <svg id="emoji" xmlns="http://www.w3.org/2000/svg" viewBox="-63 -35  200 200">
    <g id="color">
      <circle fill="#92D3F5" stroke="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" cx="36" cy="36" r="28"/>
      <path fill="#B1CC33" d="M9,34c0.5363,0.13,2.3029,0.3956,3,1c0.8804,0.7633-0.0786,1.4353,1,3c0.8754,1.2699,1.4379,3.0859,2,3 c0.7427-0.1134,0.5561-2.6591,2-4c0.4647-0.4316,1.2271-2.1396,2-2c1.4918,0.2695,1.2206,3.3712,3,4 c1.0358,0.366,2.3338,0.7411,3,0c0.8521-0.9479,0.3369-1.7146,1-3c0.8275-1.6039,2.0751-1.2738,4-3 c2.0099-1.8025-0.7353-2.7141,1-4c2.0988-1.5552,4.5219-0.4686,6-2c1.3787-1.4284-0.4493-2.7987,1-4 c0.6379-0.5287,3.0773-0.4945,6-1c1.2827-0.2218,3.239-0.5602,5-1c1.4183-0.3542,2.0643-1.2649,2-2 c-0.0632-0.7224-0.6832-0.9777-1-1c-2.0169-0.1422-2.2701,0.1908-4,0c-1.9902-0.2195-1.9509-0.6928-4-1 c-0.9448-0.1416-1.0863-0.061-5,0c-2.2653,0.0353-3.4099,0.0519-4,0c-2.562-0.2253-4.642-0.8844-5-1 c-2.0319-0.6559-2.0007-0.9771-3-1c-1.5103-0.0345-2.1089,0.6871-4,1c-1.2519,0.2071-2.313,0.1098-3,0l-1.004-0.5618 l-2.8295,3.0328l-2.2612,3.2599l-1.5459,3.005l-1.199,3.265l-0.8482,3.8116l-0.2314,2.0592L9,34z" stroke="none"/>
      <path fill="#B1CC33" stroke="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M32,47c-1.5469,0.1652-2.6099,0.7611-3,1c-0.7033,0.4307-1.5549,0.9523-2,2c-0.4653,1.0953-0.2139,2.1245,0,3 c0.2472,1.012,0.4286,1.7547,1,2c0.7282,0.3127,1.2331,0.4499,3,0c0.7713-0.1964,1.9404-0.4941,3,0c0.9949,0.464,0.8162,0.1239,2,1 c0.4182,0.3095,1.5387,1.1387,3,1c1.2722-0.1208,2.4038-0.9373,3-2c0.7448-1.3275,0.5882-2.9215,0-4 c-0.8341-1.5294-2.0909-1.2053-3-3c-0.4124-0.8142-0.3632-1.2944-1-2c-0.6519-0.7223-1.6523-1.2702-2-1 c-0.4014,0.312,0.4546,1.413,0,2C35.5139,47.6277,34.2306,46.7618,32,47z"/>
      <path fill="#B1CC33" stroke="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M27,41c-1.0128,0.5427-1.9557,1.547-2,2c-0.0252,0.2579,0.3162,0.5088,1,1c1.0589,0.7607,1.0884,1.8078,1.5,1.6667 c0.5548-0.1901,1.3464-1.7906,2.0426-2.8333c0.814-1.2191,3.0778-1.1972,3.2908-2.0833C33.0298,39.9323,30.613,38.0735,30,38 C29.1395,37.8969,29.0017,39.9274,27,41z"/>
      <path fill="#B1CC33" stroke="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M9,34c0.5363,0.13,2.3029,0.3956,3,1c0.8804,0.7633-0.0786,1.4353,1,3c0.8754,1.2699,1.4379,3.0859,2,3 c0.7427-0.1134,0.5561-2.6591,2-4c0.4647-0.4316,1.2271-2.1396,2-2c1.4918,0.2695,1.2206,3.3712,3,4 c1.0358,0.366,2.3338,0.7411,3,0c0.8521-0.9479,0.3369-1.7146,1-3c0.8275-1.6039,2.0751-1.2738,4-3 c2.0099-1.8025-0.7353-2.7141,1-4c2.0988-1.5552,4.5219-0.4686,6-2c1.3787-1.4284-0.4493-2.7987,1-4 c0.6379-0.5287,3.0773-0.4945,6-1c1.2827-0.2218,2.239,0.4398,4,0c1.4183-0.3542,4.0643-2.2649,4-3 c-0.0632-0.7224-1.6832-0.9777-2-1c-2.0169-0.1422-2.2701,0.1908-4,0c-1.9902-0.2195-1.9509-0.6928-4-1 c-0.9448-0.1416-1.0863-0.061-5,0c-2.2653,0.0353-3.4099,0.0519-4,0c-2.562-0.2253-4.642-0.8844-5-1 c-2.0319-0.6559-2.0007-0.9771-3-1c-1.5103-0.0345-2.1089,0.6871-4,1c-1.2519,0.2071-2.313,0.1098-3,0"/>
    </g>
    <g id="line">
      <circle fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" cx="36" cy="36" r="28"/>
      <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M32,47c-1.5469,0.1652-2.6099,0.7611-3,1c-0.7033,0.4307-1.5549,0.9523-2,2c-0.4653,1.0953-0.2139,2.1245,0,3 c0.2472,1.012,0.4286,1.7547,1,2c0.7282,0.3127,1.2331,0.4499,3,0c0.7713-0.1964,1.9404-0.4941,3,0c0.9949,0.464,0.8162,0.1239,2,1 c0.4182,0.3095,1.5387,1.1387,3,1c1.2722-0.1208,2.4038-0.9373,3-2c0.7448-1.3275,0.5882-2.9215,0-4 c-0.8341-1.5294-2.0909-1.2053-3-3c-0.4124-0.8142-0.3632-1.2944-1-2c-0.6519-0.7223-1.6523-1.2702-2-1 c-0.4014,0.312,0.4546,1.413,0,2C35.5139,47.6277,34.2306,46.7618,32,47z"/>
      <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M27,41c-1.0128,0.5427-1.9557,1.547-2,2c-0.0252,0.2579,0.3162,0.5088,1,1c1.0589,0.7607,1.0884,1.8078,1.5,1.6667 c0.5548-0.1901,1.3464-1.7906,2.0426-2.8333c0.814-1.2191,3.0778-1.1972,3.2908-2.0833C33.0298,39.9323,30.613,38.0735,30,38 C29.1395,37.8969,29.0017,39.9274,27,41z"/>
      <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M9,34c0.5363,0.13,2.3029,0.3956,3,1c0.8804,0.7633-0.0786,1.4353,1,3c0.8754,1.2699,1.4379,3.0859,2,3 c0.7427-0.1134,0.5561-2.6591,2-4c0.4647-0.4316,1.2271-2.1396,2-2c1.4918,0.2695,1.2206,3.3712,3,4 c1.0358,0.366,2.3338,0.7411,3,0c0.8521-0.9479,0.3369-1.7146,1-3c0.8275-1.6039,2.0751-1.2738,4-3 c2.0099-1.8025-0.7353-2.7141,1-4c2.0988-1.5552,4.5219-0.4686,6-2c1.3787-1.4284-0.4493-2.7987,1-4 c0.6379-0.5287,3.0773-0.4945,6-1c1.2827-0.2218,2.239,0.4398,4,0c1.4183-0.3542,4.0643-2.2649,4-3 c-0.0632-0.7224-1.6832-0.9777-2-1c-2.0169-0.1422-2.2701,0.1908-4,0c-1.9902-0.2195-1.9509-0.6928-4-1 c-0.9448-0.1416-1.0863-0.061-5,0c-2.2653,0.0353-3.4099,0.0519-4,0c-2.562-0.2253-4.642-0.8844-5-1 c-2.0319-0.6559-2.0007-0.9771-3-1c-1.5103-0.0345-2.1089,0.6871-4,1c-1.2519,0.2071-2.313,0.1098-3,0"/>
      <circle fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" cx="36" cy="36" r="28"/>
    </g>
  </svg>
  <rect x="27" y="8" width="16" height="11" fill="#3f3f3f" stroke="#3f3f3f" stroke-linecap="round" stroke-linejoin="round"/>
  <line x1="23.5" y1="18.5" x2="47.5" y2="18.5" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
  <rect x="27.5" y="7.5" width="16" height="11" stroke-width="2" stroke="#000" stroke-linecap="round" stroke-linejoin="round" fill="none"/>
  <line x1="60" y1="31" x2="65" y2="31" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2.0351"/>
  <svg version="1.1" id="emoji" xmlns="http://www.w3.org/2000/svg" x="0" y="0" viewBox="10 -50 200 200" enable-background="new 0 0 72 72" xml:space="preserve">
    <g id="color">
      <rect x="19" y="23.2301" fill="#FCEA2B" width="29.9997" height="36.3856"/>
      <polygon fill="#F1B31C" points="40.5264,23.2301 33,59.6157 48.9998,59.6157 48.9998,23.2301"/>
      <path fill="#FFFFFF" d="M44.1933,15.3999c-1.304-0.001-2.5018,0.4709-3.4585,1.2577c-0.9376-1.9375-2.8336-3.2665-5.0258-3.2682 c-0.8005-0.0006-1.5606,0.1771-2.2511,0.4952c-1.1199-1.5208-2.8597-2.5031-4.819-2.5046c-2.9465-0.0023-5.4063,2.205-5.997,5.1492 c-0.3479-0.0874-0.7061-0.1448-1.0785-0.1451c-2.6033-0.0021-4.7162,2.2396-4.7184,5.0059l-0.0063,8.0154 c-0.0009,1.1021,0.847,2.0045,1.8842,2.0053l0.9429,0.0007c1.0372,0.0008,1.8865-0.9002,1.8873-2.0024l0.0013-1.5991 c0.5711,0.3722,1.2338,0.5981,1.9494,0.5987l1.8546,0.0015c1.2022,0.0009,2.2653-0.6144,2.9581-1.5517 c1.0256,1.5428,2.7125,2.5581,4.6153,2.5596c3.1115,0.0025,5.6594-2.7007,5.662-6.0071l10.9214,0.0086 c0.2098-0.627,0.3301-1.3002,0.3306-2.0036C49.8485,18.0956,47.318,15.4024,44.1933,15.3999z"/>
      <path fill="#FFFFFF" d="M19.8066,24.8075c0.0022-2.6882,2.115-4.8665,4.7184-4.8646c0.3724,0.0003,0.7307,0.0561,1.0785,0.141 c0.5907-2.861,3.0506-5.006,5.9971-5.0037c1.9593,0.0015,3.699,0.956,4.8189,2.4339c0.6904-0.3091,1.4505-0.4818,2.2511-0.4812 c2.1922,0.0017,4.0882,1.2932,5.0258,3.1759c0.9567-0.7645,2.1545-1.2232,3.4585-1.2222c0.5297,0.0004,1.0401,0.0815,1.5261,0.2223 c-0.7688-2.2807-2.8627-3.9207-5.3338-3.9226c-1.304-0.001-2.5018,0.4577-3.4585,1.2222 c-0.9376-1.8828-2.8336-3.1742-5.0258-3.1759c-0.8005-0.0006-1.5607,0.1721-2.2511,0.4812 c-1.1199-1.4778-2.8597-2.4324-4.8189-2.4339c-2.9465-0.0023-5.4064,2.1427-5.9971,5.0037 c-0.3478-0.085-0.7061-0.1407-1.0785-0.141c-2.6034-0.002-4.7163,2.1764-4.7184,4.8646l-0.0063,7.7891 c-0.0009,1.071,0.847,1.9479,1.8842,1.9487l0.9429,0.0007c0.3605,0.0003,0.6951-0.1105,0.9824-0.2934L19.8066,24.8075z"/>
    </g>
    <g id="line">
      <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M49.5,50.5h6c2.2,0,4-1.8,4-4v-14c0-2.2-1.8-4-4-4h-6"/>
      <polyline fill="none" stroke="#000000" stroke-width="2.0185" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" points="38.5938,23.2301 48.9997,23.2301 48.9997,60 20,60 20,39.6348"/>
      <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M20.2515,31.3124c0.753-0.2628,1.3009-1.0182,1.3016-1.9033l0.0013-1.5991c0.5711,0.3722,1.2338,0.5981,1.9494,0.5987 l1.8546,0.0015c1.2022,0.0009,2.2653-0.6144,2.9581-1.5517c1.0256,1.5428,2.7125,2.5581,4.6153,2.5596 c3.1115,0.0025,5.6594-2.7007,5.662-6.0071l10.9214,0.0086c0.2098-0.627,0.3301-1.3002,0.3306-2.0036 c0.0026-3.3204-2.5278-6.0136-5.6525-6.016c-1.304-0.001-2.5018,0.4709-3.4585,1.2577c-0.9376-1.9375-2.8336-3.2665-5.0258-3.2682 c-0.8005-0.0006-1.5606,0.1771-2.2511,0.4952c-1.1199-1.5208-2.8597-2.5031-4.819-2.5046c-2.9465-0.0023-5.4063,2.205-5.997,5.1492 c-0.3479-0.0874-0.7061-0.1448-1.0785-0.1451c-2.6033-0.0021-4.7162,2.2396-4.7184,5.0059l-0.0063,8.0154 c-0.0009,1.1021,0.847,2.0045,1.8842,2.0053l0.9429,0.0007C19.87,31.4116,20.0669,31.3768,20.2515,31.3124"/>
    </g>
  </svg>
      <line x1="63" y1="26" x2="60" y2="31" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <circle cx="31.5" cy="23.5" r="0.5" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <circle cx="38.5" cy="23.5" r="0.5" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <circle cx="35.5" cy="50.5" r="0.5" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <line x1="53.677" y1="9.9536" x2="59.0703" y2="15.3469" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <line x1="59.8939" y1="11.196" x2="52.7703" y2="13.9501" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <line x1="55.3315" y1="16.2584" x2="57.3327" y2="8.8878" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <line x1="55.677" y1="39.9536" x2="61.0703" y2="45.3469" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <line x1="61.8939" y1="41.196" x2="54.7703" y2="43.9501" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <line x1="57.3315" y1="46.2584" x2="59.3327" y2="38.8878" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    </g>
  <svg width="70.636" height="86.636" viewBox="0 -5 70.636 86.636">
     <path d="M32.7567,71.1383a13.81,13.81,0,0,0,6.5219-1.0536l4.7663-1.9066,4.7664-5.72a28.1609,28.1609,0,0,0,2.86-5.72c.9533-2.86,1.9065-3.4318,2.6692-3.4318a4.1682,4.1682,0,0,1,1.7158.572s.6673,2.0972.1907,2.86c0,0-2.0019,3.05-1.43,2.3831a17.1822,17.1822,0,0,1,2.4785-.3813c.7626,0,3.5271.3813,3.8131,2.2879a3.6809,3.6809,0,0,0,1.0486,2.86c.9638,1.417,1.2817,3.014.6673,3.8131-.7853,1.0212-3.3652,1.0927-5.6353-.9188q-.6743-.4473-1.3474-.8924-1.0855-.7178-2.1687-1.43s-2.1926,1.3345-4.957,3.2411a16.7389,16.7389,0,0,1-7.812,3.1847,15.2771,15.2771,0,0,1-6.0707-.427" fill="#92d3f5" stroke="#92d3f5" stroke-miterlimit="10" stroke-width="2"/>
      <g id="line">
      <path d="M5.7237,62.6959s2.2879,1.2392,8.77,2.6691a210.2877,210.2877,0,0,0,21.7346,3.05" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <path d="M51.6711,57.7389s.9536-3.6755,2.86-3.6755a2.1691,2.1691,0,0,1,1.2741.49,2.516,2.516,0,0,1,.5977,2.6681" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <path d="M50.5013,67.49a4.6978,4.6978,0,0,1,5.044-1.7656" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <path d="M58.4333,68.6594s3.1458,2.1926,4.1944.6673c.572-.8579.858-2.86-2.0018-3.7177" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
      <path d="M32.6933,71.1256a13.6291,13.6291,0,0,0,9.1922-1.0837c3.5271-2.3832,5.9728-8.49,14.5522-9.4432" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    </g>
  </svg>
</svg>

## **Surfing Lion**

Alle dem Kopf des Surfers zugehörigen Elemente wurden mit einem Löwenkopf SVG ersetzt.

<svg id="emoji" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 200 200">
  <g id="color"transform="translate(60,0)">
    <path fill="#A57939" d="M18.921,25.5021c-0.75,0.25-8.5,9.3333-9.25,15.0833s-0.3333,8.0833-0.3333,8.0833 s2.8333,8.75,11.1667,13.0833c0,0,13.0833,13.1667,30.0833,0.25c0,0,8.3333-2.8333,12-14.5833l-0.3333-9.6667l-2.4167-6.1667 c0,0-4.5-4.3333-4.6667-4.75c-0.1667-0.4167-5.4167-4-5.4167-4l-1.9167-0.5833L23.921,22.6688L18.921,25.5021z" stroke="none"/>
    <path fill="#F4AA41" d="M60.0877,21.2105l0.25-5.75l-1.125-3.875l-5.625-0.75l-5.25,2.5l-3.125,2.625l-3.25-5.375l-5.875-2.75 l-10.125,2l-1.125,0.25c0,0-2.375,1.75-2.25,2.5c0,0-6.75-3-9.625-0.375c0,0-3.75,6.875,0.375,11.375l4,3.5 c0,0-9.5,8.625,1.25,19.5c0,0-2.6198,5.6214,1.1127,11.9173l3.2206,6.666c6,5.3333,19.4167,5.0833,25.4167-0.25l2.3253-4.8129 c0.9155-1.0835,4.6646-5.941,3.6747-11.7704c0,0,8.5-8.125,1.625-20.75l-1.625-1.5l3-1.625L60.0877,21.2105z" stroke="none"/>
    <path fill="#A57939" d="M22.3377,12.398c0,0,1-1.9375,3.875-3s5.8125-1.6875,5.8125-1.6875s6.4375,0.9375,6.9375,1 s6,6.3125,6,6.3125l0.4375,2.4375c0,0-1.8125,1.875-6.5625-0.5625s-5.8125-2.375-6-2.25c-0.1875,0.125-5.625,2.3125-5.625,2.3125 l-2.0625-1.6875L22.3377,12.398z" stroke="none"/>
    <path fill="#FFFFFF" d="M47.671,42.3355c0.0834-0.2084,1.5-8.6667,1.5-8.6667h-0.1666c0,0-2.6667,4.7917-5.625,5.6667l-0.5,1.5416 l0.0937,1.5181c-0.6256-0.0616-1.2596-0.024-1.6979,0.2527c-1.1875,0.75-2.375,0.5-2.375,0.5l-1.8125,1.6875l-0.5625,0.875 l-1.6875-0.5625c0,0-0.6875-2-0.875-2.0625c-0.1875-0.0625-2.0625-0.75-2.0625-0.75l-1.1875,0.4375 c0,0-0.9572-0.3216-1.9857-0.1018l0.1107-1.7941l-0.5-1.5416c-2.9583-0.875-5.625-5.6667-5.625-5.6667H22.546 c0,0,1.4167,8.4583,1.5,8.6667c0.0643,0.1606,1.7091,1.8027,2.4614,2.5486c-0.7147,2.222,0.2053,4.6389,0.2053,4.6389l2.25,2.8125 l5.25-0.75l1.9375-1.5625l1.8125,0.9375l3.9375,1.5l2.5-1.3125c0,0,1.6875-4.5,1.75-4.6875 c0.0327-0.098-0.2592-1.0667-0.5452-1.9694C46.4254,43.6732,47.6166,42.4716,47.671,42.3355z" stroke="none"/>
    <path fill="#f4aa41" d="M27.046,18.0855c0,0,0.4583,2.875-2.2917,5.7083c0,0-4.3333,0.9167-4.5417,1.0417 c-0.2083,0.125-2.3333,1.3333-2.6667,1.5c-0.3333,0.1667-1.7083-0.2917-2.0417-0.5417s-3.4583-5.5-3.4583-5.5l0.1667-3.625 l1.0417-4.375l4.6667-0.5833l4,1.0417l3.8333,3.0417L27.046,18.0855z" stroke="none"/>
    <path fill="#f4aa41" d="M45.033,17.2521c0,0-0.4583,2.875,2.2917,5.7083c0,0,4.3333,0.9167,4.5417,1.0417 c0.2083,0.125,2.3333,1.3333,2.6667,1.5s1.7083-0.2917,2.0417-0.5417c0.3333-0.25,3.4583-5.5,3.4583-5.5l-0.1667-3.625 l-1.0417-4.375l-4.6667-0.5833l-4,1.0417l-3.8333,3.0417L45.033,17.2521z" stroke="none"/>
    <path fill="#FFFFFF" d="M27.671,51.3355l2,4.5l2.5833,1.5833l5.75,0.4167l4.4167-1.5833l2.4167-5.25l-2.9375,1.4583l-4.3958-1.4583 l-1.5-1.3333l-3.0833,1.6667c0,0,0,1.3333-1.75,0.9167C29.421,51.8355,27.671,51.3355,27.671,51.3355z" stroke="none"/>
  </g>
  <g id="line" transform="translate(60,0)">
    <ellipse transform="matrix(0.5156 -0.8568 0.8568 0.5156 -13.1061 39.9485)" cx="28.7782" cy="31.5656" rx="2" ry="2" fill="#000000" stroke="none"/>
    <ellipse transform="matrix(0.8568 -0.5156 0.5156 0.8568 -10.0526 26.9285)" cx="43.4629" cy="31.5656" rx="2" ry="2" fill="#000000" stroke="none"/>
    <line fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" x1="36.0282" y1="46.2322" x2="36.0282" y2="48.9822"/>
  </g>
  <g id="line">
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M100.3928,43.0656c0,0-1.8705-1.3333-2.9394,2.0833l-1.4252,1.0833l-1.4252-1.0833c-1.0689-3.4167-2.9394-2.0833-2.9394-2.0833"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M102.9467,39.9822l2.1482,3.519c0.1941,0.3179,0.3227,0.6662,0.3793,1.0272l0.326,2.0779c0.0856,0.5453,0.0042,1.1018-0.235,1.6067 l-1.1399,2.407c-0.4169,0.8804-1.2717,1.5195-2.2925,1.7141l0,0c-0.6475,0.1234-1.3206,0.0597-1.9273-0.1826l-1.3016-0.5197 c-0.3174-0.1267-0.6105-0.2999-0.868-0.5128l-1.3748-1.1369h-1.2661l-1.3748,1.1369c-0.2575,0.2129-0.5505,0.3861-0.868,0.5128 l-1.3016,0.5197c-0.6067,0.2423-1.2798,0.306-1.9273,0.1826h0c-1.0208-0.1946-1.8756-0.8337-2.2925-1.7141l-1.1399-2.407 c-0.2391-0.505-0.3205-1.0614-0.235-1.6067l0.326-2.0779c0.0566-0.361,0.1853-0.7093,0.3793-1.0272l2.1482-3.519"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M90.5366,55.5239l0.7708,0.7941c0.8297,0.8549,1.9545,1.3607,3.1446,1.4142l3.0167,0.1356 c1.1576,0.052,2.2933-0.3278,3.1868-1.0657l0.8644-0.714"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M77.7391,26.8288c-9.9983-4.0396-4.7942-14.1799-4.7942-14.1799c7.5833-4.5833,13.833,4.75,13.833,4.75 s4.8857-4.6468,12.3055-1.3781"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M84.0282,23.1489c0,0-17.3333,6.0833-13.75,25"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M79.456,45.1873c-2.6014,3.7405-3.5847,9.9899,4.4889,19.4616"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M84.0282,27.7322c0,0-5.6115,8.4105,2.1526,17.7886"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M85.3605,10.9187c0,0,12.7053-9.5,19.8616,5.3333"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M105.2221,16.4903c0,0,6.2497-9.3333,13.833-4.75c0,0,5.2041,10.1403-4.7942,14.1799"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M107.9718,22.2403c0,0,17.3333,6.0833,13.75,25"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M113.6231,46.2342c1.6075,3.8321,1.2349,9.5252-5.5679,17.5062"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M107.9718,26.8237c0,0,5.6115,8.4105-2.1526,17.7886"/>
  </g>
<svg id="emoji" xmlns="http://www.w3.org/2000/svg" viewBox="-2 0 80.636 68.636">
  <g id="skin" transform="translate(0,10)">    
    <path d="M41.2252,21.7565A38.5074,38.5074,0,0,0,40.21,29.785c-.0095,1.9332.52,3.3974.4538,5.3335l.6873,8.01s-1.2612,9.36-1.9247,11.3992c-.2945.9065-2.0543.8369-2.0543.8369V42.9725l-1.9065-7.6262h-.9533l-5.72,7.6262L24.98,52.5052s-1.36-.4089-1.4337-1.3593c-.1583-2.0658,1.5881-11.0637,1.5881-11.0637l4.612-8.5489,1.9065-4.7664.04-3.6148A21.4423,21.4423,0,0,0,29.09,20.5849c-.88-.6768-1.8226-.7769-4.0152.3671a20.9394,20.9394,0,0,1-6.7682,2.0018c-1.43.0954-6.3869,0-6.7682,0a1.7742,1.7742,0,0,1-1.9037-1.9361s8.2906.03,9.8158-.5424,9.7234-3.9084,9.7234-3.9084L43.187,15.3277l11.4392,6.3869,3.672,1.4928s-.4308,1.9389-2.814,1.1763a31.64,31.64,0,0,1-5.6014-2.4117c-1.8427-1.08-3.1516-2.0877-4.8169-3.1735a2.4631,2.4631,0,0,0-2.1411-.162,1.577,1.577,0,0,0-1.2745,1.407C41.5226,20.56,41.3548,21.1912,41.2252,21.7565Z" fill="#fadcbc"/>
  </g>
  <g id="color">
    <path d="M32.7567,71.1383a13.81,13.81,0,0,0,6.5219-1.0536l4.7663-1.9066,4.7664-5.72a28.1609,28.1609,0,0,0,2.86-5.72c.9533-2.86,1.9065-3.4318,2.6692-3.4318a4.1682,4.1682,0,0,1,1.7158.572s.6673,2.0972.1907,2.86c0,0-2.0019,3.05-1.43,2.3831a17.1822,17.1822,0,0,1,2.4785-.3813c.7626,0,3.5271.3813,3.8131,2.2879a3.6809,3.6809,0,0,0,1.0486,2.86c.9638,1.417,1.2817,3.014.6673,3.8131-.7853,1.0212-3.3652,1.0927-5.6353-.9188q-.6743-.4473-1.3474-.8924-1.0855-.7178-2.1687-1.43s-2.1926,1.3345-4.957,3.2411a16.7389,16.7389,0,0,1-7.812,3.1847,15.2771,15.2771,0,0,1-6.0707-.427" fill="#92d3f5" stroke="#92d3f5" stroke-miterlimit="10" stroke-width="2"/>
  </g>
  <g id="line">
    <path d="M5.7237,62.6959s2.2879,1.2392,8.77,2.6691a210.2877,210.2877,0,0,0,21.7346,3.05" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <path d="M51.6711,57.7389s.9536-3.6755,2.86-3.6755a2.1691,2.1691,0,0,1,1.2741.49,2.516,2.516,0,0,1,.5977,2.6681" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <path d="M50.5013,67.49a4.6978,4.6978,0,0,1,5.044-1.7656" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <path d="M58.4333,68.6594s3.1458,2.1926,4.1944.6673c.572-.8579.858-2.86-2.0018-3.7177" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <path d="M32.6933,71.1256a13.6291,13.6291,0,0,0,9.1922-1.0837c3.5271-2.3832,5.9728-8.49,14.5522-9.4432" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <path d="M10.5851,31.0473h4.8617a18.6309,18.6309,0,0,0,8.5794-2.3832,22.68,22.68,0,0,1,7.6262-2.86,77.4464,77.4464,0,0,1,8.5794-.4766,13.6688,13.6688,0,0,1,7.6262,2.3831,30.1609,30.1609,0,0,0,6.1963,3.8131c1.8112.7626,3.3364,1.43,3.3364,1.43" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
  </g>
  <g id="line" transform="translate(0,10)">
  <path d="M40.7661,20.0435s-1.052,7.93-.9934,10.03a21.2083,21.2083,0,0,0,.5105,3.8426A92.3713,92.3713,0,0,1,40.82,44.8791l-1.0976,8.5794c-.1722,1.0486-.8609,1.9065-1.55,1.9065s-1.2914-.8579-1.2914-1.9065V44.8791a17.5053,17.5053,0,0,0-.43-3.7178L35.59,37.2529c-.2583-1.0486-.6027-1.8112-.8609-1.8112s-5.7956,5.4126-6.3508,7.3163c-.4,1.3737-1.8725,7.8655-1.8725,7.8655-.2574.9637-.9452,1.6186-1.6916,1.469-.7637-.1526-1.0038-1.1935-.96-2.1354a77.0643,77.0643,0,0,1,.9909-8.3344c.65-1.9294,4.6359-8.0838,4.6359-8.0838A15.2485,15.2485,0,0,0,31.1551,29.75a21.3952,21.3952,0,0,0,.6465-5.652,5.3294,5.3294,0,0,0-.8609-2.86,5.107,5.107,0,0,0-.8609-.9532" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
  </g>
  </svg>
</svg>


## **Zombie**

Hier haben wir an der offenen stelle des Schädels ein Hirn eingefügt.

<svg id="emoji" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 72 72">
  <g id="color">
      <path d="M53.0521,51.4424s6.0211-3.94,3.7911-8.3254c-1.865-3.6679-3.05-2.9718-5.5723-6.6808,0,0,4.5573.7879,4.9282-3.0695,0,0-4.1419-.5987-4.5869-2.6015,2.032.3261.315-14.02-6.6162-6.9837.2355-1.2222,8.9306,17.7872-7.1192,21.454-15.3929,3.5166-17.0529-28.1861-2.3575-28.141l2.7526,1.31c.609-.5622,1.5694-2.5768.5622-4.0525-1.4611-2.1406-6.4019-3.4788-13.79.6178-2.8847-.8727-7.5511,13.4479-10.4593,13.8716,0,0,2.5221,3.4864,5.5634,1.3352,0,0-.0313,1.2369-3.7089,8.3082-4.4193,8.4972,4.9328,11.9654,4.1292,11.9166,0,0,5.2327-3.6286,6.9235-2.8668,2.3857,1.0749,8.0418,8.8,17.4322.0742C44.9238,47.6092,51.6993,48.6878,53.0521,51.4424Z" fill="#3f3f3f"/>
  <svg id="emoji" xmlns="http://www.w3.org/2000/svg" viewBox="-82.5 -17 190 190">
  <g id="color">
    <line fill="#ea5a47" x1="16" y1="35" x2="25.875" y2="35" stroke="none"/>
    <path fill="#ea5a47" d="M25.875,35c3.4167,0,4.75-2.9167,4.75-6.1667" stroke="none"/>
    <line fill="#ea5a47" x1="16" y1="45.5" x2="19.75" y2="45.5" stroke="none"/>
    <line fill="#ea5a47" x1="35.2997" y1="45.5" x2="35.2997" y2="39.4375" stroke="none"/>
    <path fill="#ea5a47" d="M35.2997,39.4375c0-2.2455,1.2003-5.25,5.0756-5.25" stroke="none"/>
    <line fill="#ea5a47" x1="58.4583" y1="34.5417" x2="49.875" y2="34.5417" stroke="none"/>
    <path fill="#FFA7C0" d="M40.375,45.5c0,0,0.1642,10.5-7.9583,10.5H16c-7.2083,0-7.6667-10.5,0-10.5C8.7917,45.5,8.3333,35,16,35 c-8.1667-7.25,1.875-13.5625,6.5-8.6875c-4.799-6.625,5.375-10.3125,8.875-5C30.9627,16,36.2222,15.0417,41.1003,19.024 l-0.4336,0.351c2.375-2.375,10.1776-1.0833,10.1776,5.3141l-2.2192,1.6234c6.8646-6.8646,14.2083,4.1875,8.5,8.2292h1.3333 c4.75,0,5.2917,10.9583-1.3333,10.9583H29.2917" stroke="none"/>
    <path fill="#ea5a47" d="M40.6667,19.375c-2.4167,2.4167-0.2822,3.1782-4.2707,7.1667" stroke="none"/>
  </g>
  <g id="hair"/>
  <g id="skin"/>
  <g id="skin-shadow"/>
  <g id="line">
    <line fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" x1="16" y1="35" x2="25.875" y2="35"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M25.875,35c3.4167,0,4.75-2.9167,4.75-6.1667"/>
    <line fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" x1="16" y1="45.5" x2="19.75" y2="45.5"/>
    <line fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" x1="35.2997" y1="45.5" x2="35.2997" y2="39.4375"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M35.2997,39.4375c0-2.2455,1.2003-5.25,5.0756-5.25"/>
    <line fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" x1="58.4583" y1="34.5417" x2="49.875" y2="34.5417"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M40.375,45.5c0,0,0.1642,10.5-7.9583,10.5H16c-7.2083,0-7.6667-10.5,0-10.5C8.7917,45.5,8.3333,35,16,35 c-8.1667-7.25,1.875-13.5625,6.5-8.6875c-4.799-6.625,5.375-10.3125,8.875-5C30.9627,16,36.2222,15.0417,41.1003,19.024 l-0.4336,0.351c2.375-2.375,10.1776-1.0833,10.1776,5.3141l-2.2192,1.6234c6.8646-6.8646,14.2083,4.1875,8.5,8.2292h1.3333 c4.75,0,5.2917,10.9583-1.3333,10.9583H29.2917"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M40.6667,19.375c-2.4167,2.4167-0.2822,3.1782-4.2707,7.1667"/>
  </g>
</svg>
<g>
    <path d="M35.1853,17.2058c-5.8765.5287-10.5159,6.6407-10.5159,14.1212,0,7.8277,5.0764,14.1733,11.3386,14.1733S47.3467,39.1547,47.3467,31.327a17.2594,17.2594,0,0,0-.7674-5.0941,9.9175,9.9175,0,0,1-11.394-9.0271Z" fill="#b1cc33"/>
    <path d="M54.9455,60.9585s2-12.6032-10-12.6032c-3.1918,2.128-5.9264,3.5985-9,3.5922h.125c-3.0736.0063-5.8081-1.4642-9-3.5922-12,0-10,12.6032-10,12.6032" fill="#b1cc33"/>
    <path d="M46.362,48.3253l-.9075.8851a15.6367,15.6367,0,0,1-5.3451,5.81L38.1065,60.765l-2-4.5853c-3.337.02-6.674-2.2824-9.3481-6.9693l-.55-.9118c-10.9306.6777-9.0393,12.6875-9.0393,12.6875l3.1531-.007,2.0839-4.7825,1.5287,4.8108,31.18-.05" fill="#d0cfce"/>
    <path d="M32.0082,38.3478s8-3.11,8,0C40.0082,44.59,32.0082,38.3478,32.0082,38.3478Z" fill="#fcea2b"/>
    <path d="M42.5157,52.7743c6.4062,1.661,6.5337,5.0343,7.1339,8.1842h5.1128s1.8925-11.904-9.05-12.5747q-.46-.0282-.95-.0285" fill="#9b9b9a"/>
    <path d="M30.0082,29.9816v2.041a2.1088,2.1088,0,0,0,1.7064,2.1339,2.0016,2.0016,0,0,0,2.2936-1.9791V29.9816a.0571.0571,0,0,0-.0571-.0571H30.0653A.057.057,0,0,0,30.0082,29.9816Z" fill="#5c9e31"/>
    <path d="M38.0082,29.9245v2.2529a2,2,0,0,0,4,0V29.9245Z" fill="#5c9e31"/>
    <path d="M42.0082,29.9662a2,2,0,1,1-2-2,2.0007,2.0007,0,0,1,2,2" fill="#fff"/>
    <path d="M34.0082,29.9662a2,2,0,1,1-2-2,2.0007,2.0007,0,0,1,2,2" fill="#fff"/>
  </g>
  <g id="line">
    <path d="M35.1853,17.2058c-5.8765.5287-10.5159,6.6407-10.5159,14.1212,0,7.8277,5.0764,14.1733,11.3386,14.1733S47.3467,39.1547,47.3467,31.327a17.2594,17.2594,0,0,0-.7674-5.0941,9.9175,9.9175,0,0,1-11.394-9.0271Z" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>    
    <path d="M35.1853,17.2058q.0408.48.1262.9464A9.9978,9.9978,0,0,0,44.7328,26.34q.2037.0082.4093.0082a10.0162,10.0162,0,0,0,1.4372-.1149" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <path d="M32.0082,38.3478s8-3.11,8,0C40.0082,44.59,32.0082,38.3478,32.0082,38.3478Z" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <line x1="39.4412" y1="40.0644" x2="35.142" y2="40.0644" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <line x1="36.9515" y1="40.0644" x2="36.9515" y2="37.1387" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5"/>
    <path d="M26.66,48.974c2.6741,4.6869,6.0111,6.99,9.3481,6.9693l2,4.0183,2.0029-5.1777a15.6376,15.6376,0,0,0,5.3451-5.81" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <line x1="43.5576" y1="57.2892" x2="42.8019" y2="59.952" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <polyline points="20.224 59.92 22.308 56.357 23.836 59.92" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <path d="M55.008,60.9662a1,1,0,0,1-1-1v-3c0-4.4517-4.4961-7.81-8.6518-7.9922-6.2051,5.0117-12.4912,5.0117-18.6963,0-4.1558.1817-8.6519,3.5405-8.6519,7.9922v3a1,1,0,0,1-2,0v-3c0-5.3247,5.14-9.9976,11-10h0a.9994.9994,0,0,1,.64.2319c5.625,4.6875,11.0947,4.6875,16.72,0a.9994.9994,0,0,1,.64-.2319h0c5.8594.0024,11,4.6753,11,10v3A1,1,0,0,1,55.008,60.9662Z"/>
    <path d="M42.0082,29.9662a2,2,0,1,1-2-2,2.0007,2.0007,0,0,1,2,2" fill="none" stroke="#000" stroke-miterlimit="10" stroke-width="1.5"/>
    <path d="M34.0082,29.9662a2,2,0,1,1-2-2,2.0007,2.0007,0,0,1,2,2" fill="none" stroke="#000" stroke-miterlimit="10" stroke-width="1.5"/>
    <path d="M48.5353,22.8288c5.0381.18,3.4578,6.7348,3.03,7.2054a4.4742,4.4742,0,0,0,4.6831,2.5273c-.3149,3.5538-3.68,3.2945-4.7574,3.2707a9.3964,9.3964,0,0,0,2.899,4.6831,5.02,5.02,0,0,1,.5947,7.7308" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <path d="M18.1522,47.2228c-3.1087-2.9376-3.6951-8.0927-.2186-11.1464a7.2646,7.2646,0,0,0,2.1143-5.2045c-2.6565,1.2469-5.1757-.6366-5.9093-1.6807,1.5855-.3927,4.1821-3.7919,4.6165-5.89,1.48-5.5,5.1875-9.769,11.5628-10.6191,4.2819-.5709,6.484.4078,7.6666,2.1614" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
  </g>
</svg>

### **Verzerrt**
Diese Kunstwerke entstanden durch das verschieben der Füllfläche von Emojis, während die schwarzen Konturpfade nicht berührt worden sind. Die anderen Flächen und Details bestanden aus einer inkonsequenten Mischung aus Versalien und Kleinbuchstaben, sodass das verschieben der Startposition der Pfade nur einen gewissen Anteil des Elements betraf, so entstand eine Art aufteilender Effekt der ein Emoji in zwei Teile spaltet, aber dennoch verbunden bleibt durch die Absoluten Koordinatenangaben der Pfade.

## **Dripping Unicorn**

<svg id="emoji" xmlns="http://www.w3.org/2000/svg" viewBox="0 6 100 120">
  <g id="color">
    <path fill="#FFFFFF" d="M23.7544,61.3618l1.6667,7.1667l-5.3333,5.3333l-8.3333,14.3333l1,4.6667l2.1667,1.3333l4-0.1667 l3.5-3.3333l6.8333-1.8333c0,0,1.3333,1.5,2.1667,3s3.6667,4.1667,3.6667,4.1667l0.5,6l-1.8333,6.1667l-2,2.8333 c0,0,22,9.5,33.1667-7l-0.5-6l-1.8333-5l-3.3333-5.1667l-1-1.5l-0.1667-5.1667l-2.8333-5.3333l-5-3l-2.6667-4.5l-5.1667-4.1667 l-6.5-1.5l-5.6667,1l-4.1667-2.1667L23.7544,12.3618z" stroke="none"/>
    <path fill="#EA5A47" d="M50.671,73.155l5.2083,4.095c0,0,5.5638,8.2181-0.3258,17.8201c-7.0492,11.4924,0,0,0,0 c-1.6183,3.4754-2.3141,6.7423-1.738,9.7216l-5.3111-4.4167V34.2917L50.671,23.155z" stroke="none"/>
    <polyline fill="#EA5A47" points="25.8985,69.2712 10.7847,12.0212 15.951,18.1399 21.1747,23.995 25.8985,19.2712" stroke="none"/>
    <path fill="#92D3F5" d="M29.7367,63.6311l10.7677,0.1362c0,0,9.2377,4.0661,10.5355,11.8161l0.6874,8.9567 c-2.6337,6.5386-3.0562,14.1267,2.0883,20.8336l0,0c0,0-7.1444,1.3215-9.8944-7.1094L42.3377,43.5l0.3258-6.0341l1.4169-5.6426 l-0.2833-4.8929l-2.2761-4.3124l-3.5322-2.8413l-5.792-2.0801L29.7367,13.6311" stroke="none"/>
    <path fill="#61B2E4" d="M58.4549,86.75c0,0,5.5192,6.4066,6.9982,15.1193c0.1838,1.0826,0.1251,2.193-0.1377,3.2591 c-0.4317,1.7512-0.8179,4.9979,0.1452,7.3825c0.4689,1.1611-0.5621,2.3655-1.7883,2.1115 c-3.7094-0.7686-9.2437-3.6474-10.2567-8.0876c-0.0239-0.1047-0.0368-0.2138-0.0417-0.321l-0.266-5.7459 c-0.0132-0.2857,0.0516-0.5695,0.1875-0.8211l3.692-6.8359c0.0666-0.1233,0.1164-0.2549,0.1482-0.3914L58.4549,36.75" stroke="none"/>
  </g>
  <g id="hair"/>
  <g id="skin"/>
  <g id="skin-shadow"/>
  <g id="line">
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M58.4549,37.7826C60.2229,40.1443,65,44.4647,64.5,54.0208"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M32.5,41.8854c0,0,8.4783,6.7823,0,18.7647"/>
    <polyline fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" points="24.809,19.1338 10.25,11.75 21.1747,23.995"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M35.1962,30.8696c0.5489,8.3555-9.3225,9.703-11.954,10.3347c-0.3325,0.0798-0.6318,0.25-0.8736,0.4919l-2.2227,2.2227 c-0.3494,0.3494-0.8234,0.5458-1.3176,0.5458h-3.5121c-1.203,0-2.2711-0.7698-2.6515-1.9111l-0.531-1.5931 c-0.258-0.774-0.1649-1.6222,0.2549-2.3218l8.7862-14.6436l4.7238-4.7238l-2.1151-6.9054c0,0,7.8026-0.6987,8.4135,5.3308 c0,0,16.9281,2.4418,10.5531,19.383c0,0-1.625,5.9489,2.375,11.1846"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M30.9167,14.0208c0,0,22.2444-4.0208,19.9583,19.9583"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M49.9187,23.155c0,0,14.7665,6.5865,5.4563,22.22c0,0-5.375,6.5625,0.625,13.6042"/>
  </g>
</svg>

## **Split Lion**
<svg id="emoji" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 180 180">
  <g id="color">
    <path fill="#A57939" d="M118.921,25.5021c-0.75,0.25-8.5,9.3333-9.25,15.0833s-0.3333,8.0833-0.3333,8.0833 s2.8333,8.75,11.1667,13.0833c0,0,13.0833,13.1667,30.0833,0.25c0,0,8.3333-2.8333,12-14.5833l-0.3333-9.6667l-2.4167-6.1667 c0,0-4.5-4.3333-4.6667-4.75c-0.1667-0.4167-5.4167-4-5.4167-4l-1.9167-0.5833L23.921,22.6688L18.921,25.5021z" stroke="none"/>
    <path fill="#F4AA41" d="M160.0877,21.2105l0.25-5.75l-1.125-3.875l-5.625-0.75l-5.25,2.5l-3.125,2.625l-3.25-5.375l-5.875-2.75 l-10.125,2l-1.125,0.25c0,0-2.375,1.75-2.25,2.5c0,0-6.75-3-9.625-0.375c0,0-3.75,6.875,0.375,11.375l4,3.5 c0,0-9.5,8.625,1.25,19.5c0,0-2.6198,5.6214,1.1127,11.9173l3.2206,6.666c6,5.3333,19.4167,5.0833,25.4167-0.25l2.3253-4.8129 c0.9155-1.0835,4.6646-5.941,3.6747-11.7704c0,0,8.5-8.125,1.625-20.75l-1.625-1.5l3-1.625L60.0877,21.2105z" stroke="none"/>
    <path fill="#A57939" d="M122.3377,12.398c0,0,1-1.9375,3.875-3s5.8125-1.6875,5.8125-1.6875s6.4375,0.9375,6.9375,1 s6,6.3125,6,6.3125l0.4375,2.4375c0,0-1.8125,1.875-6.5625-0.5625s-5.8125-2.375-6-2.25c-0.1875,0.125-5.625,2.3125-5.625,2.3125 l-2.0625-1.6875L22.3377,12.398z" stroke="none"/>
    <path fill="#FFFFFF" d="M147.671,42.3355c0.0834-0.2084,1.5-8.6667,1.5-8.6667h-0.1666c0,0-2.6667,4.7917-5.625,5.6667l-0.5,1.5416 l0.0937,1.5181c-0.6256-0.0616-1.2596-0.024-1.6979,0.2527c-1.1875,0.75-2.375,0.5-2.375,0.5l-1.8125,1.6875l-0.5625,0.875 l-1.6875-0.5625c0,0-0.6875-2-0.875-2.0625c-0.1875-0.0625-2.0625-0.75-2.0625-0.75l-1.1875,0.4375 c0,0-0.9572-0.3216-1.9857-0.1018l0.1107-1.7941l-0.5-1.5416c-2.9583-0.875-5.625-5.6667-5.625-5.6667H22.546 c0,0,1.4167,8.4583,1.5,8.6667c0.0643,0.1606,1.7091,1.8027,2.4614,2.5486c-0.7147,2.222,0.2053,4.6389,0.2053,4.6389l2.25,2.8125 l5.25-0.75l1.9375-1.5625l1.8125,0.9375l3.9375,1.5l2.5-1.3125c0,0,1.6875-4.5,1.75-4.6875 c0.0327-0.098-0.2592-1.0667-0.5452-1.9694C46.4254,43.6732,47.6166,42.4716,47.671,42.3355z" stroke="none"/>
    <path fill="#f4aa41" d="M127.046,18.0855c0,0,0.4583,2.875-2.2917,5.7083c0,0-4.3333,0.9167-4.5417,1.0417 c-0.2083,0.125-2.3333,1.3333-2.6667,1.5c-0.3333,0.1667-1.7083-0.2917-2.0417-0.5417s-3.4583-5.5-3.4583-5.5l0.1667-3.625 l1.0417-4.375l4.6667-0.5833l4,1.0417l3.8333,3.0417L27.046,18.0855z" stroke="none"/>
    <path fill="#f4aa41" d="M145.033,17.2521c0,0-0.4583,2.875,2.2917,5.7083c0,0,4.3333,0.9167,4.5417,1.0417 c0.2083,0.125,2.3333,1.3333,2.6667,1.5s1.7083-0.2917,2.0417-0.5417c0.3333-0.25,3.4583-5.5,3.4583-5.5l-0.1667-3.625 l-1.0417-4.375l-4.6667-0.5833l-4,1.0417l-3.8333,3.0417L45.033,17.2521z" stroke="none"/>
    <path fill="#FFFFFF" d="M127.671,51.3355l2,4.5l2.5833,1.5833l5.75,0.4167l4.4167-1.5833l2.4167-5.25l-2.9375,1.4583l-4.3958-1.4583 l-1.5-1.3333l-3.0833,1.6667c0,0,0,1.3333-1.75,0.9167C29.421,51.8355,27.671,51.3355,27.671,51.3355z" stroke="none"/>
  </g>
  <g id="hair"/>
  <g id="skin"/>
  <g id="skin-shadow"/>
  <g id="line">
    <ellipse transform="matrix(0.5156 -0.8568 0.8568 0.5156 -13.1061 39.9485)" cx="28.7782" cy="31.5656" rx="2" ry="2" fill="#000000" stroke="none"/>
    <ellipse transform="matrix(0.8568 -0.5156 0.5156 0.8568 -10.0526 26.9285)" cx="43.4629" cy="31.5656" rx="2" ry="2" fill="#000000" stroke="none"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M40.3928,43.0656c0,0-1.8705-1.3333-2.9394,2.0833l-1.4252,1.0833l-1.4252-1.0833c-1.0689-3.4167-2.9394-2.0833-2.9394-2.0833"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M42.9467,39.9822l2.1482,3.519c0.1941,0.3179,0.3227,0.6662,0.3793,1.0272l0.326,2.0779c0.0856,0.5453,0.0042,1.1018-0.235,1.6067 l-1.1399,2.407c-0.4169,0.8804-1.2717,1.5195-2.2925,1.7141l0,0c-0.6475,0.1234-1.3206,0.0597-1.9273-0.1826l-1.3016-0.5197 c-0.3174-0.1267-0.6105-0.2999-0.868-0.5128l-1.3748-1.1369h-1.2661l-1.3748,1.1369c-0.2575,0.2129-0.5505,0.3861-0.868,0.5128 l-1.3016,0.5197c-0.6067,0.2423-1.2798,0.306-1.9273,0.1826h0c-1.0208-0.1946-1.8756-0.8337-2.2925-1.7141l-1.1399-2.407 c-0.2391-0.505-0.3205-1.0614-0.235-1.6067l0.326-2.0779c0.0566-0.361,0.1853-0.7093,0.3793-1.0272l2.1482-3.519"/>
    <line fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" x1="36.0282" y1="46.2322" x2="36.0282" y2="48.9822"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M30.5366,55.5239l0.7708,0.7941c0.8297,0.8549,1.9545,1.3607,3.1446,1.4142l3.0167,0.1356 c1.1576,0.052,2.2933-0.3278,3.1868-1.0657l0.8644-0.714"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M17.7391,26.8288c-9.9983-4.0396-4.7942-14.1799-4.7942-14.1799c7.5833-4.5833,13.833,4.75,13.833,4.75 s4.8857-4.6468,12.3055-1.3781"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M24.0282,23.1489c0,0-17.3333,6.0833-13.75,25"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M19.456,45.1873c-2.6014,3.7405-3.5847,9.9899,4.4889,19.4616"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M24.0282,27.7322c0,0-5.6115,8.4105,2.1526,17.7886"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M25.3605,10.9187c0,0,12.7053-9.5,19.8616,5.3333"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M45.2221,16.4903c0,0,6.2497-9.3333,13.833-4.75c0,0,5.2041,10.1403-4.7942,14.1799"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M47.9718,22.2403c0,0,17.3333,6.0833,13.75,25"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M53.6231,46.2342c1.6075,3.8321,1.2349,9.5252-5.5679,17.5062"/>
    <path fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" stroke-miterlimit="10" d="M47.9718,26.8237c0,0,5.6115,8.4105-2.1526,17.7886"/>
  </g>
</svg>

### **Animiert**

Für die Krönung unserer Kollektion haben wir die Augen eines Mondemojis animiert, so dass sie sich hin und her bewegen. Das linke Auge funktioniert mit einem &lt;animateTransform&gt; tag, wo lediglich die Position langsam verschoben wird. Das rechte hingegen nutzt den &lt;animateMotion&gt; tag, um einem Pfad, in diesem Fall lediglich die horizontale Achse des Auges, zu folgen und so mit gleicher Geschwindigkeit sich von links nach rechts und zurück zu bewegen ohne ständig zurückzuzucken.

## **Hypnosemond**

<svg id="emoji" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 72 72">
  <g id="color">
    <circle  cx="36" cy="36" r="28" fill="#3f3f3f" stroke="#3f3f3f" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <path d="M29,62c20.0033,0,16.6634-52,16.6634-52s24.9582,7,16.6388,35S13.4011,62,29,62Z" stroke="#000" stroke-miterlimit="10" stroke-width="0.204" opacity="0.4"/>
  </g>
  <g id="line">
    <rect x="34" y="37" width="4" height="2" stroke-width="0.25" stroke="#000" stroke-linecap="round" stroke-linejoin="round"/>
    <path d="M36,64A28,28,0,0,1,36,8" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <path d="M36,8a28,28,0,0,1,0,56" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <path d="M36,39.5c1.1046,0,2.5-.8954,2.5-2H34A2,2,0,0,0,36,39.5Z" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <path d="M27,40s2.256,2.7023,1,9C41,51,47,46,47,36" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <circle cx="26.5" cy="27.5" r="5" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <circle cx="45.5" cy="27.5" r="5" fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    <circle cx="45.5" cy="27.5" r="5" fill="#fff" stroke="#000" stroke-linecap="round" stroke-linejoin="round"/>
    <g>
    <animateMotion attributeName="transform" id="rightEyeToLeft" path="M20, 25 h5 z" begin="0s" dur="4s" repeatCount="indefinite"/>
    <circle cx="22.75" cy="2.75" r="1.75" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    </g>
    <circle cx="26.5" cy="27.5" r="5" fill="#fff" stroke="#000" stroke-linecap="round" stroke-linejoin="round"/>
    <g>
    <animateTransform attributeName="transform" type="translate" from="20, 25" to="25, 25" begin="0s" dur="2.2s"   repeatCount="indefinite"/>     
    <circle cx="3.75" cy="2.75" r="1.75" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"/>
    </g>
  </g>
</svg>


Gute Nacht