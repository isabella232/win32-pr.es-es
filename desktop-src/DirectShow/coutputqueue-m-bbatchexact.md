---
description: Marca que especifica si el objeto entrega muestras en lotes exactos.
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: COutputQueue::m_bBatchExact miembro (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bBatchExact
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5f38d8a0e7335025688f52015ff9ed4d4892820
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246753"
---
# <a name="coutputqueuem_bbatchexact-member"></a>Miembro COutputQueue::m \_ bBatchExact

Marca que especifica si el objeto entrega muestras en lotes exactos.

## <a name="syntax"></a>Sintaxis


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a>Observaciones

Si el valor es **TRUE**, el objeto espera hasta que tenga un lote completo de ejemplos multimedia antes de entregar cualquiera. De lo contrario, entrega ejemplos a medida que llegan. La variable [**miembro COutputQueue::m \_ lBatchSize**](coutputqueue-m-lbatchsize.md) define el tamaño del lote.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COutputQueue (clase)**](coutputqueue.md)
</dt> </dl>

 

 




