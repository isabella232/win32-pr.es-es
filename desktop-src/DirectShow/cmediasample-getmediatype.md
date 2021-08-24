---
description: El método GetMediaType recupera el tipo de medio, si el tipo de medio difiere del ejemplo anterior. Este método implementa el método IMediaSample::GetMediaType.
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: Método CMediaSample.GetMediaType (Amfilter.h)
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
ms.openlocfilehash: ee7b5464ff2620dbc0247b006dc323232131de3936d2c5e56f2232b67c00ba5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832305"
---
# <a name="cmediasamplegetmediatype-method"></a>Método CMediaSample.GetMediaType

El `GetMediaType` método recupera el tipo de medio, si el tipo de medio difiere del ejemplo anterior. Este método implementa el [**método IMediaSample::GetMediaType.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype)

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

Dirección de una variable que recibe un puntero a una [**estructura \_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Si el tipo de medio no ha cambiado con respecto al ejemplo anterior, *\* ppMediaType* se establece en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | El tipo de medio no ha cambiado con respecto al ejemplo anterior.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto.<br/>                                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/>                                     |



 

## <a name="remarks"></a>Comentarios

Cuando haya terminado con el tipo de medio, liberará el bloque de memoria mediante una llamada a la función de utilidad [**DeleteMediaType.**](deletemediatype.md)

La variable [**miembro CMediaSample::m \_ pMediaType**](cmediasample-m-pmediatype.md) especifica el tipo de medio. La variable [**miembro CMediaSample::m \_ dwFlags**](cmediasample-m-dwflags.md) especifica si el tipo de medio ha cambiado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




