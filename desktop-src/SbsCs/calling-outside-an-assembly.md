---
description: Llamar fuera de un ensamblado
ms.assetid: 7a59f707-fb89-4899-891f-4cd556b62b26
title: Llamar fuera de un ensamblado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed60536c3daa62957929dd1d3f1a850fd551ae9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652773"
---
# <a name="calling-outside-an-assembly"></a>Llamar fuera de un ensamblado

Los componentes hospedados deben asegurarse de que el contexto de activación correcto está activo cuando se llama fuera del componente. Las llamadas a código externo que se encontró llamando a [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) y, a continuación, a [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), deben llamarse con el mismo contexto que se usó para encontrarla. Las llamadas al código que se encontró fuera de los contextos de activación o a las llamadas de vuelta a la aplicación de hospedaje deben llamarse con el contexto de activación predeterminado de la aplicación.

La compilación con \_ reconocimiento de aislamiento \_ habilitado puede ser útil cuando se llama a fuera de los componentes hospedados. Sin embargo, esto significa que solo las llamadas a las API de Windows están aisladas en el contexto de activación del componente. Esto es suficiente para la mayoría de los casos, ya que las llamadas a funciones de terceros no tienen un contexto activado antes de llamarse. La compilación con \_ reconocimiento de aislamiento \_ habilitado no ayuda si el componente usa varios contextos de activación con varias API de la plataforma.

Para implementar esto, use un activador de contexto de activación como el ejemplo presentado en [aislar componentes](isolating-components.md). Aquí externals. manifest es el conjunto de dependencias fuera de las que se compiló el componente; Quizás contiene una lista ampliable de componentes que se van a cargar y usar durante el tiempo de ejecución. El internalcontext. manifest contiene el conjunto de dependencias que el componente está seguro de usar durante su duración y que se debe establecer en todos los entryPoints desde fuera. Observe que este contexto interno está activado en todos los entryPoints, mientras que el activador de contexto se usa con el ámbito de C++ para que se establezca el contexto adecuado al llamar a los distintos códigos externos que usa este componente.

``` syntax
CActivationContext s_InternalContext;
CActivationContext s_OutboundContext;
CActivationContext s_ExternalContext;

void MyInitializeFunction() 
{
    HANDLE hActCtx;
    ACTCTX actctx = {sizeof(actctx)};

    s_OutboundContext.Set(NULL);

    actctx.lpSource = TEXT("internalcontext.manifest");
    hActCtx = CreateActCtx(&actctx);
    s_InternalActCtx.Set(hActCtx);
    ReleaseActCtx(hActCtx);

    actctx.lpSource = TEXT("externals.manifest");
    hActCtx = CreateActCtx(&actctx);
    s_ExternalContext.Set(hActCtx);
    ReleaseActCtx(hActCtx);
}

void foo() 
{
    // Some code that makes a few calls
    {
        CActCtxActivator CallUnknown(s_OutboundContext);
        pfnUnknownImplementor(...);
    }
    {
        CActCtxActivator CallDependency(s_ExternalContext);
        KnownExternalDependencyPtr->Call();
    }
}

void WINAPI MyEntrypoint() 
{
    CActCtxActivator ContextFirewall(s_InternalContext);
    // Do some work here
    foo();
    // Some more work here
}
```

 

 
