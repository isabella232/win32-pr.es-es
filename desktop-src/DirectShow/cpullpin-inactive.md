---
description: El método inactivo cierra el subproceso de trabajo que extrae datos del pin de salida. Este método también desasigna el asignador.
ms.assetid: 90b91686-b9a8-4196-b559-de924334f11c
title: Método CPullPin.Inactive (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f32084428a36032152d3c3297b1fc9419e51cb3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063310"
---
# <a name="cpullpininactive-method"></a>CPullPin.Inactive (método)

El `Inactive` método cierra el subproceso de trabajo que extrae datos del pin de salida. Este método también desasigna el asignador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Llame a este método cuando el filtro propietario se vuelva inactivo. (Si el pin de entrada deriva de [**CBasePin,**](cbasepin.md)invalide el [**método CBasePin::Inactive).**](cbasepin-inactive.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




