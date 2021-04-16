---
description: Se llama al método OnThreadStartPlay al principio del método CSourceStream::D oBufferProcessingLoop.
ms.assetid: 16d3b28f-bfae-49af-b8e4-8cc8cb15ecab
title: CSourceStream. OnThreadStartPlay (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadStartPlay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857f27ad39fb9169e1ef67253d5232c7cbc3dbb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690592"
---
# <a name="csourcestreamonthreadstartplay-method"></a>CSourceStream. OnThreadStartPlay, método

`OnThreadStartPlay`Se llama al método al principio del método [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT OnThreadStartPlay();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Este método no hace nada en la clase base; está disponible para que la clase derivada se invalide.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




