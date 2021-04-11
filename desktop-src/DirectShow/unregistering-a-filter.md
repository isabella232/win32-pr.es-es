---
description: Anulación del registro de un filtro
ms.assetid: 5459d172-7dfe-4786-bcf2-031e441e30a2
title: Anulación del registro de un filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d161b7d1f169b84ba43ac734bf01708a37eb700a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911082"
---
# <a name="unregistering-a-filter"></a><span data-ttu-id="d2e10-103">Anulación del registro de un filtro</span><span class="sxs-lookup"><span data-stu-id="d2e10-103">Unregistering a Filter</span></span>

<span data-ttu-id="d2e10-104">Para anular el registro de un filtro, implemente la función **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="d2e10-104">To unregister a filter, implement the **DllUnregisterServer** function.</span></span> <span data-ttu-id="d2e10-105">Dentro de esta función, llame a la función [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) de DirectShow con un valor de **false**.</span><span class="sxs-lookup"><span data-stu-id="d2e10-105">Within this function, call the DirectShow [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function with a value of **FALSE**.</span></span> <span data-ttu-id="d2e10-106">Si llamó a **IFilterMapper2:: RegisterFilter** al registrar el filtro, llame aquí al método [**IFilterMapper2:: UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) .</span><span class="sxs-lookup"><span data-stu-id="d2e10-106">If you called **IFilterMapper2::RegisterFilter** when you registered the filter, call the [**IFilterMapper2::UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) method here.</span></span>

<span data-ttu-id="d2e10-107">En el ejemplo siguiente se muestra cómo anular el registro de un filtro:</span><span class="sxs-lookup"><span data-stu-id="d2e10-107">The following example shows how to unregister a filter:</span></span>


```C++
STDAPI DllUnregisterServer()
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(FALSE);
    if (FAILED(hr))
        return hr;
 
    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->UnregisterFilter(&CLSID_VideoCompressorCategory, 
            g_wszName, CLSID_SomeFilter);

    pFM2->Release();
    return hr;
}
```



 

 



