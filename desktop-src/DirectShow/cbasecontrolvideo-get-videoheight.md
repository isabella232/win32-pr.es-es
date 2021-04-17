---
description: El \_ método get VideoHeight recupera el alto del vídeo nativo.
ms.assetid: f33ba789-f9c6-47f1-879b-241bfdc72010
title: Método CBaseControlVideo.get_VideoHeight (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e738636cecd8031962ae31ebf54ac258d868013
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690342"
---
# <a name="cbasecontrolvideoget_videoheight-method"></a>CBaseControlVideo. Get \_ VideoHeight (método)

El `get_VideoHeight` método recupera el alto del vídeo nativo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_VideoHeight(
   long *pVideoHeight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVideoHeight* 
</dt> <dd>

Puntero al alto del vídeo nativo, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un ERROR Si se realiza correctamente o E \_ OUTOFMEMORY si no hay suficiente memoria disponible.

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método [**IBasicVideo:: get \_ VideoHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) . Llama al CBaseControlVideo virtual puro [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) para recuperar la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) de la clase derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




