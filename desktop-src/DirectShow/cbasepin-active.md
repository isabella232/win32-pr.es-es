---
description: El método activo notifica al pin que el filtro está activo ahora.
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: Método CBasePin. Active (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a89c0c75671e6eb29b6ddb260c5f5ec0c385399
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661009"
---
# <a name="cbasepinactive-method"></a>CBasePin. Active (método)

El `Active` método notifica al pin que el filtro está activo ahora.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Cuando el filtro pasa de detenido a en pausa, la clase [**CBaseFilter**](cbasefilter.md) llama a este método en todos los pin conectados del filtro.

Este método no hace nada en la clase base. Las clases derivadas pueden invalidar este método; por ejemplo, un PIN podría confirmar asignadores u obtener recursos de hardware.

El estado interno del administrador de gráficos de filtro no se actualiza hasta que se devuelve esta función miembro, de modo que no se prueba el estado desde este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




