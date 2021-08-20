---
description: El método GetRequest espera la siguiente solicitud de subproceso.
ms.assetid: 2938374b-174f-4276-98a2-20a084bd9bbd
title: Método CSourceStream.GetRequest (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e28a8e57535a49903cd2a7b23fb0d0d179bf910b20225042c65b3bdcda620f51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073209"
---
# <a name="csourcestreamgetrequest-method"></a>Método CSourceStream.GetRequest

El `GetRequest` método espera la siguiente solicitud de subproceso.

## <a name="syntax"></a>Sintaxis


```C++
Command GetRequest();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la siguiente solicitud de subproceso.

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CAMThread::GetRequest.**](camthread-getrequest.md) El valor devuelto se convierte al siguiente tipo enumerado:


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Source.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceStream (clase)**](csourcestream.md)
</dt> </dl>

 

 




