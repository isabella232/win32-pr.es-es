---
description: Evento opcional que se señala cada vez que el objeto quita un ejemplo de la cola. El valor es inicialmente NULL. Llame al método COutputQueue::SetPopEvent para especificar un identificador de evento.
ms.assetid: f2602532-b045-4384-b87c-b28cc34c81b0
title: COutputQueue::m_hEventPop miembro (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hEventPop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88ab5235a3d4df5b60b53279c444ae99b12fe0c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246740"
---
# <a name="coutputqueuem_heventpop-member"></a>Miembro COutputQueue::m \_ hEventPop

Evento opcional que se señala cada vez que el objeto quita un ejemplo de la cola. El valor es inicialmente **NULL.** Llame al [**método COutputQueue::SetPopEvent**](coutputqueue-setpopevent.md) para especificar un identificador de evento.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE m_hEventPop;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




