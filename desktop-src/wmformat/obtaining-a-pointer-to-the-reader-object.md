---
title: Obtener un puntero al objeto reader (Windows SDK de formato multimedia 11)
description: Obtenga información sobre cómo obtener un puntero al objeto reader del SDK Windows Media Format mediante la interfaz IWMReaderAdvanced2.
ms.assetid: 70696ffc-2612-460d-b445-f200ba85d3c7
keywords:
- Windows SDK de formato multimedia, DirectShow
- Windows SDK de formato multimedia, objetos de lector
- Windows SDK de formato multimedia, interfaz IWMReaderAdvanced2
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Formato de sistemas avanzados (ASF), objetos de lector
- ASF (formato de sistemas avanzados), objetos de lector
- Advanced Systems Format (ASF), interfaz IWMReaderAdvanced2
- ASF (formato de sistemas avanzados), interfaz IWMReaderAdvanced2
- DirectShow,Reader Objects
- DirectShow, punteros a objetos de lector
- DirectShow interfaz IWMReaderAdvanced2
- objetos de lector, obtener punteros
- streams,Reader Objects
- streams,pointers to Reader Objects
- IWMReaderAdvanced2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4b2829e56d08825234dcefdc4fb1012f48c894419e7c328f10afeb76cb6c4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808055"
---
# <a name="obtaining-a-pointer-to-the-reader-object-windows-media-format-11-sdk"></a>Obtener un puntero al objeto reader (Windows SDK de formato multimedia 11)

En algunos casos, por ejemplo, al determinar qué extensiones de unidad de [](reader-object.md) datos se establecen en una secuencia determinada, es posible que tenga que acceder directamente al objeto lector del SDK de Windows Media Format. La función siguiente muestra cómo obtener la [**interfaz IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) en el propio objeto Reader:


```C++
HRESULT GetReaderAdvanced (IGraphBuilder *pGraph, IWMReaderAdvanced2** pReaderAdvanced2) 
{
  // We use CComPtr's to avoid headaches at cleanup time
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
    // Only the WM ASF Reader will have interface. This filter should be
    // the first one returned in this loop.
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



 

 




