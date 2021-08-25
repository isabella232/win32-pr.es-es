---
description: El método CompleteStateChange determina si se ha completado una transición al estado en pausa.
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: Método CBaseRenderer.CompleteStateChange (Renbase.h)
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
ms.openlocfilehash: 260cd5692e10fb6e6adaa3ed715944eb773064afaea68f5e0909fa08f45adfb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872365"
---
# <a name="cbaserenderercompletestatechange-method"></a>Método CBaseRenderer.CompleteStateChange

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

Devuelve S \_ OK si la transición se ha completado. De lo contrario, devuelve S \_ FALSE.

## <a name="remarks"></a>Comentarios

El [**método CBaseRenderer::P ause**](cbaserenderer-pause.md) llama a este método para actualizar el estado de transición de estado. En general, la transición a en pausa no finaliza hasta que el filtro recibe una muestra. Sin embargo, en algunas situaciones, la transición se completa inmediatamente: por ejemplo, si el filtro no está desconectado o si se ha alcanzado el final de la secuencia. Este método comprueba los distintos criterios y llama al método [**CBaseRenderer::Ready**](cbaserenderer-ready.md) o al método [**CBaseRenderer::NotReady**](cbaserenderer-notready.md) para actualizar el estado de transición.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




