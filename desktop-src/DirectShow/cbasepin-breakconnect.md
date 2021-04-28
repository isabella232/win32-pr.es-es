---
description: 'Método CBasePin.BreakConnect: el método BreakConnect libera el pin de una conexión.'
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: Método CBasePin.BreakConnect (Amfilter.h)
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
ms.openlocfilehash: a9a099b1001c2b8c30398ca350e05d15562a8bc2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099443"
---
# <a name="cbasepinbreakconnect-method"></a>Método CBasePin.BreakConnect

El `BreakConnect` método libera el pin de una conexión.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

El método [**CBasePin::D isconnect**](cbasepin-disconnect.md) llama a este método durante la desconexión del pin. También se llama durante un intento de conexión si se produce un error en el método [**CBasePin::CheckConnect.**](cbasepin-checkconnect.md)

Este método debe liberar los recursos obtenidos por el **método CheckConnect.** Por ejemplo, si **CheckConnect** asigna memoria, `BreakConnect` debe liberar la memoria. Si **CheckConnect** consulta el pin de conexión de una interfaz, `BreakConnect` debe liberar la interfaz.

Tenga en `BreakConnect` cuenta que se puede llamar a sin una llamada correspondiente a **CompleteConnect.** Por lo tanto, no puede suponer que se ha llamado a **CompleteConnect** anteriormente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




