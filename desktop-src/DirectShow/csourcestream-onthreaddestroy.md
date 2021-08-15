---
description: Se llama al método OnThreadDestroy cuando el subproceso de streaming está a punto de salir.
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: Método CSourceStream.OnThreadDestroy (Source.h)
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
ms.openlocfilehash: b71bd7ff9da79ed42ad7d36ff176a60687ca5fd0edcd6003d77c20084adc1b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953704"
---
# <a name="csourcestreamonthreaddestroy-method"></a>Método CSourceStream.OnThreadDestroy

Se `OnThreadDestroy` llama al método cuando el subproceso de streaming está a punto de salir.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

El procedimiento de subproceso, [**CSourceStream::ThreadProc**](csourcestream-threadproc.md), llama a este método antes de salir. El método no hace nada en la clase base; está disponible para que la clase derivada invalide. Si la clase derivada devuelve un código de error, el subproceso se cierra con un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




