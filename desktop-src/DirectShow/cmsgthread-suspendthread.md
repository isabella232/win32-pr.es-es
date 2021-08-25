---
description: Usa la función SuspendThread de Microsoft Win32 para suspender la operación de un subproceso en ejecución.
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: Método CMsgThread.SuspendThread (Msgthrd.h)
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
ms.openlocfilehash: f5242c8708c07beb85d297dff706dbe192f59f1f7b46b05eba7362c9f0182d52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915745"
---
# <a name="cmsgthreadsuspendthread-method"></a>Método CMsgThread.SuspendThread

Usa la función **SuspendThread** de Microsoft Win32 para suspender el funcionamiento de un subproceso en ejecución.

## <a name="syntax"></a>Sintaxis


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si la función miembro se realiza correctamente, el valor devuelto es el recuento de suspensión anterior del subproceso. Si se produce un error en la función miembro, el valor devuelto es 0xFFFFFFFF. Para obtener información de error extendida, llame a la función **GetLastError** de Microsoft Win32.

## <a name="remarks"></a>Comentarios

El subproceso de cliente llama a esta función miembro para suspender la operación del subproceso de trabajo. El subproceso de trabajo permanece suspendido y no se ejecutará hasta que se realiza una llamada adicional a la función miembro [**CMsgThread::ResumeThread.**](cmsgthread-resumethread.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMsgThread (clase)**](cmsgthread.md)
</dt> </dl>

 

 




