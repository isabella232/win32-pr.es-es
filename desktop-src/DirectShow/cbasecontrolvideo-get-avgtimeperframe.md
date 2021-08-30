---
description: El método get \_ AvgTimePerFrame recupera el tiempo medio por fotograma.
ms.assetid: bcfdb241-9ec1-49f4-b2b5-0869c27da953
title: CBaseControlVideo.get_AvgTimePerFrame método (Ctlutil.h)
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
ms.openlocfilehash: f80a9b39bf18d92499687e38bac31f3b1105892506b61a5a685d938a60e382cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057315"
---
# <a name="cbasecontrolvideoget_avgtimeperframe-method"></a>CBaseControlVideo.get \_ AvgTimePerFrame (método)

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

Puntero al tiempo medio por fotograma.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve NOERROR si se realiza correctamente o \_ E OUTOFMEMORY si no hay suficiente memoria disponible.

## <a name="remarks"></a>Comentarios

Esta función miembro implementa el [**método IBasicVideo::get \_ AvgTimePerFrame.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) Llama a la función miembro [**virtual pura CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) para recuperar la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) de la clase derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




