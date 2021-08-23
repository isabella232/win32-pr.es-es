---
description: Obtenga información sobre cómo obtener un puntero al objeto reader del SDK Windows Media Format mediante la interfaz IWMReaderAdvanced2 en DirectShow.
ms.assetid: d1292e2f-bd0e-4961-a6fa-8cdaeb28b692
title: Obtener un puntero al objeto reader (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c1395a9d1c2cb764e8994600845362816ac2c158ca9ab7d8fdf630a1a51ed00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633625"
---
# <a name="obtaining-a-pointer-to-the-reader-object-directshow"></a>Obtener un puntero al objeto reader (DirectShow)

En determinados casos, por ejemplo, al determinar qué extensiones de unidad de datos se establecen en una secuencia determinada, es posible que tenga que acceder directamente al objeto lector del SDK de formato multimedia de Windows. La función siguiente muestra cómo obtener la [**interfaz IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) en el propio objeto reader:


```C++
#include <wmsdk.h>
HRESULT GetReaderAdvanced(IGraphBuilder *pGraph, IWMReaderAdvanced2** pReaderAdvanced2) 
{
  CComPtr<IEnumFilters> pEnum;
  CComPtr<IBaseFilter> pFilter;
  ULONG cFetched;

  HRESULT hr = pGraph->EnumFilters(&pEnum);
  if (FAILED(hr)) 
  {
    return hr;
  }

  while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
  {
    IWMHeaderInfo *pHI = NULL;
    // Only the WM ASF Reader will have interface. 
    hr = pFilter->QueryInterface(__uuidof(IWMHeaderInfo), (void**)&pHI);
    if (SUCCEEDED(hr))
    {
      // We use the IWMDRMReader interface only as a way to get
      // a pointer to the Reader Object.
      CComPtr<IWMDRMReader> pWMDRMReader;
      CComQIPtr<IServiceProvider, &IID_IServiceProvider> pSP;
      hr = pHI->QueryInterface(__uuidof(IServiceProvider), (void**)&pSP);
      if (!pSP)
      {
        return E_NOINTERFACE;
      }
      
      hr = pSP->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader);
      if (FAILED(hr))
      {
        return hr;
      }

      CComQIPtr<IWMReaderAdvanced2, &IID_IWMReaderAdvanced2> pRA2(pWMDRMReader);
      if (pRA2)
      {
        *pReaderAdvanced2 = pRA2.Detach();
        return S_OK;
      }

    }
    pFilter.Release();
  }
  
  //if we get here, we didn't find the WM ASF Reader
  return E_FAIL;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Leer archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
