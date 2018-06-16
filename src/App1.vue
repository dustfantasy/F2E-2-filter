<template>
  <div id="app">
    <header class="pageTitle">
      <div class="left left-area haveFun">
        HaveFun
      </div>
      <div class="left right-area">
        <div class="searchbox">
          <span class="search">
            <Icon type="search"></Icon>
            <input type="text">
          </span>
        </div>
      </div>
    </header>
      <div class="left left-area">
        <div class="filterbox right">
          <div class="filter">
            <div class="area">
              <b>Location</b>
              <Icon type="plus" style="float:right"></Icon>
              <div class="test">
                <Select placeholder="">
                  <Option>Taiwan</Option>
                </Select>
              </div>
            </div>
            <div class="area">
              <b>Date</b>
              <div>
                <div class="datefromto">from</div>
                <DatePicker></DatePicker>
              </div>
              <div>
                <div class="datefromto">to</div>
                <DatePicker></DatePicker>
              </div>
            </div>
            <div class="area">
              <b>Categories</b>
              <!-- <CheckboxGroup v-model="Categories"> -->
              <CheckboxGroup>
                <div><Checkbox label="All"></Checkbox></div>
                <div><Checkbox label="Entertainment"></Checkbox></div>
                <div><Checkbox label="Food"></Checkbox></div>
                <div><Checkbox label="Learning"></Checkbox></div>
                <div><Checkbox label="Outdoors"></Checkbox></div>
              </CheckboxGroup>
            </div>
          </div>
        </div>
      </div>
      <div class="left right-area">
          <div class="result">
            <div> Showing 15 results by...</div>
            <div class="tag">Koahsiung <Icon type="ios-close-outline"></Icon></div>
            <div class="tag">Entertainment <Icon type="ios-close-outline"></Icon></div>
            <div style="clear:both"></div>
            <div class="content" v-for="i in count" :key="i">
              <img class="contentImg" src="@/assets/1.jpeg" alt="">
              <div class="contentDescription">
                <div class="articleTitle">
                  <b>Kogi Cosby sweater.</b>
                </div>
                <div class="articleContent">Donec euismod scelerisque ligula. Maecenas eu varius risus, eu aliquet arcu. Curabitur fermentum suscipit est, tincidunt mattis lorem luctus id. Donec eget massa a diam condimentum pretium. Aliquam erat volutpat. Integer ut tincidunt orci. Etiam tristique, elit ut consectetur iaculis, metus lectus mattis justo, vel mollis eros neque quis augue. Sed lobortis ultrices lacus, a placerat metus rutrum sit amet. Aenean ut suscipit justo.</div>
                <div class="author">
                  <b>Ethan Foster</b>
                </div>
                <div class="articleTag">Entertainment</div>
            
                <div style="clear:both;margin: 10px 0px;"></div>

                <div class="location">
                  <Icon type="ios-location-outline"></Icon>
                  Kaohsiung City
                </div>
                <div class="date">
                  <Icon type="android-calendar"></Icon>
                  2018/5/24 - 2018/5/31
                </div>
              </div>
            </div>
            <div style="clear:both"></div>
            <div style="float:right;margin: 30px">
              <Page :total="100"></Page>
            </div>
          </div>
      </div>
      
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data: function(){
    return {
      count: [1,2,3]
    }
  },
  created () {
  },
  computed: {
   
  },
  methods: {
  }
}
</script>

<style>
html {
  height: 100%;
}
body {
  margin: 0px 0px;
  height: 100%;
  background: #F2F2F2 ;
}


#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}
.pageTitle {
  background-color: #7828B4;
  height: 85px;
}

.haveFun {
  text-align: center;
  line-height: 85px;
  font-family: Optima-ExtraBlack;
  font-size: 36px;
  color: #FFFFFF;
}
.searchbox {
  display:flex;
  align-items:center;
  width: 388px;
  font-size: 20px;
  height: 85px;
  padding: 0px 20px;
}
.search {
  width: 100%;
  border-bottom: 1px solid #fff;
}
.search i {
  float: left;
  color: #fff
}
.search input {
  margin-left: 20px;
  float: left;
  width: auto;
  background-color: rgba( 0, 0, 0, 0);
  border: 0px;
}
.search input:focus {
  outline: none;
}
.right {
  float: right;
}
.right-area {
  width: 850px;
}
.left {
  float: left;
  position: relative;
}
.left-area {
  width: 350px;
}
.filterbox {
  display:flex;
  align-items:center;
  justify-content: center;
}
.filter {
  font-family: Roboto-Bold;
  font-size: 20px;
  width: 300px;
  background-color: #EBEBEB;
}
.area {
  text-align: left;
  padding: 20px 30px;
  border-bottom: 1px solid #D7D7D7;
}
.datefromto {
  width: 40px;
  text-align: right;
  float: left;
  margin-right: 5px;
}
.ivu-checkbox-wrapper {
  font-size: 16px;
}

.result {
  position: absolute;
  left: 0;
  right: 0;
  margin: 20px auto;
  text-align: left;
  font-family: Roboto-Regular;
  font-size: 24px;
  padding: 20px;
  width: 100%;
}
.tag {
  border: 1px solid #9013FE;
  border-radius: 100px;
  padding: 4px 10px;
  font-family: Roboto-Italic;
  font-size: 16px;
  color: #9013FE;
  float: left;
  margin-right: 10px;
}
.content {
  display: flex;
  height: 220px;
  margin-top: 30px;
}
.contentImg {
  flex:1;
  height: auto;
  min-width: 230px;
}
.contentDescription {
  min-width: 388px;
  width: 100%;;
  padding: 10px 20px;
  height: 100%;
  background-color: #fff;
  flex:4;
}
.articleTitle {
  font-family: Roboto-Bold;
  font-size: 24px;
  color: #9013FE;
  line-height: 36px;
  margin: 10px 0px;
}
.articleContent {
  font-family: Roboto-Regular;
  font-size: 16px;
  color: #000000;
  line-height: 24px;
  height: 50px;
  overflow: hidden;
  margin: 10px 0px;
}
.articleTag {
  float: left;
  padding: 2px 10px;
  background: #D7D7D7;
  border-radius: 100px; 
  font-family: Roboto-Italic;
  font-size: 16px;
  color: #FFFFFF;
  text-align: center;
}
.author {
  float: left;
  font-family: Roboto-Bold;
  font-size: 16px;
  color: #000000;
  margin-right: 10px;
}
.location {
  margin-right: 10px;
  float: left;
  font-family: Roboto-Regular;
  font-size: 16px;
  color: #9B9B9B;
}
.location i {
  color: #000000;
}
.date {
  float: left;
  font-family: Roboto-Regular;
  font-size: 16px;
  color: #9B9B9B;
}
.date i {
  color: #000000;
}
.ivu-page-item-active {
  background-color: #7828B4;
  border: 1px solid #7828B4;
}
.ivu-page-item-active a{
  color: #fff;
}
.ivu-page-item:hover {
  color: #fff;
  border: 1px solid #7828B4;
}
.ivu-page-item {
  color: #7828B4;
}

@media screen and (min-width: 591px) and (max-width: 768px) { 
  .left-area {
    width: 300px;
  }
  .right-area {
    width: 450px
  }
  .content {
    flex-wrap: wrap;
    margin-bottom: 250px;
  }
  .contentImg {
    min-width: 388px;
  }
  .contentDescription {
  width: 388px;
  }
}
@media screen and (min-width: 414px) and (max-width: 591px) { 
  body {
    background-color: red
  }
}

</style>
