# BinderTF.NET
Dockerfile to use TensorFlow in Jupiter Notebooks.

This dockerfile is based in [Try .NET](<https://github.com/dotnet/try>)'s dockerfile, more precisely in Scott Hanselman's [Dashboard for NightScout](<https://github.com/shanselman/NightscoutDashboard>)

It adds the Tensorflow library install:

```
# Install TF libraries
RUN wget https://storage.googleapis.com/tensorflow/libtensorflow/libtensorflow-cpu-linux-x86_64-1.14.0.tar.gz
RUN tar -C /usr/local -xzf libtensorflow-cpu-linux-x86_64-1.14.0.tar.gz
RUN rm libtensorflow-cpu-linux-x86_64-1.14.0.tar.gz
RUN ldconfig
```

And with that, in the notebooks, you can install the [Scisharp Tensorflow bindings](<https://github.com/SciSharp/TensorFlow.NET>):

```
#r "nuget: TensorFlow.NET, 0.12.0"
```

And start playing!!!

Here's the link to test with it with Binder:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/javiercp/BinderTF.NET/master?urlpath=lab)

## Useful links
- https://github.com/dotnet/try
- https://github.com/shanselman/NightscoutDashboard
- https://github.com/SciSharp
- https://github.com/SciSharp/TensorFlow.NET
- https://github.com/SciSharp/SciSharpCube