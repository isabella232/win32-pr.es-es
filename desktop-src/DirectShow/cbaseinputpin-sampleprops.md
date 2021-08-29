---
description: El método SampleProps recupera las propiedades del ejemplo más reciente, en una estructura \_ PROPIEDADES DE AM \_ SAMPLE2.
ms.assetid: d4c98c35-f8b2-4111-bae9-4e0f58a0cc8a
title: Método CBaseInputPin.SampleProps (Amfilter.h)
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
ms.openlocfilehash: 9b654063cc448c8f8e87dcd57442d36b2ed2b2cf2d3135d0ab987c01ff1a7569
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983655"
---
# <a name="cbaseinputpinsampleprops-method"></a>Método CBaseInputPin.SampleProps

El método recupera las propiedades del ejemplo más `SampleProps` reciente, en una [**estructura PROPIEDADES DE AM \_ SAMPLE2. \_**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)

## <a name="syntax"></a>Sintaxis


```C++
AM_SAMPLE2_PROPERTIES* SampleProps();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la dirección de la variable [**miembro CBaseInputPin::m \_ SampleProps.**](cbaseinputpin-m-sampleprops.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseInputPin (clase)**](cbaseinputpin.md)
</dt> </dl>

 

 




