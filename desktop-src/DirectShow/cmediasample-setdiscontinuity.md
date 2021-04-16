---
description: 'El método SetDiscontinuity especifica si este ejemplo representa una interrupción en el flujo de datos. Este método implementa el método IMediaSample:: SetDiscontinuity.'
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: Método CMediaSample. SetDiscontinuity (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35565b2cee0284d0e5b9f85d7335a630b5f54e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679080"
---
# <a name="cmediasamplesetdiscontinuity-method"></a>CMediaSample. SetDiscontinuity, método

El `SetDiscontinuity` método especifica si este ejemplo representa una interrupción en el flujo de datos. Este método implementa el método [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bDiscont* 
</dt> <dd>

Valor booleano que especifica si este ejemplo es una discontinuidad. Si es **true**, el ejemplo multimedia es discontinuo con el ejemplo anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Este método actualiza la variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica la propiedad discontinuidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




