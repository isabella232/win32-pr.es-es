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
ms.openlocfilehash: 57019ee8844f73fdb6cf6e7943e7e22f72d2c98b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246747"
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

 

 




