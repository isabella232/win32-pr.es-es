---
description: El método PAUSE indica al subproceso de streaming que se active.
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: Método CSourceStream. PAUSE (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6f7cd3b38144edebd98ca655b32bf6092f44269
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680690"
---
# <a name="csourcestreampause-method"></a>CSourceStream. PAUSE (método)

El `Pause` método indica al subproceso de streaming que se active.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto o E \_ inesperados.

## <a name="remarks"></a>Observaciones

El método [**CSourceStream:: Active**](csourcestream-active.md) llama a este método. Cuando el método [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md) recibe esta solicitud, llama al método [**obufferprocessingloop de CSourceStream::D**](csourcestream-dobufferprocessingloop.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




