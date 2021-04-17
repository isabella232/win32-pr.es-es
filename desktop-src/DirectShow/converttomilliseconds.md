---
description: La función ConvertToMilliseconds convierte una hora de referencia en milisegundos.
ms.assetid: fae3baa4-9344-4197-b375-4abe2656e1b7
title: Función ConvertToMilliseconds (Refclock. h)
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
ms.openlocfilehash: 066f50856824a9bc7b5bbb8c4918c7cbfe5b9da5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670755"
---
# <a name="converttomilliseconds-function"></a>ConvertToMilliseconds función)

La `ConvertToMilliseconds` función convierte una hora de referencia en milisegundos.

## <a name="syntax"></a>Sintaxis


```C++
LONGLONG ConvertToMilliseconds(
   const REFERENCE_TIME &RT
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*RT* \[ CLI\]
</dt> <dd>

Tiempo de referencia, en unidades de 100-nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la hora de referencia convertida en milisegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Refclock. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




