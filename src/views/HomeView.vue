<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-grey">Hi,</h1>
              <h1 class="text-white">I'M Sertaç Haloğlu</h1>
              <span class="text-grey">Web Designer & Developer</span><br />
              <v-btn
                tile
                dark
                class="mt-8"
                style="color: #0e8388"
                variant="outlined"
                >Contact Me</v-btn
              >
            </div>
          </v-col>
          <v-col cols="2">
            <div
              style="
                position: absolute;
                z-index: 9999;
                bottom: 0;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                text-align: center;
              "
            >
              <v-icon style="color: #0e8388">fas fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999" class="mt-16">
              <v-img src="../../public/me.png" contain max-height="300"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>

      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6" class="mx-auto">
              <div class="egg">
                <v-img src="../../public/me2.png" max-height="310"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h2 class="mt-16">About Me</h2>
              <div style="width: 120px">
                <v-slider
                  v-model="slider2"
                  color="#0e8388"
                  track-color="#0e8388"
                >
                </v-slider>
              </div>
              <h4 class="mt-n4">I Am a Creative Web Designer</h4>
              <h4>And Developer</h4>
              <p class="text-grey">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse
                repudiandae autem debitis, fugiat nesciunt accusamus nobis
                minima distinctio impedit excepturi repellendus facilis eveniet
                quis cumque?
              </p>
              <br />
              <p class="text-grey">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse
                repudiandae autem debitis, fugiat nesciunt accusamus nobis
                minima distinctio impedit excepturi repellendus facilis eveniet
                quis cumque?
              </p>
              <br />
              <p class="text-grey">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse
                repudiandae autem debitis, fugiat nesciunt accusamus nobis
                minima distinctio impedit excepturi repellendus facilis eveniet
                quis cumque?
              </p>
              <v-btn tile dark color="#0e8388" class="mt-4">
                Download Resume
              </v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h2>What we Do</h2>
        <div style="width: 120px; margin: 0 auto">
          <v-slider
            v-model="slider2"
            color="#0e8388"
            track-color="#0e8388"
          ></v-slider>
        </div>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn
                  icon="fas fa-laptop"
                  color="#0e8388"
                  class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">Web Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor sit amet <br />
                  consectetur adipisicing elit. <br />
                  Fugiat, voluptate!
                </p>
              </div>
              <div class="child">
                <v-btn
                  icon="fas fa-mobile-alt"
                  color="#0e8388"
                  class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">App Design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor sit amet <br />
                  consectetur adipisicing elit. <br />
                  Fugiat, voluptate!
                </p>
              </div>
              <div class="child">
                <v-btn
                  icon="fas fa-camera"
                  color="#0e8388"
                  class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">Photography</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor sit amet <br />
                  consectetur adipisicing elit. <br />
                  Fugiat, voluptate!
                </p>
              </div>
            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>
      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#0e8388" class="mr-2 text-white">All</v-btn>
          <v-btn class="mr-2" variant="tonal">Web Design</v-btn>
          <v-btn class="mr-2" variant="tonal">App Design</v-btn>
          <v-btn class="mr-2" variant="tonal">Photography</v-btn>
          <v-btn variant="tonal">Graphic Design</v-btn>
        </div>
      </v-col>
      <v-col cols="12" class="imgHover">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{ isHovering, props }">
                <v-card
                  :elevation="isHovering ? 12 : 2"
                  :class="{ 'on-hover': isHovering }"
                  v-bind="props"
                >
                  <v-img :src="item.img" height="300px" cover> </v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#CBE4DE" class="mt-4">Load More</v-btn>
        </div>
      </v-col>
      <v-col cols="12" id="page">
        <div class="pre">
          <v-row>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="600" height="">
                <v-img src="slider1.png" height="300px" cover></v-img>
                <v-card-title>We provide you for the best</v-card-title>
                <v-card-subtitle>
                  By Sertaç Haloğlu | 09 March 2023
                </v-card-subtitle>
                <v-card-text>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Vitae
                  quia, temporibus harum, ipsam aliquid cumque quaerat
                  exercitationem voluptatibus laudantium itaque voluptate nemo
                  atque labore?
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="600" height="">
                <v-img src="slider2.png" height="300px" cover></v-img>
                <v-card-title>We provide you for the best</v-card-title>
                <v-card-subtitle>
                  By Sertaç Haloğlu | 09 March 2023
                </v-card-subtitle>
                <v-card-text>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Vitae
                  quia, temporibus harum, ipsam aliquid cumque quaerat
                  exercitationem voluptatibus laudantium itaque voluptate nemo
                  atque labore?
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="600" height="">
                <v-img src="slider3.png" height="300px" cover></v-img>
                <v-card-title>We provide you for the best</v-card-title>
                <v-card-subtitle>
                  By Sertaç Haloğlu | 09 March 2023
                </v-card-subtitle>
                <v-card-text>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Vitae
                  quia, temporibus harum, ipsam aliquid cumque quaerat
                  exercitationem voluptatibus laudantium itaque voluptate nemo
                  atque labore?
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" id="blog">
        <div class="hire">
          <v-row>
            <v-col cols="12" sm="9">
              <h1 class="mt-9">Hire me for your project of the dreams</h1>
              <p class="text-grey">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ipsum
                fugiat nulla quidem dignissimos pariatur nobis minima delectus,
                aperiam ea consequuntur quos expedita quod reiciendis numquam.
              </p>
            </v-col>
            <v-col cols="12" sm="3">
              <v-btn color="#0e8388" class="mt-15 text-white" width="150px"
                >Hire Me</v-btn
              >
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>
          <v-col cols="12" sm="4">
            <div class="child">
              <h1>Contact info.</h1>
              <v-btn
                icon="fas fa-map-marker-alt"
                color=""
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">Your Street, Your Zone </span><br />
              <v-btn
                icon="fas fa-phone-alt"
                color=""
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">0-(555)-555-55-55</span> <br />
              <span class="text-caption">0-(555)-555-55-55</span> <br />
              <v-btn
                icon="fas fa-envelope"
                color=""
                class="mt-10"
                variant="outlined"
              ></v-btn
              ><br />
              <span class="text-caption">example@gmail.com </span> <br />
              <span class="text-caption">example@gmail.com </span> <br />
            </div>
          </v-col>
          <v-col cols="12" sm="8">
            <h1 class="mt-8">Send your message</h1>
            <v-divider></v-divider>
            <span class="text-caption"
              >Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt
              fugiat officia, odio eaque exercitationem libero nesciunt placeat,
              repellat obcaecati sed tenetur! Est labore aliquam amet
              consequatur necessitatibus fugit obcaecati facilis!</span
            >
            <v-row class="mt-10">
              <v-col cols="12" sm="6">
                <v-text-field
                  label="Name"
                  persistent-hint
                  variant="outlined"
                ></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-text-field
                  label="Phone No"
                  persistent-hint
                  variant="outlined"
                ></v-text-field>
              </v-col>
            </v-row>
            <v-textarea
              label="Message"
              persistent-hint
              variant="outlined"
            ></v-textarea>
            <v-btn color="#0e8388" class="mt-2 text-white">Submit Now</v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-container>
    <FooterView />
  </v-app>
