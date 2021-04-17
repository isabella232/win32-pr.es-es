---
description: El método DisconnectInternal interrumpe la conexión del PIN actual.
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: Método CBasePin. DisconnectInternal (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisconnectInternal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0891a9446e09c56e3845c02217d39037aad38bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660793"
---
# <a name="cbasepindisconnectinternal-method"></a>CBasePin. DisconnectInternal, método

El `DisconnectInternal` método interrumpe la conexión del PIN actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los de la tabla siguiente.



| Código devuelto                                                                                         | Descripción                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>             | El PIN no estaba conectado.<br/>                                              |
| <dl> <dt>**S \_ correcto**</dt> </dl>                | Correcto.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ no \_ detenido**</dt> </dl> | El filtro está activo y el PIN no admite la reconexión dinámica.<br/> |



 

## <a name="remarks"></a>Observaciones

El método [**CBasePin::D Ulta**](cbasepin-disconnect.md) delega el proceso de desconexión a este método. Este método llama al método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) . También libera el recuento de referencias en el otro PIN, que está contenido en la variable de miembro [**\_ conectada CBasePin:: m**](cbasepin-m-connected.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




