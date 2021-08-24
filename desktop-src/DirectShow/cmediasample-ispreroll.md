---
description: El método IsPreroll determina si este ejemplo es un ejemplo de preinselección. No se debe mostrar un ejemplo de inscripción previa. Este método implementa el método IMediaSample::IsPreroll.
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
ms.openlocfilehash: 7f4c4b192d72c5edcfdb9c318f7420ca6ae5797446ec4f99cb6871aad2abd241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634645"
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

Devuelve S OK si el ejemplo es un ejemplo de inscripción previa y S FALSE en caso \_ \_ contrario.

## <a name="remarks"></a>Comentarios

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

 

 




