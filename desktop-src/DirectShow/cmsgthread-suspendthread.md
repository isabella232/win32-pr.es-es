---
description: Usa la función SuspendThread de Microsoft Win32 para suspender el funcionamiento de un subproceso en ejecución.
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: Método CMsgThread. SuspendThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SuspendThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69190015104d712864965e757d82afbdcc852884
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671724"
---
# <a name="cmsgthreadsuspendthread-method"></a>CMsgThread. SuspendThread, método

Usa la función **SuspendThread** de Microsoft Win32 para suspender el funcionamiento de un subproceso en ejecución.

## <a name="syntax"></a>Sintaxis


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si la función miembro se ejecuta correctamente, el valor devuelto es el recuento de suspensión anterior del subproceso. Si se produce un error en la función miembro, el valor devuelto es 0xFFFFFFFF. Para obtener información de error extendida, llame a la función **GetLastError** de Microsoft Win32.

## <a name="remarks"></a>Observaciones

El subproceso de cliente llama a esta función miembro para suspender la operación del subproceso de trabajo. El subproceso de trabajo permanece suspendido y no se ejecutará hasta que se realice una llamada adicional a la función miembro [**CMsgThread:: ResumeThread**](cmsgthread-resumethread.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




