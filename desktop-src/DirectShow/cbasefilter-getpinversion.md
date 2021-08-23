---
description: El método GetPinVersion recupera un número de versión para el conjunto de pines de este filtro.
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: Método CBaseFilter.GetPinVersion (Amfilter.h)
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
ms.openlocfilehash: a40890ce40e75ebea9f7dd10edb78572eb865ea5f94cd1ec674c082d6df8c631
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640465"
---
# <a name="cbasefiltergetpinversion-method"></a>Método CBaseFilter.GetPinVersion

El `GetPinVersion` método recupera un número de versión para el conjunto de pines de este filtro.

## <a name="syntax"></a>Sintaxis


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la [**variable miembro CBaseFilter::m \_ PinVersion.**](cbasefilter-m-pinversion.md)

## <a name="remarks"></a>Comentarios

El **constructor CBaseFilter** inicializa la versión del pin en 1. En la clase base, este número nunca cambia. Si el filtro crea o destruye de forma dinámica los pins, debe incrementar la versión del pin cada vez que cambien. Para incrementar el número de versión, llame al [**método CBaseFilter::IncrementPinVersion.**](cbasefilter-incrementpinversion.md)

El objeto de enumerador de pin, que implementa la clase [**CEnumPins,**](cenumpins.md) usa la versión de pin para mantenerse sincronizado con el filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




