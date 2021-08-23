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
ms.openlocfilehash: 38e1e3fef83bab4d598cfd36294c5c405c1eca938372b43f12a6401c4be3c46b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586045"
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

## <a name="remarks"></a>Comentarios

Se llama a esta función miembro dos veces, una vez al pausar y otra vez cuando la secuencia se detiene realmente.

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

 

 




