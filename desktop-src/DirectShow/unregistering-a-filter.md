---
description: Anular el registro de un filtro
ms.assetid: 5459d172-7dfe-4786-bcf2-031e441e30a2
title: Anular el registro de un filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e26f2d524ff501fcff1db645c9ccdf1a1c9c80c4056af1af206b996f801207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049685"
---
# <a name="unregistering-a-filter"></a>Anular el registro de un filtro

Para anular el registro de un filtro, implemente **la función DllUnregisterServer.** Dentro de esta función, llame al DirectShow [**función AMovieDllRegisterServer2**](amoviedllregisterserver2.md) con un valor de **FALSE**. Si llamó a **IFilterMapper2::RegisterFilter** al registrar el filtro, llame al método [**IFilterMapper2::UnregisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-unregisterfilter) aquí.

En el ejemplo siguiente se muestra cómo anular el registro de un filtro:


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



 

 



