---
description: Obtención de búferes
ms.assetid: be61aee9-41d5-42bc-b905-d0216d301faf
title: Obtención de búferes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf516096397eca1fce3a023ee4987d8e8feaa4b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061103"
---
# <a name="getting-buffers"></a>Obtención de búferes

Si el filtro tiene un asignador personalizado que usa recursos de filtro, el método [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) del asignador debe contener el bloqueo de streaming, como con otros métodos de streaming:


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

 

 



