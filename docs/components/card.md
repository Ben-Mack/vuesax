---
API:
  - name: header
    type: slot
    parameters:
    description: slot header card
    default: null
  - name: footer
    type: slot
    parameters:
    description: slot footer card
    default: null
  - name: media
    type: slot
    parameters:
    description: slot image media
    default: null
  - name: extra-content
    type: slot
    parameters:
    description: slot extra contend and card
    default: null
  - name: actionable
    type: Boolean
    parameters:
    description: Hover effect
    default: false
contributors:
  - fergardi
  - RodSwanston
---

# Card **- ssr**

<box header>

  Cards contain content and actions about a single subject.

</box>

<box>

## Default

To add a card we have the `vs-card` component, for the internal structure we use several **slots** (`header`, `footer`, `media`, ... )

<vuecode md>
<div slot="demo">
<vs-row vs-justify="center">
  <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-w="6">
    <vs-card>
      <div slot="header">
        <h3>
          Hello world !
        </h3>
      </div>
      <div>
        <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</span>
      </div>
      <div slot="footer">
        <vs-row vs-justify="flex-end">
          <vs-button vs-type="gradient" vs-color="danger" vs-icon="favorite"></vs-button>
          <vs-button vs-color="primary" vs-icon="turned_in_not"></vs-button>
          <vs-button vs-color="rgb(230,230,230)" vs-color-text="rgb(50,50,50)" vs-icon="settings"></vs-button>
        </vs-row>
      </div>
    </vs-card>
  </vs-col>
</vs-row>
</div>
<div slot="code">

```html
<vs-row vs-justify="center">
  <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-w="6">
    <vs-card>
      <div slot="header">
        <h3>
          Hello world !
        </h3>
      </div>
      <div>
        <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</span>
      </div>
      <div slot="footer">
        <vs-row vs-justify="flex-end">
          <vs-button vs-type="gradient" vs-color="danger" vs-icon="favorite"></vs-button>
          <vs-button vs-color="primary" vs-icon="turned_in_not"></vs-button>
          <vs-button vs-color="rgb(230,230,230)" vs-color-text="rgb(50,50,50)" vs-icon="settings"></vs-button>
        </vs-row>
      </div>
    </vs-card>
  </vs-col>
</vs-row>
```

</div>
</vuecode>
</box>

<box>

## Media

There are cases in which you need to add an image or video on the card so we have the `slot="media"`

<vuecode md>
<div slot="demo">
  <Demos-Card-Media />
</div>
<div slot="code">

```html
<template>
  <vs-row vs-justify="center">
    <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-w="6">
      <vs-card class="cardx">
        <div slot="header">
          <h3>
            Hello world !
          </h3>
        </div>
        <div slot="media">
          <img :src="$withBase('/card.png')">
        </div>
        <div>
          <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</span>
        </div>
        <div slot="footer">
          <vs-row vs-justify="flex-end">
            <vs-button vs-type="gradient" vs-color="danger" vs-icon="favorite"></vs-button>
            <vs-button vs-color="primary" vs-icon="turned_in_not"></vs-button>
            <vs-button vs-color="rgb(230,230,230)" vs-color-text="rgb(50,50,50)" vs-icon="settings"></vs-button>
          </vs-row>
        </div>
      </vs-card>
    </vs-col>
    <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-w="6">
      <vs-card class="cardx">
        <div slot="header">
          <h3>
            Hello world !
          </h3>
        </div>
        <div slot="media">
          <img :src="$withBase('/card2.png')">
        </div>
        <div>
          <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</span>
        </div>
        <div slot="footer">
          <vs-row vs-justify="flex-end">
            <vs-button vs-type="gradient" vs-color="danger" vs-icon="favorite"></vs-button>
            <vs-button vs-color="primary" vs-icon="turned_in_not"></vs-button>
            <vs-button vs-color="rgb(230,230,230)" vs-color-text="rgb(50,50,50)" vs-icon="settings"></vs-button>
          </vs-row>
        </div>
      </vs-card>
    </vs-col>
  </vs-row>
</template>
<script>
export default {

}
</script>
<style lang="stylus">
.cardx
  margin 15px
</style>
```

</div>
</vuecode>
</box>

<box>

## Hover

You can add hover functionality with the property `actionable`

<vuecode md>
<div slot="demo">
    <vs-row vs-justify="center">
    <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-w="6">
      <vs-card actionable class="cardx">
        <div slot="header">
          <h3>
            Hello world !
          </h3>
        </div>
        <div slot="media">
          <img :src="$withBase('/card.png')">
        </div>
        <div>
          <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit</span>
        </div>
        <div slot="footer">
          <vs-row vs-justify="flex-end">
            <vs-button vs-color="primary" vs-type="gradient" >View</vs-button>
            <vs-button vs-color="danger" vs-type="gradient">Delete</vs-button>
          </vs-row>
        </div>
      </vs-card>
    </vs-col>
    <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-w="6">
      <vs-card actionable class="cardx">
        <div slot="header">
          <h3>
            Hello world !
          </h3>
        </div>
        <div slot="media">
          <img :src="$withBase('/card2.png')">
        </div>
        <div>
          <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit</span>
        </div>
        <div slot="footer">
          <vs-row vs-justify="flex-end">
            <vs-button vs-color="primary" vs-type="gradient" >View</vs-button>
            <vs-button vs-color="danger" vs-type="gradient" >Delete</vs-button>
          </vs-row>
        </div>
      </vs-card>
    </vs-col>
  </vs-row>
</div>
<div slot="code">

```html
<vs-row vs-justify="center">
    <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-w="6">
      <vs-card actionable class="cardx">
        <div slot="header">
          <h3>
            Hello world !
          </h3>
        </div>
        <div slot="media">
          <img :src="$withBase('/card.png')">
        </div>
        <div>
          <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit</span>
        </div>
        <div slot="footer">
          <vs-row vs-justify="flex-end">
            <vs-button vs-color="primary" vs-type="gradient" >View</vs-button>
            <vs-button vs-color="danger" vs-type="gradient">Delete</vs-button>
          </vs-row>
        </div>
      </vs-card>
    </vs-col>
    <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-w="6">
      <vs-card actionable class="cardx">
        <div slot="header">
          <h3>
            Hello world !
          </h3>
        </div>
        <div slot="media">
          <img :src="$withBase('/card2.png')">
        </div>
        <div>
          <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit</span>
        </div>
        <div slot="footer">
          <vs-row vs-justify="flex-end">
            <vs-button vs-color="primary" vs-type="gradient" >View</vs-button>
            <vs-button vs-color="danger" vs-type="gradient" >Delete</vs-button>
          </vs-row>
        </div>
      </vs-card>
    </vs-col>
  </vs-row>
```

</div>
</vuecode>
</box>





