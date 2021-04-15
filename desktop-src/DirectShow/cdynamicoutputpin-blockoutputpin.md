---
description: El método BlockOutputPin bloquea el código PIN.
ms.assetid: 49f6b8da-a8b2-482d-b70d-2c68a1b45a10
title: Método CDynamicOutputPin. BlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.BlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3998774550363b7d22e05ca491f1d76ba7f2ff2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661359"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a>CDynamicOutputPin. BlockOutputPin, método

El `BlockOutputPin` método bloquea el código PIN. Mientras se bloquea el PIN, el método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) espera a que el PIN se desbloquee. El estado bloqueado impide que la clavija de salida entregue ejemplos, cambie su formato de salida o vuelva a conectarse a sí mismo.

## <a name="syntax"></a>Sintaxis


```C++
void BlockOutputPin();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, conserve la sección crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) . No llame a este método si un subproceso de streaming está utilizando el PIN, ya sea para proporcionar datos o para cambiar la conexión. Para comprobar si un subproceso de streaming está utilizando el PIN, llame al método [**CDynamicOutputPin:: StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




