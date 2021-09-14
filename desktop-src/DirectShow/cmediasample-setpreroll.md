---
description: El método SetPreroll especifica si este ejemplo es un ejemplo de inscripción previa. No se debe mostrar un ejemplo de inscripción previa. Este método implementa el método IMediaSample::SetPreroll.
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: Método CMediaSample.SetPreroll (Amfilter.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251168"
---
# <a name="cmediasamplesetpreroll-method"></a>Método CMediaSample.SetPreroll

El `SetPreroll` método especifica si este ejemplo es un ejemplo de inscripción previa. No se debe mostrar un ejemplo de inscripción previa. Este método implementa el [**método IMediaSample::SetPreroll.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll)

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

Valor booleano que especifica si se trata de un ejemplo de inscripción previa. Si **es TRUE,** se trata de un ejemplo de inscripción previa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Este método actualiza la variable [**miembro CMediaSample::m \_ dwFlags,**](cmediasample-m-dwflags.md) que especifica la propiedad preroll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




