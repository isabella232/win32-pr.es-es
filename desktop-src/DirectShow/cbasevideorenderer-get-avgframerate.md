---
description: El método \_ get AvgFrameRate calcula y recupera la velocidad media de fotogramas lograda.
ms.assetid: f36fc020-8c1a-491f-9f55-18265fde8bf8
title: CBaseVideoRenderer.get_AvgFrameRate método (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgFrameRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79aab0677cfd5cba5f6a889519e0c12ed2236d8f82eca28b3fa7b227b941b2b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658788"
---
# <a name="cbasevideorendererget_avgframerate-method"></a>Método CBaseVideoRenderer.get \_ AvgFrameRate

El `get_AvgFrameRate` método calcula y recupera la velocidad media de fotogramas lograda.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_AvgFrameRate(
   int *piAvgFrameRate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*piAvgFrameRate* 
</dt> <dd>

Puntero al número de fotogramas por segundo desde que comenzó el streaming.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el [**método IQualProp::get \_ AvgFrameRate.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




