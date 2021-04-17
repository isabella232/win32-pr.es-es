---
description: El método GetCurrentImage recupera una copia de la imagen actual en el representador.
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: Método CBaseControlVideo. GetCurrentImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetCurrentImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d44e6930d0d7e179162939c13a54f2953c5ab965
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691100"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a>CBaseControlVideo. GetCurrentImage, método

El `GetCurrentImage` método recupera una copia de la imagen actual en el representador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCurrentImage(
   long *pBufferSize,
   long *pVideoImage
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBufferSize* 
</dt> <dd>

Puntero al tamaño del búfer de salida.

</dd> <dt>

*pVideoImage* 
</dt> <dd>

Puntero al búfer de salida de la imagen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.



| Código devuelto                                                                                        | Descripción                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>             | Error.<br/>                                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>       | Argumento no válido.<br/>                                                      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>      | Memoria insuficiente Se devuelve cuando el parámetro *pVideoInfo* es **null**.<br/>   |
| <dl> <dt>**NOERROR**</dt> </dl>             | Correcto.<br/>                                                               |
| <dl> <dt>**VFW \_ E \_ no \_ pausado**</dt> </dl> | No se pudo realizar la operación porque el filtro no está en pausa.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta función miembro recupera la imagen de la muestra y la copia en el búfer de salida. La sección de vídeo copiada en el búfer de salida refleja el rectángulo de origen establecido a través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . No refleja el rectángulo de destino.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




