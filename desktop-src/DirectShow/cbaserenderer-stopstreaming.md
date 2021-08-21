---
description: El método StopStreaming detiene el streaming cuando el filtro sale del estado en ejecución.
ms.assetid: 465dde15-adec-46da-b8c8-56743e0cbd29
title: Método CBaseRenderer.StopStreaming (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 097ad9fd1548b709f7eb74a3e468c34c3b18a73621720e249a3c626c252c898d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016803"
---
# <a name="cbaserendererstopstreaming-method"></a>Método CBaseRenderer.StopStreaming

El `StopStreaming` método detiene el streaming cuando el filtro sale del estado en ejecución.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Este método llama al [**método CBaseRenderer::OnStopStreaming.**](cbaserenderer-onstopstreaming.md) Ese método no hace nada en la clase base, pero la clase derivada puede invalidarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




