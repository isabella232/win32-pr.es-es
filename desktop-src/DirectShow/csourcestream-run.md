---
description: El método Run indica el subproceso de streaming que se ejecutará.
ms.assetid: 9aef7801-dcfb-4597-bccb-5ba19327b2d5
title: Método CSourceStream.Run (Source.h)
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
ms.openlocfilehash: fb7d1d9c86759331127b3db893e05e075d0fffb5988a61935cc28d2e0027ba39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823945"
---
# <a name="csourcestreamrun-method"></a>Método CSourceStream.Run

El `Run` método indica el subproceso de streaming que se ejecutará.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Run();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ UNEXPECTED.

## <a name="remarks"></a>Comentarios

En la clase base, este método tiene el mismo efecto que la [**solicitud CSourceStream::P ause**](csourcestream-pause.md) y no se usa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




