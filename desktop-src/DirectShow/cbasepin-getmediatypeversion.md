---
description: El método GetMediaTypeVersion recupera un número de versión para el conjunto de tipos de medios preferidos.
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: Método CBasePin.GetMediaTypeVersion (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f1b50b16a099c8698bbf5bef270173334f1c3ac2c3d2d67ff87778cffddf2ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955194"
---
# <a name="cbasepingetmediatypeversion-method"></a>Método CBasePin.GetMediaTypeVersion

El `GetMediaTypeVersion` método recupera un número de versión para el conjunto de tipos de medios preferidos.

## <a name="syntax"></a>Sintaxis


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la [**variable miembro CBasePin::m \_ TypeVersion.**](cbasepin-m-typeversion.md)

## <a name="remarks"></a>Comentarios

El constructor **CBasePin** inicializa el número de versión en 1. En la clase base, este número nunca cambia. Si el pin cambia dinámicamente su lista de tipos de medios preferidos, debe incrementar el número de versión cada vez que cambie la lista. Para incrementar el número de versión, llame al [**método CBasePin::IncrementTypeVersion.**](cbasepin-incrementtypeversion.md)

El enumerador de tipo de medio, que implementa la clase [**CEnumMediaTypes,**](cenummediatypes.md) usa el número de versión para mantenerse sincronizado con el pin.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




