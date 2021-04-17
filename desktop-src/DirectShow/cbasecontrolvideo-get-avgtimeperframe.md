---
description: El \_ método get AvgTimePerFrame recupera el tiempo medio por fotograma.
ms.assetid: bcfdb241-9ec1-49f4-b2b5-0869c27da953
title: Método CBaseControlVideo.get_AvgTimePerFrame (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_AvgTimePerFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae69140348be6e2fdfc120ee7fb40096d663f720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690349"
---
# <a name="cbasecontrolvideoget_avgtimeperframe-method"></a>CBaseControlVideo. Get \_ AvgTimePerFrame (método)

El `get_AvgTimePerFrame` método recupera el tiempo medio por fotograma.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_AvgTimePerFrame(
   REFTIME *pAvgTimePerFrame
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAvgTimePerFrame* 
</dt> <dd>

Puntero al promedio de tiempo por fotograma.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un ERROR Si se realiza correctamente o E \_ OUTOFMEMORY si no hay suficiente memoria disponible.

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método [**IBasicVideo:: get \_ AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) . Llama a la función miembro virtual [**CBaseControlVideo:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) pura para recuperar la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) de la clase derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




