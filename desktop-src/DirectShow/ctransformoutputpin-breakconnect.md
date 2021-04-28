---
description: 'Método CTransformOutputPin.BreakConnect: el método BreakConnect libera el pin de una conexión.'
ms.assetid: bf68aca3-93e5-4f9d-9980-1a5eed1513f5
title: Método CTransformOutputPin.BreakConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92854041e1d553945d0a1ab1755ef3557bd4a8b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084963"
---
# <a name="ctransformoutputpinbreakconnect-method"></a>Método CTransformOutputPin.BreakConnect

El `BreakConnect` método libera el pin de una conexión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método invalida el método [**CBaseOutputPin::BreakConnect.**](cbaseoutputpin-breakconnect.md) Llama al método [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) del filtro, que devuelve S \_ OK en la clase base. La clase derivada puede invalidar el **método CTransformFilter::BreakConnect.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




