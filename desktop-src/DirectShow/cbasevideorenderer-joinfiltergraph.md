---
description: El método JoinFilterGraph envía una notificación de eventos EC \_ WINDOW \_ DESTROYED cuando se quita un filtro del gráfico de filtros.
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: Método CBaseVideoRenderer.JoinFilterGraph (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3aed2c887bc7a452cda978e96cd369a71cad4fab60a72e0c914ebe9d9790a41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052215"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a>Método CBaseVideoRenderer.JoinFilterGraph

El `JoinFilterGraph` método envía una notificación de eventos EC WINDOW [**\_ \_ DESTROYED**](ec-window-destroyed.md) cuando se quita un filtro del gráfico de filtros.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT JoinFilterGraph(
       IBaseFilterGraph *pGraph,
  [in] LPCWSTR          pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pgraph* 
</dt> <dd>

Puntero al gráfico de filtro que se unirá.

</dd> <dt>

*pName* \[ En\]
</dt> <dd>

Puntero al nombre del filtro que se va a agregar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Esta función miembro invalida la función [**miembro CBaseFilter::JoinFilterGraph.**](cbasefilter-joinfiltergraph.md) Si el filtro deja el gráfico de filtros *(pGraph* es **NULL),** envía una notificación de eventos [**EC WINDOW \_ \_ DESTROYED**](ec-window-destroyed.md) para que el administrador de recursos no se mantenga en el representador como un objeto de foco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




