---
description: La función ConvertToMilliseconds convierte un tiempo de referencia en milisegundos.
ms.assetid: fae3baa4-9344-4197-b375-4abe2656e1b7
title: Función ConvertToMilliseconds (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertToMilliseconds
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e68b84482a437789c620efee7455144905fd33e7b1bdb651df207958ee6befc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073749"
---
# <a name="converttomilliseconds-function"></a>Función ConvertToMilliseconds

La `ConvertToMilliseconds` función convierte un tiempo de referencia en milisegundos.

## <a name="syntax"></a>Sintaxis


```C++
LONGLONG ConvertToMilliseconds(
   const REFERENCE_TIME &RT
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RT* \[ Ref\]
</dt> <dd>

Tiempo de referencia, en unidades de 100 nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el tiempo de referencia convertido en milisegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseReferenceClock (clase)**](cbasereferenceclock.md)
</dt> </dl>

 

 




