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
ms.openlocfilehash: 4e738636cecd8031962ae31ebf54ac258d868013
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273356"
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

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el [**método IBasicVideo::get \_ VideoHeight.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) Llama al [**CBaseControlVideo virtual puro::GetVideoFormat para**](cbasecontrolvideo-getvideoformat.md) recuperar la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) de la clase derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




