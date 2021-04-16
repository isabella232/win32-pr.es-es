---
description: El método BreakConnect libera el PIN de una conexión.
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: Método CBasePin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8964ea76e48e4753f42923663ab45962cd672e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671635"
---
# <a name="cbasepinbreakconnect-method"></a>CBasePin. BreakConnect, método

El `BreakConnect` método libera el PIN de una conexión.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Se llama a este método durante la desconexión del PIN por el método [**CBasePin::D Ulta**](cbasepin-disconnect.md) . También se llama durante un intento de conexión si se produce un error en el método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) .

Este método debe liberar los recursos obtenidos por el método **CheckConnect** . Por ejemplo, si **CheckConnect** asigna memoria, `BreakConnect` debe liberar la memoria. Si **CheckConnect** consulta el PIN de conexión de una interfaz, `BreakConnect` debe liberar la interfaz.

Tenga en cuenta que `BreakConnect` se puede llamar a sin una llamada correspondiente a **CompleteConnect**. Por lo tanto, no puede suponer que se ha llamado previamente a **CompleteConnect** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




