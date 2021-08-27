---
description: El método \_ get VideoHeight recupera el alto del vídeo nativo.
ms.assetid: f33ba789-f9c6-47f1-879b-241bfdc72010
title: CBaseControlVideo.get_VideoHeight método (Ctlutil.h)
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
ms.openlocfilehash: 31a7ca4b87a9196a8b59ec00cdc0e458855fa1db4e1e8f7b5bfd233924475519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057085"
---
# <a name="cbasecontrolvideoget_videoheight-method"></a>Método CBaseControlVideo.get \_ VideoHeight

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

Devuelve NOERROR si se realiza correctamente o \_ E OUTOFMEMORY si no hay suficiente memoria disponible.

## <a name="remarks"></a>Comentarios

Esta función miembro implementa el [**método IBasicVideo::get \_ VideoHeight.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) Llama al [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) virtual puro para recuperar la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) de la clase derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




