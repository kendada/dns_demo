# dns_demo
android客户端防DNS劫持      
每次发出api.xxxx.com的请求时，都会先自己请求DNS解析，得到IP，判断IP是否是内置IP    
情况一：DNS拿到的IP是内置IP，直接用，这是绝大部分的情况  
情况二：当DNS拿到的IP不是内置的IP，那就直接用默认IP去访问，并且把全部内置IP、新得到的IP，都增加到测试案例当中，当测试跑完后，
默认IP就是一个最好的IP，如果新IP可用，那原先的逻辑就会直接用新IP，如果新IP不可用，那就会用一个最快的IP。
