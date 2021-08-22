---
description: El método EndRun cambia al modo detenido o en pausa.
ms.assetid: 2c41262c-a809-4f3b-898c-02c0891dc6f8
title: Método CCmdQueue.EndRun (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.EndRun
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c5a20917c82ba26c941b063941e8667a3a30adce15176aed52362140a15ce90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757365"
---
# <a name="ccmdqueueendrun-method"></a>Método CCmdQueue.EndRun

El `EndRun` método cambia al modo detenido o en pausa.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT EndRun();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT** que depende de la implementación.

## <a name="remarks"></a>Comentarios

La asignación de tiempo entre el tiempo de transmisión y el tiempo de presentación no se conoce después de llamar a esta función miembro. Llame a [**la función miembro CCmdQueue::Run**](ccmdqueue-run.md) para llevar a cabo esta asignación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CCmdQueue (clase)**](ccmdqueue.md)
</dt> </dl>

 

 




