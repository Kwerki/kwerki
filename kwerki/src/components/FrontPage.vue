<template>
    <div class="container">
        <div class="headline_1">
            <h1>
                <span>H</span>
                <span>a</span>
                <span>l</span>
                <span>l</span>
                <span>o</span>
                <span>.</span>
            </h1>
        </div>
        <div class="headline_2">
            <h1>Mein Name ist <span style="white-space: nowrap;">Paul Hublitz</span>.</h1>
        </div>
        <div class="introducing">
            <div class="absatz">
                <p>
                    Ich habe an der Hochschule für Technik, Wirtschaft und Kultur in Leipzig
                    <a href="https://www.htwk-leipzig.de/studieren/studiengaenge/bachelorstudiengaenge/medieninformatik"
                        target="_blank" rel="noopener noreferrer">
                        Medieninformatik B.Sc.</a>
                    studiert. Dort lernte ich die essentiellen Konzepte der Informatik kennen, darunter die Prinzipien
                    der Softwareentwicklung, Datenbankentwicklung und Algorithmen.
                </p>
            </div>
            <div class="absatz">
                <p>
                    Während des Studiums haben wir ein einjähriges Projekt namens
                    <a href="https://gitlab.dit.htwk-leipzig.de/projekt2023-s-self-service-text-mining" target="_blank"
                        rel="noopener noreferrer">
                        Self-Service Text Mining</a>
                    für die TIB Leibniz umgesetzt, an dem ich als Fullstack Entwickler beteiligt war.
                    Die Idee hinter dem Projekt war, die Einstiegshürde für Textmining-Tools niedrig zu halten und sie
                    einem breiten Publikum zugänglich zu machen.
                </p>
            </div>
            <div class="absatz">
                <p>
                    Inbegriffen war auch ein Praktikum, welches ich bei
                    <a href="https://alvara.eu/de/home" target="_blank" rel="noopener noreferrer">ALVARA Digital
                        Solutions</a>
                    gemacht habe. Dort habe ich als Backend Java Entwickler gearbeitet und meine
                    <a href="/bachelorarbeit.pdf" target="_blank">Bachelorarbeit</a>
                    über die Integration des Elster Rich Client in Java Cloud Applikationen geschrieben.
                </p>
            </div>
            <div class="absatz">
                <p>
                    Neben der Zeit, die ich am Computer verbringe, bin ich gerne aktiv und gehe zum Bouldern, Sqashen,
                    Fitness und genieße die Natur.
                    Ich schaue gerne CounterStrike 2 Esport und lese viel über meine Passion
                    <a href="https://hyperbitcoinization.com/" target="_blank" rel="noopener noreferrer">Bitcoin</a>.
                </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "FrontPage",
};
</script>

<style scoped>
.container {
    margin-left: 250px;
    margin-right: 150px;
    max-width: 650px;
    text-align: right;
    color: black;
    font-family: 'Inter', sans-serif;
}

@media (max-width: 1024px) { 
    .container {
        margin: 0 auto;  
        text-align: right;
        padding: 20px; 
    }

    .headline_1 h1 {
        justify-content: flex-end;
    }

}

.headline_1 {
    font-size: 30px;
}

.headline_2 {
    font-size: 15px;
}

.introducing {
    line-height: 1.6;
    font-size: 109%;
}

.absatz {
    margin-top: 50px;
}

a {
    text-decoration: none;
    white-space: nowrap;
    position: relative;
    color: black;
}

a::before {
    content: "";
    position: absolute;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 35%;
    background-color: rgb(138, 203, 243);
    z-index: -1;
    transition: height 0.2s ease-in-out;
}

a:hover::before {
    height: 100%;
}

.headline_1 h1 {
    display: flex;
    gap: 5px;
    justify-content: flex-end; 
}

.headline_1 span {
    display: inline-block;
    opacity: 0;
    transform: translateY(20px);
    animation: waveIn 0.6s ease-out forwards;
}

@keyframes waveIn {
    0% { opacity: 0; transform: translateY(20px); }
    50% { opacity: 1; transform: translateY(-5px); }
    100% { opacity: 1; transform: translateY(0); }
}

.headline_1 span:nth-child(1) { animation-delay: 0s; }
.headline_1 span:nth-child(2) { animation-delay: 0.1s; }
.headline_1 span:nth-child(3) { animation-delay: 0.2s; }
.headline_1 span:nth-child(4) { animation-delay: 0.3s; }
.headline_1 span:nth-child(5) { animation-delay: 0.4s; }
.headline_1 span:nth-child(6) { animation-delay: 0.5s; }

</style>