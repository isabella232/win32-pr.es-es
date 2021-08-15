---
description: El método IsUsingDefaultDestination determina si el representador usa la ventana de destino predeterminada.
ms.assetid: 0b956575-4cf0-4f1f-9223-bb1ec3ae8b10
title: Método CBaseControlVideo.IsUsingDefaultDestination (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultDestination
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf254ec89cc6804af86c98abaaa0c53ae5f76a25766391529ca4de85bee7d084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955224"
---
# <a name="cbasecontrolvideoisusingdefaultdestination-method"></a>Método CBaseControlVideo.IsUsingDefaultDestination

El `IsUsingDefaultDestination` método determina si el representador usa la ventana de destino predeterminada.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT IsUsingDefaultDestination() = 0;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se usa el destino predeterminado; de lo contrario, devuelve S \_ FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




