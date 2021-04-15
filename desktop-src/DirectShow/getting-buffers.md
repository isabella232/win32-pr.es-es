---
description: Obtener búferes
ms.assetid: be61aee9-41d5-42bc-b905-d0216d301faf
title: Obtener búferes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf516096397eca1fce3a023ee4987d8e8feaa4b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536556"
---
# <a name="getting-buffers"></a><span data-ttu-id="0bd77-103">Obtener búferes</span><span class="sxs-lookup"><span data-stu-id="0bd77-103">Getting Buffers</span></span>

<span data-ttu-id="0bd77-104">Si el filtro tiene un asignador personalizado que utiliza recursos de filtro, el método [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) del asignador debe contener el bloqueo de streaming, al igual que con otros métodos de streaming:</span><span class="sxs-lookup"><span data-stu-id="0bd77-104">If your filter has a custom allocator that uses filter resources, the allocator's [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method should hold the streaming lock, as with other streaming methods:</span></span>


```C++
HRESULT CMyInputAllocator::GetBuffer(
    IMediaSample **ppBuffer,
    REFERENCE_TIME *pStartTime, 
    REFERENCE_TIME *pEndTime,
    DWORD dwFlags)
{
    CAutoLock cObjectLock(&m_csReceive);

    /* Use resources. */

    return CMemAllocator::GetBuffer(ppBuffer, pStartTime, pEndTime, dwFlags);    
}
```



## <a name="related-topics"></a><span data-ttu-id="0bd77-105">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0bd77-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bd77-106">Subprocesos y secciones críticas</span><span class="sxs-lookup"><span data-stu-id="0bd77-106">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



