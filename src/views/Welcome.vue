<template>
   <app-master>


        <div slot='breadcrumb'>
        <app-breadcrumb>
             <div class="title-box text-left" >
                <div class="page-title-heading" style="text-align: center">
                    <h1 class="title" >{{ this.$store.state.config.app_name }}</h1>
                </div><!-- /.page-title-captions -->
                <div class="breadcrumb-wrapper" style="text-align: center">
                    <span class="ttm-textcolor-skincolor"> &nbsp;&nbsp; {{ this.$store.state.config.tagline }} </span>
                </div>  

                <div class="about-overlay-02 center-overlay-style1 overlay-improved">
                     <router-link tag="a" to="/products"> 
                    <div class="ttm-icon ttm-icon_element-color-skincolor ttm-icon_element-size-md">
                        <i class="flaticon flaticon-cow-3"></i>
                        <!--  ttm-icon --> 
                    </div>
                   <h6>Shop Now </h6>

                    </router-link>
                </div>
            </div>
        </app-breadcrumb>
    </div>

    

      <div slot="main-content">

          <div class="shopping-bar">
               <div class="shopping-bar__button">
                   <router-link to="/products">
                     Shop Now
                  </router-link>
                 
              </div>
              <div class="shopping-bar__content">
                 
                  Experience best shopping experience 
              </div>
             
          </div>

           <section class="ttm-row about-section clearfix" style="padding-bottom:0px; padding-top: 70px;">
                <div class="container">
                    <div class="row"><!-- row -->
                        <div class="col-lg-4">
                           <div class="ml_130 res-991-ml-0">
                                            <!-- ttm_single_image-wrapper -->
                                            <div class="ttm_single_image-wrapper after-border style1 position-relative">
                                                <img class="img-fluid" src="/img/chic.jpg" title="single-img-three" alt="single-img-three">
                                            </div><!-- ttm_single_image-wrapper end -->
                                            <div class="about-overlay-02 center-overlay-style1">
                                                <!-- <div class="ttm-icon ttm-icon_element-color-skincolor ttm-icon_element-size-md">
                                                    <i class="flaticon flaticon-cow-3"></i> -->
                                                    <!--  ttm-icon --> 
                                                <!-- </div> -->
                                               <router-link tag="a" to="/category/fish-&-meat"> <h6 style="margin-top:40px;">Organic Chicken</h6> </router-link>
                                            </div>
                                        </div>
                        </div>
                        <div class="col-lg-8">
                            <div class="res-991-mt-30">
                                <!-- section title -->
                                <div class="section-title clearfix">
                                    <div class="title-header">
                                        <!-- <h5>ABOUT FOOD PARK</h5> -->
                                        <h2 class="title">Welcome to Food Park</h2>
                                    </div>
                                    <div class="heading-seperator">
                                        <span></span>
                                    </div>
                                </div><!-- section title end -->
                                <p class="mine">Food Park provides high quality food processing infrastructure near farms.</p>
                                <p class="mine">Our mission is to foster a world of healthy food through establishing direct linkages from the farm - to processing - to consumer markets.</p>
                                <p class="mine"> Ecommerce Focus: we solely enrol food products that are; </p>
                                   <div class="mt-15">
                                    <ul class="ttm-list ttm-list-style-icon">
                                        <li><i class="fa fa-check-circle-o ttm-textcolor-skincolor"></i><span class="ttm-list-li-content">Naturally grown</span></li>
                                        <li><i class="fa fa-check-circle-o ttm-textcolor-skincolor"></i><span class="ttm-list-li-content">Under gone Good Agricultural Practices</span></li>
                                        <li><i class="fa fa-check-circle-o ttm-textcolor-skincolor"></i><span class="ttm-list-li-content">Good Manufacturing Practices </span></li>
                                        <li><i class="fa fa-check-circle-o ttm-textcolor-skincolor"></i><span class="ttm-list-li-content">Standard Hygiene Process</span></li>
                                        <li><i class="fa fa-check-circle-o ttm-textcolor-skincolor"></i><span class="ttm-list-li-content">Food Safety and Traceability</span></li>
                                    </ul>
                                </div>
                                <p class="mine"> Over 800 farmers have been enlisted on our platform.</p>
                                <p class="mine"> Patronize us to Change your Food Experience. </p>
                                
                            </div>
                        </div>
                    </div>
                    <!-- row end -->
                </div>
            </section>
            <!-- aboutus-section end -->


          



              <!-- team-section -->
            <section class="ttm-row second-team-section clearfix" style="margin-top: 0px; padding-top: 40px">
                <div class="container">
                    <div class="row"> 
                    
                        <div class="col-lg-12 col-xl-12 col-md-12">
                            <!-- section-title -->
                             <div class="section-title clearfix">
                                    <div class="title-header">
                                        <!-- <h5>ABOUT FOOD PARK</h5> -->
                                        <h2 class="title" style="font-size: 1.5rem">Product Categories</h2>
                                    </div>
                                    <div class="heading-seperator">
                                        <span></span>
                                    </div>
                                </div><!-- section title end -->
                            <!-- section-title end -->
                         </div>
          
                    </div>
                   
                    <!-- row -->
                    <div class="row slick_slider ttm-boxes-spacing-15px" data-slick='{"slidesToShow": 3, "slidesToScroll": 3, "dots":false, "arrows":false, "autoplay":false, "infinite":true, "centerMode":false}'>
                        
                        <div class="ttm-box-col-wrapper col-lg-3" v-for="(category, index) in product_categories" :key="index+'category'">
                            <!-- featured-imagebox-team -->
                            <div class="featured-imagebox featured-imagebox-team style1">
                                <div class="featured-thumbnail"><!-- featured-thumbnail -->
                                    <img class="img-fluid" :src="category.featured_image" alt="image">
                                    <div class="ttm-social-links-wrapper">
                                      <router-link  :to="{ name: 'Category', params: { name: convertToSlug(category.name) } }" class="main-category__items__content__link" > <a> View Products </a></router-link>
                                    </div>
                                </div> 
                                <div class="featured-content box-shadow">
                                    <div class="featured-title"><!-- featured-title -->
                                         <router-link  :to="{ name: 'Category', params: { name: convertToSlug(category.name) } }" class="main-category__items__content__link"  tag="h5"> <a> {{ category.name }} </a></router-link>
                                    </div>
                                    <p class="category">{{ category.description }}</p><!-- category -->
                                </div>
                            </div><!-- featured-imagebox-team end-->
                        </div>
                        
                     
                    </div>
                    <!-- row end-->
                </div>
            </section>
            <!-- team-section end -->




      </div>
   </app-master>
