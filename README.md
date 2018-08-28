#35km项目前端规范

    author:Jesse
    date:2018 - 08 - 27

####**一.目录结构**

    -35km
        -static
            -css        
            -images     //图片文件
                -icon   //图标
            -js
            -plugins    //所有插件存放此文件夹下
            -videos     //视频文件
         -views         //所有页面存放此文件夹下
            -index.html //index页

####**二.基本原则**
    1.结构, 样式, 行为分离  
      
      确保文档和模板只包含 HTML 结构, 样式都放到样式表里, 行为都放到脚本里.
      For Example:
                   -person.html
                   -person.css
                   -person.js
    
    2.统一使用Tab键缩进
    
    3.全项目utf8格式
    
    4.统一注释
        
        HTML注释:
            
            模块注释:
                
                <!-- 模块注释 -->
            
            区块注释:
                
                <!--
                @name:35km
                @des:区块注释
                @author:Jesse
                -->
        
        CSS注释:
            
            组件块:
                
                /* ======================================================
                    组件块
                ====================================================== */
            
            子组件块:
                
                /* 自组件块
                ====================================================== */
            
            注释:
                
                .login {
                    display: block; /* 注释 */
                }    
        
        JS注释:
            
            单行注释:
                
                // 单行注释 (必须独占一行, // 后跟一空格)
            
            多行注释:
                
                使用多个单行注释
             
            函数/方法注释:
                
                /**
                 * 函数描述
                 * @param p1 参数p1的说明
                 * @param p2 参数p2的说明
                 * @returns  返回值描述
                 */
####**三.HTML规范**
    1.标签:
        
        自闭合(self-closing)标签(For Example: img, input, br, hr 等)
        标签嵌套时, 注意嵌套规范
        
    2.class与id
        
        命名要见名知意
        多个单词组成时, 采用中划线分隔
    
    3.标签属性顺序:
        
        id -> class -> name -> data-xxx -> src,for,type,href -> title,alt -> role
    
    4.引号:
        
        属性的定义统一使用双引号
        For Example:
            <span id="j-hook" class="text"></span>
    
    5.为每个HTML页面的第一行添加标准模式的声明, 这样能够确保在每个浏览器中拥有一致的表现
        
        <!DOCTYPE html>
    
    6.语言属性
        
        <!-- 中文 -->
        <html lang="zh-Hans">
        
        <!-- 简体中文 -->
        <html lang="zh-cmn-Hans">
        
        <!-- 繁体中文 -->
        <html lang="zh-cmn-Hant">
        
        <!-- English -->
        <html lang="en">
####**四.CSS规范**
    1.模块和模块之间空一行
    
    2.注意注释的规范
    
    3.声明块的左括号 { 前添加一个空格
    
    4.声明块的右括号 } 应单独成行
    
    5.声明语句中的 : 后应添加一个空格
    
    6.声明语句以 ; 号结束
    
    7.十六进制值全部小写
    
    8.避免为0值指定单位, 例如 用 margin: 0; 代替 margin: 0px;
    
    For Example:
        .selector,
        .selector-secondary,
        .selectp[type="text"] {
            padding: 15px;
            margin-bottom: 15px;
            background-color:　rgab(0,0,0,.5);
            box-shadow: 0 1px 2px
####**五.JS规范**
    
    1.变量,函数,方法,参数 命名使用驼峰命名法
        
    2.boolean类型变量使用is开头
        
        var isShaBi = true;
        
    3.私有属性, 变量和方法以下划线_开头
        
        var _privateMethod = {};
    
    4.常量使用全部字母大写，单词间下划线分隔的命名方式
        
        var HTML_ENTITY = {};
    
    5.类名使用名词
        
        function Engine(options) {}
        
    6.函数名 使用动宾短语
    
        funciton getStyle(element) {}
    
    7.不要在Array上使用for-in循环(因为该循环并不是从0开始进行遍历), object/map/hash 可以使用
    
    