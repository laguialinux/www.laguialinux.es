<template>
  <ion-header>
    <ion-navbar>
      <ion-row>
        <ion-col>
          <ion-buttons>
            <ion-menu-button menuToggle="main-menu"></ion-menu-button>
          </ion-buttons>
        </ion-col>

        <ion-col>
          <ion-title>
            (logo) La Guía Linux
          </ion-title>
        </ion-col>
      </ion-row>

      <ion-row>
        <ion-col class="center">
          <ion-button color="secondary">Publicaciones</ion-button>
          <ion-button color="tertiary">Noticias</ion-button>
          <ion-button color="success">Apps</ion-button>
          <ion-button color="warning">Contacto</ion-button>
          <ion-button color="danger">Videotutoriales</ion-button>
          <ion-button color="light">Distribuciones</ion-button>
          <ion-button color="medium">Juegos</ion-button>


          <ion-button color="primary" @click="setOpen(true, $event)">
            Enlaces Amigos
          </ion-button>
          <ion-popover
            :is-open="isOpenRef"
            css-class="my-custom-class"
            :event="event"
            :translucent="true"
            @onDidDismiss="setOpen(false)"
          >
            <ion-list>
              <ion-item>
                <ion-avatar slot="start">
                  <img src="https://gravatar.com/avatar/dba6bae8c566f9d4041fb9cd9ada7741?d=identicon&f=y">
                </ion-avatar>
                <ion-label>
                  <ion-button color="danger" expand="full" size="large">
                    Asociaciones
                    </ion-button>
                  </ion-label>
              </ion-item>

              <ion-item>
                <ion-avatar slot="start">
                  <img src="https://gravatar.com/avatar/dba6bae8c566f9d4041fb9cd9ada7741?d=identicon&f=y">
                </ion-avatar>
                <ion-label>
                  <ion-button color="danger" expand="full" size="large">
                    Podcasts
                    </ion-button>
                  </ion-label>
              </ion-item>
              
              <ion-item>
                <ion-avatar slot="start">
                  <img src="https://gravatar.com/avatar/dba6bae8c566f9d4041fb9cd9ada7741?d=identicon&f=y">
                </ion-avatar>
                <ion-label>
                  <ion-button color="danger" expand="full" size="large">
                    Canales de Telegram
                    </ion-button>
                  </ion-label>
              </ion-item>

              <ion-item>
                <ion-avatar slot="start">
                  <img src="https://gravatar.com/avatar/dba6bae8c566f9d4041fb9cd9ada7741?d=identicon&f=y">
                </ion-avatar>
                <ion-label>
                  <ion-button color="danger" expand="full" size="large">
                    Blogs
                    </ion-button>
                  </ion-label>
              </ion-item>

              <ion-item>
                <ion-avatar slot="start">
                  <img src="https://gravatar.com/avatar/dba6bae8c566f9d4041fb9cd9ada7741?d=identicon&f=y">
                </ion-avatar>
                <ion-label>
                  <ion-button color="danger" expand="full" size="large">
                    Webs
                    </ion-button>
                  </ion-label>
              </ion-item>

              <ion-item>
                <ion-avatar slot="start">
                  <img src="https://gravatar.com/avatar/dba6bae8c566f9d4041fb9cd9ada7741?d=identicon&f=y">
                </ion-avatar>
                <ion-label>
                  <ion-button color="danger" expand="full" size="large">
                    Canales de Youtube
                    </ion-button>
                  </ion-label>
              </ion-item>

              <ion-item>
                <ion-avatar slot="start">
                  <img src="https://gravatar.com/avatar/dba6bae8c566f9d4041fb9cd9ada7741?d=identicon&f=y">
                </ion-avatar>
                <ion-label>
                  <ion-button color="danger" expand="full" size="large">
                    Scripts
                    </ion-button>
                  </ion-label>
              </ion-item>

              <ion-item>
                <ion-avatar slot="start">
                  <img src="https://gravatar.com/avatar/dba6bae8c566f9d4041fb9cd9ada7741?d=identicon&f=y">
                </ion-avatar>
                <ion-label>
                  <ion-button color="danger" expand="full" size="large">
                    Distribuciones
                    </ion-button>
                  </ion-label>
              </ion-item>
              
            </ion-list>
          </ion-popover>
          

          <ion-button color="dark">About</ion-button>
          
          
        </ion-col>
      </ion-row>
    </ion-navbar>
  </ion-header>
</template>
<style scoped>
.center {
  text-align: center;
}
</style>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import { IonButton, IonPopover } from '@ionic/vue';

export default defineComponent({
  name: 'NavBar',
  components: {
    IonButton, 
    IonPopover
  },
  setup() {
    const isOpenRef = ref(false);
    const event = ref();
    const setOpen = (state: boolean, event?: Event) => {
      //event.value = event; 
      isOpenRef.value = state;
    }
    return { isOpenRef, setOpen, event }
  },
  methods: {

  }
});
</script>