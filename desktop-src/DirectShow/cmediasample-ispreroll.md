---
description: 'El método IsPreroll determina si este ejemplo es un ejemplo de relanzamiento. No se debe mostrar un ejemplo de prelanzamiento. Este método implementa el método IMediaSample:: IsPreroll.'
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: Método CMediaSample. IsPreroll (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40cf8fd6a1adb5186309f47da0f0ae3dc30412a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670473"
---
# <a name="cmediasampleispreroll-method"></a>CMediaSample. IsPreroll, método

El `IsPreroll` método determina si este ejemplo es un ejemplo de relanzamiento. No se debe mostrar un ejemplo de prelanzamiento. Este método implementa el método [**IMediaSample:: IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el ejemplo es un ejemplo de relanzamiento y S \_ false en caso contrario.

## <a name="remarks"></a>Observaciones

La variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




