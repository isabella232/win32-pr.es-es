---
description: El método StartStreaming inicia el streaming cuando el filtro cambia a un estado de ejecución.
ms.assetid: 198e9c1b-be69-4ba6-aa67-9f24ed080ab6
title: Método CBaseRenderer. StartStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf1fcb1cbfb651221296054493688b2d9f33bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671670"
---
# <a name="cbaserendererstartstreaming-method"></a>CBaseRenderer. StartStreaming, método

El `StartStreaming` método inicia la transmisión por secuencias cuando el filtro cambia a un estado de ejecución.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Si el filtro tiene un ejemplo, programa el ejemplo para su representación. De lo contrario, si hay una notificación de final de secuencia pendiente, el filtro envía un evento [**EC \_ Complete**](ec-complete.md) al administrador de gráficos de filtro.

Este método llama al método [**CBaseRenderer:: OnStartStreaming**](cbaserenderer-onstartstreaming.md) . Ese método no hace nada en la clase base, pero la clase derivada puede invalidarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




