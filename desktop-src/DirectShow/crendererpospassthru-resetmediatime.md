---
description: El método ResetMediaTime restablece las marcas de tiempo almacenadas en caché en cero.
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: Método CRendererPosPassThru.ResetMediaTime (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.ResetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f1babc39ad3329ec18be663ffcc6eb882933bead0be5f631ef82ce363391f737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953824"
---
# <a name="crendererpospassthruresetmediatime-method"></a>Método CRendererPosPassThru.ResetMediaTime

El `ResetMediaTime` método restablece las marcas de tiempo almacenadas en caché a cero.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

El filtro debe llamar a este método cada vez que las marcas de tiempo almacenadas en caché por el método [**CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) no son válidas. En concreto, debe llamar a este método en respuesta a los métodos [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) [**e IMediaFilter::Stop.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop)

Después de llamar a este método, el método [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) devuelve cero para las horas de inicio y finalización.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




