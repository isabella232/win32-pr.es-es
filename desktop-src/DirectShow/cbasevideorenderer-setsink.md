---
description: El método SetSink establece el objeto IQualityControl que recibirá los mensajes de calidad.
ms.assetid: f5789781-1871-4fea-9d1f-bd1a21b70439
title: Método CBaseVideoRenderer. SetSink (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9658ab4a1099e7baaef0a3e1a0ae3c0d495e89e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679094"
---
# <a name="cbasevideorenderersetsink-method"></a>CBaseVideoRenderer. SetSink, método

El `SetSink` método establece el objeto [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) que recibirá los mensajes de calidad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*piqc* 
</dt> <dd>

Puntero al objeto [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) al que se deben enviar las notificaciones.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método [**IQualityControl:: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) en el representador de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




