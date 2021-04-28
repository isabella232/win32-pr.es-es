---
description: 'Método CBasePin.Active: el método Active notifica al pin que el filtro ahora está activo.'
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: Método CBasePin.Active (Amfilter.h)
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
ms.openlocfilehash: 8ccee76dbf89cf82abcd8d4758305ddec91f1afa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096113"
---
# <a name="cbasepinactive-method"></a>Método CBasePin.Active

El `Active` método notifica al pin que el filtro ahora está activo.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Cuando el filtro pasa de detenido a en pausa, la clase [**CBaseFilter**](cbasefilter.md) llama a este método en todos los pines conectados del filtro.

Este método no hace nada en la clase base. Las clases derivadas pueden invalidar este método; Por ejemplo, un pin podría confirmar asignadores u obtener recursos de hardware.

El estado interno del administrador de gráficos de filtro no se actualiza hasta después de que se devuelva esta función miembro, por lo que no pruebe el estado desde este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




