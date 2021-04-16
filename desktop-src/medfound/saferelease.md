---
description: SafeRelease
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: SafeRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0661b8515c1d8a79c81eef19f49cf8996fcbf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715500"
---
# <a name="saferelease"></a><span data-ttu-id="8142d-103">SafeRelease</span><span class="sxs-lookup"><span data-stu-id="8142d-103">SafeRelease</span></span>


<span data-ttu-id="8142d-104">Muchos de los ejemplos de código de esta documentación usan la siguiente función para liberar punteros de interfaz COM.</span><span class="sxs-lookup"><span data-stu-id="8142d-104">Many of the code examples in this documentation use the following function to release COM interface pointers.</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



> [!Note]  
> <span data-ttu-id="8142d-105">Esta función no está definida en un encabezado de SDK.</span><span class="sxs-lookup"><span data-stu-id="8142d-105">This function is not defined in an SDK header.</span></span> <span data-ttu-id="8142d-106">Para usar esta función, debe definirla en su propio código.</span><span class="sxs-lookup"><span data-stu-id="8142d-106">To use this function, you must define it in your own code.</span></span>

 

<span data-ttu-id="8142d-107">Esta función libera el puntero *ppT* y lo establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="8142d-107">This function releases the pointer *ppT* and sets it equal to **NULL**.</span></span>

<span data-ttu-id="8142d-108">Otra opción es usar una clase de puntero inteligente, como **CComPtr**, que se define en el Active Template Library (ATL).</span><span class="sxs-lookup"><span data-stu-id="8142d-108">Another option is to use a smart pointer class, such as **CComPtr**, which is defined in the Active Template Library (ATL).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8142d-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8142d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8142d-110">Acerca de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8142d-110">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="8142d-111">**IUnknown:: Release**</span><span class="sxs-lookup"><span data-stu-id="8142d-111">**IUnknown::Release**</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
