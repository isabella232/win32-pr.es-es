---
description: El método IsPreroll determina si este ejemplo es un ejemplo de inscripción previa. No se debe mostrar un ejemplo de inscripción previa. Este método implementa el método IMediaSample::IsPreroll.
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: Método CMediaSample.IsPreroll (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40cf8fd6a1adb5186309f47da0f0ae3dc30412a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254420"
---
# <a name="cmediasampleispreroll-method"></a>Método CMediaSample.IsPreroll

El `IsPreroll` método determina si este ejemplo es un ejemplo de inscripción previa. No se debe mostrar un ejemplo de inscripción previa. Este método implementa el [**método IMediaSample::IsPreroll.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el ejemplo es un ejemplo de inscripción previa y S FALSE en caso \_ contrario.

## <a name="remarks"></a>Observaciones

La variable [**miembro CMediaSample::m \_ dwFlags**](cmediasample-m-dwflags.md) especifica esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaSample (clase)**](cmediasample.md)
</dt> </dl>

 

 




