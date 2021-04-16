---
description: El método SetTimeAdvise configura un evento de temporizador con el reloj de referencia.
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: Método CCmdQueue. SetTimeAdvise (Winutil. h)
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
ms.openlocfilehash: 24313b908f1271f270e28b08058c415ed82396fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678889"
---
# <a name="ccmdqueuesettimeadvise-method"></a>CCmdQueue. SetTimeAdvise, método

El `SetTimeAdvise` método configura un evento de temporizador con el reloj de referencia.

## <a name="syntax"></a>Sintaxis


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función miembro llama al método [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) para configurar una notificación para el tiempo más antiguo necesario en la cola. Los comandos en tiempo de presentación que se difieren siempre se comprueban. Si el gráfico de filtros está en modo de ejecución, también se comprueban los comandos diferidos que usan el tiempo de flujo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




