# Sondaggio-Nathalia-
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sondaggio Viaggi Culturali Emozionali</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #000;
            color: #00bcd4;
            margin: 0;
            padding: 0;
        }
        h1, h2, h3, label {
            text-align: center;
        }
        .container {
            width: 80%;
            margin: 50px auto;
            padding: 20px;
            background-color: #1a1a1a;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        .question {
            margin-bottom: 30px;
            color: #00bcd4;
        }
        .question input[type="radio"] {
            margin-right: 10px;
        }
        .question input[type="text"] {
            width: 60%;
            padding: 5px;
            border-radius: 5px;
            border: 1px solid #00bcd4;
            color: #00bcd4;
            background-color: #333;
        }
        .question label {
            font-size: 18px;
            display: block;
            margin-bottom: 10px;
        }
        .submit-btn {
            background-color: #00bcd4;
            color: white;
            border: none;
            padding: 15px;
            font-size: 18px;
            width: 100%;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        .submit-btn:hover {
            background-color: #008c9e;
        }
        .container h1 {
            font-size: 32px;
        }
        .container h2 {
            font-size: 24px;
        }
        .container h3 {
            font-size: 20px;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Viaggi Culturali Emozionali: Condividi la tua esperienza!</h1>
    <h2>Sono pronto a scoprire i tuoi segreti di viaggio!</h2>
    <p>Rispondi a questo questionario e condividi la tua esperienza di viaggio con focus sui viaggi culturali emozionali! Sarò onorata di conoscere le tue abitudini, preferenze e aspettative.</p>
    
    <form id="surveyForm">
        <!-- 1. Informazioni Generali -->
        <div class="question">
            <label for="age">1. Faccia d'età: Scegli la tua fascia d'età</label>
            <input type="radio" name="age" value="18-24" required> 18-24 anni
            <input type="radio" name="age" value="25-34"> 25-34 anni
            <input type="radio" name="age" value="35-44"> 35-44 anni
            <input type="radio" name="age" value="45-54"> 45-54 anni
            <input type="radio" name="age" value="55+"> 55+ anni
        </div>

        <div class="question">
            <label for="gender">2. Genere: Scegli il tuo genere</label>
            <input type="radio" name="gender" value="Maschio" required> Maschio
            <input type="radio" name="gender" value="Femmina"> Femmina
            <input type="radio" name="gender" value="Non binario"> Non binario
            <input type="radio" name="gender" value="Preferisco non rispondere"> Preferisco non rispondere
        </div>

        <div class="question">
            <label for="relationship">3. Stato relazionale: Scegli il tuo stato relazionale</label>
            <input type="radio" name="relationship" value="Single" required> Single
            <input type="radio" name="relationship" value="Fidanzato/a"> Fidanzato/a
            <input type="radio" name="relationship" value="Sposato/a"> Sposato/a
            <input type="radio" name="relationship" value="Convivente"> Convivente
            <input type="radio" name="relationship" value="Relazione a distanza"> Relazione a distanza
        </div>

        <!-- 2. Abitudini di Viaggio -->
        <div class="question">
            <label for="frequency">4. Frequenza di viaggio: Quante volte viaggi all'anno?</label>
            <input type="radio" name="frequency" value="1-2" required> 1-2 volte
            <input type="radio" name="frequency" value="3-5"> 3-5 volte
            <input type="radio" name="frequency" value="more_than_5"> Più di 5 volte
        </div>

        <div class="question">
            <label for="destination">5. Destinazione: Preferisci viaggiare in</label>
            <input type="radio" name="destination" value="cultura_simile" required> Paesi con cultura simile alla tua
            <input type="radio" name="destination" value="cultura_differente"> Paesi con cultura diversa dalla tua
            <input type="radio" name="destination" value="storia_arte"> Paesi con storia e arte antica
            <input type="radio" name="destination" value="natura_selvaggia"> Paesi con natura e ambiente selvaggio
        </div>

        <div class="question">
            <label for="activity">6. Attività: Ti piace fare</label>
            <input type="radio" name="activity" value="musei_gallerie" required> Visite guidate a musei e gallerie d'arte
            <input type="radio" name="activity" value="citta_storiche"> Esplorare città storiche e antiche
            <input type="radio" name="activity" value="escursioni_natura"> Fare escursioni in natura e ambiente selvaggio
            <input type="radio" name="activity" value="cucine_locali"> Assaggiare cucine locali e tradizionali
            <input type="text" name="other_activity" placeholder="Altro">
        </div>

        <!-- 3. Viaggi Culturali Emozionali -->
        <div class="question">
            <label for="cultural_experience">7. Quanto conta nel tuo viaggio l’esperienza culturale?</label>
            <input type="radio" name="cultural_experience" value="molto" required> Molto
            <input type="radio" name="cultural_experience" value="poco"> Non mi interessa, preferisco fare altro
            <input type="radio" name="cultural_experience" value="media"> Non ci faccio particolare attenzione, ma se c’è ben venga
        </div>

        <div class="question">
            <label for="emotions">8. Quale emozione cerchi di provare durante il tuo viaggio?</label>
            <input type="radio" name="emotions" value="meraviglia" required> Meraviglia
            <input type="radio" name="emotions" value="sorpresa"> Sorpresa
            <input type="radio" name="emotions" value="emozione"> Emozione
            <input type="radio" name="emotions" value="calma"> Calma
            <input type="text" name="other_emotion" placeholder="Altro">
        </div>

        <button type="submit" class="submit-btn">Invia Risposte</button>
    </form>
</div>

<script>
    document.getElementById("surveyForm").addEventListener("submit", function(event) {
        event.preventDefault();

        const formData = new FormData(this);
        const data = {};
        formData.forEach((value, key) => {
            data[key] = value;
        });

        fetch("YOUR_BACKEND_URL_HERE", {
            method: "POST",
            headers: {
                "Content-Type": "application/json"
            },
            body: JSON.stringify(data)
        })
        .then(response => response.json())
        .then(data => {
            alert("Grazie per aver completato il sondaggio!");
            document.getElementById("surveyForm").reset();
        })
        .catch(error => {
            console.error("Errore:", error);
            alert("Qualcosa è andato storto. Riprova.");
        });
    });
</script>

</body>
</html>
