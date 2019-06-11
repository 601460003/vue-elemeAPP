<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <link rel="stylesheet" href="https://unpkg.com/element-ui/lib/theme-chalk/index.css">
    <script src="https://cdn.jsdelivr.net/npm/vue"></script>
    <script src="https://unpkg.com/element-ui/lib/index.js"></script>
</head>
<body>
<style>
.el-button{
    width: 120px;
    letter-spacing: 5px;
    background: #169BD5;
}

.header_content {
    display: flex;
    justify-content: space-around;
    margin-top: 30px;

}
</style>
<div id="app">
    <div  style="text-align: center">
        <header>
            <el-form :inline="true"  class="demo-form-inline">
                <el-form-item label="报表名称">
                    <el-input placeholder="请输入报表名称"></el-input>
                </el-form-item>
                <el-form-item>
                    <el-button type="primary">查询</el-button>
                </el-form-item>
            </el-form>
        </header>
        <hr>
        <div style="text-align: center;line-height: 30px;color: #333">
            <table  width="800px"  align="center" >
                <tr>
                    <th>序号</th>
                    <th>报表名称</th>
                    <th>备注</th>
                </tr>
                <tr>
                    <td>1</td>
                    <td>短信接收统计报表</td>
                    <td>统计用户在某时间段内短信的接收量</td>
                </tr>
                <tr>
                    <td>2</td>
                    <td>积分概况统计报表</td>
                    <td>统计用户在某时间段内获取的积分</td>
                </tr>
                <tr>
                    <td>3</td>
                    <td>学校应用点击量统计</td>
                    <td>统计学校月/周应用点击量</td>
                </tr>
            </table>
        </div>
    </div>
    <div>
        <br>
        <p style="margin-left: 13px">当前位置：短信接收统计报表>页面详情</p>
        <!--列表头部-->
        <div class="demo-input-suffix header_content">
            <!--日期范围-->
            <div >
                <lable>日期范围</lable>
                <el-date-picker type="date" placeholder="请选择日期范围" ></el-date-picker>
            </div>
            <!--地区-->
           <div>
               <el-form :inline="true" class="demo-form-inline" >
                   <el-form-item label="地区">
                       <el-select placeholder="地区">
                           <el-option label="区域一" value="shanghai"></el-option>
                           <el-option label="区域二" value="beijing"></el-option>
                       </el-select>
                   </el-form-item>
               </el-form>
           </div>
            <!--学校名称-->
            <div>
                <el-form :inline="true"  class="demo-form-inline">
                <el-form-item label="学校名称">
                    <el-input placeholder="请输入学校名称"></el-input>
                </el-form-item>
                </el-form>
            </div>
            <!--按钮-->
            <div>
                <el-button type="primary">查询</el-button>
                <el-button type="primary">导出</el-button>
            </div>
        </div>
        <!--表格-->
        <template>
            <el-table
                    :data="tableData"
                    border
                    style="width: 100%">
                <el-table-column
                        align="center"
                        prop="date"
                        label="序号"
                        width="180">
                </el-table-column>
                <el-table-column
                        align="center"
                        prop="name"
                        label="地区"
                        width="180">
                </el-table-column>
                <el-table-column
                        align="center"
                        prop="address"
                        label="学校">
                </el-table-column>
                <el-table-column
                        align="center"
                        prop="name"
                        label="班级/部门"
                        width="180">
                </el-table-column>
                <el-table-column
                        align="center"
                        prop="name"
                        label="姓名"
                        width="160">
                </el-table-column>
                <el-table-column
                        align="center"
                        prop="name"
                        label="角色"
                        width="160">
                </el-table-column>
                <el-table-column
                        align="center"
                        prop="name"
                        label="手机号码"
                        width="160">
                </el-table-column>
                <el-table-column
                        align="center"
                        prop="name"
                        label="是否本网"
                        width="160">
                </el-table-column>
                <el-table-column
                        align="center"
                        prop="name"
                        label="短信接收（条）"
                        width="160">
                </el-table-column>
            </el-table>
        </template>
    </div>
</div>

<script>
    new Vue({
        el: '#app',
        methods: {
            handleClick(row) {
                console.log(row);
            }
        },
        data: {
            input1: '',
            input2: '',
            tableData: [{
                date: '20',
                name: '王小虎',
                province: '上海',
                city: '普陀区',
                address: '上海市普陀区',
                zip: 200333
            }, {
                date: '20',
                name: '王小虎',
                province: '上海',
                city: '普陀区',
                address: '上海市普陀区',
                zip: 200333
            }, {
                date: '20',
                name: '王小虎',
                province: '上海',
                city: '普陀区',
                address: '上海市普陀区',
                zip: 200333
            }, {
                date: '20',
                name: '王小虎',
                province: '上海',
                city: '普陀区',
                address: '上海市普陀区',
                zip: 200333
            }]
        }
    })
</script>
</body>
</html>
