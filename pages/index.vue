<template>
  <div>
    <section id="timeline">
      <h1>Kashmir</h1>
      <div class="demo-card-wrapper">
        <div
          v-for="(item, i) in timeline"
          :key="i"
          :class="'demo-card demo-card--step' + (i + 1)"
        >
          <div class="head">
            <div class="number-box">
              <span>{{ i + 1 < 10 ? `0` + (i + 1) : i + 1 }}</span>
            </div>
            <h2>
              <span class="small">{{ item.subtitle }}</span>
              {{ item.title }}
            </h2>
          </div>
          <div class="body">
            <p>{{ item.text }}</p>
            <img class="img" v-if="item.img" :src="item.img" :alt="item.title" />
          </div>
        </div>
        <p style="position: fixed; color: white; left: 10px;">Scroll nedover</p>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "index",
  data: () => ({
    timeline: [
      {
        title: "Kashmir",
        subtitle: "",
        text: "Kashmir er navnet på et vakkert fjellområde. Området har vært preget av konflikt i mange år og anses for å være et strategisk område på grunn av fjell og naturressurser. Deler av befolkningen ønsker uavhengighet, mens India og Pakistan krangler om hvem som er den rettmessige eier.",
        img: "kashmir-mountains.jpg",
      },
      {
        title: "Begynnelsen",
        subtitle: "1850 ish",
        text: "På midten av 1800-tallet var dagens India og Pakistan, inkludert Kashmir, under britisk kontroll. Kashmir ble på den tiden ledet av en fyrste under et slags selvstyre.",
        img: "kashmir-prince.jpg",
      },
      {
        title: "Splittelsen",
        subtitle: "Etter andre verdenskrig",
        text: "Etter andre verdenskrig vant Britisk India selvstendighet og kvittet seg dermed med britene. Britisk India ble da til India og Pakistan siden de ønsket å ha ett land for muslimer og ett for hinduer. I all hast bestemte britene seg for å splitte kashmir. Ved splittelsen oppsto det en blodig konflikt om hvilket land Kashmir skulle tilhøre siden mesteparten av befolkningen i Kashmir var muslimer, men fyrsten var hindu. Da fyrsten fikk et valg om å velge side valgte han å være nøytral.",
        img: "Muslim-Hindu.png",
      },
      {
        title: "Frykten",
        subtitle: "Oktober, 1947",
        text: "I frykt for at fyrsten skulle bli en del av india, så protesterte befolkningen av kashmir i byen Poonch. Ikke lenger etterpå kom gruppe bevæpnede stammefolk fra Pakistan's norden som gikk til angrep på fyrstedømmet oktober, 1947",
        img: ""
      },
      {
        title: "Selvstendighet",
        subtitle: "",
        text: "Ut av frykt ba fyrsten India om militærisk hjelp imot å bli en del av india. India aksepterte dette forslaget og gikk dermed inn med tropper i kashmir. Pakisten var ikke helt enige i dette og mente at fyrsten ikke hadde rett til å gi Kashmir til India og sendte derfor også inn styrker i kashmir. Dette endte opp i en 2 årig krig som kostet mellom 3000 og 5000 liv.",
        img: "da-war.png",
      },
      {
        title: "Fredsavtalen",
        subtitle: "Høsten, 1948",
        text: "FN prøvde å få til en fredsavstale og våpenhvile mellom india og pakistan. Fredsavtalen endte med at pakisten fikk rundt en tredjedel av Kashmir, mens India satt igjen med resten.",
        img: "peace-line.png",
      },
      {
        title: "Avstemningen",
        subtitle: "",
        text: "Det skulle holdes en folkeavstemning om Kashmirs fremtid. India skulle også få lov å beholde en liten styrke for å overvåke sikkerheten. Etter hvert som årene gikk nektet Pakistan å trekke ut styrkene sine, samtidig som India mente det ikke var nødvendig med folkeavstemning. Dermed brøt begge fredsavtalen. FN foreslo deretter at begge landene skulle trekke ut samtidig. Dette ble godtatt av Pakistan, men ikke India. Det endte med at avstemningen aldri ble holdt...",
        img: "",
      },  
      {
        title: "China has come",
        subtitle: "1962",
        text: "Plutselig valgte Kina å overta den nordlige delen av Kashmir. Etter en liten krig med India overtok de rundt 17% av Kashmir. Kina har til den dag idag kontroll over område til tross for at India mener Kina ikke har noen rett på det.",
        img: "Kashmir.png",
      },
      {
        title: "Protesten",
        subtitle: "1987",
        text: "På den politiske fronten i 1987 rigget India valget og erklærte et pro-India parti som vinner. Dette fikk mange kashmirer til å se rødt, som igjen følte de ikke fikk muligheten til å bli hørt. Kashmirene gikk dermed til protest mot okkupasjoen.",
        img: "kashmir-protest.png"
      },
      {
        title: "Protesten møter motstand",
        subtitle: "1987",
        text: "India møtte denne protesten med hard motstand. Dette eskalerte fort til mer voldlighet.",
        img: "kashmir-protest-resist.png"
      },
      {
        title: "India går til angrep",
        subtitle: "Januar, 1988",
        text: "I Januar 1988, så våpnet India ild på demonstrantene. Mer enn 600 demonstranter døde. Motstandsorganisasjonen jammu & kashmir liberation front begynte til og med å rekrutere unge muslimere til å kjempe for friheten.",
        img: "india-open-fire.png"
      },
      {
        title: "Løsningen?",
        subtitle: "Slutten av 19-tallet",
        text: "Pakistan så en mulighet i denne konflikten. De introduserte en ny gruppe av radikale islamske krigere som kjempet for et mer pakistan kontrollert kashmir. På slutten av 90-tallet hadde disse gruppene stor kontroll over opprøret. India svarte med å plassere ut 500.000 soldater i Kashmir som slo ned på disse pakistanske gruppene og demonstranter.",
        img: "da-fighters.png"
      },
      {
        title: "Eskalasjon",
        subtitle: "Februar, 2019",
        text: "I februar 2019 begynte situasjonen mellom pakistan og india og eskalere igjen da en konvoi med Indiske sikkerhetstropper ble angrepet av en selvmordsbomber fra en terrorgruppe i pakistan. Selvmordsbomberen klarte å drepte minst 40 indiske soldater. 12 dager senere utførte India flere luftangrep i det nord-vestlige pakistan. Deretter skjøt Pakistan ned minst ett indisk fly. ",
        img: ""
      },
      {
        title: "Kashmir i dag",
        subtitle: "",
        text: "Kashmir er i dag er splittet mellom India, Pakistan og Kina. Området er beskyttet av mer enn en halv million indiske styrker og en dødlig blanding av terrorgrupper",
        img: "kashmir-mountains.jpg",
      },
    ]
  }),
  methods: {
    fade() {
      let lastKnownScrollPosition = 0;
      let ticking = false;
      const faders = document.querySelectorAll(".demo-card");
      faders[0].classList.add("appear");
      document.addEventListener('scroll', function(e) {
        lastKnownScrollPosition = window.scrollY;

        function isScrolledIntoView(el) {
          var rect = el.getBoundingClientRect();
          var elemTop = rect.top;
          var elemBottom = rect.bottom;

          // Only completely visible elements return true:
          var isVisible = (elemTop >= 0) && (elemBottom <= window.innerHeight);
          // Partially visible elements return true:
          //isVisible = elemTop < window.innerHeight && elemBottom >= 0;
          return isVisible;
        }
        if (!ticking) {
          window.requestAnimationFrame(function() {
            
            faders.forEach((fader) => {
              // fader.addEventListener("mouseover", () => {
                
              // });
            
              if (isScrolledIntoView(fader)) {
                fader.classList.add("appear");
              }
            });
            ticking = false;
          });

          ticking = true;
        }
      });
      console.log('fade')
      
    },
  },
  computed: {},
  mounted() {
    this.fade();
  },
};
</script>
<style lang="scss">
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

