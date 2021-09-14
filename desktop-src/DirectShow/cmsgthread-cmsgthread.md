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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361366"
---
# <a name="cmsgthreadcmsgthread-constructor"></a>Constructor CMsgThread.CMsgThread

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CMsgThread();
```



## <a name="parameters"></a>Parámetros

Este constructor no tiene parámetros.

## <a name="remarks"></a>Observaciones

La construcción de un objeto de subproceso de mensaje no crea automáticamente el subproceso. Debe llamar a la [**función miembro CMsgThread::CreateThread**](cmsgthread-createthread.md) para crear el subproceso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMsgThread (clase)**](cmsgthread.md)
</dt> </dl>

 

 




