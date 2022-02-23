<template>
  <div class="HomeTickets">
    <center>
      <h1 class="section-title">Tickets</h1>
    </center>
    <div class="HomeTickets__tickets">
      <div class="HomeTickets__ticket HomeTickets__ticket--active">
        <h1 class="HomeTickets__ticketName">Regular</h1>
        <h2 class="HomeTickets__ticketPrice">Php 3,000</h2>
        <p class="HomeTickets__ticketDetails">
          <b>Limited tickets available!</b>
        </p>
        <a class="HomeTickets__button" @click.prevent="scrollToPaymentMethods()">
          <svg style="width:24px;height:24px" viewBox="0 0 24 24">
            <path
              fill="#ffffff"
              d="M15.58,16.8L12,14.5L8.42,16.8L9.5,12.68L6.21,10L10.46,9.74L12,5.8L13.54,9.74L17.79,10L14.5,12.68M20,12C20,10.89 20.9,10 22,10V6C22,4.89 21.1,4 20,4H4A2,2 0 0,0 2,6V10C3.11,10 4,10.9 4,12A2,2 0 0,1 2,14V18A2,2 0 0,0 4,20H20A2,2 0 0,0 22,18V14A2,2 0 0,1 20,12Z"
            />
          </svg>
          <span>Buy Ticket</span>
        </a>
      </div>
      <div class="HomeTickets__ticket">
        <h1 class="HomeTickets__ticketName">Early Bird</h1>
        <h2 class="HomeTickets__ticketPrice"></h2>
        <p class="HomeTickets__ticketDetails" style="transform: scale(1.75); margin: 2rem">Sold out!</p>
        <a class="HomeTickets__button">
          <svg style="width:24px;height:24px" viewBox="0 0 24 24">
            <path
              fill="#ffffff"
              d="M15.58,16.8L12,14.5L8.42,16.8L9.5,12.68L6.21,10L10.46,9.74L12,5.8L13.54,9.74L17.79,10L14.5,12.68M20,12C20,10.89 20.9,10 22,10V6C22,4.89 21.1,4 20,4H4A2,2 0 0,0 2,6V10C3.11,10 4,10.9 4,12A2,2 0 0,1 2,14V18A2,2 0 0,0 4,20H20A2,2 0 0,0 22,18V14A2,2 0 0,1 20,12Z"
            />
          </svg>
          <span>Buy Ticket</span>
        </a>
      </div>
      <div class="HomeTickets__ticket">
        <h1 class="HomeTickets__ticketName">Blind Bird</h1>
        <h2 class="HomeTickets__ticketPrice"></h2>
        <p class="HomeTickets__ticketDetails" style="transform: scale(1.75); margin: 2rem">Sold out!</p>
        <a class="HomeTickets__button">
          <svg style="width:24px;height:24px" viewBox="0 0 24 24">
            <path
              fill="#ffffff"
              d="M15.58,16.8L12,14.5L8.42,16.8L9.5,12.68L6.21,10L10.46,9.74L12,5.8L13.54,9.74L17.79,10L14.5,12.68M20,12C20,10.89 20.9,10 22,10V6C22,4.89 21.1,4 20,4H4A2,2 0 0,0 2,6V10C3.11,10 4,10.9 4,12A2,2 0 0,1 2,14V18A2,2 0 0,0 4,20H20A2,2 0 0,0 22,18V14A2,2 0 0,1 20,12Z"
            />
          </svg>
          <span>Buy Ticket</span>
        </a>
      </div>
    </div>
    <br />
    <br />
  </div>
</template>

<style lang="sass">
@import '../assets/style'

