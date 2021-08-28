---
description: 'Método CBasePin.Inactive: el método Inactivo notifica al pin que el filtro ya no está activo.'
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: Método CBasePin.Inactive (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8307f3823758eee2f70368e41d3f2dc01333fd538fe2feed30d31b7db876f118
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052745"
---
# <a name="cbasepininactive-method"></a>Método CBasePin.Inactive

El `Inactive` método notifica al pin que el filtro ya no está activo.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Cuando se detiene el filtro, la [**clase CBaseFilter**](cbasefilter.md) llama a este método en todos los pines conectados del filtro.

Este método no hace nada en la clase base. Las clases derivadas deben invalidar este método para liberar los recursos obtenidos por el [**método CBasePin::Active;**](cbasepin-active.md) por ejemplo, para desasignar los asignadores del pin.

El estado interno del administrador de gráficos de filtro no se actualiza hasta después de que este método vuelva, por lo que no pruebe el estado de este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




