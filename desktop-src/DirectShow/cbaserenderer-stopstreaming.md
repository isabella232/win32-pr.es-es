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
ms.openlocfilehash: dfd943de6a53383d7505fa9e884dcc152da6e5f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061757"
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

## <a name="remarks"></a>Observaciones

Este método llama al [**método CBaseRenderer::OnStopStreaming.**](cbaserenderer-onstopstreaming.md) Ese método no hace nada en la clase base, pero la clase derivada puede invalidarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




