---
description: El método Run indica al subproceso de streaming que se ejecute.
ms.assetid: 9aef7801-dcfb-4597-bccb-5ba19327b2d5
title: Método CSourceStream. Run (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39093654677ab4828f8a1d5a01a8cf7deaf42507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681012"
---
# <a name="csourcestreamrun-method"></a>CSourceStream. Run (método)

El `Run` método indica al subproceso de streaming que se ejecute.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Run();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto o E \_ inesperados.

## <a name="remarks"></a>Observaciones

En la clase base, este método tiene el mismo efecto que la solicitud [**CSourceStream::P ause**](csourcestream-pause.md) , y no se utiliza.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




