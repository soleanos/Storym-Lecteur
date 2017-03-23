<template>
  <div id="app">
               <md-toolbar>
                    <div class="md-toolbar-container">
                      <md-button class="md-icon-button" @click.native="toggleLeftSidenav">
                        <md-icon>menu</md-icon>
                      </md-button>
                      <h2 class="md-title">Storym</h2>
                      <span style="flex: 1;"></span>

                      <md-button class="md-icon-button" @click.native="openDialog('Searchbox')">
                        <md-icon>search</md-icon>
                      </md-button>

                      <md-button class="md-icon-button">
                        <md-icon>filter_list</md-icon>
                      </md-button>
                    </div>


<!--Searchbox setion-->
  <md-dialog md-open-from="#fab" md-close-to="#fab" ref="Searchbox" class="md-large">
    <md-dialog-title>Filter</md-dialog-title>

    <md-dialog-content>
      <form>
        <md-input-container>
          <label>Recherche</label>
          <md-input></md-input>
        </md-input-container>

        <md-checkbox id="Realistic" name="Realistic" class="md-primary">Realistic fiction</md-checkbox><br>
        <md-checkbox id="Comedy" name="Comedy"  class="md-primary">Comedy</md-checkbox><br>
        <md-checkbox id="Thriller" name="Thriller"  class="md-primary">Thriller/Horror</md-checkbox><br>
        <md-checkbox id="Classiques" name="Classiques"  class="md-primary">Classiques</md-checkbox><br>
        <md-checkbox id="sci-fi" name="sci-fi"  class="md-primary">sci-fi</md-checkbox><br>
        <md-checkbox id="Tragedy" name="Tragedy"  class="md-primary">Tragedy</md-checkbox><br>
        <md-checkbox id="Tragicomedy" name="Tragicomedy" class="md-primary">Tragicomedy</md-checkbox>
      </form>
    </md-dialog-content>

    <md-dialog-actions>
      <md-button class="md-primary" @click.native="closeDialog('Searchbox')">Cancel</md-button>
      <md-button class="md-primary" @click.native="closeDialog('Searchbox')">GO</md-button>
    </md-dialog-actions>
  </md-dialog>
<!--End Searchbox setion-->


<!--sidebar section-->
              </md-toolbar>

                <md-sidenav class="md-left" ref="leftSidenav">
                    <md-toolbar class="md-account-header">
                        <md-list class="md-transparent">
                            <md-list-item class="md-avatar-list">
                              <md-avatar class="md-large">
                                <img src="https://placeimg.com/80/80/people/8" alt="People">
                              </md-avatar>
                            </md-list-item>

                            <md-list-item>
                              <div class="md-list-text-container">
                                <span>Dupont Jean-Marc</span>
                                <span>jm.dupont@storym.com</span>
                              </div>

                              <md-button class="md-icon-button md-list-action">
                                <md-icon>arrow_drop_down</md-icon>
                              </md-button>
                            </md-list-item>
                      </md-list>
                    </md-toolbar>

                    <md-list>
                        <md-list-item @click.native="$refs.leftSidenav.toggle()" class="md-primary">
                          <md-icon class="md-primary">people</md-icon> <span>My profile</span>
                        </md-list-item>
                        <md-list-item @click.native="$refs.leftSidenav.toggle()" class="md-primary">
                          <md-icon class="md-primary">favorite</md-icon> <span>My favorite stories</span>
                        </md-list-item>
                    </md-list>

                </md-sidenav>
<!--sidebar section-->


    <storyList></storyList>
  </div>
</template>

<script>
import storyList from './components/listeHistoire'
export default {
  name: 'app',
  components: {
    storyList
  },
  methods: {
    toggleLeftSidenav() {
      this.$refs.leftSidenav.toggle();
    },
    openDialog(ref) {
      this.$refs[ref].open();
    },
    closeDialog(ref) {
      this.$refs[ref].close();
    },
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0;
}
</style>
