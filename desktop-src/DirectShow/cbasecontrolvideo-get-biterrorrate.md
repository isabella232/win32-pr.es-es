---
description: El método get \_ BitErrorRate recupera una tasa de errores de bits aproximada para el vídeo.
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: CBaseControlVideo.get_BitErrorRate método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitErrorRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2602d203ca5a418dcc889d26932cd28be78d984390e71cff996e6fd3938030a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057295"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a>Método CBaseControlVideo.get \_ BitErrorRate

El `get_BitErrorRate` método recupera una tasa de errores de bits aproximada para el vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_BitErrorRate(
   long *pBitErrorRate
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBitErrorRate* 
</dt> <dd>

Puntero a la tasa de errores de bits (un error para aproximadamente este número de bits).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve NOERROR si se realiza correctamente o \_ E OUTOFMEMORY si no hay suficiente memoria disponible.

## <a name="remarks"></a>Comentarios

Esta función miembro implementa el [**método IBasicVideo::get \_ BitErrorRate.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) Llama al método [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) virtual puro para recuperar la [**estructura VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) de la clase derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




