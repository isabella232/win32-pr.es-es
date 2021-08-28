---
description: El método get AvgSyncOffset recupera el promedio del tiempo en milisegundos entre el momento en que se debía cada fotograma y el momento en que se representó realmente para todos los fotogramas desde que se inició el \_ streaming.
ms.assetid: b41741e9-e0b5-4c49-93ef-cb8c0cf2ddeb
title: CBaseVideoRenderer.get_AvgSyncOffset método (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4550445d0a2596edcb9d76b88b371eb060257b29730a386c4f9444dae2624b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526505"
---
# <a name="cbasevideorendererget_avgsyncoffset-method"></a>CBaseVideoRenderer.get \_ AvgSyncOffset (método)

El método recupera el promedio del tiempo en milisegundos entre el momento en que se debía cada fotograma y el momento en que se representó realmente para todos los fotogramas desde que se inició `get_AvgSyncOffset` el streaming.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_AvgSyncOffset(
   int *piAvg
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*piAvg* 
</dt> <dd>

Puntero al promedio del tiempo como se describió anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Esta función miembro implementa el [**método IQualProp::get \_ AvgSyncOffset.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




