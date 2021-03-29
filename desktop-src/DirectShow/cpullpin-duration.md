---
description: El método Duration recupera la duración de la secuencia.
ms.assetid: 82fbd7f5-36dc-4e81-9ce5-9ee28adf73ef
title: Método CPullPin. Duration (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecd05478f67934368aa6d1de84ae32a209ddcad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680835"
---
# <a name="cpullpinduration-method"></a>CPullPin. Duration (método)

El `Duration` método recupera la duración de la secuencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Duration(
   REFERENCE_TIME *ptDuration
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ptDuration* 
</dt> <dd>

Puntero a una variable que recibe la duración, en bytes multiplicada por 10 millones.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

La duración es indeterminada hasta que se llama al método [**CPullPin:: Connect**](cpullpin-connect.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPullPin**](cpullpin.md)
</dt> </dl>

 

 




