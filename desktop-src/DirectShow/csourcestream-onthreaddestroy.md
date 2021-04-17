---
description: Se llama al método OnThreadDestroy cuando el subproceso de streaming está a punto de salir.
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: CSourceStream. OnThreadDestroy (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadDestroy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e7377ce11955d7121a33311d390464e042b98f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660901"
---
# <a name="csourcestreamonthreaddestroy-method"></a>CSourceStream. OnThreadDestroy, método

`OnThreadDestroy`Se llama al método cuando el subproceso de streaming está a punto de salir.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

El procedimiento de subproceso, [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md), llama a este método antes de salir. El método no hace nada en la clase base; está disponible para que la clase derivada se invalide. Si la clase derivada devuelve un código de error, el subproceso se cierra con un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




