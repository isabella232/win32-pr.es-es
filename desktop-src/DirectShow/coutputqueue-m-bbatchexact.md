---
description: Marca que especifica si el objeto proporciona ejemplos en lotes exactos.
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: 'Miembro COutputQueue:: m_bBatchExact (Outputq. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671343"
---
# <a name="coutputqueuem_bbatchexact-member"></a>Miembro bBatchExact COutputQueue:: m \_

Marca que especifica si el objeto proporciona ejemplos en lotes exactos.

## <a name="syntax"></a>Sintaxis


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a>Observaciones

Si el valor es **true**, el objeto espera hasta que tenga un lote completo de ejemplos de medios antes de entregar cualquiera. De lo contrario, proporciona ejemplos a medida que llegan. La variable miembro [**COutputQueue:: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md) define el tamaño del lote.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