button {
  background: transparent;
  border: none;
  cursor: pointer;
  outline: none;
}


/* .section SECTION
–––––––––––––––––––––––––––––––––––––––––––––––––– */

.section {
  background: #f45b69;
  padding: 50px 0;
}

.section .container {
  width: 90%;
  max-width: 1200px;
  margin: 0 auto;
  text-align: center;
}

.section h1 {
  font-size: 2.5rem;
}

.section h2 {
  font-size: 1.3rem;
}

/* TIMELINE
–––––––––––––––––––––––––––––––––––––––––––––––––– */

.timeline {
  white-space: nowrap;
  overflow-x: hidden;
  ol {
    font-size: 0;
    width: 100vw;
    padding: 550px 0;
    transition: all 1s;
    li {
      position: relative;
      display: inline-block;
      list-style-type: none;
      width: 160px;
      height: 3px;
      background: #fff;
      &:last-child {
        width: 280px;
      }
      &:not(:first-child) {
        margin-left: 14px;
      }
      &:not(:last-child)::after {
        content: "";
        position: absolute;
        top: 50%;
        left: calc(100% + 1px);
        bottom: 0;
        width: 12px;
        height: 12px;
        transform: translateY(-50%);
        border-radius: 50%;
        background: #f45b69;
      }
      &:nth-child(odd) div {
        top: -16px;
        transform: translateY(-100%);
      }
      &:nth-child(even) {
        div {
          top: calc(100% + 16px);
          &::before {
            top: -8px;
            border-width: 8px 0 0 8px;
            border-color: transparent transparent transparent white;
          }
        }
      }
      div {
        position: absolute;
        left: calc(100% + 7px);
        width: 280px;
        padding: 15px;
        font-size: 1rem;
        white-space: normal;
        color: black;
        background: white;
        &::before {
          content: "";
          position: absolute;
          top: 100%;
          left: 0;
          width: 0;
          height: 0;
          border-style: solid;
        }
        &::before {
          top: 100%;
          border-width: 8px 8px 0 0;
          border-color: white transparent transparent transparent;
        }
      }
    }
  }
  time {
    display: block;
    font-size: 1.2rem;
    font-weight: bold;
    margin-bottom: 8px;
  }
}



