<template>
    <div>
        <el-row>
            <el-container>
                <el-header>
                    <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
                        <el-menu-item>Kyo's Blog</el-menu-item>
                        <el-menu-item index="1"><i class="el-icon-house"></i>首页|Home</el-menu-item>
                        <el-submenu index="2">
                            <template slot="title"><i class="el-icon-menu"></i>分类查询</template>
                            <el-menu-item index="2-1"><i class="el-icon-paperclip"></i>分类</el-menu-item>
                            <el-menu-item index="2-2"><i class="el-icon-price-tag"></i>标签</el-menu-item>
                            <el-menu-item index="2-3"><i class="el-icon-tickets"></i>归档</el-menu-item>
                        </el-submenu>
                        <el-menu-item index="3"><i class="el-icon-user"></i>关于我</el-menu-item>
                        <el-menu-item index="4" class="search-box">
                            <el-input
                                    placeholder="请输入搜索内容 | Search..."
                                    suffix-icon="el-icon-search"
                                    v-model="searchInput">
                            </el-input>
                        </el-menu-item>
                    </el-menu>
                </el-header>
                <el-main>
                    <el-row :gutter="20">
                        <el-col :span="18">
                            <el-card class="box-card">
                                <div slot="header">
                                    <span>博客 | Blog</span>
                                    <span>共 ? 篇</span>
                                </div>
                                <div v-for="o in 4" :key="o" class="text item">
                                    {{'列表内容 ' + o }}
                                </div>
                            </el-card>
                        </el-col>
                        <el-col :span="6">
                            <el-row>
                                <el-col>
                                    <el-card class="aside-box">
                                        <div v-for="o in 4" :key="o" class="text item">
                                            {{'列表内容 ' + o }}
                                        </div>
                                    </el-card>
                                </el-col>
                                <el-col>
                                    <el-card class="aside-box">
                                    <div v-for="o in 4" :key="o" class="text item">
                                        {{'列表内容 ' + o }}
                                    </div>
                                </el-card>
                                </el-col>
                                <el-col>
                                    <el-card class="aside-box">
                                        <div v-for="o in 4" :key="o" class="text item">
                                            {{'列表内容 ' + o }}
                                        </div>
                                    </el-card>
                                </el-col>
                                <el-col>
                                    <el-card class="aside-box">
                                    <div v-for="o in 4" :key="o" class="text item">
                                        {{'列表内容 ' + o }}
                                    </div>
                                </el-card>
                                </el-col>
                                <el-col>
                                    <el-card class="aside-box">
                                        <div v-for="o in 4" :key="o" class="text item">
                                            {{'列表内容 ' + o }}
                                        </div>
                                    </el-card>
                                </el-col>
                            </el-row>
                        </el-col>
                    </el-row>
                </el-main>
                <el-footer>
                    <el-row>
                        <el-col :span="6">
                            <span>雨纷纷</span>
                        </el-col>
                        <el-col :span="1">
                            <el-divider direction="vertical"></el-divider>
                        </el-col>
                        <el-col :span="6">
                            <span>旧故里</span>
                        </el-col>
                        <el-col :span="1">
                            <el-divider direction="vertical"></el-divider>
                        </el-col>
                        <el-col :span="10">
                            <span>草木深</span>
                        </el-col>
                    </el-row>
                    <el-divider></el-divider>
                    <el-row>最后</el-row>
                </el-footer>
            </el-container>
        </el-row>
    </div>
</template>

<script>
    export default {
        data(){
            return{
                //默认激活index
                activeIndex: '1',
                //搜索框
                searchInput: '',
            }
        },
        created() {
        },
        methods:{
            handleSelect(key, keyPath) {
                console.log(key, keyPath);
            }
        }
    }
</script>

<style lang="less" scoped>

    .aside-box{
        margin-bottom: 15px;
    }
    .search-box{
        float: right !important;
    }
</style>