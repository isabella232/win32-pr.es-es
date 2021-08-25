---
description: El método DisconnectInternal interrumpe la conexión de pin actual.
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: Método CBasePin.DisconnectInternal (Amfilter.h)
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
ms.openlocfilehash: c420419e49f7093e6fdf1fdc66880035f4844d03277db18b5c134d9ee69b10fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916535"
---
# <a name="cbasepindisconnectinternal-method"></a>Método CBasePin.DisconnectInternal

El `DisconnectInternal` método interrumpe la conexión de pin actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los de la tabla siguiente.



| Código devuelto                                                                                         | Descripción                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>             | El pin no estaba conectado.<br/>                                              |
| <dl> <dt>**S \_ OK**</dt> </dl>                | Correcto.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ NOT \_ STOPPED**</dt> </dl> | El filtro está activo y el pin no admite la reconexión dinámica.<br/> |



 

## <a name="remarks"></a>Comentarios

El [**método CBasePin::D isconnect**](cbasepin-disconnect.md) delega el proceso de desconexión en este método. Este método llama al [**método CBasePin::BreakConnect.**](cbasepin-breakconnect.md) También libera el recuento de referencias en el otro pin, que se mantiene en la variable miembro [**conectado CBasePin::m. \_**](cbasepin-m-connected.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




