---
description: Recupera el identificador del subproceso.
ms.assetid: c2b25342-841a-46cb-862c-01761fc60363
title: Método CMsgThread.GetThreadID (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3b0837a7f050f09794b06e490f45012e0704e187b02668cd2af2a5bf8edf34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119214105"
---
# <a name="cmsgthreadgetthreadid-method"></a>Método CMsgThread.GetThreadID

Recupera el identificador del subproceso.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetThreadID();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el **miembro de datos privado m \_ ThreadId.**

## <a name="remarks"></a>Comentarios

Esta función devuelve el identificador de Microsoft Win32 para el subproceso de trabajo. Puede llamar a esta función miembro en el subproceso de trabajo o en un subproceso de cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Msgthrd.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMsgThread (clase)**](cmsgthread.md)
</dt> </dl>

 

 




