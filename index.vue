<template>
  <footer class="footer p-t-20 p-b-40 m-t-40" id="rodape">
    <div class="container">
      <ul class="footer__list__1 p-b-0-touch p-b-16">
        <li class="footer__list__1__item">
          <div class="footer__list__1__cielo" :class="{openMobile: mobileOpen.includes(`${1}_${2}`)}">
            <AppLink
              v-if="page_content.columnsTop[0].menus[0].title.href"
              class="footer__list__1__title is-size-10-touch lh-10-touch is-size-8 lh-8 has-text-cloudy-600 has-text-weight-bold"
              :to="page_content.columnsTop[0].menus[0].title.href"
              :target="page_content.columnsTop[0].menus[0].title.target"
              :trackData="page_content.columnsTop[0].menus[0].title.trackData"
            >
              {{page_content.columnsTop[0].menus[0].title.label}}
              <img 
                class="icon" 
                :src="page_content.icons.direction.src" 
                :alt="page_content.icons.direction.alt" 
                :title="page_content.icons.direction.title" 
              />
              <!-- @click.prevent="openMenuMobile(1, 2)"-->
            </AppLink>
            <div class="footer__list__1__content is-family-secondary">
              <AppLink
                v-for="(link, k) in page_content.columnsTop[0].menus[0].links" 
                :key="k"
                class="is-size-10 lh-12 has-text-cloudy-600"
                :to="link.href"
                :target="link.target"
                :trackData="link.trackData"
                v-html="link.label"
              />
            </div>
          </div>
        </li>
        <li class="footer__list__1__item">
          <div class="footer__list__1__machines">
            <AppLink
              v-if="page_content.columnsTop[1].menus[0].title.href"
              class="footer__list__1__title is-size-10-touch lh-10-touch is-size-8 lh-8 has-text-cloudy-600 has-text-weight-bold"
              :to="page_content.columnsTop[1].menus[0].title.href"
              :target="page_content.columnsTop[1].menus[0].title.target"
              :trackData="page_content.columnsTop[1].menus[0].title.trackData"
              v-html="page_content.columnsTop[1].menus[0].title.label"
            />
            <div class="footer__list__1__content is-family-secondary">
              <AppLink
                v-for="(link, k) in page_content.columnsTop[1].menus[0].links" 
                :key="k"
                class="is-size-10 lh-12 has-text-cloudy-600"
                :to="link.href"
                :target="link.target"
                :trackData="link.trackData"
                v-html="link.label"
              />
            </div>
          </div>
          <div class="footer__list__1__ecommerce">
            <AppLink
              v-if="page_content.columnsTop[1].menus[1].title.href"
              class="footer__list__1__title is-size-10-touch lh-10-touch is-size-8 lh-8 has-text-cloudy-600 has-text-weight-bold"
              :to="page_content.columnsTop[1].menus[1].title.href"
              :target="page_content.columnsTop[1].menus[1].title.target"
              :trackData="page_content.columnsTop[1].menus[1].title.trackData"
            >
              {{page_content.columnsTop[1].menus[1].title.label}}
              <img 
                class="icon" 
                :src="page_content.icons.direction.src" 
                :alt="page_content.icons.direction.alt" 
                :title="page_content.icons.direction.title" 
              />
            </AppLink>
            <div class="footer__list__1__content is-family-secondary">
              <AppLink
                v-for="(link, k) in page_content.columnsTop[1].menus[1].links" 
                :key="k"
                class="is-size-10 lh-12 has-text-cloudy-600"
                :to="link.href"
                :target="link.target"
                :trackData="link.trackData"
                v-html="link.label"
              />
            </div>
          </div>
          <div class="footer__list__1__portal">
            <AppLink
              v-if="page_content.columnsTop[1].menus[2].title.href"
              class="footer__list__1__title is-size-10-touch lh-10-touch is-size-10 lh-12 has-text-cloudy-600 has-text-weight-bold"
              :to="page_content.columnsTop[1].menus[2].title.href"
              :target="page_content.columnsTop[1].menus[2].title.target"
              :trackData="page_content.columnsTop[1].menus[2].title.trackData"
            >
              <div class="footer__list__1__portal__icon is-flex">
                <img 
                  class="icon" 
                  :src="page_content.icons.direction.src" 
                  :alt="page_content.icons.direction.alt" 
                  :title="page_content.icons.direction.title" 
                />
                <img 
                  class="icon" 
                  :src="page_content.icons.direction.src" 
                  :alt="page_content.icons.direction.alt" 
                  :title="page_content.icons.direction.title" 
                />
              </div>
              {{page_content.columnsTop[1].menus[2].title.label}}
            </AppLink>
          </div>
        </li>
        <li class="footer__list__1__item">
          <div class="footer__list__1__sell-more" :class="{openMobile: mobileOpen.includes(`${2}_${3}`)}">
            <AppLink
              v-if="page_content.columnsTop[2].menus[0].title.href"
              class="footer__list__1__title is-size-10-touch lh-10-touch is-size-8 lh-8 has-text-cloudy-600 has-text-weight-bold"
              :to="page_content.columnsTop[2].menus[0].title.href"
              :target="page_content.columnsTop[2].menus[0].title.target"
              :trackData="page_content.columnsTop[2].menus[0].title.trackData"  
            >
              {{page_content.columnsTop[2].menus[0].title.label}}
              <img 
                class="icon" 
                :src="page_content.icons.direction.src" 
                :alt="page_content.icons.direction.alt" 
                :title="page_content.icons.direction.title" 
              />
            </AppLink>
            <!-- @click.prevent="openMenuMobile(2, 3)" -->
            <div class="footer__list__1__content is-family-secondary">
              <AppLink
                v-for="(link, k) in page_content.columnsTop[2].menus[0].links" 
                :key="k"
                class="is-size-10 lh-12 has-text-cloudy-600"
                :to="link.href"
                :target="link.target"
                :trackData="link.trackData"
                v-html="link.label"
              />
            </div>
          </div>
          <div class="footer__list__1__ecommerce">
            <AppLink
              v-if="page_content.columnsTop[1].menus[1].title.href"
              class="footer__list__1__title is-size-10-touch lh-10-touch is-size-8 lh-8 has-text-cloudy-600 has-text-weight-bold"
              :to="page_content.columnsTop[1].menus[1].title.href"
              :target="page_content.columnsTop[1].menus[1].title.target"
              :trackData="page_content.columnsTop[1].menus[1].title.trackData"
            >
              {{page_content.columnsTop[1].menus[1].title.label}}
              <img 
                class="icon" 
                :src="page_content.icons.direction.src" 
                :alt="page_content.icons.direction.alt" 
                :title="page_content.icons.direction.title" 
              />
            </AppLink>
            <div class="footer__list__1__content is-family-secondary">
              <AppLink
                v-for="(link, k) in page_content.columnsTop[1].menus[1].links" 
                :key="k"
                class="is-size-10 lh-12 has-text-cloudy-600"
                :to="link.href"
                :target="link.target"
                :trackData="link.trackData"
                v-html="link.label"
              />
            </div>
          </div>
        </li>
        <li class="footer__list__1__item">
          <div class="footer__list__1__management">
            <AppLink
              v-if="page_content.columnsTop[3].menus[0].title.href"
              class="footer__list__1__title is-size-10-touch lh-10-touch is-size-8 lh-8 has-text-cloudy-600 has-text-weight-bold"
              :to="page_content.columnsTop[3].menus[0].title.href"
              :target="page_content.columnsTop[3].menus[0].title.target"
              :trackData="page_content.columnsTop[3].menus[0].title.trackData"
            >
              {{page_content.columnsTop[3].menus[0].title.label}}
              <img 
                class="icon" 
                :src="page_content.icons.direction.src" 
                :alt="page_content.icons.direction.alt" 
                :title="page_content.icons.direction.title" 
              />
            </AppLink>
            <div class="footer__list__1__content is-family-secondary">
              <AppLink
                v-for="(link, k) in page_content.columnsTop[3].menus[0].links" 
                :key="k"
                class="is-size-10 lh-12 has-text-cloudy-600"
                :to="link.href"
                :target="link.target"
                :trackData="link.trackData"
                v-html="link.label"
              />
            </div>
          </div>
          <div class="footer__list__1__blog">
            <AppLink
              v-if="page_content.columnsTop[3].menus[1].title.href"
              class="footer__list__1__title is-size-10-touch lh-10-touch is-size-8 lh-8 has-text-cloudy-600 has-text-weight-bold"
              :to="page_content.columnsTop[3].menus[1].title.href"
              :target="page_content.columnsTop[3].menus[1].title.target"
              :trackData="page_content.columnsTop[3].menus[1].title.trackData"
              v-html="page_content.columnsTop[3].menus[1].title.label"
            />
          </div>
          <div class="footer__list__1__icva">
            <AppLink
              v-if="page_content.columnsTop[3].menus[2].title.href"
              class="footer__list__1__title is-size-10-touch lh-10-touch is-size-8 lh-8 has-text-cloudy-600 has-text-weight-bold"
              :to="page_content.columnsTop[3].menus[2].title.href"
              :target="page_content.columnsTop[3].menus[2].title.target"
              :trackData="page_content.columnsTop[3].menus[2].title.trackData"
              v-html="page_content.columnsTop[3].menus[2].title.label"
            />
          </div>
          <div class="footer__list__1__portal">
            <AppLink
              v-if="page_content.columnsTop[1].menus[2].title.href"
              class="footer__list__1__title is-size-10-touch lh-10-touch is-size-10 lh-12 has-text-cloudy-600 has-text-weight-bold"
              :to="page_content.columnsTop[1].menus[2].title.href"
              :target="page_content.columnsTop[1].menus[2].title.target"
              :trackData="page_content.columnsTop[1].menus[2].title.trackData"
            >
              <div class="footer__list__1__portal__icon is-flex">
                <img 
                  class="icon" 
                  :src="page_content.icons.direction.src" 
                  :alt="page_content.icons.direction.alt" 
                  :title="page_content.icons.direction.title" 
                />
                <img 
                  class="icon" 
                  :src="page_content.icons.direction.src" 
                  :alt="page_content.icons.direction.alt" 
                  :title="page_content.icons.direction.title" 
                />
              </div>
              {{page_content.columnsTop[1].menus[2].title.label}}
            </AppLink>
          </div>
        </li>
      </ul>
      <ul class="footer__list__2 p-t-16-touch p-t-32">
        <li
          v-for="(item, i) in page_content.columnsBottom" 
          :key="i"
          class="footer__list__2__item"
        >
          <div 
            v-for="(menu, m) in item.menus" 
            :key="m"
            :class="`footer__list__2__${menu.id}`"
          >
            <p 
              v-html="menu.title" 
              v-if="menu.title" 
              class="footer__list__2__title is-size-8 lh-9 p-b-16 has-text-cloudy-600 has-text-weight-bold" 
              :class="menu.title === 'Atendimento' ? 'is-size-8-touch lh-8-touch' : 'is-size-10-touch lh-10-touch'"
            />
            <div class="footer__list__2__content is-family-secondary">
              <AppLink
                v-for="(link, k) in menu.links" 
                :key="k"
                v-if="link.href"
                class="is-size-10 lh-12 has-text-cielo-300 has-text-underline"
                :to="link.href"
                :target="link.target"
                :trackData="link.trackData"
              >
                <img 
                  :src="link.icon" v-if="menu.id === 'attendance'"
                  class="icon m-b-8" 
                  :class="`footer__list__2__${menu.id}__icon`" 
                />
                <img 
                  class="icon" 
                  :src="page_content.icons.location.src" :alt="page_content.icons.location.alt" :title="page_content.icons.location.title" 
                  v-if="menu.id === 'store'" 
                />
                {{link.label}}
              </AppLink>
              <p class="is-size-10 lh-12 has-text-cloudy-600" v-else v-html="link" />
            </div>
          </div>
        </li>
      </ul>
    </div>
    <div class="container">
      <div class="social">
        <div class="social__container is-flex p-t-24-touch p-t-32">
          <span v-for="(link, i) in page_content.social.links" :key="i">
            <AppLink :to="link.href" :target="link.target" :trackData="link.trackData">
              <LazyImage
                class="svg_icon"
                :src="link.icon"
                :alt="link.label"
                :title="link.title"
              />
            </AppLink>
          </span>
        </div>
      </div>
      <div class="copyright is-flex-desktop p-t-16 is-block-touch">
        <img class="is-block-touch copyright__logo" src="~assets/img/logo_footer.svg" alt="Cielo" title="Logo da Cielo">
        <div class="copyright__text is-block-touch m-t-16-touch is-size-11 lh-11 m-l-0-touch m-l-20" v-html="page_content.copyright.label" />
      </div>
    </div>
  </footer>
