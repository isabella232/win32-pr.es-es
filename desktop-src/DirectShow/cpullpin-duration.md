---
description: El método Duration recupera la duración de la secuencia.
ms.assetid: 82fbd7f5-36dc-4e81-9ce5-9ee28adf73ef
title: Método CPullPin.Duration (Pullpin.h)
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
ms.openlocfilehash: fdc944400bc80fbd5228ac06e2ba1c01f7315305071f7a24c0b38eb125ee1399
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767985"
---
# <a name="cpullpinduration-method"></a>Método CPullPin.Duration

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

Puntero a una variable que recibe la duración, en bytes multiplicado por 10 000 000.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

La duración es indeterminada hasta que se llama al [**método CPullPin::Conectar.**](cpullpin-connect.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




