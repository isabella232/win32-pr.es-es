---
description: 'El método SetMediaType establece el tipo de medio para el ejemplo. Este método implementa el método IMediaSample:: SetMediaType.'
ms.assetid: 4423cc1e-d6e1-49e7-9cc1-1a1d71a3497b
title: Método CMediaSample. SetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f46fc4e8c348b1d03d19e815f658e0f637b8f880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679074"
---
# <a name="cmediasamplesetmediatype-method"></a>CMediaSample. SetMediaType, método

El `SetMediaType` método establece el tipo de medio para el ejemplo. Este método implementa el método [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMediaType(
   AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaType* 
</dt> <dd>

Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/> |



 

## <a name="remarks"></a>Observaciones

Este método establece la variable miembro [**CMediaSample:: m \_ pMediaType**](cmediasample-m-pmediatype.md) , que especifica el tipo de medio y la variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica si el tipo de medio ha cambiado.

Este método realiza una copia de la \_ estructura de tipo de medio am \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




