---
description: 'Método CDynamicOutputPin.DeliverEndFlush: el método DeliverEndFlush solicita el pin de entrada conectado para finalizar una operación de vaciado.'
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: Método CDynamicOutputPin.DeliverEndFlush (Amfilter.h)
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
ms.openlocfilehash: 4cdd7e26b0c08b154c6cffd08066e8ae841a6aa849db4751ffa0cdf252848719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055955"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a>Método CDynamicOutputPin.DeliverEndFlush

El `DeliverEndFlush` método solicita el pin de entrada conectado para finalizar una operación de vaciado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CBaseOutputPin::D eliverEndFlush.**](cbaseoutputpin-deliverendflush.md) Restablece el evento [**CDynamicOutputPin::m \_ hStopEvent.**](cdynamicoutputpin-m-hstopevent.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




