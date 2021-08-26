---
description: El método BlockOutputPin bloquea el pin.
ms.assetid: 49f6b8da-a8b2-482d-b70d-2c68a1b45a10
title: Método CDynamicOutputPin.BlockOutputPin (Amfilter.h)
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
ms.openlocfilehash: 9dc1f4cdafd732821398ee04e127c0525798dd6cc02f67f8af5d977b195a6a74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983365"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a>Método CDynamicOutputPin.BlockOutputPin

El `BlockOutputPin` método bloquea el pin. Mientras se bloquea el pin, el método [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) espera a que el pin se desbloquee. El estado bloqueado impide que el pin de salida entregue ejemplos, cambie su formato de salida o vuelva a conectarse.

## <a name="syntax"></a>Sintaxis


```C++
void BlockOutputPin();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Antes de llamar a este método, mantenga [**la sección crítica CDynamicOutputPin::m \_ BlockStateLock.**](cdynamicoutputpin-m-blockstatelock.md) No llame a este método si un subproceso de streaming usa el pin, ya sea para entregar datos o para cambiar la conexión. Para comprobar si un subproceso de streaming usa el pin, llame al método [**CDynamicOutputPin::StreamingThreadUsingOutputPin.**](cdynamicoutputpin-streamingthreadusingoutputpin.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




