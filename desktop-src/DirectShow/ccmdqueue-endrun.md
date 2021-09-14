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
ms.openlocfilehash: 367ef026402ff191ceb04657c21d6f3bd11ebe73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973902"
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

## <a name="remarks"></a>Observaciones

La asignación de tiempo entre el tiempo de transmisión y el tiempo de presentación no se conoce después de llamar a esta función miembro. Llame a [**la función miembro CCmdQueue::Run**](ccmdqueue-run.md) para llevar a cabo esta asignación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CCmdQueue (clase)**](ccmdqueue.md)
</dt> </dl>

 

 




