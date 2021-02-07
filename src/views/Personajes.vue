<template>
<div>
  
  <!-- Seccion Central TABLA -->

  <div class="section-personajes">

    <div>
      <img class="imagen-trans" src="../assets/fondo-personajes2.jpg" alt="foto fondo">
    </div>

  </div>



  <div class="seccion-tabla">



    <h1 class="titulo-personajes"> PERSONAJES DEL JUEGO</h1>



    <div class="container">
      <div class="row">
        <div class="col-6 col-md-6">

          <div class="zona-boton">

            <label class="switch">
              <input id="checkbox-filtro" type="checkbox">
              <span class="slider round"></span>
            </label>
            <p class="parrafo-filtro">Activar / Desactivar FILTRO</p>

          </div>

        </div>
        <div class="col-6 col-md-6">

          <div class="zona-buscar" id="buscador-filtro">

            <input class="form-control input-filtro hidden" id="inputTabla" type="search" placeholder="Filtrar Busqueda"
              aria-label="Search">

          </div>

        </div>
      </div>
    </div>




    <table id="tablaDinamica"> </table>



    <!-- Button modal AGREGAR -->
    <button type="button" class="btn btn-success btn-agregar" data-toggle="modal" data-target="#staticBackdrop">
      Agregar Personaje
    </button>

    <!-- Modal AGREGAR -->
    <div class="modal fade" id="staticBackdrop" data-backdrop="static" data-keyboard="false" tabindex="-1"
      aria-labelledby="staticBackdropLabel" aria-hidden="true">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="staticBackdropLabel">AGREGAR PERSONAJE</h5>
            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            <div>
              <input id="nombreModal" type="text" class="form-control" placeholder="NOMBRE">
              <input id="origenModal" type="text" class="form-control" placeholder="ORIGEN">
              <input id="edadModal" type="text" class="form-control" placeholder="EDAD">
              <input id="caracteristicaModal" type="text" class="form-control" placeholder="CARACTERISTICA">
              <input id="habilidadModal" type="text" class="form-control" placeholder="HABILIDAD">
            </div>
            <h4 class="titulo-modal">
              SE ESTA POR AGREGAR UN NUEVO PERSONAJE!
              DESEA CONTINUAR?
            </h4>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-dismiss="modal">Cancelar</button>
            <button id="agregar" type="button" class="btn btn-primary" data-dismiss="modal">Continuar</button>
          </div>
        </div>
      </div>
    </div>

    <!-- SPINNER -->

    <button id="boton-cargar" class="btn btn-primary text-nowrap btn-spinner hidden" type="button">
      <span class="spinner-border spinner-border-sm mr-2"></span>
      Enviando datos...
    </button>



  </div>






  <!-- MODAL EDITAR -->

  <div class="modal fade" id="modal-edit" data-backdrop="static" data-keyboard="false" tabindex="-1"
    aria-labelledby="staticBackdropLabel2" aria-hidden="true">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="staticBackdropLabel2">INGRESE SUS NUEVOS DATOS :</h5>
          <button type="button" class="close" data-dismiss="modal" aria-label="Close">
            <span aria-hidden="true">&times;</span>
          </button>
        </div>
        <div class="modal-body">
          <div>
            <input id="editarNombre" type="text" class="form-control" placeholder="Nombre">
            <input id="editarOrigen" type="text" class="form-control" placeholder="Origen">
            <input id="editarEdad" type="text" class="form-control" placeholder="Edad">
            <input id="editarCaracteristica" type="text" class="form-control" placeholder="Caracteristica">
            <input id="editarHabilidad" type="text" class="form-control" placeholder="Habilidad">
          </div>
          <h4 class="titulo-modal">
            ESTA POR EDITAR EL PERSONAJE!
            DESEA GUARDARLO?
          </h4>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-secondary" data-dismiss="modal">Cancelar</button>
          <button id="btn-editar-modal" type="button" class="btn btn-primary btn-edit" data-dismiss="modal">Guardar</button>
        </div>
      </div>
    </div>
  </div>



  <!-- MODAL ELIMINAR -->

  <div id="modal-eliminar">
    <div class="modal" tabindex="-1" id="modal-elim">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title">ELIMINAR PERSONAJE</h5>
            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            <p>ESTA POR ELIMINAR EL PERSONAJE! DESEA CONTINUAR?</p>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-dismiss="modal">Cancelar</button>
            <button id="btn-eliminar-modal" type="button" data-dismiss="modal"
              class="btn btn-primary botonesEliminar">Continuar</button>
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

       
.section-personajes {
    width: 100%;
    height: 591.3px;
    display: flex;

}

