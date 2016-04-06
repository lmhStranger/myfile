### Spring-aop-proxy 源码分析
主要的类是 ProxyFactory,其中构造方法

    public ProxyFactory(Class proxyInterface,Interceptor interceptor){
        addInterface(proxyInterface);
        addAdvice(interceptor);
    }
该构造方法通过指定要代理的接口以及请求处理的拦截器来创建一个代理工厂类，然后通过该类的getProxy（）方法来得到具体的代理类。
> 通常的代码写法为
>> new ProxyFactory(proxyInterface,interceptor).getProxy();

这样就得到了代理类，所有通过该类的请求都会委托到interceptor的invoke方法。

    public Object getProxy() {
		return createAopProxy().getProxy();
	}
上面的方法我们能看到其实是先创建了一个aopProxy
