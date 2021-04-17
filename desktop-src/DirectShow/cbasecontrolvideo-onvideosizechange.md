---
description: Pasa un \_ \_ mensaje de tamaño de vídeo \_ de EC cambiado al administrador de gráficos de filtro.
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: Método CBaseControlVideo. OnVideoSizeChange (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.OnVideoSizeChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37caa05d164c23484c749730796d6a5f10d67d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670383"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a>CBaseControlVideo. OnVideoSizeChange, método

Pasa un \_ \_ mensaje de tamaño de vídeo \_ de EC cambiado al administrador de gráficos de filtro.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.



| Código devuelto                                                                                   | Descripción               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/> |



 

## <a name="remarks"></a>Observaciones

Un representador de vídeo debe llamar a esta función miembro cada vez que se cambia el tamaño del vídeo; Normalmente, se llamará una vez después de la conexión inicial. Si el representador puede admitir cambios de formato dinámico (de 320 x 240 a 160 x 120), también debe llamarlo después de cada cambio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




