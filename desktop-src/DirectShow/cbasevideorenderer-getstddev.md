---
description: El método GetStdDev calcula la desviación estándar en milisegundos entre el momento en que se debe cada fotograma y cuándo se representa realmente, para las estadísticas por fotograma.
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: Método CBaseVideoRenderer.GetStdDev (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.GetStdDev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f7b6ab85000f537179fcc9ae6b979194ae4e975ea2b394d0c58afb8515158aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157087"
---
# <a name="cbasevideorenderergetstddev-method"></a>Método CBaseVideoRenderer.GetStdDev

El método calcula la desviación estándar en milisegundos entre el momento en que se debe cada fotograma y el momento en que se representa realmente, para las `GetStdDev` estadísticas por fotograma.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStdDev(
   int      nSamples,
   int      *piResult,
   LONGLONG llSumSq,
   LONGLONG iTot
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nSamples* 
</dt> <dd>

Valor entero que contiene el número de muestras de vídeo recibidas por el representador de vídeo.

</dd> <dt>

*piResult* 
</dt> <dd>

Puntero a un valor entero que contendrá la desviación estándar.

</dd> <dt>

*llSumSq* 
</dt> <dd>

Valor que representa la desviación estándar, en milisegundos, de todos los ejemplos de vídeo representados. A menor valor, más coherente es la representación.

</dd> <dt>

*iTot* 
</dt> <dd>

Valor que representa el valor medio, en milisegundos, entre la hora de la marca y el tiempo representado para todos los ejemplos de vídeo representados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve NOERROR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




