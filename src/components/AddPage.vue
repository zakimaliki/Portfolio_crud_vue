<template>
  <div class="container text-left my-5">
    <form class="border p-2 rounded bg-light">
      <h1>Form Biodata</h1>
      <div class="form-group">
        <label for="frolepertama">Role Pertama</label>
        <input
          type="text"
          class="form-control"
          id="frolepertama"
          v-model="biodata[0].rolePertama"
        />
      </div>
      <div class="form-group">
        <label for="frolekedua">Role kedua</label>
        <input
          type="text"
          class="form-control"
          id="frolekedua"
          v-model="biodata[0].roleKedua"
        />
      </div>
      <div class="form-group">
        <label for="froleketiga">Role ketiga</label>
        <input
          type="text"
          class="form-control"
          id="froleketiga"
          v-model="biodata[0].roleKetiga"
        />
      </div>
      <div class="form-group">
        <label for="textPertama">Text Pertama</label>
        <textarea
          class="form-control"
          id="textPertama"
          v-model="biodata[0].textPertama"
        ></textarea>
      </div>
      <div class="form-group">
        <label for="textkedua">Text Kedua</label>
        <textarea
          class="form-control"
          id="textkedua"
          v-model="biodata[0].textKedua"
        ></textarea>
      </div>
      <div class="form-group">
        <label for="imageProfile">Image Profile</label>
        <input
          type="text"
          class="form-control"
          id="imageProfile"
          v-model="biodata[0].imageProfile"
        />
      </div>
      <div class="form-group">
        <label for="imageResumePertama">Image Resume Pertama</label>
        <input
          type="text"
          class="form-control"
          id="imageResumePertama"
          v-model="biodata[0].imageResumePertama"
        />
      </div>
      <div class="form-group">
        <label for="imageResumeKedua">Image Resume Kedua</label>
        <input
          type="text"
          class="form-control"
          id="imageResumeKedua"
          v-model="biodata[0].imageResumeKedua"
        />
      </div>
      <div class="form-group">
        <label for="imagePortfolioPertama">Image Portfolio Pertama</label>
        <input
          type="text"
          class="form-control"
          id="imagePortfolioPertama"
          v-model="biodata[0].imagePortfolioPertama"
        />
      </div>
      <div class="form-group">
        <label for="imagePortfolioKedua">Image Portfolio Kedua</label>
        <input
          type="text"
          class="form-control"
          id="imagePortfolioKedua"
          v-model="biodata[0].imagePortfolioKedua"
        />
      </div>
      <div class="form-group">
        <label for="imagePortfolioKetiga">Image Portfolio Ketiga</label>
        <input
          type="text"
          class="form-control"
          id="imagePortfolioKetiga"
          v-model="biodata[0].imagePortfolioKetiga"
        />
      </div>
      <div class="form-group">
        <label for="imagePortfolioKeempat">Image Portfolio Keempat</label>
        <input
          type="text"
          class="form-control"
          id="imagePortfolioKeempat"
          v-model="biodata[0].imagePortfolioKeempat"
        />
      </div>
      <div class="form-group">
        <label for="imagePortfolioKelima">Image Portfolio Kelima</label>
        <input
          type="text"
          class="form-control"
          id="imagePortfolioKelima"
          v-model="biodata[0].imagePortfolioKelima"
        />
      </div>
      <div class="form-group">
        <label for="imagePortfolioKeenam">Image Portfolio Keenam</label>
        <input
          type="text"
          class="form-control"
          id="imagePortfolioKeenam"
          v-model="biodata[0].imagePortfolioKeenam"
        />
      </div>
      <div class="form-group">
        <label for="imageSkillPertama">Image Skill Pertama</label>
        <input
          type="text"
          class="form-control"
          id="imageSkillPertama"
          v-model="biodata[0].imageSkillPertama"
        />
      </div>
      <div class="form-group">
        <label for="imageSkillKedua">Image Skill Kedua</label>
        <input
          type="text"
          class="form-control"
          id="imageSkillKedua"
          v-model="biodata[0].imageSkillKedua"
        />
      </div>
      <div class="form-group">
        <label for="imageSkillKetiga">Image Skill Ketiga</label>
        <input
          type="text"
          class="form-control"
          id="imageSkillKetiga"
          v-model="biodata[0].imageSkillKetiga"
        />
      </div>
      <div class="form-group">
        <label for="imageSkillKeempat">Image Skill Keempat</label>
        <input
          type="text"
          class="form-control"
          id="imageSkillKeempat"
          v-model="biodata[0].imageSkillKeempat"
        />
      </div>
      <div class="form-group">
        <label for="imageSkillKelima">Image Skill Kelima</label>
        <input
          type="text"
          class="form-control"
          id="imageSkillKelima"
          v-model="biodata[0].imageSkillKelima"
        />
      </div>
      <div class="form-group">
        <label for="imageSkillKeenam">Image Skill Keenam</label>
        <input
          type="text"
          class="form-control"
          id="imageSkillKeenam"
          v-model="biodata[0].imageSkillKeenam"
        />
      </div>
      <button type="submit" class="btn btn-primary" @click.prevent="createData">
        Submit
      </button>
    </form>
  </div>
</template>
<script>
import axios from "axios";
export default {
  name: "addPage",
  data() {
    return {
      biodata: [],
    };
  },
  created() {
    axios
      .get("https://template-be-json-baru.vercel.app/biodata")
      .then((biodata) => {
        this.biodata = biodata.data;
      })
      .catch(() => {
        alert("data gagal ditambah");
      });
  },
  methods: {
    createData() {
      axios
        .put("https://template-be-json-baru.vercel.app/biodata/1", {
          rolePertama: this.biodata[0].rolePertama,
          roleKedua: this.biodata[0].roleKedua,
          roleKetiga: this.biodata[0].roleKetiga,
          textPertama: this.biodata[0].textPertama,
          textKedua: this.biodata[0].textKedua,
          imageProfile: this.biodata[0].imageProfile,
          imageResumePertama: this.biodata[0].imageResumePertama,
          imageResumeKedua: this.biodata[0].imageResumeKedua,
          imagePortfolioPertama: this.biodata[0].imagePortfolioPertama,
          imagePortfolioKedua: this.biodata[0].imagePortfolioKedua,
          imagePortfolioKetiga: this.biodata[0].imagePortfolioKetiga,
          imagePortfolioKeempat: this.biodata[0].imagePortfolioKeempat,
          imagePortfolioKelima: this.biodata[0].imagePortfolioKelima,
          imagePortfolioKeenam: this.biodata[0].imagePortfolioKetiga,
          imageSkillPertama: this.biodata[0].imageSkillPertama,
          imageSkillKedua: this.biodata[0].imageSkillKedua,
          imageSkillKetiga: this.biodata[0].imageSkillKetiga,
          imageSkillKeempat: this.biodata[0].imageSkillKeempat,
          imageSkillKelima: this.biodata[0].imageSkillKelima,
          imageSkillKeenam: this.biodata[0].imageSkillKetiga,
        })
        .then(() => {
          alert("data berhasil ditambah");
          })
        .catch(() => {
          this.$router.push('/')
        });
    },
  },
};
</script>
