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
ms.openlocfilehash: 659ad34c01ca6c74a24f6bbf5f5bef42df46f94f06b7e03541f9caf3398b39e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768195"
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

## <a name="remarks"></a>Comentarios

Este método llama al [**método CBasePin::Inactive**](cbasepin-inactive.md) en cada uno de los pines conectados del filtro. También establece el estado del filtro en Estado \_ detenido.

Cuando se detiene el filtro, debe rechazar muestras de nivel superior, dejar de entregar muestras de bajada, apagar subprocesos de trabajo y liberar los recursos que usó para el streaming.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseFilter (clase)**](cbasefilter.md)
</dt> </dl>

 

 




