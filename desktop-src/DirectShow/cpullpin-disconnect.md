---
description: El método Disconnect interrumpe la conexión con el PIN de salida.
ms.assetid: 6e362e32-7b74-4392-b46f-1ab47a30a07b
title: Método CPullPin. disconnect (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec13a7f29a06bab4f79ddb58932796f8363adadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671391"
---
# <a name="cpullpindisconnect-method"></a>CPullPin. disconnect (método)

El `Disconnect` método interrumpe la conexión con el PIN de salida.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Este método interrumpe cualquier conexión realizada en el método [**CPullPin:: Connect**](cpullpin-connect.md) . Llame a este método dentro del método [**IPin::D Ulta**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) . (Si el código PIN deriva de [**CBasePin**](cbasepin.md), invalide [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) para llamar a este método).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPullPin**](cpullpin.md)
</dt> </dl>

 

 