/* TIMELINE ARROWS
–––––––––––––––––––––––––––––––––––––––––––––––––– */

.timeline .arrows {
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
}

.timeline .arrows .arrow__prev {
  margin-right: 20px;
}

.timeline .disabled {
  opacity: 0.5;
}

.timeline .arrows img {
  width: 45px;
  height: 45px;
}

/* GENERAL MEDIA QUERIES
–––––––––––––––––––––––––––––––––––––––––––––––––– */
@media screen and (max-width: 599px) {
  .timeline ol,
  .timeline ol li {
    width: auto;
  }

  .timeline ol {
    padding: 0;
    transform: none !important;
  }

  .timeline ol li {
    display: block;
    height: auto;
    background: transparent;
  }

  .timeline ol li:first-child {
    margin-top: 25px;
  }

  .timeline ol li:not(:first-child) {
    margin-left: auto;
  }

  .timeline ol li div {
    width: 94%;
    height: auto !important;
    margin: 0 auto 25px;
  }

  .timeline ol li div {
    position: static;
  }

  .timeline ol li:nth-child(odd) div {
    transform: none;
  }

  .timeline ol li:nth-child(odd) div::before,
  .timeline ol li:nth-child(even) div::before {
    left: 50%;
    top: 100%;
    transform: translateX(-50%);
    border: none;
    border-left: 1px solid white;
    height: 25px;
  }

  .timeline ol li:last-child,
  .timeline ol li:nth-last-child(2) div::before,
  .timeline ol li:not(:last-child)::after,
  .timeline .arrows {
    display: none;
  }
}


/* Font Imports */

@import url('https://fonts.googleapis.com/css2?family=Skranji&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Oxygen:wght@300&family=Skranji&display=swap');


/* Media Queries */


@mixin mq-xs {
  @media (min-width: 320px) {
    @content;
  }
}

@mixin mq-sm {
  @media (min-width: 480px) {
    @content;
  }
}

@mixin mq-md {
  @media (min-width: 720px) {
    @content;
  }
}

@mixin mq-lg {
  @media (min-width: 1000px) {
    @content;
  }
}

$background: #1d1d1e;
$box-shadow: 0px 1px 22px 4px rgba(0, 0, 0, 0.07);
$border: 1px solid rgba(191, 191, 191, 0.4);
$items: 14;
$rows: ceil(calc($items/2));

/* Card sizing */

$card-height: 400px;
$card-width: 450px;
$inner-margin: 15px;
$number-size: 35px;
$stagger: 180px;
$outer-margin: 90px;
$marker-size: 9px;

/* Colors */

$steps: #46b8e9;
$colors: #00FF40,
#00E157,
#00CA70,
#00BA8E,
#00B4B4,
#008EBA,
#0070CA,
#0057E1,
#0040FF,
#001AE1,
#0C00CA,
#3100BA,
#5A00B4,
#8800BA,
#BE00CA,
#E100C8,
#FF00BF,
#E1008B,
#CA0059,
#BA002B,
#B40000,
#BA2B00,
#CA5900,
#E18B00
#FFBF00;
$timeline: #bdbdbd;

/* Calculations */

$container-height: $rows * ($card-height + $outer-margin) + $stagger;
$container-width: $card-width*2 + $outer-margin*3;
$head-height: $number-size + 50;
$body-height: $card-height - $head-height;
$marker-dist: $card-width + calc($outer-margin/2) - calc($marker-size/2);

/* Placeholders */

