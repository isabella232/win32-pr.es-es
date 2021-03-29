---
description: 'El método SetPreroll especifica si este ejemplo es un ejemplo de relanzamiento. No se debe mostrar un ejemplo de prelanzamiento. Este método implementa el método IMediaSample:: SetPreroll.'
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: Método CMediaSample. SetPreroll (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 594f26ebb738a986c85a14b88f8896b122b58f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679072"
---
# <a name="cmediasamplesetpreroll-method"></a>CMediaSample. SetPreroll, método

El `SetPreroll` método especifica si este ejemplo es un ejemplo de relanzamiento. No se debe mostrar un ejemplo de prelanzamiento. Este método implementa el método [**IMediaSample:: SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPreroll(
   BOOL bIsPreroll
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bIsPreroll* 
</dt> <dd>

Valor booleano que especifica si se trata de un ejemplo de relanzamiento. Si es **true**, se trata de un ejemplo de relanzamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Este método actualiza la variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica la propiedad preroll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




