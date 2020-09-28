# testtest
aaa

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>トップページ</title>
    <link rel="stylesheet" href="../css/style.css">
</head>
<style>

/* メインここから */
.main-glid{
    display:grid;
    grid-template-rows: 0 100px auto  auto  ;
    grid-template-columns: 0.1fr 0.35fr 0.1fr 0.35fr 0.1fr;
    grid-template-areas:
        "header header header header header"
        "...    ...     ...    ...    ..."
        "...  title1 title1   title1  ...";       
      }
/* ヘッダー */
header{
    grid-area:header;
    background: rgba(177, 212, 238,0.3);
    position: fixed;
    width: 100%;
    
}
/* メイン画像 */


/* タイトル１ */
.title1{
    grid-area:title1;
    /* background: #f88; */
}
.title1 h1{
    padding-left:2%;
    background: rgba(250, 237, 207, 0.6);
}

/* エディターエリア */
.editar-area{
    display:grid;
    grid-template-rows: auto   ;
    grid-template-columns: 0.1fr 0.35fr 0.1fr 0.35fr 0.1fr;
    grid-template-areas:
        "... container container container ..."
     

       
      }

.container {
  grid-area:container;
  display: -webkit-flex;
  display: flex;
}
.main {
  display: block;
  width: 60%;
  margin-right: 20px;
}
.diaryImg{
    width: 100%;
    max-height: 500px;

}
.sidebar {
  width: 35%;
  /* background-color: rgb(94, 227, 112); */

}

.sidebar__item {
  margin-bottom: 20px;
  /* background-color: blue; */
}

.form{
    margin-top:-20px;
    width: 100%;
    padding: 15px;
    background:#f8f8f8;
    border:1px solid rgba(0, 0, 0, 0.075);
    margin-bottom:25px;
    color:#727272 !important;
    font-size:13px;
    -webkit-transition: all 0.4s;
    -moz-transition: all 0.4s;
    transition: all 0.4s;
  }
  .textarea{
    height: 200px;
    max-height: 200px;
    max-width: 100%;
  }
 
  .lbutton{
  width: 60%;
    padding: 7px;
    border: 2px solid #d7dee2;
    font-size: 13px;
    margin-top:2%;
    margin-left:20%;
    color:#727272 !important;
    vertical-align: middle;
    -webkit-border-radius: 4px;
    -moz-border-radius: 4px;
    border-radius: 4px;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;

}


.sidebar__item--fixed {
  position: sticky;
  margin-bottom: 0;
  top: 100px;
  z-index: 1;
}

/* エディタここまで ＝＝＝＝＝＝＝＝＝＝＝＝*/

/* コメント */
.comment-area{
    display:grid;
    grid-template-rows: auto   ;
    grid-template-columns: 0.1fr 0.35fr 0.1fr 0.35fr 0.1fr;
    grid-template-areas:
        "... dcomment dcomment ... ..."
     
}

.dcomment{
    grid-area:dcomment;
    background-color: rgba(235, 228, 161, 0.5);
}

</style>
<body>
<div class="main-glid">


    <header>
       <ul>
         <li>
             <a href="/mypage">
                <% if (typeof user !== 'undefined') { %>
                    <img src="../images/account.jpg" class='aimg' alt="" >  
                  <% } %>
            </a>
        </li>
        <li><a href="/">Home</a></li>
         <li><a href="/shops">Shop</a></li>
         <li><a href="/diarys">Diary</a></li>
         <li><a href="/flowers">Flower</a></li>
         <!-- <li><div id='search'>検索</div></li> -->
         <% if (typeof user == 'undefined') { %>
         <li><a href="/login">Login</a></li>
         <% } else{%>
         <li><a href="/logout">Logout</a></li>
         <% } %>
       </ul>
    </header>


   <div class="title1">
       <h1>diary</h1>
   </div>

</div>


<div class="editar-area">
   <div class="container">
    <main class="main">
      <!-- メインコンテンツ -->
      <div><img class='diaryImg' src="../images/uploads/<%= item.image %>"></div>
      <h2><%=item.title%></h2>
      <h3><%=item.tag%></h3>
      <p name="" id="" cols="30" rows="10"><%=item.text%></p>
      <div class="dcomment">
        <p>名前</p> <p>こめんと</p>
        <p>名前</p> <p>こめんと</p>
        <p>名前</p> <p>こめんと</p>
        <p>名前</p> <p>こめんと</p>
        <p>名前</p> <p>こめんと</p>
        <p>名前</p> <p>こめんと</p>
        <p>名前</p> <p>こめんと</p>
     
    </div>
    </main>
    <div class="sidebar">
      <div class="sidebar__item">
        <!-- 中身 -->
      </div>
      <div class="sidebar__item sidebar__item--fixed">
        <!-- 固定・追従させたいエリア -->
        <form action="/message/<%= item.id %>" method="post">
            <textarea name="comment" id="message" class="form textarea"  placeholder="Comment"></textarea>
            <button class="lbutton" type="submit" class="submit">submit</button>
        </form>
        
        <!-- <img src="../images/img1.jpg" alt="" style='height: 300px;'> -->
      </div>
    </div>
  </div>
</div>

<!-- 
<div class="comment-area">
  <div class="dcomment">
      <p>名前</p> <p>こめんと</p>
   
  </div>


</div> -->






     <footer>
         <h3>Copyright  second-cube</h3>
     </footer>








</body>
</html>
```
