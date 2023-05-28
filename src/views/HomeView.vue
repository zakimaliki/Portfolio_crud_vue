<template>
  <div>
    <div id="nav">
      <router-link to="/add">
        <button class="btn btn-primary">Add</button>
      </router-link>
    </div>
    <div class="container-fluid">
      <div class="row text-center bg-secondary pt-3 text-white">
        <div class="col-12">
          <img
            class="profile"
            src="../assets/saya.jpg"
            style="width: 100px; height: 120px;-radius: 20px;"
          />
          <h1>Priscillia Candra</h1>
          <h4 class="pb-5">{{biodata[0].rolePertama}} | {{biodata[0].roleKedua}} | {{biodata[0].roleKetiga}}</h4>
        </div>
      </div>
    </div>
    <!-- about -->
    <h1 class="text-center pt-5">About</h1>
    <hr class="pb-3" />
    <div class="container">
      <div class="row text-center">
        <div class="col-md-6 col-sm-12">
          <p>
            {{biodata[0].textPertama}} 
          </p>
          <img
            class="sekolah"
            :src="biodata[0].imageResumePertama"
          />
        </div>
        <div class="col-md-6 col-sm-12">
          <p>
            {{biodata[0].textPertama}} 
          </p>
          <img
            class="sekolah"
            :src="biodata[0].imageResumeKedua"
          />
        </div>
      </div>
    </div>
    <!-- portfolio -->
    <h1 class="text-center pt-5">Portfolio</h1>
    <hr class="pb-3" />
    <div class="container-fluid">
      <div class="row text-center bg-secondary">
        <div class="col-md-4 col-sm-12">
          <img
            class="ability"
            :src="biodata[0].imagePortfolioPertama"
          />
        </div>
        <div class="col-md-4 col-sm-12">
          <img
            class="ability"
            :src="biodata[0].imagePortfolioKedua"
          />
        </div>
        <div class="col-md-4 col-sm-12">
          <img
            class="ability"
            :src="biodata[0].imagePortfolioKetiga"
          />
        </div>
        <div class="col-md-4 col-sm-12">
          <img
            class="ability"
            :src="biodata[0].imagePortfolioKeempat"
          />
        </div>
        <div class="col-md-4 col-sm-12">
          <img
            class="ability"
            :src="biodata[0].imagePortfolioKelima"
          />
        </div>
        <div class="col-md-4 col-sm-12">
          <img
            class="ability"
            :src="biodata[0].imagePortfolioKeenam"
          />
        </div>
      </div>
    </div>
    <!-- skill -->
    <h1 class="text-center pt-5">Skills</h1>
    <hr class="pb-3" />
    <div class="container">
      <div class="row text-center">
        <div class="col-md-2 col-sm-12">
          <img
            class="skill"
            :src="biodata[0].imageSkillPertama"
          />
        </div>
        <div class="col-md-2 col-sm-12">
          <img
            class="skill"
            :src="biodata[0].imageSkillKedua"
          />
        </div>
        <div class="col-md-2 col-sm-12">
          <img
            class="skill"
            :src="biodata[0].imageSkillKetiga"
          />
        </div>
        <div class="col-md-2 col-sm-12">
          <img
            class="skill"
            :src="biodata[0].imageSkillKeempat"
          />
        </div>
        <div class="col-md-2 col-sm-12">
          <img
            class="skill"
            :src="biodata[0].imageSkillKelima"
          />
        </div>
        <div class="col-md-2 col-sm-12">
          <img
            class="skill"
            :src="biodata[0].imageSkillKeenam"
          />
        </div>
      </div>
    </div>
    <!-- contact -->
    <h1 class="text-center pt-5">Contact</h1>
    <hr class="pb-3" />
    <div class="container">
      <div class="row text-center">
        <div class="col-12 mt-2">
          <form>
            <div class="kontak text-left">
              <p><strong>Nama</strong></p>
              <input type="text" placeholder="Masukan Nama" />
            </div>
            <div class="kontak text-left">
              <p><strong>Email</strong></p>
              <input type="text" placeholder="Masukan Email" />
            </div>
            <div class="kontak text-left">
              <p><strong>Nomor Telepon</strong></p>
              <input type="text" placeholder="Masukan Nomor Telepon" />
            </div>
            <div class="kontak text-left">
              <p><strong>Pesan</strong></p>
              <input class="pesan" type="text" placeholder="Masukan Pesan" />
            </div>
            <div class="kontak text-center">
              <button class="kirim">Kirim Pesan</button>
            </div>
          </form>
        </div>
      </div>
    </div>
    <!-- footer -->
    <div class="container-fluid">
      <div class="row text-center bg-secondary mt-3">
        <div class="col-12 mt-2 text-white">
          <!-- <div class="icon-logo text-left">
            <div class="">
              <img class="icon kotak"
                src="https://th.bing.com/th/id/R.d880faebb3dfcb0da6b568aacf561c2a?rik=bqxPrvnatG6JIA&riu=http%3a%2f%2fgetdrawings.com%2fvectors%2fwhite-instagram-logo-vector-11.png&ehk=isFxUg5rwr7XhEmf8OtI5ao5tlhI%2f1fJnM0htGnZ3qQ%3d&risl=&pid=ImgRaw&r=0"
                alt=""
              />
              <p class="keterangan">: @priscilliacandraa</p>
            </div>
            <div class="">
              <img class="icon kotak"
                src="https://pngimg.com/uploads/whatsapp/whatsapp_PNG95148.png"
                alt=""
              />
              <p class="keterangan">: 08118131010</p>
            </div>
            <div class="">
              <img class="icon kotak"
                src="https://th.bing.com/th/id/R.9547261541e93756194b51bc704ead65?rik=UqdU%2fFetHG2dXQ&riu=http%3a%2f%2fcdn.onlinewebfonts.com%2fsvg%2fimg_500737.png&ehk=3Ri7ovVdevl2qL%2be4Oz9P%2fpAsz5jq77px%2fo9dSaHRqg%3d&risl=&pid=ImgRaw&r=0"
                alt=""
              />
              <p class="keterangan">: priscilcandra.98@gmail.com</p>
            </div>
          </div> -->
          <div class="row">
            <div class="kotak">
              <div class="col-6 text-white">
                <img
                  class="icon kotak"
                  src="https://th.bing.com/th/id/R.d880faebb3dfcb0da6b568aacf561c2a?rik=bqxPrvnatG6JIA&riu=http%3a%2f%2fgetdrawings.com%2fvectors%2fwhite-instagram-logo-vector-11.png&ehk=isFxUg5rwr7XhEmf8OtI5ao5tlhI%2f1fJnM0htGnZ3qQ%3d&risl=&pid=ImgRaw&r=0"
                  alt=""
                />
              </div>
              <div class="col-6 text-white">
                <p class="keterangan">: @priscilliacandraa</p>
              </div>
            </div>
            <div class="kotak">
              <div class="col-6 text-white">
                <img
                  class="icon kotak"
                  src="https://pngimg.com/uploads/whatsapp/whatsapp_PNG95148.png"
                  alt=""
                />
              </div>
              <div class="col-6 text-white">
                <p class="keterangan">: 08118131010</p>
              </div>
            </div>
            <div class="kotak">
              <div class="col-6 text-white">
                <img
                  class="icon kotak"
                  src="https://th.bing.com/th/id/R.9547261541e93756194b51bc704ead65?rik=UqdU%2fFetHG2dXQ&riu=http%3a%2f%2fcdn.onlinewebfonts.com%2fsvg%2fimg_500737.png&ehk=3Ri7ovVdevl2qL%2be4Oz9P%2fpAsz5jq77px%2fo9dSaHRqg%3d&risl=&pid=ImgRaw&r=0"
                  alt=""
                />
              </div>
              <div class="col-6 text-white">
                <p class="keterangan">: priscilcandra.98@gmail.com</p>
              </div>
            </div>
          </div>
          <p class="mt-3">&copy; copyright 2023 | by Priscillia Candra</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'App',
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
}
</script>

    <style scoped> 
      .profile {
        width: 100px;
        height: 120px;
        border: 2px solid white;
        border-radius: 20px;
      }

      .sekolah {
        width: 300px;
        height: 200px;
        border: 5px solid gray;
      }

      hr {
        width: 250px;
        border-top: 3px solid #999;
        margin-top: 20px;
        margin-bottom: 20px;
      }

      img {
        max-width: 100%;
        height: 300px;
        border: 5px solid white;
        margin: 30px;
      }

      .ability {
        width: 300px;
        height: 230px;
        border: 5px solid white;
        margin: 30px;
      }

      .kontak {
        align-items: center;
        line-height: 1px;
        margin-bottom: 30px;
        outline: black;
      }

      form {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
      }

      input {
        width: 500px;
        height: 40px;
        padding: 6px 12px;
        font-size: 14px;
        border: 1.5px solid #ccc;
        border-radius: 5px;
      }

      .pesan {
        height: 200px;
        padding: 6px 12px;
        text-align: left;
        padding-bottom: 165px;
      }

      .kirim {
        width: 120px;
        height: 40px;
        background-color: gray;
        color: white;
        border-radius: 8px;
        border: none;
      }

      .skill {
        width: 230px;
        height: 180px;
        border: 5px solid gray;
      }

      .kotak {
        width: 88%;
        height: 30px;
        display: flex;
        flex-direction: row;
        align-items: center;
        float: right;
      }

      .keterangan {
        flex-direction: column;
        justify-content: space-between;
        margin-top: 10px;
        float: left;
      }

      .icon {
        width: 20px;
        height: 20px;
        border: none;
      }
    </style>