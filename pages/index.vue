<template>
  <div class="px-4">
    <div class="is-fix-menu columns box is-centered p-3">
      <div
        class="is-10 column is-flex p-0 is-justify-content-space-between is-align-items-center pt-1"
      >
        <div class="is-flex p-0 is-align-items-center">
          <img
            src="@/assets/icon.png"
            width="75px"
            class="p-0"
            alt=""
            srcset=""
          />
          <span class="is-bold pl-4 is-hidden-mobile"> SOLU-IT </span>
        </div>

        <div class="is-flex p-0 is-align-items-center">
          <span class="is-bold pl-4 is-size-7 navlink"> ACCEUIL </span>
          <span class="is-bold pl-4 is-size-7 navlink"> REALISATIONS </span>
          <span class="is-bold pl-4 is-size-7 navlink"> CONTACT </span>
        </div>
      </div>
    </div>

    <div style="widh: 100px; height: 100px"></div>

    <!-- INTRODUCE -->
    <div class="columns is-centered has-background-light pt-6">
      <div class="column is-10">
        <div class="columns is-centered p-4">
          <div class="column is-6 is-size-3 p-3 pt-6 is-zoomed">
            <span>
              Développement Web & Mobile ,
              <span class="is-red">
                Interlocuteur unique pour un site internet réussi
              </span>
              .
            </span>
            <br />
            <p class="is-size-8 pt-4 has-text-grey">
              Développeur <b class="has-text-dark"> Web front </b> &
              <b class="has-text-dark"> back-end </b> &
              <b class="has-text-dark">Webdesigner</b> freelance, je suis à
              votre disposition pour répondre à tout type de projets de création
              de sites internet, de développement spécifique ou d'<b
                class="has-text-dark"
                >applications web</b
              >. Passionné par les
              <b class="has-text-dark">technologies</b> liées au Web, je mets
              mes <b class="has-text-dark">compétences</b> au service de vos
              besoins dans divers domaines.
            </p>
            <b-button @click="mailto()" class="is-bg-red p-3 px-5 has-text-light mt-5"
              >Prendre contact</b-button
            >
          </div>

          <div class="column is-6 is-hidden-mobile">
            <img src="@/assets/template.svg" width="85%" alt="" srcset="" />
          </div>
        </div>
      </div>
    </div>

     <!-- MESSAGE -->

     <div class="columns mt-4 is-centered my-4">
      <div class="column is-5 pt-6">
        <center class="is-size-4 is-zoomed">
        EBAUCHE DES PROJETS <br />
          <p class="is-size-8">
            Des solutions adaptées à votre domaine d'activité 
          </p>
          <div class="is-bar-red mt-4"></div>
        </center>
      </div>
    </div>

    <!-- FILTRE -->
    <div class="columns is-centered mt-6 m-3">
      <div class="column is-10">
        <div class="is-flex is-justify-content-space-between is-flex-wrap-wrap">
          <div class="">
            <p><i class="is-size-7">Categories</i></p>
            <b-dropdown :triggers="['click']" aria-role="list">
              <template #trigger>
                <p class="box px-4 is-zoom">
                  Tous
                  <i class="mdi mdi-chevron-right"></i>
                </p>
              </template>

              <b-dropdown-item aria-role="listitem">Action</b-dropdown-item>
              <b-dropdown-item aria-role="listitem"
                >Another action</b-dropdown-item
              >
              <b-dropdown-item aria-role="listitem"
                >Something else</b-dropdown-item
              >
            </b-dropdown>
          </div>

          <div
            class="is-flex is-justify-content-space-between is-flex-wrap-wrap set-gap"
          >
            <div class="">
              <p><i class="is-size-7">Technologies</i></p>
              <div class="box is-zoom">
                <b-checkbox
                  size="is-small"
                  type="is-danger"
                  v-model="electron"
                  true-value="1"
                  false-value="0"
                  >ELECTRON</b-checkbox
                >
                <b-checkbox
                  size="is-small"
                  type="is-danger"
                  v-model="nuxt"
                  true-value="1"
                  false-value="0"
                  >NUXT(VUEJS)</b-checkbox
                >
                <b-checkbox
                  size="is-small"
                  type="is-danger"
                  v-model="flutter"
                  true-value="1"
                  false-value="0"
                  >FLUTTER (DART)</b-checkbox
                >
                <b-checkbox
                  size="is-small"
                  type="is-danger"
                  v-model="angular"
                  true-value="1"
                  false-value="0"
                  >ANGULAR</b-checkbox
                >
              </div>
            </div>

            <div class="">
              <p><i class="is-size-7">Formules</i></p>
              <div class="box is-zoom">
                <b-checkbox
                  size="is-small"
                  type="is-danger"
                  v-model="standard"
                  true-value="1"
                  false-value="0"
                  >STANDARD</b-checkbox
                >
                <b-checkbox
                  size="is-small"
                  type="is-danger"
                  v-model="perso"
                  true-value="1"
                  false-value="0"
                  >PERSONNALISÉ</b-checkbox
                >
                <b-checkbox
                  size="is-small"
                  type="is-danger"
                  v-model="ecommerce"
                  true-value="1"
                  false-value="0"
                  >E-COMMERCE</b-checkbox
                >
                <b-checkbox
                  size="is-small"
                  type="is-danger"
                  v-model="maintenance"
                  true-value="1"
                  false-value="0"
                  >MAINTENANCE</b-checkbox
                >
              </div>
            </div>
          </div>
        </div>
        <br />
        <hr class="dropdown-divider" />
      </div>
    </div>

    <!-- PROJET -->
    <div class="columns is-centered mt-4 m-3">
      <div class="column is-11">
        <div
          class="is-flex is-justify-content-center is-flex-wrap-wrap set-gap-2"
        >
          <!-- FLASH -->
          <div class="is-box-4 navlink" v-if="standard == 1 || nuxt == 1">
            <div class="box p-0 mt-6">
              <img
                src="@/assets/flash.png"
                style="border-radius: 10px"
                alt=""
                srcset=""
              />
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <b>UMNG-FLASH</b>
              <p class="is-size-7 box p-1 is-red has-text-light px-3">
                STANDARD
              </p>
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <p class="has-text-grey is-size-8 mt-2">
                Faculté des Lettres, Arts et Sciences Humaines (FLASH)
              </p>
            </div>
          </div>

          <!-- AFRI-SCHOOL -->
          <div class="is-box-4 navlink" v-if="perso == 1 || nuxt == 1">
            <div class="box p-0 mt-6">
              <img
                src="@/assets/afri-school.png"
                style="border-radius: 10px"
                alt=""
                srcset=""
              />
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <b>MTN AFRI-SCHOOL</b>
              <p class="is-size-7 box p-1 is-red has-text-light px-3">
                PERSONNALISÉ
              </p>
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <p class="has-text-grey is-size-8 mt-2">
                la gestion administrative, académique et financière des
                établissements
              </p>
            </div>
          </div>

          <!-- TEKISSA -->

          <div class="is-box-4 navlink" v-if="ecommerce == 1 || nuxt == 1">
            <div class="box p-0 mt-6">
              <img
                src="@/assets/tekissa.png"
                style="border-radius: 10px"
                alt=""
                srcset=""
              />
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <b>TEKISSA</b>
              <p class="is-size-7 box p-1 is-red has-text-light px-3">
                E-COMMERCE
              </p>
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <p class="has-text-grey is-size-8 mt-2">
                La solution des ventes en ligne au congo-brazza
              </p>
            </div>
          </div>

          <!-- NKAMAR -->

          <div class="is-box-4 navlink" v-if="perso == 1 || nuxt == 1">
            <div class="box p-0 mt-6">
              <img
                src="@/assets/nkamar.png"
                style="border-radius: 10px"
                alt=""
                srcset=""
              />
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <b>NKAMAR</b>
              <p class="is-size-7 box p-1 is-red has-text-light px-3">
                PERSONNALISÉ
              </p>
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <p class="has-text-grey is-size-8 mt-2">
                La solution pour vos tontines au congo-brazza
              </p>
            </div>
          </div>


           <!-- APP MOBILE HFINANCE -->

           <div class="is-box-4 navlink">
            <div class="box p-0 mt-6">
              <img
                src="@/assets/hfinance.png"
                style="border-radius: 10px"
                alt=""
                srcset=""
              />
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <b>HFINANCE</b>
              <p class="is-size-7 box p-1 is-red has-text-light px-3">
                PERSONNALISÉ
              </p>
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <p class="has-text-grey is-size-8 mt-2">
                Application mobile de gestion de poche et tontines
              </p>
            </div>
          </div>

          <!-- FRAIS SCOLAIRE -->

          <div class="is-box-4 navlink" v-if="perso == 1 || nuxt == 1">
            <div class="box p-0 mt-6">
              <img
                src="@/assets/frais.png"
                style="border-radius: 10px"
                alt=""
                srcset=""
              />
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <b>PPFS</b>
              <p class="is-size-7 box p-1 is-red has-text-light px-3">
                PERSONNALISÉ
              </p>
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <p class="has-text-grey is-size-8 mt-2">
                Portail web pour paiement des frais scolaires
              </p>
            </div>
          </div>

          <!-- SOLU-IT -->

          <div class="is-box-4 navlink" v-if="standard == 1 || nuxt == 1">
            <div class="box p-0 mt-6">
              <img
                src="@/assets/solu-it.png"
                style="border-radius: 10px"
                alt=""
                srcset=""
              />
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <b>SOLU-IT</b>
              <p class="is-size-7 box p-1 is-red has-text-light px-3">
                STANDARD
              </p>
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <p class="has-text-grey is-size-8 mt-2">
                Site vitrine pour presentation des services
              </p>
            </div>
          </div>

          <!-- HBM -->

          <div class="is-box-4 navlink" v-if="perso == 1 || nuxt == 1">
            <div class="box p-0 mt-6">
              <img
                src="@/assets/hbm.png"
                style="border-radius: 10px"
                alt=""
                srcset=""
              />
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <b>HBM</b>
              <p class="is-size-7 box p-1 is-red has-text-light px-3">
                PERSONNALISÉ
              </p>
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <p class="has-text-grey is-size-8 mt-2">
                BM est un système complet pour la gestion des réservations de
                votre flotte d'autocars et bus
              </p>
            </div>
          </div>

          

          <!-- LEKOL -->

          <div class="is-box-4 navlink" v-if="electron == 1 || nuxt == 1">
            <div class="box p-0 mt-6">
              <img
                src="@/assets/lekol.png"
                style="border-radius: 10px"
                alt=""
                srcset=""
              />
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <b>LEKOL</b>
              <p class="is-size-7 box p-1 is-red has-text-light px-3">
                PERSONNALISÉ
              </p>
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <p class="has-text-grey is-size-8 mt-2">
                LEKOL est un système complet pour la gestion des etablissements
                (Bureau)
              </p>
            </div>
          </div>

           <!-- RAPPPORT -->

           <div class="is-box-4 navlink">
            <div class="box p-0 mt-6">
              <img
                src="@/assets/rapport.png"
                style="border-radius: 10px"
                alt=""
                srcset=""
              />
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <b>RAPPORT CYB</b>
              <p class="is-size-7 box p-1 is-red has-text-light px-3">
                PERSONNALISÉ
              </p>
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <p class="has-text-grey is-size-8 mt-2">
                RAPPORT CY est un système complet pour la gestion des rapports des agents de votre entreprise
            
              </p>
            </div>
          </div>

           <!-- APP MOBILE FLASH -->

           <div class="is-box-4 navlink">
            <div class="box p-0 mt-6">
              <img
                src="@/assets/Flash-app.png"
                style="border-radius: 10px"
                alt=""
                srcset=""
              />
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <b>FLASH</b>
              <p class="is-size-7 box p-1 is-red has-text-light px-3">
                PERSONNALISÉ
              </p>
            </div>
            <div class="is-flex is-justify-content-space-between is-zoom">
              <p class="has-text-grey is-size-8 mt-2">
                Application mobile de gestion des preinscriptions  a la  Faculté des Lettres, Arts et Sciences Humaines (FLASH)
              </p>
            </div>
          </div>

        </div>
      </div>
    </div>

    <!-- MESSAGE -->

    <div class="columns mt-4 is-centered my-4">
      <div class="column is-5 pt-6">
        <center class="is-size-4 is-zoomed">
          A PROPOS <br />
          <p class="is-size-8">
            Je suis développeur web freelance et j'aime ça !
          </p>
          <div class="is-bar-red mt-4"></div>
        </center>
      </div>
    </div>



    <!-- APROPOS -->
    <div class="columns is-centered mt-6">
      <div class="column is-11">
        <div class="columns has-text-grey">
          <div class="column">
            <div class="is-red is-bold">Un développeur web passionné ! </div>
            <br>
             Ma passion pour le développement web 
            commence en<b class="has-text-dark"> 2017</b> et m'a demandé un changement radical de cursus afin
            de pouvoir pleinement l'exploiter. Dès lors, <b class="has-text-dark">je mis tout en oeuvre
            pour percer dans cette voie</b>, tout en prenant du plaisir sur les
            divers projets développés. En <b class="has-text-dark"> 2022 </b>, je décide de devenir
            développeur web indépendant après plusieurs postes en tant que
            <b class="has-text-dark">développeur web « full-stack » réussis </b>, qui me conforteront dans
            cette idée afin de toucher un plus large panel de domaines
            d'activités, voir du pays !
          </div>

          <div class="column">
            <img src="@/assets/coder.webp" alt="" srcset="" />
          </div>

          <div class="column">
            <div class="is-red is-bold">Expérience en développement</div>
            <br> Mon expérience acquise au fil des
            projets me permet de <b class="has-text-dark">mieux comprendre les attentes d'un client et de
            répondre précisement au besoin demandé en fonction du domaine
            d'activité </b>. Du site vitrine au projet plus complexe, je vous propose
            une <b class="has-text-dark">expertise</b> et un développement web qui correspond à vos attentes
            & à vos besoins.
       
            
             <div class="has-text-dark mt-5 is-red is-bold">Un tarif adapté à votre projet</div>
            <br> Travaillant
            régulièrement avec des <b class="has-text-dark">PME</b>, ou particuliers, je vous
            propose des solutions à votre portée & adaptée à votre <b class="has-text-dark">budget</b>.
          </div>
        </div>
      </div>
    </div>

     <!-- MESSAGE -->

     <div class="columns mt-4 is-centered my-4">
      <div class="column is-5 pt-6">
        <center class="is-size-4 is-zoomed">
        EBAUCHE DE STATS <br />
          <p class="is-size-8">
            Un interlocuteur unique pour un site internet réussi 
          </p>
          <div class="is-bar-red mt-4"></div>
        </center>
      </div>
    </div>

    <!-- STATS -->

    <div class="columns is-centered mt-6">
        <div class="column is-10">
            <div class="columns is-centered">
                <div class="column is-12 is-flex is-justify-content-center is-flex-wrap-wrap set-gap-2">
                    <div class="is-box-4-2">
                        <p class="is-bold is-size-1">
                          <i class="mdi mdi-code-json is-size-3"></i>  5+
                        </p>
                        <div class="is-bar-red my-4"></div>
                        <p class="is-size-8">ANNÉES D'EXPÉRIENCE</p>
                    </div>

                    <div class="is-box-4-2">
                        <p class="is-bold is-size-1">
                          <i class="mdi mdi-star-check is-size-3"></i>  17+
                        </p>
                        <div class="is-bar-red my-4"></div>
                        <p class="is-size-8">TECHNOLIGIES UTILISÉES</p>
                    </div>

                    <div class="is-box-4-2">
                        <p class="is-bold is-size-1">
                          <i class="mdi mdi-cogs is-size-3"></i>  10+                       </p>
                        <div class="is-bar-red my-4"></div>
                        <p class="is-size-8">PROJETS WEB TERMINÉS</p>
                    </div>

                    <div class="is-box-4-2">
                        <p class="is-bold is-size-1">
                          <i class="mdi mdi-account-tie is-size-3"></i>  14+                        </p>
                        <div class="is-bar-red my-4"></div>
                        <p class="is-size-8">CLIENTS SATISFAITS</p>
                    </div>

                </div>
            </div>
        </div>
    </div>

    <!-- MESSAGE -->

    <div class="columns mt-4 is-centered my-4">
      <div class="column is-5 pt-6">
        <center class="is-size-4 is-zoomed">
            CONTACTEZ-MOI <br />
          <p class="is-size-8">
            Une idée ? Un projet ? N'hésites pas à demander un devis! [GRATUIT]
          </p>
          <div class="is-bar-red mt-4"></div>
        </center>
      </div>
    </div>

       <!-- CONTACTS -->
       <div class="columns is-centered mt-6">
      <div class="column is-11">
        <div class="columns has-text-grey">
          <div class="column is-3">
           <!-- ADRESSE -->
            <div class="py-3">
                <i class="mdi mdi-map-marker-outline is-red "></i>
            <span class="is-bold is-size-8">ADRESSE</span>
            <p class="is-size-7">Moungali, Arr 4 . Brazzaville</p>
            <hr class="dropdown-divider" />
            </div>

            <!-- PHONE -->
            <div class="py-3">
                <i class="mdi mdi-phone is-red "></i>
            <span class="is-bold is-size-8">TELEPHONE</span>
            <p class="is-size-7">(+242) 06 950 08 86</p>
            <hr class="dropdown-divider" />
            </div>

            <!-- EMAIL -->
            <div class="py-3">
                <i class="mdi mdi-at is-red "></i>
            <span class="is-bold is-size-8">EMAIL</span>
            <p class="is-size-7">alexisng90210@gmail.com</p>
            <hr class="dropdown-divider" />
            </div>

             <!-- GITHUB -->
             <div class="py-3">
                <i class="mdi mdi-github is-red "></i>
            <span class="is-bold is-size-8">GITHUB</span>
            <p class="is-size-7">@alexis90210 <a href="https://github.com/alexis90210"> <i class="mdi mdi-link"></i></a></p>
            <hr class="dropdown-divider" />
            </div>

             <!-- WAKATIME SINCE -->
             <div class="py-3">
                <i class="mdi mdi-github is-red "></i>
            <span class="is-bold is-size-8">WAKATIME since 20/09/2022</span>
            <p class="is-size-7 py-2">
              <a href="https://wakatime.com/@Hisoka_tegiro" class="has-text-dark"> @Hisoka_tegiro(Alexis Ngoyi)</a>
             </p>
            <a href="https://wakatime.com/@87ba5400-e128-4aec-a89d-85310b743b49"><img src="https://wakatime.com/badge/user/87ba5400-e128-4aec-a89d-85310b743b49.svg" alt="Total time coded since Sep 20 2022" /></a>
            <hr class="dropdown-divider" />
            </div>

            <!-- HORAIRE -->
            <div class="py-3">
                <i class="mdi mdi-calendar is-red "></i>
            <span class="is-bold is-size-8">HORAIRE</span>
            <p class="is-size-7">Lundi - Vendredi</p>
            <p class="is-size-7">09H - 18H</p>
            <hr class="dropdown-divider" />
            </div>


          </div>

          <div class="column is-hidden-mobile">
            <img src="@/assets/contact.webp" alt="" srcset="" />
          </div>

          <div class="column">

            <b-input class="py-3" placeholder="Nom / Prenom"></b-input>
            <b-input class="py-3" placeholder="Email"></b-input>
            <b-input class="py-3" placeholder="Telephone"></b-input>
            <b-input class="py-3" maxlength="200" type="textarea"  placeholder="Message"></b-input>

            <p class="is-size-8">
                <b-checkbox type="is-danger">
                    En soumettant ce formulaire, j'accepte que les informations saisies soient exploitées dans le cadre de la demande de contact et de la relation commerciale qui peut en découler.
                </b-checkbox>
            </p>
                 <div class="go-right">
                    <b-button class="is-bg-red p-3 px-5 has-text-light mt-5"
                    @click="mailto()"
              >Prendre contact</b-button
            >
                 </div>
            
          </div>
        </div>
      </div>
    </div>


    <!-- FOOTER -->

    <div class="columns has-background-dark px-4 py-5 mt-5 add-clip">
        <div class="go-right">
            <p class="is-bold has-text-light is-size-7 px-5">
                ALEXIS NGOYI  - COPYRIGHT © 2017 - {{new Date().getFullYear()}}
            </p>
        </div>
    </div>

  </div>