.seccion-tabla{
    width: 100%;
    height: 1300px;
}


.imagen-trans{

        display: flex;
        position: absolute;
        width: 100%;
        height: 90%;
        top: 100px;
        left: 0;
        
}

    


.titulo-personajes{
    text-align: center;
    font-size: 20px;
    text-decoration: underline;
    padding: 25px;
}


table {
    width: 1000px;
    font-size: 16px;
    text-align: center;
    border: 1px solid black;
    height: 340px; 
    margin-left: 170px;
       
}

.td-Head{
    background-color: #f4f4f4;
    border: solid 1px black;
    padding: 14px;
    font-size: 18px;
    font-weight: bold;   
}
 

.td-Elementos{
   border: 1px solid black;
   padding: 6px;
}

.btn-accion{
    margin-top: 5px;
    margin-right: 5px;
    display: inline-block;
    width: 75px;
    border-radius: 5px;
    padding: 1px;
    margin-bottom: 5px;
}

.btn-agregar{
 
    margin-left: 580px;
    margin-top: 40px;   
    margin-bottom: 30px;
}

.tr-Elementos{
    border: 1px solid black;
 }


 .btn-eliminar{
    margin-top: 5px;
    margin-right: 5px;
    display: inline-block;
    width: 75px;
    border-radius: 5px;
    padding: 1px;
    margin-bottom: 5px;
 }

 .titulo-modal{
     font-size: 15px;
     margin-top: 15px;
 }

 .form-control{
      margin-bottom: 10px;
      width: 50%;
 }

 .input-filtro{
   width: 200px;
 }


 .zona-boton{
width: 100%;
height: 100px;

 }
 .zona-buscar{
    width: 100%;
    height: 100px;
    margin-top: 35px;
  
    
 }
 .parrafo-filtro{
     font: bold;
     font-size: 15px;
     font-weight: 500;
     margin-left: 65px;
     
 }



 .filtro{
     width: 100%;
     padding-bottom: 25px;
     
 }
 
    


 
/* progress bar */

.btn-spinner{
    display: flex;
    margin-bottom: px;
    margin-left: 573px;
    
  
}


.hidden{

    visibility: hidden;
}

.visible{
    visibility: visible;
}

.none{
   display: none;
}

.block{
    display: block;
}



/* Toggle Bar */

.switch {
    position: relative;
    display: inline-block;
    width: 60px;
    height: 34px;
    margin-top: 28px;
    margin-left: 127px;
  }
  
  .switch input { 
    opacity: 0;
    width: 0;
    height: 0;
  }
  
  .slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: #ccc;
    -webkit-transition: .4s;
    transition: .4s;
  }
  
  .slider:before {
    position: absolute;
    content: "";
    height: 26px;
    width: 26px;
    left: 4px;
    bottom: 4px;
    background-color: white;
    -webkit-transition: .4s;
    transition: .4s;
  }
  
  input:checked + .slider {
    background-color: #2196F3;
  }
  
  input:focus + .slider {
    box-shadow: 0 0 1px #2196F3;
  }
  
  input:checked + .slider:before {
    -webkit-transform: translateX(26px);
    -ms-transform: translateX(26px);
    transform: translateX(26px);
  }
  
  /* Rounded sliders */
  .slider.round {
    border-radius: 34px;
  }
  
  .slider.round:before {
    border-radius: 50%;
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