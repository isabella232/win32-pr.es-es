---
description: El método Inactivo cierra el subproceso de trabajo que extrae datos del pin de salida. Este método también desasigna el asignador.
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
ms.openlocfilehash: 56307362651761dbe2bc5c0242a24f189cf14d1e820df6a5ba21bdeb9c7deb0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565375"
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

## <a name="remarks"></a>Comentarios

Llame a este método cuando el filtro propietario se vuelva inactivo. (Si el pin de entrada deriva de [**CBasePin,**](cbasepin.md)invalide el [**método CBasePin::Inactive).**](cbasepin-inactive.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPullPin (clase)**](cpullpin.md)
</dt> </dl>

 

 




