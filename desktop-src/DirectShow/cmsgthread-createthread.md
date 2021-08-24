---
description: Crea un subproceso.
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: Método CMsgThread.CreateThread (Msgthrd.h)
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
ms.openlocfilehash: 3681716af79d0c47ae08371caa2d03d236b9748d98b08098d7a6834a93ed9b2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831875"
---
# <a name="cmsgthreadcreatethread-method"></a>Método CMsgThread.CreateThread

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
| <dl> <dt>TRUE*"</dt> </dl>  | El subproceso se creó correctamente.<br/>     |
| <dl> <dt>FALSE**</dt> </dl> | El subproceso no se creó correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

El subproceso se recorrerá en bucle, bloqueando hasta que se pone en cola una solicitud (a través de la función miembro [**CMsgThread::P utThreadMsg)**](cmsgthread-putthreadmsg.md) y, a continuación, llamando a la función miembro [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) con cada mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMsgThread (clase)**](cmsgthread.md)
</dt> </dl>

 

 