</template>

<script>
import { mapGetters } from 'vuex'

export default {

  data(){
    return{
      mobileOpen: [],
      isOpen: false,
    }
  },

  computed: {
    ...mapGetters({
      content: 'content_headerFooter'
    }),

    page_content() {
      const route = this.$store.getters['content/route']
      let subcanal
      try {
        subcanal = this.$store.getters['content/pageContent'](route).dataLayer.pagina.subcanal
      } catch {
        subcanal = ''
      }
      
      let pageContent = JSON.stringify(this.content.footer)
      pageContent = pageContent.replace(/"Institucional \| "/g , `"Institucional | ${subcanal}"`)
      return JSON.parse(pageContent)
    },
  },

  methods:{
    openMenuMobile(col,id){
      let _id = `${col}_${id}`
      if(this.mobileOpen.includes(_id)) {
        this.mobileOpen = this.mobileOpen.filter(item => item !== _id)
      }else{
        this.mobileOpen.push(_id)
      }
    }
  }
};
</script>

<style lang="scss" scoped>
@import "~assets/css/abstract/index";
.footer{
  background: $cloudy-50;
  .footer__list__1 {
    display: grid;
    @include until ($desktop) {
      grid-gap: 0;
      grid-template-columns: auto;
    }
    @include from ($desktop) {
      grid-gap: 16px;
      grid-template-columns: auto auto auto auto;
    }
    @include from ($widescreen) {
      grid-gap: 32px;
      grid-template-columns: 280px 296px 280px 296px;
    }
    .footer__list__1__item {
      &:nth-child(1) {
        order: 1;
        @include until ($desktop) {
          order: 2;
          
        }
      }
      &:nth-child(2) {
        order: 2;
        @include until ($desktop) {
          order: 1;
          .footer__list__1__ecommerce,
          .footer__list__1__portal {
            display: none;
          }
        }
      }
      &:nth-child(3) {
        order: 3;
        .footer__list__1__ecommerce {
          display: none;
          @include until ($desktop) {
            display: block;
          }
        }
      }
      &:nth-child(4) {
        order: 4;
        .footer__list__1__portal {
          display: none;
          @include until ($desktop) {
            display: block;
          }
        }
      }
      .footer__list__1__portal__icon {
        padding-right: 12px;
        img {
          width: 12px;
          height: 7px;
          &:first-child {
            transform: rotate(90deg);
          }
          &:last-child {
            transform: rotate(-90deg);
          }
        }
      }
      .footer__list__1__content {
        display: flex;
        flex-direction: column;
        @include until ($desktop) {
          padding-top: 14px;
        }
        @include from ($desktop) {
          padding-top: calc(8px + 16px);
        }
        a, p {
          &:not(:last-child) {
            padding-bottom: 16px;
          }
          &:last-child {
            padding-bottom: 16px;
          }
        }
      }
      .footer__list__1__cielo,
      .footer__list__1__machines,
      .footer__list__1__ecommerce,
      .footer__list__1__sell-more,
      .footer__list__1__management,
      .footer__list__1__blog,
      .footer__list__1__icva {
        .footer__list__1__title {
          position: relative;
          &::after {
            content: "";
            position: absolute;
            height: 2px;
            background: $cielo-300;
            left: 0;
            bottom: -8px;
          }
        }
        .icon {
          width: 12px;
          height: 7px;
          margin-left: 8px;
          margin-bottom: 2px;
          display: none !important;
          @include from ($desktop) {
            display: none !important;
          }
        }
        @include until ($desktop) {
          &.is-open {
            .footer__list__1__content {
              display: flex;
            }
          }
          &.is-close {
            padding-bottom: 14px;
            .footer__list__1__content {
              display: none;
            }
          }
        }
      }
       .footer__list__1__cielo {
        .footer__list__1__title {
          @include from ($desktop) {
            &::after {
              width: 169px;
            }
          }
        }
      }
      .footer__list__1__machines {
        .footer__list__1__title {
          @include from ($desktop) {
            &::after {
              width: 206px;
            }
          }
        }
      }
      .footer__list__1__ecommerce {
        .footer__list__1__title {
          @include from ($desktop) {
            &::after {
              width: 134px;
            }
          }
        }
      }
      .footer__list__1__portal {
        .footer__list__1__title {
          height: 36px;
          width: 280px;
          background: $cloudy-100;
          border-radius: 999px;
          display: flex;
          flex-direction: row;
          justify-content: center;
          align-items: center;
          padding: 6px 12px;
          @include until ($desktop) {
            margin: auto;
          }
        }
      }
      .footer__list__1__sell-more {
        .footer__list__1__title {
          @include from ($desktop) {
            &::after {
              width: 121px;
            }
          }
        }
      }
      .footer__list__1__management {
        .footer__list__1__title {
          @include from ($desktop) {
            &::after {
              width: 134px;
            }
          }
        }
      }
      .footer__list__1__blog {
        @include until ($desktop) {
          padding-bottom: 16px;
        }
        @include from ($desktop) {
          padding-bottom: calc(8px + 16px);
        }
        .footer__list__1__title {
          @include from ($desktop) {
            &::after {
              width: 134px;
            }
          }
        }
      }
      .footer__list__1__icva {
        @include until ($desktop) {
          padding-bottom: 16px;
        }
        @include from ($desktop) {
          padding-bottom: calc(8px + 16px);
        }
        .footer__list__1__title {
          @include from ($desktop) {
            &::after {
              width: 134px;
            }
          }
        }
      }
    }
  }
  .footer__list__2 {
    display: grid;
    position: relative;
    @include until ($desktop) {
      grid-gap: 0;
      grid-template-columns: auto;
    }
    @include from ($desktop) {
      grid-template-columns: auto auto auto;
      grid-gap: 92px;
      &::before {
        content: "";
        position: absolute;
        width: 500px;
        height: 0px;
        border: 1px solid $cloudy-200;
        margin: auto;
        display: flex;
        justify-content: center;
        align-items: center;
        left: calc(50% - 500px/2);
        top: 0;
      }
    }
    @include from ($widescreen) {
      grid-template-columns: 345px 345px 345px;
      grid-gap: 92px;
    }
    .footer__list__2__item {
      position: relative;
      @include until ($desktop) {
        width: 345px;
        display: grid;
      }
      &:not(:first-child) {
        &::before {
          content: "";
          position: absolute;
          width: 119px;
          height: 0px;
          border: 1px solid #C5CED7;
          transform: rotate(90deg);
          left: calc(-119px/2 - 46px);
          top: calc(119px + 20px);
        }
      }
      &:nth-child(2) {
        display: grid;
        @include until ($desktop) {
          grid-template-columns: 1fr 1fr;
          .footer__list__2__store {
            order: 1;
            grid-column: span 2;
          }
          .footer__list__2__relationship {
            order: 2;
          }
          .footer__list__2__support {
            order: 3;
          }
        }
      }
      .footer__list__2__content {
        display: flex;
        flex-direction: column;
        a, p {
          padding-bottom: 16px;
        }
      }
      .footer__list__2__attendance {
        @include from ($desktop) {
          flex-direction: column;
        }
        .footer__list__2__attendance__icon {
          width: 32px;
          height: 32px;
          @include from ($desktop) {
            display: none;
          }
        }
        .footer__list__2__title {}
        .footer__list__2__content {
          //display: none !important;
          @include until ($desktop) {
            display: flex;
            flex-direction: row-reverse;
            justify-content: center;
            margin-bottom: 16px;
            a {
              color: $cloudy-400 !important;
              text-decoration: none;
              font-weight: 500;
              display: flex;
              flex-direction: column;
              justify-content: center;
              align-items: center;
              padding: 19px 0px;
              width: 104px;
              height: 94px;
              background: #FFFFFF;
              box-shadow: 0px 2px 8px rgba(35, 31, 32, 0.16);
              border-radius: 16px;
              &:not(:first-child) {
                margin-right: 8px;
              }
            }
          }
        }
      }
      .footer__list__2__channels {
        .footer__list__2__title {
          @include from ($desktop) {
            /deep/br {
              &:first-child {
                display: none;
              }
            }
          }
          @include until ($desktop) {
            /deep/br {
              &:last-child {
                display: none;
              }
            }
          }
        }
      }
      .footer__list__2__store {
        @include until ($desktop) {
          order: 1;
          margin-bottom: 16px;
        }
        a {
          text-decoration: none;
          color: #fff !important;
          font-weight: 700;
          font-size: 14px;
          line-height: 19px;
          width: 280px;
          height: 40px;
          background: $cielo-300;
          border-radius: 999px;
          display: flex;
          flex-direction: row;
          justify-content: center;
          align-items: center;
          padding-bottom: 0 !important;
          margin: auto;

          img {
            width: 22px;
            height: 22px;
            margin-right: 14px;
          }
        }
      }
      .footer__list__2__ethic {}
      .footer__list__2__platform {
        display: flex;
        align-items: center;
        gap: 10px;
      }
      .footer__list__2__ombudsman {}
      .footer__list__2__relationship {}
      .footer__list__2__support {}
    }
  }
}

.social {
  position: relative;
  @include until ($desktop) {
    &::before {
      position: absolute;
      content: "";
      width: 200px;
      height: 0;
      border: 1px solid #EAEEF3;
      left: calc(50% - 200px/2);
    }
  }
  .social__container {
    justify-content: center;
    gap: 12px;
    @include from ($desktop) {
      gap: 20px;
    }
    .svg_icon {
      width: 32px;
      height: 32px;
    }
  }
}
.copyright {
  display: flex;
  align-items: center;
  .copyright__logo {
    @include until ($desktop) {
      margin: auto;
    }
  }
  .copyright__text {
    /deep/strong{
      margin-right: .75rem;
      @include until($fullhd){
        display: block;
      }
    }
  }
}
</style>
