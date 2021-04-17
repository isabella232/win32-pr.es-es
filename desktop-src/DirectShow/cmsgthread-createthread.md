---
description: Crea un subproceso.
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: Método CMsgThread. CreateThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CreateThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8951995de18158fe4d1e5f84b1d98da701067ab6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670989"
---
# <a name="cmsgthreadcreatethread-method"></a>CMsgThread. CreateThread (método)

Crea un subproceso.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CreateThread();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                              | Descripción                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>TRUE * * * *</dt> </dl>  | El subproceso se ha creado correctamente.<br/>     |
| <dl> <dt>FALSE * * * *</dt> </dl> | El subproceso no se creó correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

El subproceso creará un bucle, se bloqueará hasta que una solicitud se pone en cola (a través de la función miembro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ) y, a continuación, llama a la función miembro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) con cada mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




