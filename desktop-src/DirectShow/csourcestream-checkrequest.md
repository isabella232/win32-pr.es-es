---
description: El método CheckRequest comprueba si hay una solicitud de subproceso, sin bloquear.
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: Método CSourceStream.CheckRequest (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3100d449d2f29b2080541c5968cad6abc5643b26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072241"
---
# <a name="csourcestreamcheckrequest-method"></a>Método CSourceStream.CheckRequest

El `CheckRequest` método comprueba si hay una solicitud de subproceso, sin bloquear.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CheckRequest(
   Command *pCom
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCom* 
</dt> <dd>

Puntero a una variable que recibe el valor pasado en la última llamada al [**método CAMThread::CallWorker.**](camthread-callworker.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si hay una solicitud pendiente o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CAMThread::CheckRequest**](camthread-checkrequest.md) para realizar la comprobación de tipos. La **clase CSourceStream** define el siguiente tipo enumerado para el *parámetro pCom:*


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




