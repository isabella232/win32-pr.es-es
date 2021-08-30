---
description: El método get Jitter recupera la desviación estándar del tiempo en milisegundos entre cada fotograma y el siguiente para todos los fotogramas desde que se inició \_ el streaming.
ms.assetid: 629e725e-7dee-4824-8f79-cd3335f4901b
title: CBaseVideoRenderer.get_Jitter método (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_Jitter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ac86cb74267c508a1f0f266455955e486d3686548202d2a524ee4a49288793e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052285"
---
# <a name="cbasevideorendererget_jitter-method"></a>Método CBaseVideoRenderer.get \_ Jitter

El método recupera la desviación estándar del tiempo en milisegundos entre cada fotograma y el siguiente para todos los fotogramas desde que se `get_Jitter` inició el streaming.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Jitter(
   int *piJitter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*piJitter* 
</dt> <dd>

Puntero a la desviación estándar del tiempo de interframe, en milisegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Esta función miembro implementa el [**método IQualProp::get \_ Jitter.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




