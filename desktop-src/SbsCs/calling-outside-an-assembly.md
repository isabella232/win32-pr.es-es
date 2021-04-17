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
# <a name="calling-outside-an-assembly"></a><span data-ttu-id="afef7-103">Llamar fuera de un ensamblado</span><span class="sxs-lookup"><span data-stu-id="afef7-103">Calling Outside An Assembly</span></span>

<span data-ttu-id="afef7-104">Los componentes hospedados deben asegurarse de que el contexto de activación correcto está activo cuando se llama fuera del componente.</span><span class="sxs-lookup"><span data-stu-id="afef7-104">Hosted components should ensure that the correct activation context is active when calling outside the component.</span></span> <span data-ttu-id="afef7-105">Las llamadas a código externo que se encontró llamando a [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) y, a continuación, a [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), deben llamarse con el mismo contexto que se usó para encontrarla.</span><span class="sxs-lookup"><span data-stu-id="afef7-105">Calls into outside code that was found by calling [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) and then [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), should be called with the same context that was used to find it.</span></span> <span data-ttu-id="afef7-106">Las llamadas al código que se encontró fuera de los contextos de activación o a las llamadas de vuelta a la aplicación de hospedaje deben llamarse con el contexto de activación predeterminado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="afef7-106">Calls into code that was found outside of activation contexts, or calls back into the hosting application should be called with the application default activation context.</span></span>

<span data-ttu-id="afef7-107">La compilación con \_ reconocimiento de aislamiento \_ habilitado puede ser útil cuando se llama a fuera de los componentes hospedados.</span><span class="sxs-lookup"><span data-stu-id="afef7-107">Compiling with ISOLATION\_AWARE\_ENABLED defined may be useful when calling outside of hosted components.</span></span> <span data-ttu-id="afef7-108">Sin embargo, esto significa que solo las llamadas a las API de Windows están aisladas en el contexto de activación del componente.</span><span class="sxs-lookup"><span data-stu-id="afef7-108">However this means that only calls to Windows APIs are isolated to the component's activation context.</span></span> <span data-ttu-id="afef7-109">Esto es suficiente para la mayoría de los casos, ya que las llamadas a funciones de terceros no tienen un contexto activado antes de llamarse.</span><span class="sxs-lookup"><span data-stu-id="afef7-109">This is sufficient for most cases because calls to third-party functions do not have a context activated before being called.</span></span> <span data-ttu-id="afef7-110">La compilación con \_ reconocimiento de aislamiento \_ habilitado no ayuda si el componente usa varios contextos de activación con varias API de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="afef7-110">Compiling with ISOLATION\_AWARE\_ENABLED defined does not help if your component uses several activation contexts with various platform APIs.</span></span>

<span data-ttu-id="afef7-111">Para implementar esto, use un activador de contexto de activación como el ejemplo presentado en [aislar componentes](isolating-components.md).</span><span class="sxs-lookup"><span data-stu-id="afef7-111">To implement this, use an activation context activator like the example presented in [Isolating Components](isolating-components.md).</span></span> <span data-ttu-id="afef7-112">Aquí externals. manifest es el conjunto de dependencias fuera de las que se compiló el componente; Quizás contiene una lista ampliable de componentes que se van a cargar y usar durante el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="afef7-112">Here externals.manifest is the set of dependencies outside those the component was built with; perhaps it contains some extendable list of components that are to be loaded and used during runtime.</span></span> <span data-ttu-id="afef7-113">El internalcontext. manifest contiene el conjunto de dependencias que el componente está seguro de usar durante su duración y que se debe establecer en todos los entryPoints desde fuera.</span><span class="sxs-lookup"><span data-stu-id="afef7-113">The internalcontext.manifest contains the set of dependencies that the component is sure to use during its lifetime, and which should be set in all entrypoints from the outside.</span></span> <span data-ttu-id="afef7-114">Observe que este contexto interno está activado en todos los entryPoints, mientras que el activador de contexto se usa con el ámbito de C++ para que se establezca el contexto adecuado al llamar a los distintos códigos externos que usa este componente.</span><span class="sxs-lookup"><span data-stu-id="afef7-114">Notice that this internal context is activated in all entrypoints, while the context activator is used with C++ scoping so that the proper context is set when calling out to the various outside code that this component uses.</span></span>

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

 

 
