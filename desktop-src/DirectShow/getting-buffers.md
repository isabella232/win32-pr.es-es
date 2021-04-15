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
# <a name="getting-buffers"></a>Obtener búferes

Si el filtro tiene un asignador personalizado que utiliza recursos de filtro, el método [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) del asignador debe contener el bloqueo de streaming, al igual que con otros métodos de streaming:


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Subprocesos y secciones críticas](threads-and-critical-sections.md)
</dt> </dl>

 

 



