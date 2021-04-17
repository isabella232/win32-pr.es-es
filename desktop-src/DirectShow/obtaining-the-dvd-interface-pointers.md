---
description: Obtener los punteros de interfaz de DVD
ms.assetid: 3d9315fc-dcfb-483a-9437-55c440813dc2
title: Obtener los punteros de interfaz de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24825b2d24ffae70e3def131e8aa522a987c11d0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686312"
---
# <a name="obtaining-the-dvd-interface-pointers"></a><span data-ttu-id="ff5fe-103">Obtener los punteros de interfaz de DVD</span><span class="sxs-lookup"><span data-stu-id="ff5fe-103">Obtaining the DVD Interface Pointers</span></span>

<span data-ttu-id="ff5fe-104">Una vez creado el gráfico de filtros, la aplicación puede obtener los punteros que necesita para controlar el navegador de DVD, el administrador de gráficos de filtro y la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ff5fe-104">After the filter graph is built, your application can obtain the pointers it needs to control the DVD Navigator, the Filter Graph Manager, and the video window.</span></span> <span data-ttu-id="ff5fe-105">En el ejemplo de código siguiente se muestran los pasos básicos, con comprobación de errores y otro código que se ha dejado por simplicidad.</span><span class="sxs-lookup"><span data-stu-id="ff5fe-105">The basic steps, with error-checking and other code left out for simplicity, are illustrated in the following code example.</span></span> <span data-ttu-id="ff5fe-106">El código completo se encuentra en la aplicación de ejemplo de DVD en el método CDvdCore:: BuildGraph.</span><span class="sxs-lookup"><span data-stu-id="ff5fe-106">The complete code is found in the DVD Sample application in the CDvdCore::BuildGraph method.</span></span> <span data-ttu-id="ff5fe-107">(Para obtener más información, vea [ejemplos de DirectShow](directshow-samples.md)).</span><span class="sxs-lookup"><span data-stu-id="ff5fe-107">(For more information, see [DirectShow Samples](directshow-samples.md).)</span></span>


```C++
// Create an instance of the DVD Graph Builder object.
HRESULT hr;
hr = CoCreateInstance(CLSID_DvdGraphBuilder,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IDvdGraphBuilder,
                          reinterpret_cast<void**>(&m_pIDvdGB));

// Build the DVD filter graph.
AM_DVD_RENDERSTATUS buildStatus;
hr = m_pIDvdGB->RenderDvdVideoVolume(pszwDiscPath, m_dwRenderFlags, &buildStatus);

// Get the pointers to the DVD Navigator interfaces.
hr = m_pIDvdGB->GetDvdInterface(IID_IDvdInfo2, reinterpret_cast<void**>(&m_pIDvdI2));
hr = m_pIDvdGB->GetDvdInterface(IID_IDvdControl2, reinterpret_cast<void**>(&m_pIDvdC2));
   ...    
// Get a pointer to the filter graph manager.
hr = m_pDvdGB->GetFiltergraph(&m_pGraph);
...   
// Use the graph pointer to get a pointer to IMediaControl,
// for controlling the filter graph as a whole.
hr = m_pGraph->QueryInterface(IID_IMediaControl, reinterpret_cast<void**>(&m_pIMC));
...   
// Get a pointer to IMediaEventEx,
// used for handling DVD and other filter graph events.
hr = m_pGraph->QueryInterface(IID_IMediaEventEx, reinterpret_cast<void**>(&m_pME)); 
...                
// Use the graph builder pointer again to get the IVideoWindow interface,
// to set the window style and message-handling behavior of the video renderer filter.
hr = m_pIDvdGB->GetDvdInterface(IID_IVideoWindow, reinterpret_cast<void**>(&m_pIVW));
  
hr = m_pDvdGB->GetDvdInterface(IID_IAMLine21Decoder, reinterpret_cast<void**>(&pL21Dec));
```



## <a name="related-topics"></a><span data-ttu-id="ff5fe-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff5fe-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff5fe-109">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="ff5fe-109">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



