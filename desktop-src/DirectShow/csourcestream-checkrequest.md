---
description: El método CheckRequest comprueba si hay una solicitud de subproceso, sin bloqueos.
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: CSourceStream. CheckRequest (método) (Source. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690508"
---
# <a name="csourcestreamcheckrequest-method"></a>CSourceStream. CheckRequest, método

El `CheckRequest` método comprueba si hay una solicitud de subproceso, sin bloqueos.

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

Puntero a una variable que recibe el valor pasado en la última llamada al método [**CAMThread:: CallWorker**](camthread-callworker.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si hay una solicitud pendiente o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CAMThread:: CheckRequest**](camthread-checkrequest.md) para realizar la comprobación de tipos. La clase **CSourceStream** define el siguiente tipo enumerado para el parámetro *pCom* :


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




