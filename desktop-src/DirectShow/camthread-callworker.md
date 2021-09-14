---
description: El método CallWorker señala el subproceso con una solicitud.
ms.assetid: 51431688-bf55-4778-afc0-91b6ab336aa3
title: Método CAMThread.CallWorker (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CallWorker
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7410fbee4ece729d1579f525731bddaceded1153
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160269"
---
# <a name="camthreadcallworker-method"></a>Método CAMThread.CallWorker

El `CallWorker` método señala el subproceso con una solicitud.

## <a name="syntax"></a>Sintaxis


```C++
DWORD CallWorker(
   DWORD dwParam
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwParam* 
</dt> <dd>

Parámetro de solicitud. La clase derivada define el significado del parámetro .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor definido por la clase derivada.

## <a name="remarks"></a>Observaciones

Los [**métodos CAMThread::GetRequest**](camthread-getrequest.md) y [**CAMThread::CheckRequest**](camthread-checkrequest.md) recuperan el valor del *parámetro dwParam.* El método GetRequest se bloquea hasta `CallWorker` que se llama a .

Este método se bloquea hasta que se llama al método [**CAMThread::Reply.**](camthread-reply.md) El valor devuelto es el parámetro dado a Reply.

Este método contiene el bloqueo [**DE BLOQUEO DE ACCESO DE SUBPROCESO::m \_**](camthread-m-accesslock.md) para serializar las solicitudes. Por lo tanto, llame a este método desde el propio subproceso o desde cualquier función miembro que se ejecute en el contexto del subproceso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




