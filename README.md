# java

http://bbs.csdn.net/topics/391909962

1. 说出Servlet的生命周期，并说出Servlet和CGI的区别。
   Servlet被服务器实例化后，容器运行其init方法，请求到达时运行其service方法，service方法自动派遣运行与请求对应的doXXX方法（doGet，doPost）等，当服务器决定将实例销毁的时候调用其destroy方法。与cgi的区别在于servlet处于服务器进程中，它通过多线程方式运行其service方法，一个实例可以服务于多个请求，并且其实例一般不会销毁，而CGI对每个请求都产生新的进程，服务完成后就销毁，所以效率上低于servlet
2. getAttribute和getParameter的区别
  1.getAttribute是取得jsp中 用setAttribute設定的attribute 
  2.parameter得到的是string；attribute得到的是object 
  3.request.getParameter()方法传递的数据，会从Web客户端传到Web服务器端，代表HTTP请求数据；request.setAttribute()和getAttribute()方法传递的数据只会存在于Web容器内部，在具有转发关系的Web组件之间共享。即request.getAttribute()方法返回request范围内存在的对象，而request.getParameter()方法是获取http提交过来的数据。
