---
description: Se bloquea hasta que el subproceso se cierra.
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: Método CMsgThread. WaitForThreadExit (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.WaitForThreadExit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b48573c4297a2d5d5d008eba88fd8ea437333c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671219"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a>CMsgThread. WaitForThreadExit, método

Se bloquea hasta que el subproceso se cierra.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WaitForThreadExit(
   LPDWORD lpdwExitCode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpdwExitCode* 
</dt> <dd>

Puntero al código de salida devuelto por el subproceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** o **false**, cuyo significado viene determinado por la clase que proporciona la función miembro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) reemplazada y la función miembro que realiza la llamada.

## <a name="remarks"></a>Observaciones

Asegúrese de que el subproceso de trabajo se ha cerrado completamente antes de completar la destrucción de la clase derivada. de lo contrario, es posible que el subproceso se siga ejecutando después de que se haya descargado la biblioteca de vínculos dinámicos (DLL) del espacio de direcciones del proceso. Incluso si la única instrucción que se deja de salir es una instrucción de devolución única, se produciría una excepción. La única manera confiable de asegurarse de que el subproceso ha salido es indicar al subproceso que salga (mediante un objeto [**CMsg**](cmsg.md) negociado de forma privada enviado a la función miembro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ) y, a continuación, llamar a esta función miembro. Debe hacerlo en el destructor de la clase derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




