---
description: 'El método EndOfStream notifica al pin que no se espera ningún dato adicional. Este método implementa el método IPin:: EndOfStream. Llame a este método solo en clavijas de entrada.'
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: Método CBasePin. EndOfStream (Amfilter. h)
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
ms.openlocfilehash: 2324bae8ec1266dce2471049f8ba2f06b0c9e6e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671633"
---
# <a name="cbasepinendofstream-method"></a>CBasePin. EndOfStream, método

El `EndOfStream` método notifica al pin que no se espera ningún dato adicional. Este método implementa el método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) . Llame a este método solo en clavijas de entrada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

El filtro debe pasar las notificaciones de final de secuencia de nivel inferior a los pin de entrada de los filtros conectados. Si el filtro es un representador, debería publicar una notificación de evento de [**\_ finalización de EC**](ec-complete.md) en el administrador de gráficos de filtro. Para obtener más información, vea [flujo de datos en el gráfico de filtros](data-flow-in-the-filter-graph.md).

En la clase base, este método no hace nada. Las clases derivadas deben invalidar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




