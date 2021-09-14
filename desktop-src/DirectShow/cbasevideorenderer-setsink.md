---
description: El método SetSink establece el objeto IQualityControl que recibirá mensajes de calidad.
ms.assetid: f5789781-1871-4fea-9d1f-bd1a21b70439
title: Método CBaseVideoRenderer.SetSink (Renbase.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255549"
---
# <a name="cbasevideorenderersetsink-method"></a>Método CBaseVideoRenderer.SetSink

El `SetSink` método establece el objeto [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) que recibirá mensajes de calidad.

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

Puntero al [**objeto IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) al que se deben enviar las notificaciones.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el [**método IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) en el representador de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseVideoRenderer (clase)**](cbasevideorenderer.md)
</dt> </dl>

 

 




