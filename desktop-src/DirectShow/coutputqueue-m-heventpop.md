---
description: Evento opcional que se señala cada vez que el objeto quita un ejemplo de la cola. El valor es inicialmente NULL. Llame al método COutputQueue::SetPopEvent para especificar un identificador de evento.
ms.assetid: f2602532-b045-4384-b87c-b28cc34c81b0
title: Miembro COutputQueue::m_hEventPop (Outputq.h)
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
ms.openlocfilehash: bb401cf9755260c797ebfb382d9f2248d9d04c5f8d9e9b49e319c390de1664c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087215"
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

 

 




