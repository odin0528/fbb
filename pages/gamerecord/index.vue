<template>
 <v-container fluid class="px-10 pt-7">
        <v-row no-gutters >  
          <span style="color:black;font-size:25px" class="ml-5"> 遊戲紀錄</span>
          <!-- memberList -->
        </v-row>
         <v-row no-gutters >  
          <v-col cols="6">
              <hr style="height:5px;background-color:#4472C4;border-width:0;">
          </v-col>
          <v-col cols="6"></v-col>
          <!-- memberList -->
        </v-row>
        <v-flex  xs12 md12  class="mt-6">
          <v-card  color="#9ABDE4" min-height="75vh" >
            <v-card  flat min-height="70vh" color="#9ABDE4">
                        <v-row no-gutters style="background-color:#4472C4;height:60px" class="d-flex align-center pa-3">  
                            <v-row no-gutters style="height:40px" justify="end">
                                <v-col sm="12" md="4">
                                    <v-text-field color="black" outlined 
                                        type="text" background-color="white" dense 
                                        append-icon="search" 
                                        @click:append="searchMembers"> 
                                    <template v-slot:prepend>
                                    <span class="d-flex  justify-end" style="width:50px;height:30px;font-size:23px"> 搜尋</span>
                                    </template>
                                    </v-text-field>
                                    <!-- use v autocomplete for async search -->
                                </v-col>
                            </v-row>
                        
                        </v-row>
                        <v-row  class="mx-4">
                            <v-col cols="3">遊戲編號</v-col>
                            <v-col cols="3">  開始時間</v-col>
                            <v-col cls="3">  遊玩人數</v-col>
                            <v-col cols="3"></v-col>
                        </v-row> 
                        <hr class="mx-4" style="height:3px;background-color:#4472C4;border-width:0;">
                        <v-row  class="mx-4 my-1" dense v-for="n in 10" :key="n">
                            <v-col cols="3">123132312312</v-col>
                            <v-col cols="3"> 2020/09/14  11:59:05</v-col>
                             <v-col cols="3"> 100</v-col>
                            <v-col cols="3">
                                <v-row no-gutters justify="end" class="mr-3">
                                    <v-btn @click="$router.push('/gamerecord/gameDetail/123')">
                                        <span style="font-weight:bold">詳細</span>
                                        <!-- detail -->
                                    </v-btn>
                                </v-row>
                            </v-col>
                        </v-row> 
            </v-card>
            <v-row no-gutters  justify="center" align="center">
                
                 <v-btn icon x-large color="#4472C4" style="transform:rotateY(180deg)" @click="changePage('-')"> 
                    <v-icon x-large>forward</v-icon>
                </v-btn>
                <div style="height:40px;width:50px;">
                <v-text-field
                    single-line
                    solo 
                    class="pa-0 ma-0"
                    dense  
                    v-model="pageNumber"
                ></v-text-field>
                </div>
                <span> /100</span>
                <v-btn icon x-large color="#4472C4" @click="changePage('+')">
                    <v-icon x-large>forward</v-icon>
                </v-btn>
            </v-row>
          </v-card>
        </v-flex>
 </v-container>
</template>
<script>
export default {
    data(){
        return{
            pageNumber:1
        }
    },
    methods:{
        searchMembers(){
            console.log('searchmember')
        },
        changePage(e){
            if(this.pageNumber<=1){
                if(e=='-'){
                    return
                }else{
                    this.pageNumber+=1
                }
            }else{

            switch(e){
                case '+':
                    this.pageNumber+=1
                    break;
                case '-':
                    this.pageNumber-=1
                    break;
            }
            }
        }
    },
     watch: {
           pageNumber: function (val, oldVal) {
               //debounce if necessary
            console.log('new: %s, old: %s', val, oldVal)
        },
     }
}
</script>