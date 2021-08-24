---
description: El método SetPreroll especifica si este ejemplo es un ejemplo de preinselección. No se debe mostrar un ejemplo de inscripción previa. Este método implementa el método IMediaSample::SetPreroll.
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
ms.openlocfilehash: 410031ccf60e830c51615d267d3324167169c5de7960f79dc05b8c9e267463bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832105"
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

## <a name="remarks"></a>Comentarios

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

 

 




