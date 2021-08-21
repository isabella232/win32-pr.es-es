---
description: Marca para invalidar el procesamiento por lotes. Al establecer esta marca en TRUE, se invalida la marca COutputQueue::m \_ bBatchExact y se entregan todos los ejemplos pendientes.
ms.assetid: 95ea6973-65c0-40c9-be22-c2a20a60b459
title: COutputQueue::m_bSendAnyway miembro (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSendAnyway
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5c01ec87fb8e1d9b33fd88806b0d2798e2b13e76eea2ec47b4e1766a7e10201f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954154"
---
# <a name="coutputqueuem_bsendanyway-member"></a>Miembro COutputQueue::m \_ bSendAnyway

Marca para invalidar el procesamiento por lotes. Al establecer esta marca en **TRUE,** se invalida la marca [**COutputQueue::m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) y se entregan todos los ejemplos pendientes.

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_bSendAnyway;
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

 

 




