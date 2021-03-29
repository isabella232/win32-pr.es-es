---
description: 'El método Stop detiene el filtro. Este método implementa el método IMediaFilter:: stop.'
ms.assetid: 68d77f9a-95a2-4a71-bbe1-28be76fbc538
title: Método CBaseFilter. STOP (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b4c4893edcf02fa18da3dc207a49f87c91b2a9ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660609"
---
# <a name="cbasefilterstop-method"></a>CBaseFilter. STOP (método)

El `Stop` método detiene el filtro. Este método implementa el método [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

Este método llama al método [**CBasePin:: Inactive**](cbasepin-inactive.md) en cada una de las clavijas conectadas del filtro. También establece el estado del filtro en \_ detenido.

Cuando el filtro se detiene, debe rechazar los ejemplos del nivel superior, detener la entrega de muestras de bajada, cerrar los subprocesos de trabajo y liberar los recursos que se utilizaron para la transmisión por secuencias.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




