---
description: El método Stop detiene el filtro.
ms.assetid: 80eac207-5db3-4b06-bbae-eca72e37d09d
title: Método CBaseRenderer.Stop (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ddd8194bbf76c4a4311aa90335f94d1e7548a356
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061759"
---
# <a name="cbaserendererstop-method"></a>Método CBaseRenderer.Stop

El `Stop` método detiene el filtro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBaseFilter::Stop.**](cbasefilter-stop.md) Las acciones que realiza son las siguientes:

-   Llama [**a CBaseFilter::Stop**](cbasefilter-stop.md).
-   Desasigna el asignador. (Vea [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit)).
-   Cancela cualquier representación programada y libera el subproceso de streaming.
-   Espera a que se complete cualquier **llamada de** recepción pendiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 




