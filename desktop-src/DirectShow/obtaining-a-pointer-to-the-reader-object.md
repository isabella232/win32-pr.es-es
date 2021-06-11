---
description: Obtenga información sobre cómo obtener un puntero al objeto reader del SDK de Windows Media Format mediante la interfaz IWMReaderAdvanced2 en DirectShow.
ms.assetid: d1292e2f-bd0e-4961-a6fa-8cdaeb28b692
title: Obtener un puntero al objeto Reader (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e131b9e111aa5e779d1208b68e04c9979e3b1d7f
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989111"
---
# <a name="obtaining-a-pointer-to-the-reader-object-directshow"></a><span data-ttu-id="e9b83-103">Obtener un puntero al objeto Reader (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="e9b83-103">Obtaining a Pointer to the Reader Object (DirectShow)</span></span>

<span data-ttu-id="e9b83-104">En algunos casos, por ejemplo, al determinar qué extensiones de unidad de datos se establecen en una secuencia determinada, es posible que tenga que acceder directamente al objeto lector del SDK Windows Media Format datos.</span><span class="sxs-lookup"><span data-stu-id="e9b83-104">In certain cases, for example when determining which data unit extensions are set on a given stream, you may need to access the Reader Object of the Windows Media Format SDK directly.</span></span> <span data-ttu-id="e9b83-105">La función siguiente muestra cómo obtener la [**interfaz IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) en el propio objeto Reader:</span><span class="sxs-lookup"><span data-stu-id="e9b83-105">The following function shows how to obtain the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface on the Reader Object itself:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e9b83-106">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e9b83-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9b83-107">Lectura de archivos ASF en DirectShow</span><span class="sxs-lookup"><span data-stu-id="e9b83-107">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
