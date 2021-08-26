---
description: El método GetVideoFormat recupera un ejemplo de vídeo que representa el formato de vídeo actual.
ms.assetid: f7457c5b-037c-4a63-963e-0fc6086609a4
title: Método CBaseControlVideo.GetVideoFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e37a59b8d002a9c081de74c4974dca1f86d1c9d0a5f7f7b0caca11be6c026d3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052775"
---
# <a name="cbasecontrolvideogetvideoformat-method"></a>Método CBaseControlVideo.GetVideoFormat

El `GetVideoFormat` método recupera un ejemplo de vídeo que representa el formato de vídeo actual.

## <a name="syntax"></a>Sintaxis


```C++
virtual VIDEOINFOHEADER* GetVideoFormat() = 0;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a una [**estructura VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contiene el formato de vídeo actual.

## <a name="remarks"></a>Comentarios

Para devolver y comprobar cierta información a través [**de IBasicVideo,**](/windows/desktop/api/Control/nn-control-ibasicvideo)el objeto debe conocer el formato de vídeo actual. Obtiene esta información llamando a este método virtual puro que las clases derivadas deben invalidar. Las siguientes funciones miembro [**de CBaseControlVideo**](cbasecontrolvideo.md) llaman a esta función miembro.

-   [**CBaseControlVideo::OnVideoSizeChange**](cbasecontrolvideo-onvideosizechange.md)
-   [**CBaseControlVideo::get \_ AvgTimePerFrame**](cbasecontrolvideo-get-avgtimeperframe.md)
-   [**CBaseControlVideo::get \_ BitRate**](cbasecontrolvideo-get-bitrate.md)
-   [**CBaseControlVideo::get \_ BitErrorRate**](cbasecontrolvideo-get-biterrorrate.md)
-   [**CBaseControlVideo::get \_ VideoWidth**](cbasecontrolvideo-get-videowidth.md)
-   [**CBaseControlVideo::get \_ VideoHeight**](cbasecontrolvideo-get-videoheight.md)
-   [**CBaseControlVideo::GetVideoPaletteEntries**](cbasecontrolvideo-getvideopaletteentries.md)
-   [**CBaseControlVideo::GetVideoSize**](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




