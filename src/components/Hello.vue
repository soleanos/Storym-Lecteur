<template>

<md-layout md-gutter class="phone-viewport">
    <!-- show the events-->
            <md-layout md-column class="md-accent" md-flex-large="100">
              List of stories
            </md-layout>      

    <div class="card-holder" md-column >
              <span style="flex: 1"></span>
              <md-card md-flex-large="150" v-for="event in events">
                <md-card-media > 
                  <img v-bind:src="event.image"/>
                </md-card-media>

                <md-card-header>
                  <h2>{{ event.Titre }}</h2>
                  <h4 class="glyphicon glyphicon-calendar">Auteur : {{ event.Auteur }}</h4>
                  <h5 class="list-group-item-text" >Genre : {{ event.genre }}</h5>
                </md-card-header>
              
                <md-card-expand>
                  <md-card-actions>
                    <md-button >Lire</md-button>
                    <span style="flex: 1"></span>
                    <md-button class="md-icon-button" >
                      <md-icon>favorite</md-icon>
                    </md-button>
                    <md-button class="md-icon-button" md-expand-trigger>
                      <md-icon>keyboard_arrow_down</md-icon>
                    </md-button>
                  </md-card-actions>

                  <md-card-content>
                    Abstract : {{ event.Synopsis }}
                  </md-card-content>
                </md-card-expand>
          </md-card>

          
        </div>
    </md-layout>

</template>

<script>
export default {
  name:'hello',
  data () {
    return {
      msg: 'Add an Event',

        event: { Titre: '', Synopsis: '', Auteur: '', Note: '', genre:'', image:'', id:'' },
        
          events: [
           {
            id:'1',
            Titre: "Rainbow List: 2017 ",
            genre: "Fiction",
            Auteur: "Maggie Reagan",
            DateCreation: "2012-04-23T18:25:43.511Z",
            DateModification: "2012-04-23T18:25:43.511Z",
            DatePublication: "2012-04-23T18:25:43.511Z",
            Note: 2,
            Synopsis: "Harry arrive à l’école des sorciers",
            image: "https://placeimg.com/380/380/animals"
          },

            {
            id:'2',
            Titre: "American Girls",
            genre: "Fiction",
            Auteur: "Alison Umminger",
            DateCreation: "2012-04-23T18:25:43.511Z",
            DateModification: "2012-04-23T18:25:43.511Z",
            DatePublication: "2012-04-23T18:25:43.511Z",
            Note: 3,
            Synopsis: "After “borrowing” her mother-in-law’s credit card to escape some trouble hangs out on the Disneyesque Chips Ahoy television-show set.",
            image: "https://placeimg.com/380/380/animals"
          },

            {
            id:'3',
            Titre: "Ask Me How I Got Here",
            genre: "Fiction",
            Auteur: "Christine Heppermann",
            DateCreation: "2012-04-23T18:25:43.511Z",
            DateModification: "2012-04-23T18:25:43.511Z",
            DatePublication: "2012-04-23T18:25:43.511Z",
            Note: 4,
            Synopsis: "Harry arrive à l’école des sorciers",
            image: "https://placeimg.com/380/380/nature"
          },
          {
            id:'4',
            Titre: "Harry Potter",
            genre: "Fiction",
            Auteur: "Jk Rolling",
            DateCreation: "2012-04-23T18:25:43.511Z",
            DateModification: "2012-04-23T18:25:43.511Z",
            DatePublication: "2012-04-23T18:25:43.511Z",
            Note: 2,
            Synopsis: "Harry arrive à l’école des sorciers",
            image: "https://placeimg.com/380/380/animals"
          },
          {
          id:'5',
            Titre: "La belle et la bette",
            genre: "Fiction",
            Auteur: "Luc Besson",
            DateCreation: "2012-04-23T18:25:43.511Z",
            DateModification: "2012-04-23T18:25:43.511Z",
            DatePublication: "2012-04-23T18:25:43.511Z",
            Note: 2,
            Synopsis: "Harry arrive à l’école des sorciers",
            image: "https://placeimg.com/380/380/animals"
          },
          {
          id:'6',
            Titre: "King Kong",
            genre: "Fiction",
            Auteur: "Maggie Reagan",
            DateCreation: "2012-04-23T18:25:43.511Z",
            DateModification: "2012-04-23T18:25:43.511Z",
            DatePublication: "2012-04-23T18:25:43.511Z",
            Note: 2,
            Synopsis: "Harry arrive à l’école des sorciers",
            image: "https://placeimg.com/380/380/animals"
          },
          {
          id:'6',
            Titre: "King Kong",
            genre: "Fiction",
            Auteur: "Maggie Reagan",
            DateCreation: "2012-04-23T18:25:43.511Z",
            DateModification: "2012-04-23T18:25:43.511Z",
            DatePublication: "2012-04-23T18:25:43.511Z",
            Note: 2,
            Synopsis: "Harry arrive à l’école des sorciers",
            image: "https://placeimg.com/380/380/animals"
          }
    ]

    }
  }
}
</script>
