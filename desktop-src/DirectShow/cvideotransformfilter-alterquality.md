---
description: El método AlterQuality notifica al filtro que se solicita un cambio de calidad. Este método invalida el método CTransformFilter::AlterQuality.
ms.assetid: 9a1d1379-8557-4b33-ab49-b5c6a684f685
title: Método CVideoTransformFilter.AlterQuality (Vtrans.h)
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
ms.openlocfilehash: 6cd2568bfc9518e2eeaf0399fa53796e305d246c511e5ee5bea1d3a1cacf7712
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998625"
---
# <a name="cvideotransformfilteralterquality-method"></a>Método CVideoTransformFilter.AlterQuality

El `AlterQuality` método notifica al filtro que se solicita un cambio de calidad. Este método invalida el [**método CTransformFilter::AlterQuality.**](ctransformfilter-alterquality.md)

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Q* 
</dt> <dd>

[**Estructura**](/windows/win32/api/strmif/ns-strmif-quality) de calidad que contiene el mensaje de control de calidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve E \_ FAIL.

## <a name="remarks"></a>Comentarios

Se llama a este método cuando el pin de salida recibe un mensaje de calidad (a través [**del método IQualityControl::Notify).**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)

El valor de retraso de *q* se almacena en la variable **miembro m \_ itrLate.** El valor devuelto de E FAIL indica que el representador debe ponerse al día quitando fotogramas, aunque la clase \_ **CVideoTransformFilter** también quitará fotogramas en las condiciones adecuadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CVideoTransformFilter (clase)**](cvideotransformfilter.md)
</dt> <dt>

[**CVideoTransformFilter::ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md)
</dt> </dl>

 

 




