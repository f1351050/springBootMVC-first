# springBootMVC-first  
 参考動画  
 https://www.youtube.com/watch?v=h9XF7j5L2fE&list=RDCMUC57H40XcMcL4Lbp_Uq2MVaQ&start_radio=1&rv=h9XF7j5L2fE&t=28  
  
# demo  
 ![20231206成果物](https://github.com/f1351050/springBootMVC-first/assets/126868552/2c451ce2-ccd2-4799-8688-91a038dc6d8d)  

# 学習memo  
 ＠Contller  
  ・クラス定義の前に、"@Controller"というアノテーションを付与することにより、Contllerとして動くことができる。  
  ＝リクエストを受け取れるクラスになる  
  ※コード量を削減できる  
  
 ＠RequestMapping(URLパス)  
  ・どういうリクエストがきたときに、どのメソッドを動かすのか？　を対応づけを指定しているアノテーション  
  例えば、/registerというリクエストがきたときに、このアノテーションを付与したメソッドを動かすことができる  
  
 @ModelAttribute  
 リクエストパラメータの割り当てができるアノテーション  
 ※ModelAttribute指定のBeanではメンバ変数名をリクエストパラメーターに合わせる  
   
@ModelAndView   
・モデルとビューの情報を保持  
どのように保持しているのか？  
　⇒　mav.addObject("rb",rb); →モデルの情報をもたせる  
      mav.setViewName("register.html");　→次のビューの情報をもたせる  
・最後に戻り値で返す必要ある  
  
Thymeeaf  
動的な部分をHTMLの属性として記述することができる  
  
EL式 ( Expression Language )  
${ 式 } で値を出力できる記述  
例：${ 2* 3 }  / ${ i < 3} / ${ age } / ${ requestScope.name }  
  
テンプレートエンジン  
<strong th:text = "${ rb.name }"></strong>  
テンプレート(フォーマット)とデータを組み合わせて文字列を出力する仕組み  
  
ーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーーー  
動画動画内容から改善するべき事項  
・registerページ（登録確認ページで[登録][戻る]ボタンを押しても反応しない  
【メモ】  
　アノテーションのGetMappng RequestMapping の違い  
　　・RequestMapping  
　　　主にクラスとクラス明日を紐づける役割を担う  
　　・GetMapping  
　　　メソッドとGETの処理を行うURLを紐づける役割を担う  
　　
