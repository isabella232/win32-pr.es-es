---
description: El método SetTimeAdvise configura un evento de temporizador con el reloj de referencia.
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: Método CCmdQueue.SetTimeAdvise (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetTimeAdvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecfa02354ad3662a6fd9060fff80b74635c63ade57539fbbd1307fa1d65e8872
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757135"
---
# <a name="ccmdqueuesettimeadvise-method"></a>Método CCmdQueue.SetTimeAdvise

El `SetTimeAdvise` método configura un evento de temporizador con el reloj de referencia.

## <a name="syntax"></a>Sintaxis


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta función miembro llama al [**método IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) para configurar una notificación la primera vez necesaria en la cola. Los comandos en tiempo de presentación que se aplazan siempre se comprueban. Si el gráfico de filtros está en modo de ejecución, también se comprueban los comandos diferidos que usan el tiempo de transmisión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CCmdQueue (clase)**](ccmdqueue.md)
</dt> </dl>

 

 




