<template>
  <el-container>
    <!-- Header -->
  <el-header class="hander-container">
      <div class="l-content">
        <span>RDR</span>  
        <span>|</span>
        <span>AI工作平台</span>
      </div>
      <div class="r-content">
        <el-dropdown>
          <span class="el-dropdown-link">
            模块名称<i class="el-icon-arrow-down el-icon--right"></i>
          </span>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>模块名称</el-dropdown-item>
            <el-dropdown-item>模块名称</el-dropdown-item>
            <el-dropdown-item>模块名称</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
        <span class="el-icon-message-solid"></span>
        <span>Name<i class="el-icon-s-fold"></i></span>
      </div>

  </el-header>
  <el-container>
    <!-- 左侧边栏 -->
    <el-aside width="200px">
      <el-row>
        <el-col >
          <h5 class="left-tital el-icon-s-custom">角色选择</h5>
          <el-menu
      default-active="2"
      class="el-menu-vertical-demo">
      <el-submenu index="1">
        <template slot="title">
          <i class="el-icon-location"></i>
          <span>产品设计</span>
        </template>
        <el-menu-item-group>
          <template slot="title">分组一</template>
          <el-menu-item index="1-1">选项1</el-menu-item>
          <el-menu-item index="1-2">选项2</el-menu-item>
        </el-menu-item-group>
        <el-menu-item-group title="分组2">
          <el-menu-item index="1-3">选项3</el-menu-item>
        </el-menu-item-group>
        <el-submenu index="1-4">
          <template slot="title">选项4</template>
          <el-menu-item index="1-4-1">选项1</el-menu-item>
        </el-submenu>
      </el-submenu>
      <el-menu-item index="2">
        <i class="el-icon-menu"></i>
        <span slot="title">技术研发</span>
      </el-menu-item>
      <el-menu-item index="3">
        <i class="el-icon-document"></i>
        <span slot="title">测试验收</span>
      </el-menu-item>
      
    </el-menu>
        </el-col>
      </el-row>

    



    </el-aside>
    <!-- 中间 -->
    <el-main class="main-container">
      <div class="main-tital">RDR问题预设</div>
      <div class="main-content">
          <div class="out-border">常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1</div>
          <div class="out-border">常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1</div>
          <div class="out-border">常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1</div>
          <div class="out-border">常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1</div>
          <div class="out-border">常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1</div>
          <div class="out-border">常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1</div>
          <div class="out-border">常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1</div>
          <div class="out-border">常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1</div>
          <div class="out-border">常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1常见问题1</div>
         
          <el-input class="main-input" type="text"  placeholder="请输入内容">
            <span slot="suffix">
              <i class="el-icon-position"></i>
            </span>
          </el-input>
      
        </div>
     
    </el-main>
    <!-- 右侧边栏 -->
    <el-aside width="200px">
      <el-row class="tac">
  <el-col :span="12">

    <el-menu
      default-active="2"
      class="el-menu-vertical-demo">
      <el-submenu index="1">
        <template slot="title">
          <i class="el-icon-location"></i>
          <span>问题预设</span>
        </template>
          <el-menu-item index="1-1">预设问题自定义</el-menu-item>
          <el-menu-item index="1-2">提问记录管理</el-menu-item>
      </el-submenu>

      <el-submenu index="2">
        <template slot="title">
            <i class="el-icon-menu"></i>
          <span >常用网站</span>
        </template>
        <el-menu-item index="2-1">常用链接管理</el-menu-item>
      </el-submenu>


      <el-submenu index="3">
        <template slot="title">
            <i class="el-icon-document"></i>
          <span >常用工具</span>
        </template>
        <el-menu-item index="3-1">语言翻译</el-menu-item>
        <el-menu-item index="3-1">语言功能</el-menu-item>
        <el-menu-item index="3-1">语言工具编辑</el-menu-item>

      </el-submenu>
      
    </el-menu>
  </el-col>
      </el-row>
    </el-aside>

  </el-container>
  <el-dialog title="添加活动" :visible.sync="dialogVisible" width="40%">
      <el-form :model="flashPromotion" ref="flashPromotionForm" label-width="150px" size="small">
        <el-form-item label="预设问题1：">
          <el-input v-model="flashPromotion.problem" style="width: 250px"></el-input>
        </el-form-item>
        <el-form-item label="预设问题1：">
          <el-input v-model="flashPromotion.problem" style="width: 250px"></el-input>
        </el-form-item>
        <el-form-item label="预设问题1：">
          <el-input v-model="flashPromotion.problem" style="width: 250px"></el-input>
        </el-form-item>
        <el-form-item label="预设问题1：">
          <el-input v-model="flashPromotion.problem" style="width: 250px"></el-input>
        </el-form-item>
        <el-form-item label="预设问题1：">
          <el-input v-model="flashPromotion.problem" style="width: 250px"></el-input>
        </el-form-item>
        <el-form-item label="预设问题1：">
          <el-input v-model="flashPromotion.problem" style="width: 250px"></el-input>
        </el-form-item>
      </el-form>
      <span slot="footer" class="dialog-footer">
        <el-button @click="dialogVisible = false" size="small">取消</el-button>
        <el-button type="primary" @click="handleDialogConfirm()" size="small">确定</el-button>
      </span>
    </el-dialog>
