---
description: El método Create crea el subproceso.
ms.assetid: 453972eb-7cf6-43c6-820e-c1992675260e
title: Método CAMThread.Create (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Create
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 135af6dd12bb53a2fa1e7ec14425c12e1c0bcc99bf9c82ce7aeaccb72df544f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103325"
---
# <a name="camthreadcreate-method"></a>Método CAMThread.Create

El `Create` método crea el subproceso.

## <a name="syntax"></a>Sintaxis


```C++
BOOL Create();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

Este método crea el subproceso mediante el [**método CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) para el procedimiento del subproceso y `this` para el argumento del subproceso.

Se produce un error en el método si el subproceso ya existe.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMThread**](camthread.md)
</dt> </dl>

 

 




