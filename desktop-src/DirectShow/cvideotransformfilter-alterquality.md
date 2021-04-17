---
description: 'El método AlterQuality notifica al filtro que se ha solicitado un cambio de calidad. Este método invalida el método CTransformFilter:: AlterQuality.'
ms.assetid: 9a1d1379-8557-4b33-ab49-b5c6a684f685
title: Método CVideoTransformFilter. AlterQuality (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1de0985b8cb3a8db6f45c247e717042cf344655f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660125"
---
# <a name="cvideotransformfilteralterquality-method"></a>CVideoTransformFilter. AlterQuality, método

El `AlterQuality` método notifica al filtro que se ha solicitado un cambio de calidad. Este método invalida el método [**CTransformFilter:: AlterQuality**](ctransformfilter-alterquality.md) .

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*respuestas* 
</dt> <dd>

Estructura de [**calidad**](/windows/win32/api/strmif/ns-strmif-quality) que contiene el mensaje de control de calidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ Fail.

## <a name="remarks"></a>Observaciones

Se llama a este método cuando el PIN de salida recibe un mensaje de calidad (a través del método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) ).

El valor de retraso de *q* se almacena en la variable de miembro **m \_ itrLate** . El valor devuelto de E \_ FAIL indica que el representador debe ponerse al día soltando fotogramas, aunque la clase **CVideoTransformFilter** también quitará los fotogramas en las condiciones correctas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CVideoTransformFilter**](cvideotransformfilter.md)
</dt> <dt>

[**CVideoTransformFilter::ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md)
</dt> </dl>

 

 