</el-container>
</template>

<script>

const defaultFlashPromotion = {
    id:null,
    problem: null,
}
  export default {
    data() {
      return {
        dialogVisible : false,
        isEdit: false,
        flashPromotion: Object.assign({}, defaultFlashPromotion),
      };
    },
    method:{
      Handleproblem() {
        this.dialogVisible = true;
        this.isEdit = true;
        this.flashPromotion = Object.assign({}, defaultFlashPromotion);
      },
      handleDialogConfirm() {
        this.$confirm('是否要确认?', '提示', {
          confirmButtonText: '确定',
          cancelButtonText: '取消',
          type: 'warning'
        }).then(() => {
          if (this.isEdit) {
            updateFlash(this.flashPromotion.id,this.flashPromotion).then(response => {
              this.$message({
                message: '修改成功！',
                type: 'success'
              });
              this.dialogVisible =false;
            })
          } else {
            createFlash(this.flashPromotion).then(response => {
              this.$message({
                message: '添加成功！',
                type: 'success'
              });
              this.dialogVisible =false;
            })
          }
        })
      },
  }
   
  }
</script>


<style scoped>
.hander-container {
  background-color: #001529;
  height: 60px;
  color:aliceblue;
}

.l-content{
  float: left;
  align-items: center;
  line-height: 60px;
  
}
.l-content span {
  margin: 0 10px;
}

.r-content {
  float: right;
  align-items: center;
  line-height: 60px;
}
.r-content span {
  margin:0 10px;
}

.el-dropdown-link {
  color:aliceblue;

}
  .el-menu-vertical-demo:not(.el-menu--collapse) {
    width: 200px;
    min-height: 400px;
  }
  .left-tital {
    width:100%;
    height: 40px;
    line-height: 40px;
    padding-left: 30px;
    font-size: 16px;
    margin: 20px 10;
    border-bottom: 1px solid #909399;
  }

.main-container {
  background-color:#efefef;
  padding:20px;
  font-size:14px;

}

.main-tital {
  width:200px;
  height: 50px;;
  font-size: 30px;
  margin: 50px auto;
}

.main-content {
  width:750px;
  height: 600px;
  margin: 0 auto;
}

.out-border {
  width: 180px;
  height: 120px;
  float: left;
  margin: 7px 30px;
  padding: 8px;
  border:1px solid #dcdfe6;
  background-color: #fff;
  border-radius: 20px;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
}

.main-input {
  width: 720px;
  height: 50px;
  margin: 70px auto;

}

.main-input i {
  width: 40px;
  height: 40px;
  font-size: 20px;
  align-items: center;
}
</style>