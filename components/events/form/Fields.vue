<template>
  <div class="list">
    <Name/>
    <Location/>
    <Dates/>
    <Email/>
    <Teaser/>
    <Description/>
    <Highlights/>
    <Organizer/>
    <Website/>
    <RegistrationInfo/>
    <Languages/>
    <Sponsors/>
    <Social/>
    <Hashtag/>
    <Categories/>
    <RelatedDapps/>
    <Tags/>
  </div>
</template>

<script>
  import Categories from '~/components/events/form/fields/Categories.vue'
  import Dates from '~/components/events/form/fields/Dates.vue'
  import Description from '~/components/events/form/fields/Description.vue'
  import Email from '~/components/events/form/fields/Email.vue'
  import Hashtag from '~/components/events/form/fields/Hashtag.vue'
  import Highlights from '~/components/events/form/fields/Highlights.vue'
  import Languages from '~/components/events/form/fields/Languages.vue'
  import Location from '~/components/events/form/fields/Location.vue'
  import Name from '~/components/events/form/fields/Name.vue'
  import Organizer from '~/components/events/form/fields/Organizer.vue'
  import RegistrationInfo from '~/components/events/form/fields/RegistrationInfo.vue'
  import RelatedDapps from '~/components/events/form/fields/RelatedDapps.vue'
  import Social from '~/components/events/form/fields/Social.vue'
  import Sponsors from '~/components/events/form/fields/Sponsors.vue'
  import Tags from '~/components/events/form/fields/Tags.vue'
  import Teaser from '~/components/events/form/fields/Teaser.vue'
  import Website from '~/components/events/form/fields/Website.vue'

  export default {
    components: {
      Categories,
      Dates,
      Description,
      Email,
      Hashtag,
      Highlights,
      Location,
      Languages,
      Name,
      Organizer,
      RelatedDapps,
      RegistrationInfo,
      Social,
      Sponsors,
      Tags,
      Teaser,
      Website
    }
  }
</script>

<style lang="scss" scoped>
  @import '~assets/css/settings';

  .list {
    width: 100%;
    max-width: 400px;
    padding: 10px;
    margin: 0 auto;
    @include tweakpoint('min-width', $tweakpoint--default) {
      margin-right: 20px;
      margin-left: 0;
    }

    .item {
      width: 100%;
      margin-bottom: 15px;
      position: relative;
      border: 1px solid transparent;
      &.-icon, &.-image {
        background: rgba(lighten($color--gray, 100%), .9);
        box-shadow: 0 0 20px rgba($color--black, .05);
        width: 150px;
        height: 150px;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
        margin-left: auto;
        margin-right: auto;
        border-radius: 50%;
        &.-drop {
          border-color: $color--black;
        }
      }
      &.-image {
        width: auto;
        height: auto;
        min-height: 200px;
        border-radius: 10px;
      }
      &.--has-errors {
        border-color: $color--error;
      }
    }

    /deep/ .required {
      display: inline-block;
      padding-left: 2px;
      color: $color--error;
    }

    /deep/ .label {
      position: absolute;
      left: 0;
      top: 10px;
      padding: 20px;
      pointer-events: none;
      font-size: .95rem;
      transition: top .2s ease;
    }

    /deep/ .text-input, /deep/ .text-area {
      border: none;
      padding: 30px 50px 30px 20px;
      width: 100%;
      box-shadow: 0 0 20px rgba($color--black,.05);
      background: rgba(lighten($color--gray, 100%),.9);
      transition: background .2s ease;
      &:focus {
        background: none;
        background: rgba(250, 250, 250, 0.7);
      }
      &:focus + .label,  &.--is-filled + .label {
        top: -11px;
        opacity: .65;
      }
    }

    /deep/ .text-area {
      vertical-align: top;
      min-height: 75px;
      resize: none;
    }

    /deep/ .remaining-characters {
      position: absolute;
      display: block;
      right: 20px;
      top: 30px;
    }

    /deep/ .help {
      padding: 10px 20px;
      margin: 0;
      background: none;
      background: rgba(250, 250, 250, 0.7);
      font-size: .9rem;
      line-height: 1.45;
    }

    /deep/ .error-list, /deep/ .warning-list {
      padding: 10px 20px;
      color: lighten($color--white, 100%);
    }

    /deep/ .error-list {
      background: $color--error;
    }

    /deep/ .warning-list {
      background: $color--warning;
    }

    /deep/ .error-item, /deep/ .warning-item {
      margin: .2rem 0;
    }
  }
</style>
