---
description: El método GetMediaTypeVersion recupera un número de versión para el conjunto de tipos de medios preferidos.
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: Método CBasePin. GetMediaTypeVersion (Amfilter. h)
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
ms.openlocfilehash: fe01d33d7a7c1cb65bc0e2391af63e3519d9cce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661383"
---
# <a name="cbasepingetmediatypeversion-method"></a>CBasePin. GetMediaTypeVersion, método

El `GetMediaTypeVersion` método recupera un número de versión para el conjunto de tipos de medios preferidos.

## <a name="syntax"></a>Sintaxis


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la variable miembro [**CBasePin:: m \_ TypeVersion**](cbasepin-m-typeversion.md) .

## <a name="remarks"></a>Observaciones

El constructor **CBasePin** inicializa el número de versión en 1. En la clase base, este número nunca cambia. Si el PIN cambia dinámicamente su lista de tipos de medios preferidos, debe incrementar el número de versión cada vez que cambie la lista. Para incrementar el número de versión, llame al método [**CBasePin:: IncrementTypeVersion**](cbasepin-incrementtypeversion.md) .

El enumerador de tipo de medio, que se implementa mediante la clase [**CEnumMediaTypes**](cenummediatypes.md) , usa el número de versión para mantenerlo sincronizado con el PIN.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




