---
description: 'El método GetMediaType recupera el tipo de medio, si el tipo de medio es distinto del ejemplo anterior. Este método implementa el método IMediaSample:: GetMediaType.'
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: Método CMediaSample. GetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a067494d6236b824ef8fbbcb583ad50503297b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670665"
---
# <a name="cmediasamplegetmediatype-method"></a>CMediaSample. GetMediaType, método

El `GetMediaType` método recupera el tipo de medio si el tipo de medio es distinto del ejemplo anterior. Este método implementa el método [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMediaType(
   AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppMediaType* 
</dt> <dd>

Dirección de una variable que recibe un puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Si el tipo de medio no ha cambiado en el ejemplo anterior, *\* ppMediaType* se establece en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>       | El tipo de medio no ha cambiado en el ejemplo anterior.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>                                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/>                                     |



 

## <a name="remarks"></a>Observaciones

Cuando haya terminado con el tipo de medio, libere el bloque de memoria mediante una llamada a la función de la utilidad [**DeleteMediaType**](deletemediatype.md) .

La variable miembro [**CMediaSample:: m \_ pMediaType**](cmediasample-m-pmediatype.md) especifica el tipo de medio. La variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica si el tipo de medio ha cambiado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




