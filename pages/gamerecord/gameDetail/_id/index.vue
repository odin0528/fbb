<template>
<v-container fluid class="px-10 pt-7" :class="{fontSize:$vuetify.breakpoint.mobile}">
        <v-row no-gutters >  
         <v-breadcrumbs :items="breadcrumbs" class="ml-5">
                <template v-slot:divider>
                <v-icon large>keyboard_arrow_right</v-icon>
                </template>
                <template v-slot:item="{ item }">
                    <v-breadcrumbs-item
                        :href="item.href"
                        :disabled="item.disabled"
                    >
                      <span :style="{color:item.disabled?'black':'blue','font-size':'20px'}" >   {{ item.text }}</span>
                    </v-breadcrumbs-item>
                </template>
        </v-breadcrumbs>
        </v-row>
         <v-row no-gutters >  
          <v-col cols="5">
              <hr style="height:5px;background-color:#4472C4;border-width:0;">
          </v-col>
          <v-col cols="7"></v-col>
          
        </v-row>
      
         
                        <v-row no-gutters class="mx-4 mt-4">
                            <v-col :sm='12' :md="7" class="mt-1" >
                                <v-card min-width="280px" style="height:40px;background-color:#9ABDE4;" class="d-flex" >
                                    <div class="d-flex justify-start align-center" style="width:25%;height:100%;">
                                        <span class="ml-2">遊戲編號 :</span>
                                    </div>
                                    <div class="d-flex justify-start align-center " style="width:75%;height:100%;">
                                        <span class="ml-2 " style="font-weight:bold;max-width: 97%;">21321231313112aasaasaaasasa</span>
                                    </div>
                                </v-card>
                            </v-col>
                            <v-col  :sm='12' :md="5" class="mt-1" >
                                <v-card min-width="280px" style="height:40px;background-color:#9ABDE4;" class="d-flex ml-1" >
                                    <div class="d-flex justify-start align-center" style="width:25%;height:100%;">
                                        <span class="ml-2">得獎寶貝 :</span>
                                    </div>
                                    <div class="d-flex justify-start align-center" style="width:75%;height:100%;">
                                        <span class="ml-2" style="font-weight:bold"> 豪哥</span>
                                    </div>
                                </v-card>
                            </v-col>
                            
                            
                        </v-row> 
                        <v-row no-gutters class="mx-4">
                            <v-col :md="4" :sm='12' class="mt-1">
                                <v-card min-width="280px" style="height:40px;background-color:#9ABDE4;" class="d-flex " >
                                    
                                    <div class="d-flex justify-start align-center" style="width:50%;height:100%;">
                                        <span class="ml-2">遊玩票數  : </span>
                                    </div>
                                    <div class="d-flex justify-start align-center" style="width:50%;height:100%;">
                                        <span class="ml-2" style="font-weight:bold"> 5000張</span>
                                    </div>
                                </v-card>
                            </v-col>
                             <v-col :md="4"  :sm='12' class="mt-1">
                                <v-card min-width="280px" class="ml-1 d-flex" style="height:40px;background-color:#9ABDE4;" >
                                    <div class="d-flex justify-start align-center" style="width:50%;height:100%;">
                                        <span class="ml-2">遊戲歷時:  </span>
                                        <!-- regs time -->
                                    </div>
                                    <div class="d-flex justify-start align-center" style="width:50%;height:100%;">
                                        <span class="ml-2" style="font-weight:bold">  10h59m59s</span>
                                    </div>
                                </v-card>
                            </v-col>
                            <v-col :md="4" :sm='12' class="mt-1">
                                <v-card min-width="280px" class="ml-1 d-flex" style="height:40px;background-color:#9ABDE4;" >
                                    <div class="d-flex justify-start align-center" style="width:50%;height:100%;">
                                        <span class="ml-2">遊玩人數 :  </span>
                                        <!-- regs time -->
                                    </div>
                                    <div class="d-flex justify-start align-center" style="width:50%;height:100%;">
                                        <span class="ml-2" style="font-weight:bold">  100人</span>
                                    </div>
                                </v-card>
                            </v-col>
                            
                            
                        </v-row> 
                       
                        <v-row no-gutters class="mx-4 ">
                            <v-col :md="6" :sm='12' class="mt-1" >
                                <v-card min-width="280px" style="height:40px;background-color:#9ABDE4;" class="d-flex " >
                                    <div class="d-flex justify-start align-center" style="width:50%;height:100%;">
                                        <span class="ml-2">開始時間:   </span>
                                    </div>
                                    <div class="d-flex justify-start align-center" style="width:50%;height:100%;">
                                        <span class="ml-2" style="font-weight:bold"> 2020/09/15 01:12</span>
                                    </div>
                                </v-card>
                            </v-col>
                             <v-col :md="6" :sm='12'  class="mt-1">
                                <v-card min-width="280px" style="height:40px;background-color:#9ABDE4;" class="d-flex ml-1" >
                                    <div class="d-flex justify-start align-center" style="width:50%;height:100%;">
                                        <span class="ml-2">結束時間 :  </span>
                                    </div>
                                    <div class="d-flex justify-start align-center" style="width:50%;height:100%;">
                                        <span class="ml-2" style="font-weight:bold"> 2020/09/15 01:12</span>
                                    </div>
                                </v-card>
                            </v-col>
                            
                            
                        </v-row> 
                         <v-row no-gutters class="mx-4 ">
                            <v-col :md="6" :sm='12'  class="mt-1">
                                <v-card min-width="280px" style="height:40px;background-color:#9ABDE4;" class="d-flex" >
                                    <div class="d-flex justify-start align-center" style="width:50%;height:100%;">
                                        <span class="ml-2">總投入彩金 :  </span>
                                    </div>
                                    <div class="d-flex justify-start align-center" style="width:50%;height:100%;">
                                        <span class="ml-2" style="font-weight:bold"> 2020/09/15 01:12</span>
                                    </div>
                                </v-card>
                            </v-col>
                             <v-col :md="6" :sm='12' class="mt-1" >
                                <v-card min-width="280px" style="height:40px;background-color:#9ABDE4;" class="d-flex ml-1" >
                                    <div class="d-flex justify-start align-center" style="width:50%;height:100%;">
                                        <span class="ml-2">總派獎彩金 :  </span>
                                    </div>
                                    <div class="d-flex justify-start align-center" style="width:50%;height:100%;">
                                        <span class="ml-2" style="font-weight:bold"> 2020/09/15 01:12</span>
                                    </div>
                                </v-card>
                            </v-col>
                            
                            
                        </v-row> 
                                <v-flex  xs12 md12  class="mt-1 mx-4 font-weight-bold">
                                                <v-card   color="#9ABDE4" min-height="45vh" >
                                                    <v-card  flat min-height="40vh" color="#9ABDE4">
                                                        <v-row no-gutters style="height:50px" justify="start" align="center">   
                                                               
                                                            <span style="color:black;font-size:22px" class="ml-5"> HASH幸運8:</span>
                                                        </v-row>
                                                                <v-row class="mx-4">
                                                                    <v-col cols="4">HASH幸運8編號 </v-col>
                                                                    <v-col cols="4"> 觸發玩家 </v-col>
                                                                    <v-col cols="4">   HASH增加彩金數</v-col>
                                                                </v-row> 
                                                                <hr class="mx-4" style="height:3px;background-color:#4472C4;border-width:0;">
                                                                <v-row  class="mx-4 my-1" dense v-for="n in 10" :key="n">
                                                                    <v-col cols="4">alskdjalsjdlkas </v-col>
                                                                    <v-col cols="4">  dasds@gmai.com.asdada </v-col>
                                                                    <v-col cols="4">  10000
                                                                       
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
<style scoped>
    .fontSize{
        font-size: 11px;
    }
</style>
<script>
export default {
    data(){
        return{
            pageNumber:1,
            breadcrumbs: [
                    {
                    text: '遊戲紀錄',
                    disabled: false,
                    href: '/gamerecord',
                    },
                    {
                    text: '詳細資料',
                    disabled: true,
                    href: '/gamerecord/gameDetail/123',
                    },
                ],
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