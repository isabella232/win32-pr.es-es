---
description: Usa la función ResumeThread de Microsoft Win32 para continuar el funcionamiento del subproceso de trabajo después de una llamada anterior a la función miembro CMsgThread::SuspendThread.
ms.assetid: 5c94a079-5c74-4024-8fb0-71c7ef9c7e73
title: Método CMsgThread.ResumeThread (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ResumeThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed9e2ea546f2c14ceea4f3766db68c1d70ce44ab4dda542315bf7dd30a2d715d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915835"
---
# <a name="cmsgthreadresumethread-method"></a>Método CMsgThread.ResumeThread

Usa la función **ResumeThread** de Microsoft Win32 para continuar el funcionamiento del subproceso de trabajo después de una llamada anterior a la función miembro [**CMsgThread::SuspendThread.**](cmsgthread-suspendthread.md)

## <a name="syntax"></a>Sintaxis


```C++
DWORD ResumeThread();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si la función miembro se realiza correctamente, el valor devuelto es el recuento de suspensión anterior del subproceso. Si se produce un error en la función miembro, el valor devuelto es 0xFFFFFFFF. Para obtener información de error extendida, llame a la función **GetLastError** de Microsoft Win32.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMsgThread (clase)**](cmsgthread.md)
</dt> </dl>

 

 




