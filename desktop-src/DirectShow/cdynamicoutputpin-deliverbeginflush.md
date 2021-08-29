---
description: 'Método CDynamicOutputPin.DeliverBeginFlush: el método DeliverBeginFlush solicita el pin de entrada conectado para iniciar una operación de vaciado.'
ms.assetid: eafc3835-7696-480b-abc8-154938e19b15
title: Método CDynamicOutputPin.DeliverBeginFlush (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06b7486fa8fbacb4f2d048da198a78aa763e9beabc1991b2ddd178b9a55781b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055945"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a>Método CDynamicOutputPin.DeliverBeginFlush

El `DeliverBeginFlush` método solicita el pin de entrada conectado para iniciar una operación de vaciado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CBaseOutputPin::D eliverBeginFlush.**](cbaseoutputpin-deliverbeginflush.md) Establece el evento [**CDynamicOutputPin::m \_ hStopEvent.**](cdynamicoutputpin-m-hstopevent.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




