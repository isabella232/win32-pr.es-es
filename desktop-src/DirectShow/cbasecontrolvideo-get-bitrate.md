---
description: El método get \_ BitRate recupera una velocidad de bits aproximada para el vídeo.
ms.assetid: e12e4677-a038-479f-8b64-937ad521c4be
title: CBaseControlVideo.get_BitRate método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b33e3584bb0460b798101d8062c3647b983841c77653adcffd18580eade25c6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057275"
---
# <a name="cbasecontrolvideoget_bitrate-method"></a>Método CBaseControlVideo.get \_ BitRate

El `get_BitRate` método recupera una velocidad de bits aproximada para el vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_BitRate(
   long *pBitRate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBitRate* 
</dt> <dd>

Puntero a la velocidad de bits, en bits por segundo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve NOERROR si se realiza correctamente o \_ E OUTOFMEMORY si no hay suficiente memoria disponible.

## <a name="remarks"></a>Comentarios

Esta función miembro implementa el [**método IBasicVideo::get \_ BitRate.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) Llama al [**CBaseControlVideo virtual puro::GetVideoFormat para**](cbasecontrolvideo-getvideoformat.md) recuperar la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) de la clase derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




