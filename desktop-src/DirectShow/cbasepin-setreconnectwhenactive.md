---
description: El método SetReconnectWhenActive especifica si el PIN admite reconexiones dinámicas.
ms.assetid: 64776008-5d1b-461c-a446-8cd6124276c0
title: Método CBasePin. SetReconnectWhenActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10840ad60c858f69164b19f2460a0039cd332700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670345"
---
# <a name="cbasepinsetreconnectwhenactive-method"></a>CBasePin. SetReconnectWhenActive, método

El `SetReconnectWhenActive` método especifica si el PIN admite reconexiones dinámicas.

## <a name="syntax"></a>Sintaxis


```C++
void SetReconnectWhenActive(
   bool bCanReconnect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bCanReconnect* 
</dt> <dd>

Valor booleano que especifica si el pin puede volver a conectarse dinámicamente. Si **es true**, el PIN se puede volver a conectar dinámicamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

De forma predeterminada, debe detener un filtro antes de volver a conectar cualquiera de sus clavijas. Si el PIN se puede volver a conectar mientras el filtro está activo, llame a este método con un valor de **true**. Para obtener más información, vea [creación de gráficos dinámicos](dynamic-graph-building.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




