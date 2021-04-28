---
description: 'Constructor CMsgThread.CMsgThread: método constructor.'
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: Constructor CMsgThread.CMsgThread (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CMsgThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08d76ebecd09d95b7ba0fca22b300c1e402f5302
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095373"
---
# <a name="cmsgthreadcmsgthread-constructor"></a>Constructor CMsgThread.CMsgThread

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CMsgThread();
```



## <a name="parameters"></a>Parámetros

Este constructor no tiene parámetros.

## <a name="remarks"></a>Comentarios

La construcción de un objeto de subproceso de mensaje no crea automáticamente el subproceso. Debe llamar a la [**función miembro CMsgThread::CreateThread**](cmsgthread-createthread.md) para crear el subproceso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMsgThread (clase)**](cmsgthread.md)
</dt> </dl>

 

 




