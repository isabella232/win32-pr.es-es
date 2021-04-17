---
description: El método BreakConnect libera el PIN de una conexión.
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: Método CTransformInputPin. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2274b71b67a54ecacb291d77d2eef4ad8a110fa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661244"
---
# <a name="ctransforminputpinbreakconnect-method"></a>CTransformInputPin. BreakConnect, método

El `BreakConnect` método libera el PIN de una conexión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBaseInputPin:: BreakConnect**](cbaseinputpin-breakconnect.md) . Llama al método [**CTransformFilter:: BreakConnect**](ctransformfilter-breakconnect.md) del filtro, que devuelve s \_ OK en la clase base. La clase derivada puede invalidar el método **CTransformFilter:: BreakConnect** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




