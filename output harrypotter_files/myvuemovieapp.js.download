Vue.component('movie-detail', {

    props: ['movie'],

    template: `
    <div>
    <div class="card" style="width: 18rem;">
  <img class="card-img-top" v-bind:src="movie.Poster" alt="Card image cap">
  <div class="card-body">
    <h5 class="card-title">{{movie.Title}}</h5>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
    </div>
    `
});

new Vue({
    el: "#mymovieapp",
    data: {
        searchkey: '',
        moviesList: []
    },

    methods: {

        searchMovies() {
            //http://www.omdbapi.com/?s=harry%20potter&apikey=e0620bd4
            var url = 'http://www.omdbapi.com/?s=' + this.searchkey + '&apikey=e0620bd4';
            fetch(url)
                .then(response => response.json())
                .then(data => {
                    this.moviesList = data;
                })
        }
    }
})