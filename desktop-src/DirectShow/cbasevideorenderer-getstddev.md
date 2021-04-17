---
description: El método GetStdDev calcula la desviación estándar en milisegundos entre el momento en que vence cada fotograma y el momento en que se representa, para las estadísticas por fotograma.
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: Método CBaseVideoRenderer. GetStdDev (Renbase. h)
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
ms.openlocfilehash: 85b40bda4715a8201cd05109b59746630c54654c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660379"
---
# <a name="cbasevideorenderergetstddev-method"></a>CBaseVideoRenderer. GetStdDev, método

El `GetStdDev` método calcula la desviación estándar en milisegundos entre el momento en que vence cada fotograma y el momento en que se representa, para las estadísticas por fotograma.

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

Valor que representa la desviación estándar, en milisegundos, de todos los ejemplos de vídeo representados. Cuanto menor sea el valor, más coherente será la representación.

</dd> <dt>

*iTot* 
</dt> <dd>

Valor que representa el valor medio, en milisegundos, entre el tiempo marcado y el tiempo de representación de todos los ejemplos de vídeo representados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve NoError.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




