---
description: El método IsEndOfStream consulta si se ha recibido la notificación de final de secuencia.
ms.assetid: 44f9b740-ff7d-4387-9c2c-a5b6b90f3295
title: Método CBaseRenderer. IsEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e07afb4dfb10e38d90184ba5747f200d1bc716d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660434"
---
# <a name="cbaserendererisendofstream-method"></a>CBaseRenderer. IsEndOfStream, método

El `IsEndOfStream` método consulta si se ha recibido la notificación de final de secuencia.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsEndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la marca [**CBaseRenderer:: m \_ bEOS**](cbaserenderer-m-beos.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




