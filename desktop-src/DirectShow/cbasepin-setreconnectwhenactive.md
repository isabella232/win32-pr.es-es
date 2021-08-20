---
description: El método SetReconnectWhenActive especifica si el pin admite reconexiones dinámicas.
ms.assetid: 64776008-5d1b-461c-a446-8cd6124276c0
title: Método CBasePin.SetReconnectWhenActive (Amfilter.h)
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
ms.openlocfilehash: bf90c32af8371d9f2dd61369e21dfeb0726c7fa044758a3d8fb9beee7fd5743e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118000847"
---
# <a name="cbasepinsetreconnectwhenactive-method"></a>Método CBasePin.SetReconnectWhenActive

El `SetReconnectWhenActive` método especifica si el pin admite reconexiones dinámicas.

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

Valor booleano que especifica si el pin puede volver a conectarse dinámicamente. Si **es TRUE,** el pin puede volver a conectarse dinámicamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

De forma predeterminada, debe detener un filtro antes de volver a conectar cualquiera de sus pines. Si el pin puede volver a conectarse mientras el filtro está activo, llame a este método con un valor **true.** Para obtener más información, vea [Dynamic Graph Building](dynamic-graph-building.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