@include mq-lg {
  %arrow {
    position: absolute;
    content: "";
    width: 0;
    height: 0;
    border-top: 15px solid transparent;
    border-bottom: 15px solid transparent;
  }
  %marker {
    position: absolute;
    content: "";
    width: $marker-size;
    height: $marker-size;
    background-color: $timeline;
    border-radius: $marker-size;
    box-shadow: 0px 0px 2px 8px $background;
  }
}


/* Some Cool Stuff */

$counter: $items - $rows + 2;
@for $i from 1 through $rows {
  .demo-card:nth-child(#{$i*2-1})   { order: $i }
  .demo-card:nth-child(#{$i*2})     { order: $counter }
  $counter: $counter + 1;
}

/* Border Box */

* {
  box-sizing: border-box;
}

/* Fonts */

body {
  font-family: Roboto;
  background-color: #1d1d1e !important;
}

.demo-card {
  opacity: 0;
  transition: opacity 250ms ease-in-out;
  &.appear {
    opacity: 1;
  }
}
#timeline {
  padding: 100px 0;
  background: $background;
  border-top: $border;
  border-bottom: $border;
  h1 {
    text-align: center;
    font-size: 3rem;
    font-weight: 200;
    margin-bottom: 20px;
    color: #ffffff;
  }
  .demo-card-wrapper {
    position: relative;
    margin: auto;
    @include mq-lg {
      display: flex;
      flex-flow: column wrap;
      width: $container-width;
      height: $container-height;
      margin: 0 auto;
    }
    &::after {
      z-index: 1;
      content: "";
      position: absolute;
      top: 0;
      bottom: 0;
      left: 50%;
      border-left: $border;
      @include mq-lg {
        border-left: 1px solid $timeline;
      }
    }
  }
  .demo-card {
    position: relative;
    display: block;
    margin: 10px auto 80px;
    max-width: 94%;
    z-index: 2;
    @include mq-sm {
      max-width: 60%;
      box-shadow: $box-shadow;
    }
    @include mq-md {
      max-width: 40%;
    }
    @include mq-lg {
      max-width: $card-width;
      height: $card-height;
      margin: $outer-margin;
      margin-top: calc($outer-margin/2);
      margin-bottom: calc($outer-margin/2);
      &:nth-child(odd) {
        margin-right: calc($outer-margin/2);
        .head::after {
          @extend %arrow;
          border-left-width: 15px;
          border-left-style: solid;
          left: 100%;
        }
        .head::before {
          @extend %marker;
          left: $marker-dist + 1;
        }
      }
      &:nth-child(even) {
        margin-left: calc($outer-margin/2);
        .head::after {
          @extend %arrow;
          border-right-width: 15px;
          border-right-style: solid;
          right: 100%;
        }
        .head::before {
          @extend %marker;
          right: $marker-dist - 1;
        }
      }
      &:nth-child(2) {
        margin-top: $stagger;
      }
    }
    .head {
      position: relative;
      display: flex;
      align-items: center;
      color: #1d1d1e;
      font-weight: 400;
      .number-box {
        display: inline;
        float: left;
        margin: $inner-margin;
        padding: 10px;
        font-size: $number-size;
        line-height: $number-size;
        font-weight: 600;
        background: rgba(0, 0, 0, 0.17);
      }
      h2 {
        text-transform: uppercase;
        font-size: 1.3rem;
        font-weight: inherit;
        letter-spacing: 2px;
        margin: 0;
        padding-bottom: 6px;
        line-height: 1rem;
        font-family: 'Skranji' !important;
        @include mq-sm {
          font-size: 165%;
          line-height: 1.2rem;
        }
        span {
          display: block;
          font-size: 0.6rem;
          margin: 0;
          @include mq-sm {
            font-size: 0.8rem;
          }
        }
      }
    }
    .body {
      background: #fff;
      border: $border;
      border-top: 0;
      padding: $inner-margin;
      @include mq-lg {
        height: $body-height;
      }
      p {
        font-size: 18px;
        line-height: 18px;
        margin-bottom: $inner-margin;
        font-family: 'Oxygen', sans-serif !important;
      }
      img {
        display: inline-block;
        width: 100%;
        height: 100%;
        // max-height: 50%;
      }
    }
    @for $i from 1 through $items {
      &--step#{$i} {
        $color: nth($colors, ((($i - 1)) + 2));
        $color2: nth($colors, ((($i)) + 3));
        // $color: nth($colors, ((($i - 1) % 4) + 1));
        background: linear-gradient(90deg, $color, $color2);
        .head::after {
          border-color: $color;
        }
      }
    }
  }
}

</style>