</template>

<script>
import { defineComponent } from "vue";

// Components
import NavBar from "@/components/NavBar.vue";
import FooterView from "@/components/FooterView.vue";
export default defineComponent({
  name: "HomeView",
  setup() {
    return {
      slider2: 50,

      items: [
        {
          img: "slider1.png",
        },
        {
          img: "slider2.png",
        },
        {
          img: "slider3.png",
        },
        {
          img: "slider4.png",
        },
        {
          img: "slider5.png",
        },
        {
          img: "slider6.png",
        },
      ],
    };
  },

  components: {
    NavBar,
    FooterView,
  },
});
</script>
<style scoped>
.v-container {
  padding: 16px 0 16px 0;
}
.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}
.head:before {
  content: "";
  position: absolute;
  top: -1px;
  left: 0;
  height: 100%;
  width: 50%;
  background: #2c3333;
  transform: skew(0deg, 6deg);
}
.head:after {
  content: "";
  position: absolute;
  top: -1px;
  right: 0;
  height: 100%;
  width: 50%;
  background: #2c3333;
  transform: skew(0deg, -6deg);
}

.egg {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #2e4f4f;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}

.first {
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2rem;
}

.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}

.imgHover {
  padding: 0 200px;
}

.pre {
  width: 100%;
  height: 500px;
  text-align: center;
  padding: 0 300px;
  background-color: #ebf8f6;
}

.hire {
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background-color: #cce5e6;
  margin-top: -24px;
}
</style>
