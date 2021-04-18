---
description: El \_ método get AvgSyncOffset recupera el promedio del tiempo en milisegundos entre el momento en que se debió cada fotograma y el momento en que se representó realmente para todos los fotogramas desde que se inició el streaming.
ms.assetid: b41741e9-e0b5-4c49-93ef-cb8c0cf2ddeb
title: Método CBaseVideoRenderer.get_AvgSyncOffset (Renbase. h)
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
ms.openlocfilehash: 35c682b8f4bb60ec629db5489e879d1ca7968b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679309"
---
# <a name="cbasevideorendererget_avgsyncoffset-method"></a>CBaseVideoRenderer. Get \_ AvgSyncOffset (método)

El `get_AvgSyncOffset` método recupera el promedio del tiempo en milisegundos entre el momento en que se debió cada fotograma y el momento en que se representó realmente para todos los fotogramas desde que se inició el streaming.

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

Puntero al promedio del tiempo tal y como se ha descrito anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método [**IQualProp:: get \_ AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




