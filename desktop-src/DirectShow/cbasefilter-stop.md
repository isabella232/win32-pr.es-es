---
description: El método Stop detiene el filtro. Este método implementa el método IMediaFilter::Stop.
ms.assetid: 68d77f9a-95a2-4a71-bbe1-28be76fbc538
title: Método CBaseFilter.Stop (Amfilter.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361401"
---
# <a name="cbasefilterstop-method"></a>Método CBaseFilter.Stop

El `Stop` método detiene el filtro. Este método implementa el [**método IMediaFilter::Stop.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

Este método llama al [**método CBasePin::Inactive**](cbasepin-inactive.md) en cada uno de los pines conectados del filtro. También establece el estado del filtro en Estado \_ detenido.

Cuando se detiene el filtro, debe rechazar muestras de nivel superior, dejar de entregar muestras de bajada, apagar subprocesos de trabajo y liberar los recursos que usó para el streaming.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




