---
description: Las devoluciones de llamada de los componentes hospedados son lo que hace posible el hospedaje. Sin embargo, es posible que el componente que está hospedando haya activado otro contexto de activación que usa para tener acceso a complementos o componentes propios.
ms.assetid: 794a2e2f-ba1f-48ad-a435-244fc7936097
title: Usar devoluciones de llamada de componentes hospedados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef302601985bc7e56a296bc8f494e48e18d785e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154094"
---
# <a name="using-callbacks-from-hosted-components"></a><span data-ttu-id="0a0c3-104">Usar devoluciones de llamada de componentes hospedados</span><span class="sxs-lookup"><span data-stu-id="0a0c3-104">Using Callbacks From Hosted Components</span></span>

<span data-ttu-id="0a0c3-105">Las devoluciones de llamada de los componentes hospedados son lo que hace posible el hospedaje.</span><span class="sxs-lookup"><span data-stu-id="0a0c3-105">Callbacks from hosted components are what make hosting possible.</span></span> <span data-ttu-id="0a0c3-106">Sin embargo, es posible que el componente que está hospedando haya activado otro contexto de activación que usa para tener acceso a complementos o componentes propios.</span><span class="sxs-lookup"><span data-stu-id="0a0c3-106">However, it is possible that the component you are hosting has activated another activation context that it uses to access plug-ins or components of its own.</span></span> <span data-ttu-id="0a0c3-107">En este caso, si el componente hospedado deja un contexto de activación en la pila que hace referencia a su propio objeto COM, la aplicación de hospedaje podría llamar a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un objeto que espera ser su propia implementación y, en su lugar, recibir el objeto del componente hospedado.</span><span class="sxs-lookup"><span data-stu-id="0a0c3-107">In this case, if the hosted component leaves an activation context on the stack that refers to its own COM object, the hosting application might call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get an object that it expects to be its own implementation and instead receive the hosted component's object.</span></span> <span data-ttu-id="0a0c3-108">Para evitar esta herencia de contextos de activación, una buena aplicación de hospedaje debe activar su propio contexto de activación conocido primero durante una devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0a0c3-108">To prevent this inheritance of activation contexts, a good hosting applications should activate its own well-known activation context first during a callback.</span></span>

<span data-ttu-id="0a0c3-109">Considere el ejemplo siguiente que protege el código de la aplicación de hospedaje:</span><span class="sxs-lookup"><span data-stu-id="0a0c3-109">Consider the following example that protects the hosting application's code:</span></span>

``` syntax
HRESULT STDCALL 
CHostingAppFirewall::ITheInterface::FunctWrapper()
{
    ULONG_PTR ulpCookie;
    HRESULT hRes = E_FAIL;
    if (!ActivateActCtx(this->m_hHostingAppContext, &ulpCookie))
        return HRESULT_FROM_WIN32(GetLastError());
    __try 
        {
        hRes = this->m_ITheInterface->Funct();
    } 
        __finally 
        {
        if (!DeactivateActCtx(0, ulpCookie))
            hRes = HRESULT_FROM_WIN32(GetLastError());
    }
    return hRes;
}
```

<span data-ttu-id="0a0c3-110">Esto garantiza que se establece un contexto de activación adecuado antes de pasar la solicitud a alguna implementación interna **de** inactiva.</span><span class="sxs-lookup"><span data-stu-id="0a0c3-110">This ensures that a proper activation context is set before passing the request on to some inner implementation of **Funct**.</span></span> <span data-ttu-id="0a0c3-111">Su propia implementación puede tener la implementación real en línea, pero el método anterior garantiza una interoperabilidad más sencilla simplemente creando contenedores delegados.</span><span class="sxs-lookup"><span data-stu-id="0a0c3-111">Your own implementation can have the actual implementation inline, but the preceding method ensures easier interoperability by just creating delegated wrappers.</span></span> <span data-ttu-id="0a0c3-112">Se recomienda utilizar un método similar al exponer devoluciones de llamada normales (no COM).</span><span class="sxs-lookup"><span data-stu-id="0a0c3-112">It is recommended to use a similar method when exposing normal (non-COM) callbacks.</span></span>

 

 
