---
description: El método ScheduleSample invalida la clase base que realiza el trabajo principal para mantener un recuento de muestras dibujadas y descartadas (que se usan en la implementación de IQualProp).
ms.assetid: 66e4e318-a7ff-4ba0-9ac5-24ba39ac86f1
title: Método CBaseVideoRenderer.ScheduleSample (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f68701fd4c4d682d6bcd89c3b82d6bf054188a9bbdcb47c9019b563fad4a877f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658241"
---
# <a name="cbasevideorendererschedulesample-method"></a>Método CBaseVideoRenderer.ScheduleSample

El método invalida la clase base que realiza el trabajo principal para mantener un recuento de muestras dibujadas y descartadas (que se usan en la `ScheduleSample` [**implementación de IQualProp).**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop)

## <a name="syntax"></a>Sintaxis


```C++
BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntero al ejemplo multimedia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el ejemplo está programado; de lo contrario, **devuelve FALSE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




