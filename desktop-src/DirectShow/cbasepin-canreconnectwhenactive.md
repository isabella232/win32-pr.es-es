---
description: El método CanReconnectWhenActive consulta si el pin admite reconexiones dinámicas.
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: Método CBasePin.CanReconnectWhenActive (Amfilter.h)
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
ms.openlocfilehash: ffe4cc09efa53ac4d3ab8089a1061d860206f9734c214d250b5c3cdc907eaf84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916925"
---
# <a name="cbasepincanreconnectwhenactive-method"></a>CBasePin.CanReconnectWhenActive (método)

El `CanReconnectWhenActive` método consulta si el pin admite reconexiones dinámicas.

## <a name="syntax"></a>Sintaxis


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que especifica si el pin puede volver a conectarse dinámicamente. Si **es TRUE,** el pin puede volver a conectarse dinámicamente.

## <a name="remarks"></a>Comentarios

De forma predeterminada, debe detener un filtro antes de volver a conectar cualquiera de sus pines. Sin embargo, si un pin admite la reconexión dinámica, puede volver a conectarse mientras el filtro está activo. Para obtener más información, vea [Dynamic Graph Building](dynamic-graph-building.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




