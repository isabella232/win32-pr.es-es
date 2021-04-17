---
description: El método DeliverEndFlush solicita que el PIN de entrada conectado finalice una operación de vaciado.
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: Método CDynamicOutputPin. DeliverEndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2666681dcd5637a8e919ced2c61d6536663d7b30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660185"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a>CDynamicOutputPin. DeliverEndFlush, método

El `DeliverEndFlush` método solicita el PIN de entrada conectado para finalizar una operación de vaciado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto si se realiza correctamente o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBaseOutputPin::D eliverendflush**](cbaseoutputpin-deliverendflush.md) . Restablece el evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




