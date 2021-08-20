---
description: El método OnStartStreaming restablece todas las veces que controla el streaming.
ms.assetid: a2bb07f2-6880-4030-96c5-d146982dfe66
title: Método CBaseVideoRenderer.OnStartStreaming (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2a55d509c900c7be68d3225826c208755d31ef66e0c24119bd1d044dad1aefc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157060"
---
# <a name="cbasevideorendereronstartstreaming-method"></a>Método CBaseVideoRenderer.OnStartStreaming

El `OnStartStreaming` método restablece todas las veces que controla el streaming.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnStartStreaming();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Esta función miembro invalida [**CBaseRenderer::OnStartStreaming**](cbaserenderer-onstartstreaming.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




