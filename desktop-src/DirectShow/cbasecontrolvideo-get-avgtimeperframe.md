---
description: El método \_ get AvgTimePerFrame recupera el tiempo medio por fotograma.
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
ms.openlocfilehash: ae69140348be6e2fdfc120ee7fb40096d663f720
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361425"
---
# <a name="cbasecontrolvideoget_avgtimeperframe-method"></a>Método CBaseControlVideo.get \_ AvgTimePerFrame

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

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el [**método IBasicVideo::get \_ AvgTimePerFrame.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) Llama a la función miembro puramente virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) para recuperar la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) de la clase derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




