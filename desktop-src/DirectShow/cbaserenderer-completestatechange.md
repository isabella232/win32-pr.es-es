---
description: El método CompleteStateChange determina si se ha completado una transición al estado en pausa.
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: Método CBaseRenderer. CompleteStateChange (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteStateChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2465aeed3347f6ebc592dbe01bc3580a30983e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671073"
---
# <a name="cbaserenderercompletestatechange-method"></a>CBaseRenderer. CompleteStateChange, método

El `CompleteStateChange` método determina si se ha completado una transición al estado en pausa.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CompleteStateChange(
   FILTER_STATE OldState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OldState* 
</dt> <dd>

Estado anterior a la transición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si la transición se ha completado. De lo contrario, devuelve S \_ false.

## <a name="remarks"></a>Observaciones

El método [**CBaseRenderer::P ause**](cbaserenderer-pause.md) llama a este método para actualizar el estado de la transición de estado. En general, la transición a pausado no finaliza hasta que el filtro recibe un ejemplo. Sin embargo, en algunas situaciones la transición se completa inmediatamente: por ejemplo, si el filtro está desconectado o si se alcanzó el final de la secuencia. Este método comprueba los distintos criterios y, a continuación, llama al método [**CBaseRenderer:: Ready**](cbaserenderer-ready.md) o al método [**CBaseRenderer::**](cbaserenderer-notready.md) para actualizar el estado de la transición.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




