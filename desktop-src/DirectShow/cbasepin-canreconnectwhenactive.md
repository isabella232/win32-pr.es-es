---
description: El método CanReconnectWhenActive consulta si el PIN admite reconexiones dinámicas.
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: Método CBasePin. CanReconnectWhenActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CanReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89a072a26afe0087ce9adfed5b29eb1cc4280dac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671344"
---
# <a name="cbasepincanreconnectwhenactive-method"></a>CBasePin. CanReconnectWhenActive, método

El `CanReconnectWhenActive` método consulta si el PIN admite reconexiones dinámicas.

## <a name="syntax"></a>Sintaxis


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que especifica si el pin puede volver a conectarse dinámicamente. Si **es true**, el PIN se puede volver a conectar dinámicamente.

## <a name="remarks"></a>Observaciones

De forma predeterminada, debe detener un filtro antes de volver a conectar cualquiera de sus clavijas. Sin embargo, si un PIN admite la reconexión dinámica, se puede volver a conectar mientras el filtro está activo. Para obtener más información, vea [creación de gráficos dinámicos](dynamic-graph-building.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




