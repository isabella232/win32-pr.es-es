---
description: El método reply responde a una solicitud.
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: Método CAMThread. reply (Wxutil. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690868"
---
# <a name="camthreadreply-method"></a>CAMThread. reply (método)

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

Valor que se va a devolver en el método [**CAMThread:: CallWorker**](camthread-callworker.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El método CallWorker se bloquea hasta que se llama a este método. El parámetro *DW* proporciona el valor devuelto para CallWorker. Llame a este método en el procedimiento del subproceso después de recuperar una solicitud, para liberar el subproceso que lo solicita.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CAMThread**](camthread.md)
</dt> </dl>

 

 




