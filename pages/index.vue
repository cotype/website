<template>
  <div>
    <header>
      <div class="logos">
        <img class="logo" src="/logo.svg" alt>
        <a href="https://github.com/cotype/core">
          <img src="/githubLogo.svg" alt>
        </a>
      </div>
      <h1 class="title">Selfhosted Headless CMS</h1>
      <a class="get-started-link" href="https://github.com/cotype/core#install">Get Started</a>
    </header>
    <main class="feature-grid">
      <Feature v-for="item in features" :key="item.headline" :headLine="item.headline">{{item.text}}</Feature>
    </main>
    <footer>
      A Project by
      <a href="https://www.cellular.de/">Cellular</a> and
      <a href="https://xiphe.net">Xiphe</a>
    </footer>
  </div>
</template>


<script>
import Feature from "../components/Feature";

export default {
  components: { Feature },
  data: function() {
    return {
      features: [
        {
          headline: "Headless",
          text:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia ab esse, mollitia optio quia sunt expedita alias explicabo vero nihil necessitatibus consequatur doloremque rem laborum aut illum qui dignissimos autem."
        },
        {
          headline: "On Premise / Open Source",
          text: "Kein Saas, die daten gehören dir."
        },
        {
          headline: "Strukturiert",
          text:
            "Fachliches Content-Modell, das sich an der Business-Domäne orientiert und nicht am Look & Feel der Ausgabe. Daten sind langlebig, Frontends nicht."
        },
        {
          headline: "Flexibel",
          text:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia ab esse, mollitia optio quia sunt expedita alias explicabo vero nihil necessitatibus consequatur doloremque rem laborum aut illum qui dignissimos autem."
        },
        {
          headline: "Easy to Use",
          text: "Da kann sogar der UI-Engineer die Daten Modelle schreiben"
        },
        {
          headline: "Specific",
          text: "Im Sinne von “hart angepasst auf die Domäne und den use-case"
        },
        {
          headline: "Typisiert/Stark für Entwickler",
          text:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia ab esse, mollitia optio quia sunt expedita alias explicabo vero nihil necessitatibus consequatur doloremque rem laborum aut illum qui dignissimos autem."
        }
      ]
    };
  }
};
</script>


<style>
:root {
  --ct-main: #ff46ad;
  --ct-grey: #343434;
}
html {
  font-size: 16px;
}

body {
  font-family: "Open Sans", sans-serif;
  padding: 1rem;
  color: var(--ct-grey);
}

header {
  max-width: 500px;
  margin: 0 auto;
}
@media (min-width: 600px) {
  header {
    padding-bottom: 2rem;
  }
}
@media (min-width: 999px) {
  header {
    padding-bottom: 6rem;
    padding-top: 4rem;
  }
}
.logos {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.logo {
  width: 100px;
}

.title {
  font-size: 4rem;
  line-height: 4.2rem;
}

.get-started-link {
  background: var(--ct-main);
  border-bottom: none;
  color: white;
  text-decoration: none;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 42px;
}

@media (min-width: 600px) {
  .feature-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 50px;
  }
}
@media (min-width: 999px) {
  .feature-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 50px;
    max-width: 1200px;
    margin: 0 auto;
  }
}
footer {
  max-width: 1200px;

  margin: 0 auto;
  border-top: 1px solid var(--ct-main);
  padding-top: 25px;
}

a {
  border-bottom: 1px solid rgba(0, 0, 0, 0.2);
  text-decoration: none;
  color: var(--ct-main);
}
</style>
