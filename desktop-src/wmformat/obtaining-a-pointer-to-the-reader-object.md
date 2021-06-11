---
title: Obtener un puntero al objeto reader (Windows Media Format SDK 11)
description: Obtenga información sobre cómo obtener un puntero al objeto reader del SDK Windows Media Format mediante la interfaz IWMReaderAdvanced2.
ms.assetid: 70696ffc-2612-460d-b445-f200ba85d3c7
keywords:
- Windows Media Format SDK,DirectShow
- Windows Media Format SDK,objetos de lector
- Windows Media Format SDK,IWMReaderAdvanced2 (interfaz)
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados),DirectShow
- Formato de sistemas avanzados (ASF), objetos de lector
- ASF (formato de sistemas avanzados), objetos de lector
- Advanced Systems Format (ASF), interfaz IWMReaderAdvanced2
- ASF (formato de sistemas avanzados), interfaz IWMReaderAdvanced2
- Objetos DirectShow,Reader
- DirectShow, punteros a objetos de lector
- Interfaz DirectShow,IWMReaderAdvanced2
- objetos de lector, obtener punteros
- streams,Reader Objects
- streams,pointers to Reader Objects
- IWMReaderAdvanced2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd31bd868365b87b38eefd0c0c81e8beafef51c
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989140"
---
# <a name="obtaining-a-pointer-to-the-reader-object-windows-media-format-11-sdk"></a><span data-ttu-id="e3b6a-119">Obtener un puntero al objeto reader (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="e3b6a-119">Obtaining a Pointer to the Reader Object (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="e3b6a-120">En determinados casos, por ejemplo, al determinar qué extensiones de unidad de datos se establecen en una secuencia determinada, es posible que tenga que acceder directamente al objeto [reader](reader-object.md) del SDK Windows Media Format datos.</span><span class="sxs-lookup"><span data-stu-id="e3b6a-120">In certain cases, for example when determining which data unit extensions are set on a given stream, you may need to access the [Reader Object](reader-object.md) of the Windows Media Format SDK directly.</span></span> <span data-ttu-id="e3b6a-121">La función siguiente muestra cómo obtener la [**interfaz IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) en el propio objeto Reader:</span><span class="sxs-lookup"><span data-stu-id="e3b6a-121">The following function shows how to obtain the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface on the Reader Object itself:</span></span>


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



 

 




