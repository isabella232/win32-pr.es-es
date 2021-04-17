---
description: El método JoinFilterGraph envía la \_ \_ notificación de eventos de la ventana de EC destruido cuando se quita un filtro del gráfico de filtros.
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: Método CBaseVideoRenderer. JoinFilterGraph (Renbase. h)
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
ms.openlocfilehash: acabb6deeb6577fa04479fc4014e210d4a5654d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680589"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a>CBaseVideoRenderer. JoinFilterGraph, método

El `JoinFilterGraph` método envía la notificación de eventos de la [**ventana de EC \_ \_ destruido**](ec-window-destroyed.md) cuando se quita un filtro del gráfico de filtros.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT JoinFilterGraph(
       IBaseFilterGraph *pGraph,
  [in] LPCWSTR          pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGraph* 
</dt> <dd>

Puntero al gráfico de filtro que se va a combinar.

</dd> <dt>

*pName* \[ de\]
</dt> <dd>

Puntero al nombre del filtro que se va a agregar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función miembro invalida la función miembro [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) . Si el filtro deja el gráfico de filtro (*pGraph* es **null**), envía una notificación de eventos de [**ventana de EC \_ \_ destruido**](ec-window-destroyed.md) para que el administrador de recursos no mantenga el representador como un objeto de foco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




