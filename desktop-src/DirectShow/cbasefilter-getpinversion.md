---
description: El método GetPinVersion recupera un número de versión para el conjunto de PIN de este filtro.
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: Método CBaseFilter. GetPinVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8cb2e67f88ef7a02958cc851dd9b8c0c751096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661085"
---
# <a name="cbasefiltergetpinversion-method"></a>CBaseFilter. GetPinVersion, método

El `GetPinVersion` método recupera un número de versión para el conjunto de PIN de este filtro.

## <a name="syntax"></a>Sintaxis


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la variable miembro [**CBaseFilter:: m \_ PinVersion**](cbasefilter-m-pinversion.md) .

## <a name="remarks"></a>Observaciones

El constructor **CBaseFilter** inicializa la versión del PIN en 1. En la clase base, este número nunca cambia. Si el filtro crea o destruye dinámicamente los pin, debe incrementar la versión del PIN cada vez que cambien los pin. Para incrementar el número de versión, llame al método [**CBaseFilter:: IncrementPinVersion**](cbasefilter-incrementpinversion.md) .

El objeto de enumerador de PIN, implementado por la clase [**CEnumPins**](cenumpins.md) , usa la versión del PIN para mantener la sincronización con el filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




