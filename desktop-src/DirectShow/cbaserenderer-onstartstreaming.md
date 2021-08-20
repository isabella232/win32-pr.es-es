---
description: Se llama al método OnStartStreaming cuando el filtro comienza a transmitirse.
ms.assetid: 02a5b334-f6c4-4cba-8882-c6b36d97feb3
title: Método CBaseRenderer.OnStartStreaming (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b0f050222b0ca6a88c7cf1d9348597e4d7b68f2a2ed431b4f6843afe97efd5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157678"
---
# <a name="cbaserendereronstartstreaming-method"></a>Método CBaseRenderer.OnStartStreaming

Se `OnStartStreaming` llama al método cuando el filtro comienza la transmisión por secuencias.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT OnStartStreaming();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

El [**método CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) llama a este método. No hace nada en la clase base, pero la clase derivada puede invalidarla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




