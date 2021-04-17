---
description: El operador asigna una nueva hora de referencia y usa el parámetro ' RT [Ref] '.
ms.assetid: e3a005c0-95d5-41e0-80bb-e70399a50dca
title: COARefTime. Operator = Method (Ctlutil. h)-RT [Ref] parámetro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bad1e0d7ee63fe9bcfa7fc1664a7349e787d9927
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105678861"
---
# <a name="coareftimeoperator-method-ctlutilh---rt-ref-parameter"></a>COARefTime. Operator = Method (Ctlutil. h)-RT [Ref] parámetro

Este operador asigna una nueva hora de referencia.

## <a name="syntax"></a>Sintaxis


```C++
COARefTime& operator=(
  [ref] const REFERENCE_TIME &rt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RT* \[ CLI\]
</dt> <dd>

Referencia a un valor de [**\_ tiempo de referencia**](reference-time.md) que especifica el nuevo tiempo de referencia en unidades de 100-nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una referencia al objeto.

## <a name="requirements"></a>Requisitos

| Requisito                    | Value                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado  | Ctlutil. h (incluir streams. h)                                                                                   |
| Biblioteca | Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COARefTime**](coareftime.md)
</dt> </dl>

 

 




