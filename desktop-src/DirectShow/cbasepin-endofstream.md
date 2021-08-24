---
description: El método EndOfStream notifica al pin que no se espera ningún dato adicional. Este método implementa el método IPin::EndOfStream. Llame a este método solo en los pines de entrada.
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: Método CBasePin.EndOfStream (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9e1549000be728da0118323303a60a23a5930ad68d3c7d2d2b6c9c92d54c3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916435"
---
# <a name="cbasepinendofstream-method"></a>Método CBasePin.EndOfStream

El `EndOfStream` método notifica al pin que no se espera ningún dato adicional. Este método implementa el [**método IPin::EndOfStream.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) Llame a este método solo en los pines de entrada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

El filtro debe pasar notificaciones de fin de flujo de bajada a las clavijas de entrada de los filtros conectados. Si el filtro es un representador, debe publicar una notificación de eventos [**EC \_ COMPLETE**](ec-complete.md) al administrador de gráficos de filtros. Para obtener más información, vea [Data Flow en filter Graph](data-flow-in-the-filter-graph.md).

En la clase base, este método no hace nada. Las clases derivadas deben invalidar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




