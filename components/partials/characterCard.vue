<template>
  <div>
    <div class="container-fluid p-3">
      <div class="row profile-card">
        <div class="col-md-7 p-0">
          <div class="profile-card_picture">
            <img
              style="width:100%; height: 100%"
              :src="images"
              alt="picture-img"
            />
          </div>
        </div>
        <div class="col-md-5">
          <div class="profile-card_content d-flex align-items-center p-2">
            <div>
              <h6>{{ profile.name }}</h6>
              <p class="mt-2">{{ profile.birth_year }}</p>
              <p>
                {{ profile.gender }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: ["profile"],
  data() {
    return {
      image: Math.round(Math.random() * (4 - 1) + 1)
    };
  },
  computed: {
    images() {
      return `/images/character-${this.image}.jpg`;
    }
  },
  mounted() {
    // console.log(this.profile);
  }
};
</script>
<style scoped>
.profile-card_picture {
  /* width: 60%; */
  height: 15rem;
}
.profile-card {
  background-color: #f5f5f5;
  /* width: 40%; */
  min-height: 15rem;
}
.profile-card_content {
  height: 100%;
}
.view-character-button {
  text-align: center;
}
.view-more {
  padding: 0.5rem;
  width: 40%;
  border: 1px solid black;
}
</style>