.HomeTickets
  padding: 2rem
  
  background: url(https://firebasestorage.googleapis.com/v0/b/devfestph.appspot.com/o/Other%20Images%2Fabstract-background.png?alt=media&token=5f3b72b8-fea2-4b61-8b50-72a11ab44853)
  background-size: cover
  overflow: hidden
  position: relative
  @include from($desktop)
    padding-bottom: 5rem

  .section-title
    color: $color-on-background

  &__tickets
    @include to($tablet)
      max-width: 500px
      margin: auto
    @include from($desktop)
      display: flex
      justify-content: center
      align-items: center
      margin-top: 4rem

  &__ticket
    position: relative
    text-align: center
    padding: 3rem 2rem
    border-radius: 0.5rem
    @include from($desktop)
      background: white // fallback
      background: radial-gradient(circle at 50% 0, transparent, 1.25rem, white, calc(1.25rem + 0.25px), white 70%, transparent 70%), radial-gradient(circle at 50% 100%, transparent, 1.25rem, white calc(1.25rem + 0.25px), white 70%, transparent 70%)
    @include from($hd)
      padding: 5rem 4rem
      border-radius: 1rem

    

    &--active
      @include to($tablet)
        background-color: white
        box-shadow: 0px 0px 10px $color-primary

    & + &
      @include to($tablet)
        margin-top: 1rem
      @include from($desktop)
        margin-left: 0.5rem

    &:not(&--active)
      @include to($tablet)
        background-color: $color-primary
      @include from($desktop)
        background: $color-primary // fallback
        background: radial-gradient(circle at 50% 0, transparent, 1.25rem, $color-primary, calc(1.25rem + 0.25px), $color-primary 70%, transparent 70%), radial-gradient(circle at 50% 100%, transparent, 1.25rem, $color-primary calc(1.25rem + 0.25px), $color-primary 70%, transparent 70%)
      

      .HomeTickets__button
          display: none

      .HomeTickets__ticketName
        color: $color-on-background
        display: block
        

      .HomeTickets__ticketDetails
        color: $color-on-background

      .HomeTickets__ticketPrice
        color: $color-on-background

        

  &__ticketName
    font-weight: normal
    
    font-size: 1.5rem
    color: $color-primary
    margin: 0
    @include from($hd)
      font-size: 1.75rem

  &__ticketPrice
    font-size: 2rem
    font-weight: normal
    
    margin-top: 0.5rem
    margin-bottom: 0
    color: $color-primary
    @include from($hd)
      font-size: 2.75rem
  
  &__ticket--active &__ticketDetails
    color: $color-primary
    font-size: 0.9rem
    @include from($hd)
      font-size: 1.25rem

  & .HomeTickets__button
    cursor: pointer
    text-decoration: none
    background-color: $color-primary
    color: $color-on-primary
    padding: 0.5rem 1rem
    border-radius: 1rem
    display: inline-block
    margin-top: 1rem
    display: inline-flex
    align-items: center
    transition: 0.2s background-color
    font-size: 1.1rem
    @include from($hd)
      font-size: 1.5rem
      padding: 0.75rem 1.5rem

    &:hover
      background-color: lighten($color-primary, 10)

    span
      margin-left: 0.5rem

  &__paymentmodes
    display: flex
    justify-content: center
    flex-wrap: wrap
    
  
  &__paymentmode
    width: 100%
    border: 2px solid $color-on-background
    border-radius: 1rem
    padding: 1rem 1rem
    margin-top: 2rem
    @include from($tablet)
      padding: 1rem 2rem
      margin: 2rem
      width: auto

  &__paymentmodetitle
    font-weight: normal

  &__customlink
    text-decoration: none
    cursor: pointer
    background-color: $color-on-background
    display: flex
    padding: 1rem
    width: 15rem
    max-width: 100%
    border-radius: 1rem
    align-items: center
    justify-content: center
    margin-bottom: 1rem
    &:hover
      filter: brightness(1.05)
    span
      font-weight: bold
      margin-left: 0.5rem
      color: #333


  &__paymentmodebank
    background-color: $color-on-background
    display: inline-block
    color: $color-primary
    padding: 0.25rem
    margin: 0
    width: 5rem

  &__modalwrapper
    transition-duration: 0.3s !important
    top: 0
    left: 0
    position: fixed
    width: 100vw
    height: 100vh
    display: flex
    z-index: 10


  &__modal
    margin: auto
    background-color: $color-surface
    padding: 0.5rem
    z-index: 10
    font-size: 1.15rem
    max-height: 90vh
    overflow: auto
    @include from($tablet)
      padding: 1rem
      max-width: 50rem

  &__modalbackground
    position: fixed
    width: 100%
    height: 100vh
    top: 0
    left: 0
    background-color: rgba(0,0,0,0.75)

  &__modalbutton
    background-color: transparent
    color: $color-on-background
    padding: 0.5rem 1rem
    border: 2px solid $color-on-background
    border-radius: 1rem
    font-size: 1.15rem
    cursor: pointer
    margin-bottom: 1rem


</style>

<script>
export default {
  data: function() {
    return {
      QRModalShown: false,
      PaymentInstructionsModalShown: false
    };
  },
  methods: {
    scrollToPaymentMethods() {
      window.document.querySelector("[name=paymentmethods]").scrollIntoView();
    }
  }
};
</script>