---
description: Consulta si el asignador usa ejemplos de medios de solo lectura.
ms.assetid: 2cb692da-f030-4265-afe4-b1608b51fd47
title: Método CBaseInputPin. IsReadOnly (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.IsReadOnly
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93d1e7930631328a277ce7332f483ee264b2d525
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661012"
---
# <a name="cbaseinputpinisreadonly-method"></a>CBaseInputPin. IsReadOnly (método)

Consulta si el asignador usa ejemplos de medios de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsReadOnly();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de la variable miembro [**CBaseInputPin:: m \_ bReadOnly**](cbaseinputpin-m-breadonly.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




