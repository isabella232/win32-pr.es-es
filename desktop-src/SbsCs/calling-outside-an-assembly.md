---
description: Llamar fuera de un ensamblado
ms.assetid: 7a59f707-fb89-4899-891f-4cd556b62b26
title: Llamar fuera de un ensamblado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed60536c3daa62957929dd1d3f1a850fd551ae9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271700"
---
# <a name="calling-outside-an-assembly"></a>Llamar fuera de un ensamblado

Los componentes hospedados deben asegurarse de que el contexto de activación correcto está activo al llamar fuera del componente. Las llamadas a código externo que se encontraron mediante una llamada a [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) y, a continuación, [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), se deben llamar con el mismo contexto que se usó para encontrarlo. Se debe llamar a las llamadas al código que se encontró fuera de los contextos de activación o a las llamadas a la aplicación de hospedaje con el contexto de activación predeterminado de la aplicación.

La compilación con ISOLATION \_ AWARE ENABLED definido puede ser útil al llamar fuera de los componentes \_ hospedados. Sin embargo, esto significa que solo las llamadas a Windows API están aisladas en el contexto de activación del componente. Esto es suficiente para la mayoría de los casos porque las llamadas a funciones de terceros no tienen un contexto activado antes de llamarse. Compilar con ISOLATION AWARE ENABLED definido no ayuda si el componente usa varios contextos de \_ activación con varias API de \_ plataforma.

Para implementar esto, use un activador de contexto de activación como el ejemplo presentado en [Aislar componentes](isolating-components.md). Aquí externals.manifest es el conjunto de dependencias fuera de aquellos con los que se comcreó el componente; quizás contenga una lista extensible de componentes que se van a cargar y usar durante el tiempo de ejecución. Internalcontext.manifest contiene el conjunto de dependencias que el componente está seguro de usar durante su vigencia y que se deben establecer en todos los puntos de entrada desde fuera. Tenga en cuenta que este contexto interno se activa en todos los puntos de entrada, mientras que el activador de contexto se usa con el ámbito de C++ para que se establezca el contexto adecuado al llamar a los distintos códigos externos que usa este componente.

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

 

 
