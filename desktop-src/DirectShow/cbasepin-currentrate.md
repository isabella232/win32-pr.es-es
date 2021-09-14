---
description: El método CurrentRate recupera la velocidad de segmento, establecida por el método CBasePin::NewSegment.
ms.assetid: 19780dd2-2dcf-4e5d-8a70-a46be05e040c
title: Método CBasePin.CurrentRate (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: adffcc02aad4c5516a8e92c247e47b7dbf389d73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061364"
---
# <a name="cbasepincurrentrate-method"></a>Método CBasePin.CurrentRate

El `CurrentRate` método recupera la velocidad de segmento, establecida por el método [**CBasePin::NewSegment.**](cbasepin-newsegment.md)

## <a name="syntax"></a>Sintaxis


```C++
double CurrentRate();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de [**CBasePin::m \_ dRate**](cbasepin-m-drate.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




