---
description: El método Reply responde a una solicitud.
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: Método CAMThread.Reply (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Reply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e86e0bc0155e527aa11c26531ae5608e6828362
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160244"
---
# <a name="camthreadreply-method"></a>Método CAMThread.Reply

El `Reply` método responde a una solicitud.

## <a name="syntax"></a>Sintaxis


```C++
void Reply(
   DWORD dw
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dw* 
</dt> <dd>

Valor que se devuelve en el [**método CAMThread::CallWorker.**](camthread-callworker.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El método CallWorker se bloquea hasta que se llama a este método. El *parámetro dw* proporciona el valor devuelto para CallWorker. Llame a este método en el procedimiento de subproceso después de recuperar una solicitud para liberar el subproceso solicitante.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




