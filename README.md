# Unity.Wcf.PerrequestLifetimeManager

Untiy.Wcf is a popular library in .net which allows WCF applications to implement IOC using Unity. This allows a developer to container that can inject dependecies to classes. Unity.Wcf has several lifetime managers to configure the lifetime of objects in the container. The Unity.Wcf library lacks a lifetime manager that expires per request to the service. The PerrequestLifetimeManager was developed to address this issue.

How to install?

Install-Package PerrequestLifetimeManager -Version 1.0.0

How to configure?

Once the library is installed into the project you can add the following lifetime manager when you register dependencies in WCF.

container.RegisterType<InterfaceName, ClassName>(new PerRequestLifetimeManager());

Inaddition to this the package gives you access to lifetime managers implemented by Unity.Wcf