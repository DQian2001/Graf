<template>
  <div>
    <div class="about-section">
      <h1>About Us</h1>
      <p>We Make Graf</p>
    </div>
    <h2 style="text-align:center">Developers</h2>

    <div class="ui six column grid">
      <div class="column" v-for="(member,name) in members" v-bind:key="name">
        <div class="ui fluid card">
          <div class="image">
            <img src="../assets/John.png" >
          </div>
          <div class="content">
            <a class="header">{{name}}</a>
            <div class="meta">
              <span class="date">{{member['Title']}}</span>
            </div>
            <div class="description">
              {{member['Info']}}
            </div>
          </div>
          <div class="extra content">
            <a :href="`mailto:${member['Email']}`" >
              <i class="at icon"></i>
              {{member['Email']}}
            <br>
            </a>
            <a :href="`${member['Email']}`" target = "_blank" rel="noopener noreferrer">
              <i class="github square icon"></i>
              GitHub
            </a>
          </div>
        </div>
      </div>
    </div>

    <br><br><br>

    <center>
        <div>
            <router-link to="/">Return to main site --></router-link>
        </div>
        <div>
            <router-link to="/donate">Donate!</router-link>
        </div>
    </center>

  </div>
</template>

<script>
export default {
  name: "Aboutv2",
  data:
  function() {
    return {
        members: {
          "James Weir": {
            "Title" : "Project Leader",
            "Info" : "Some info would be here I guess.",
            "Email" : "weirj@rpi.edu",
            "GitHub" : "https://github.com/JPWeir",
          },
          "Nicholas Desmarais": {
            "Title" : "Lead Developer",
            "Info" : "Dad.",
            "Email" : "desman@rpi.edu",
            "GitHub" : "https://github.com/N-Desmarais",
          },
          "Max Stewar Steele": {
            "Title" : "Full Stack Developer",
            "Info" : "Made this page.",
            "Email" : "stewam8@rpi.edu",
            "GitHub" : "https://github.com/maxstewartsteele",
          },
          "Michael Fitzgerald": {
            "Title" : "Frontend Developer",
            "Info" : "Design :( .",
            "Email" : "fitzgm6@rpi.edu",
            "GitHub" : "https://github.com/fitzichael",
          },
          "Max Herman": {
            "Title" : "Backend Developer",
            "Info" : "Node Guy.",
            "Email" : "hermam3@rpi.edu",
            "GitHub" : "https://github.com/max-herman",
          },
          "Joseph Casente": {
            "Title" : "Backend Developer",
            "Info" : "Fell down the stairs.",
            "Email" : "casenj@rpi.edu",
            "GitHub" : "https://github.com/jcasente",
          },
          "Chelsea Bovell": {
            "Title" : "SD+D Developer",
            "Info" : "City Girl.",
            "Email" : "@rpi.edu",
            "GitHub" : "https://github.com/ChelsMarie",
          },
          "David Quian": {
            "Title" : "SD+D Developer",
            "Info" : "Ray of Sunshine.",
            "Email" : "@rpi.edu",
            "GitHub" : "https://github.com/DQuian2001",
          },
          "Enis Aras": {
            "Title" : "SD+D Developer",
            "Info" : "Lost his Socks.",
            "Email" : "arass@rpi.edu",
            "GitHub" : "https://github.com/enisaras",
          },
          "Ian McCaffery": {
            "Title" : "SD+D Developer",
            "Info" : "Expensive Hobby Conniseur.",
            "Email" : "@rpi.edu",
            "GitHub" : "https://github.com/ianmccaffery",
          },
          "Alice Bibaud": {
            "Title" : "SD+D Developer",
            "Info" : "Clueless RCOS Mentor.",
            "Email" : "bibaua@rpi.edu",
            "GitHub" : "https://github.com/semicolon-madness",
          },
          "Sam Katzman": {
            "Title" : "SD+D Beta Tester",
            "Info" : "Did Nothing.",
            "Email" : "katzms3@rpi.edu",
            "GitHub" : "https://github.com/themanofcat",
          }
        }
    }
  }
};
</script>

<style scoped>

.about-section {
  padding: 50px;
  text-align: center;
  background-color: #3cb15f;
  color: white;
}

</style>
