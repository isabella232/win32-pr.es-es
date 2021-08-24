---
description: El método SetMediaType establece el tipo de medio para el ejemplo. Este método implementa el método IMediaSample::SetMediaType.
ms.assetid: 4423cc1e-d6e1-49e7-9cc1-1a1d71a3497b
title: Método CMediaSample.SetMediaType (Amfilter.h)
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
ms.openlocfilehash: 4e7059e0d9b2d91b6a938c67445f185a2c9be0daf5831c30b235918ab7820b1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832175"
---
# <a name="cmediasamplesetmediatype-method"></a>Método CMediaSample.SetMediaType

El `SetMediaType` método establece el tipo de medio para el ejemplo. Este método implementa el [**método IMediaSample::SetMediaType.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype)

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

Puntero a una [**estructura \_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/> |



 

## <a name="remarks"></a>Comentarios

Este método establece la variable miembro [**CMediaSample::m \_ pMediaType,**](cmediasample-m-pmediatype.md) que especifica el tipo de medio, y la variable miembro [**CMediaSample::m \_ dwFlags,**](cmediasample-m-dwflags.md) que especifica si el tipo de medio ha cambiado.

Este método realiza una copia de la estructura \_ AM MEDIA \_ TYPE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