</template>

<script>
export default {
  data() {
    return {
      standard: 1,
      ecommerce: 1,
      perso: 1,
      maintenance: 1,
      electron: 1,
      nuxt: 1,
      angular:1,
      flutter: 1,
    };
  },
  methods:{
    mailto() {
      this.$buefy.dialog.alert({
        title:'ALERTE',
        message:'Nous vous redirigeons vers votre application de mail par default, veuillez patienter svp',
        type:'is-warning',
        hasIcon:true
      })

      var a = document.createElement('a')
      a.href= 'mailto:alexisng90210@gmail.com?subject=MESSAGE PROVENANT DU PORTFOLIO'
      a.click()
    }
  }
};
</script>

<style>
.is-bold {
  font-weight: bold;
}

.is-red {
  color: rgb(221, 61, 51);
}

.is-zoom {
  zoom: 90%;
}

.is-zoomed {
  zoom: 110%;
  font-weight: 500;
}
.is-size-8 {
  font-size: 14px;
}

.navlink {
  cursor: pointer;
}

.navlink:hover {
  color: rgb(221, 61, 51);
}

.is-clip {
  clip-path: polygon(0% 0%, 100% 0, 100% 85%, 0 100%);
}

.is-bg-red {
  background-color: rgb(221, 61, 51);
}

.set-gap {
  gap: 10px;
}

.set-gap-2 {
  gap: 30px;
}

.is-box-4 {
  width: 30%;
}

.is-box-4-2 {
  width: 20%;
}

.is-fix-menu {
  position: fixed;
  width: 100% !important;
  top: 0;
  left: 0;
  z-index: 100;
  margin: 0 !important;
}
.is-red {
  color: rgb(221, 61, 51) !important;
}

.is-bar-red {
  height: 3px;
  width: 30%;
  border-radius: 5px;
  background-color: rgb(221, 61, 51) !important;
}

.go-right {
    width:100%;
    text-align: right;
}

.add-clip{
  background-color: rgb(221, 61, 51) !important;
}

@media screen and (max-width:700px) {
  .is-box-4 {
  width: 90%;
}
.is-hidden-mobile {
  display:none
}  
}
</style>
