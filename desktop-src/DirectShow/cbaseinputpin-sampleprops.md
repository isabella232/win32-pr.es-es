---
description: El método SampleProps recupera las propiedades del ejemplo más reciente, en una \_ estructura de propiedades AM SAMPLE2 \_ .
ms.assetid: d4c98c35-f8b2-4111-bae9-4e0f58a0cc8a
title: Método CBaseInputPin. SampleProps (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.SampleProps
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45663cfd221c7a31abe5f85a494869b24d1ddd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661302"
---
# <a name="cbaseinputpinsampleprops-method"></a>CBaseInputPin. SampleProps, método

El `SampleProps` método recupera las propiedades del ejemplo más reciente, en una estructura de [**\_ \_ propiedades AM SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

## <a name="syntax"></a>Sintaxis


```C++
AM_SAMPLE2_PROPERTIES* SampleProps();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la dirección de la variable miembro [**CBaseInputPin:: m \_ SampleProps**](cbaseinputpin-m-sampleprops.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




