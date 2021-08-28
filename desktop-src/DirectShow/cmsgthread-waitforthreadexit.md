---
description: Se bloquea hasta que se cierra el subproceso.
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: Método CMsgThread.WaitForThreadExit (Msgthrd.h)
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
ms.openlocfilehash: de9861a1c7cae3055be288c4624b9e0b98c7b719e1534c1841ddb17770d91cf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915715"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a>Método CMsgThread.WaitForThreadExit

Se bloquea hasta que se cierra el subproceso.

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

Devuelve **TRUE o** **FALSE**, cuyo significado viene determinado por la clase que proporciona la función miembro [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) invalidada y la función miembro que realiza la llamada.

## <a name="remarks"></a>Comentarios

Asegúrese de que el subproceso de trabajo ha salido completamente antes de completar la destrucción de la clase derivada. De lo contrario, es posible que el subproceso todavía se ejecute después de que la biblioteca de vínculos dinámicos (DLL) se haya descargado del espacio de direcciones del proceso. Incluso si la única instrucción que queda por salir es una instrucción de un solo retorno, se produciría una excepción. La única manera confiable de asegurarse de que el subproceso ha salido es indicar al subproceso que salga (mediante un objeto [**CMsg**](cmsg.md) negociado de forma privada enviado a la función miembro [**CMsgThread::P utThreadMsg)**](cmsgthread-putthreadmsg.md) y, a continuación, llamar a esta función miembro. Debe hacerlo en el destructor de la clase derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMsgThread (clase)**](cmsgthread.md)
</dt> </dl>

 

 




