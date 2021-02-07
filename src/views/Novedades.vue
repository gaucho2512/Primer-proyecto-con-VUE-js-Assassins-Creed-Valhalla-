<template>
  
  <div>
    
  <!--   SECTION CENTRAL  -->



  <div class="container">
    <div class="row">
      <div class="col-sm-12">

        <div class="novedades-video">

          <h1> Assassins Creed Valhalla - Trailer de Anuncio </h1>

          <iframe class="iframe-video" src="https://www.youtube.com/embed/1Z7mIKGzowQ"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>

        </div>
      </div>

    </div>
  </div>




  <!-- imagen central y Card -->

  <div class="row">
    <div class=" col-sm-12 col-md-12 ">

      <div class="section-novedades">

        <div class="card" style="width: 65%; ">

          <img src="../assets/fondo-coleccionista.jpg" class="card-img-top" alt="foto-coleccionista">

          <div class="card-body">
            <h5 class="card-title">Assassin's Creed Valhalla edición coleccionista</h5>
            <p class="card-text">En Assassin's Creed® Valhalla, encarnarás a Eivor, una feroz leyenda vikinga criada
              entre historias de batallas y gloria. Explora un hermoso mundo abierto y cambiante, ambientado en la
              despiadada Inglaterra de los años oscuros. Saquea a tus enemigos, haz prosperar tu asentamiento y
              consolida tu poder político mientras luchas por ganarte un sitio entre los dioses en el Valhalla. </p>
          </div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item"> - Ultimate Edicion PC </li>
            <li class="list-group-item"> - Réplica de Ubicollectibles® de alta calidad de Eivor y su Drakkar (altura:
              30cm) </li>
            <li class="list-group-item"> - Caja de coleccionista única </li>
            <li class="list-group-item"> - El Steelbook® exclusivo de Ubisoft Store, con un diseño único inspirado en
              los emblemas del juego. </li>
            <li class="list-group-item"> - Figura Vikinga de Eivor junto a su cuervo y con su Hacha Danesa (altura: 5cm)
            </li>
            <li class="list-group-item"> - Certificado de Autenticidad Premium, con un número de serie único para cada
              Edición. </li>
            <li class="list-group-item"> - Un pack de 3 litografías mostrando algunos de los artes conceptuales más
              impresionantes creados para el juego. </li>
          </ul>
          <div class="card-body ">
            <a href="https://store.ubi.com/es/assassin-s-creed-valhalla-collector-edition/5e84b6f95cdf9a21c0b4e746.html"
              class="card-link btn btn-success " target="_blank">COMPRAR</a>

          </div>
        </div>



      </div>
    </div>
  </div>



  </div>
  
</template>

<script>
export default {

}
</script>

<style>


.novedades-video{
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 700px;
    margin-top: 100px;
   

}

.novedades-video h1{
    text-align: center;
    margin: 50px;
    border-radius: 20px;
    text-shadow: 1px 1px 1px white;  

}



.section-novedades{
    display: flex;
    width: 100%;
    height: 900px;
    background-image: url(../assets/edicol1.jpg);
    background-repeat: no-repeat;
    background-size: 100% 100%;
    flex-direction: column;
    justify-content: center ;
    align-items: center;
    opacity: 0.9;


    
    
}


.card-body{
    text-align: center;
}


.iframe-video{
    width: 100%;
    height: 500px;
    
}


/* COLORES */


.novedades-video h1{
    background-color: #aaaaaa;

    }


    

    /*  @ MEDIA  */




    @media  screen and (max-width: 490px){
        footer div  h4{
            display: none;
           
        }
        .titulo-article{
            font-size: 25px;
        }

        section{
            height: 1350px;
        }

        article{
            height: 550px;
        }
        
    }



    
    @media  screen and (max-width: 576px) { 
        .novedades-video h1{
            font-size: 25px;
        }

     }





    @media screen and (max-width: 768px) { 
      footer div  h4{
            font-size: 18px;
        }

        .titulo-section{
            font-size: 18px;
        }

        .parrafo-section{
            font-size: 10px;
        }

        .titulo-article{
            margin-top: 200px;
        }
    }



      
    
    @media  screen and (max-width: 992px) { 
        .card{
            height: 1100px
        }
        .section-novedades{
            height: 1150px;
        }
    }
        


       
    
    
    @media  screen and (max-width: 1200px) { 
        .logo-copyright{
            width: 20%;
        }

     }




</style>