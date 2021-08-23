---
description: El método IsUsingDefaultSource determina si el representador usa la ventana de origen predeterminada.
ms.assetid: f68d47e7-6602-4321-8e9e-373d354077a1
title: Método CBaseControlVideo.IsUsingDefaultSource (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dce06ffa85b3736eca17f1ecb8303a41afb142fcc8b0d369e1f264a0cf47b2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955214"
---
# <a name="cbasecontrolvideoisusingdefaultsource-method"></a>Método CBaseControlVideo.IsUsingDefaultSource

El `IsUsingDefaultSource` método determina si el representador usa la ventana de origen predeterminada.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT IsUsingDefaultSource() = 0;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el representador usa el origen predeterminado; de lo contrario, devuelve S \_ FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