</template>

<script>
// @ is an alias to /src
import Master from "@/components/Master.vue";
import BreadCrumb from "@/components/BreadCrumb.vue";
import {seo} from "../Repositories/seo.js";
import { pick } from "../Repositories/pick"
import { vuesax } from "../Repositories/vuesax"
import { mapState, mapMutations, mapActions } from "vuex"



export default {
  name: "Welcome",
  mixins: [seo, pick, vuesax],
  components: {
    "app-master" : Master,
    "app-breadcrumb": BreadCrumb
  },
  data(){
      return {
          cat: '',
      }
  },
  computed: {

        ...mapState(
        'shop',
        [
            'product_categories'
        ])


  },
  methods: {},
    created(){
        //   (title, description)
        this.seoMetaData('Organic food – fish & meat, staples & vegetables, spices, household','Eat organic for food safety and better nutrition. Food Park promotes healthy living by offering up naturally-grown farm produce processed in the most hygienic environments.');

        

    }
};
</script>


<style scoped>
   .mine{
    margin : 0 0 8px;
    }

   


    
         


.ttm-page-title-row {
    display: block;
    padding-top: 2.5rem;
    padding-bottom: 2.5rem;
    z-index: 11;
}


.ttm-page-title-row {
    position: relative;
    background-image: url(/img/banner.png);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    filter: grayscale(30%);
    padding-top: 20px;
}


@media (min-width: 0px) and (max-width: 600px){

    .ttm-page-title-row{
        background-position-x: 15%;
        background-position-y: 1%;
    }
}


.breadcrumb-wrapper span{
    color: white
}


.overlay-improved{
    position: absolute;
    top: -10%;
    right: 0%;
    left:80%
}

.shopping-bar{
    display: none;
}


@media (min-width: 0px) and (max-width: 600px){
    .overlay-improved{
        display: none;
    }

    .shopping-bar{
        display: flex;
        flex-flow: row wrap;
        justify-content: flex-start;
        position: fixed;
        width: 100vw;
        height: 3rem;
        background: white;
        z-index: 1900;
        bottom: 0;
        left: 0;
        padding: 5px;
        box-shadow: 2px 2px 8px #000000c2;
    }


    
    .shopping-bar__content{
        text-align: center;
        margin-left: 0.4rem;
        font-size: 0.8rem;
        font-style: italic;
        line-height: 2.5;
    }



    .shopping-bar__button{
        margin-left: 0rem;
        color: white;
        background: green;
        width: auto;
        padding: 0.4rem 1.0rem;
        font-size: 0.7rem;
        text-align: center;
        cursor: pointer;
        border-radius: 5px;
        
        
        
    }

    .shopping-bar__button a{
        color: white;
    }

    .shopping-bar__button:hover,
    .shopping-bar__button:active{
        background: #00a85a;
    }
}
</style>
