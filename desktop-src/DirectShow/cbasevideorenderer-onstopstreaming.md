---
description: Se llama al método OnStopStreaming al final del streaming para corregir los tiempos del informe de la página de propiedades.
ms.assetid: 92174edb-2f6c-4bad-91c5-769aaebcc495
title: Método CBaseVideoRenderer.OnStopStreaming (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08cf23fd2e1a7e854625d8a369d15290591386fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173790"
---
# <a name="cbasevideorendereronstopstreaming-method"></a>Método CBaseVideoRenderer.OnStopStreaming

Se `OnStopStreaming` llama al método al final del streaming para corregir los tiempos del informe de la página de propiedades.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnStopStreaming();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

Se llama a esta función miembro dos veces, una vez al pausar y de nuevo cuando la secuencia se detiene realmente.

Esta función miembro invalida [**CBaseRenderer::OnStopStreaming.**](cbaserenderer-onstopstreaming.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




