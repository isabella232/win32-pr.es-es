---
description: El método GetCurrentImage recupera una copia de la imagen actual en el representador.
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: Método CBaseControlVideo.GetCurrentImage (Ctlutil.h)
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
ms.openlocfilehash: 782f540959b134f7ca00c2bc674a64ce60ccb4f6ddf166c79f2597e582ca9fc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087575"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a>Método CBaseControlVideo.GetCurrentImage

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

Devuelve un **valor HRESULT** que depende de la implementación; puede ser uno de los siguientes valores u otros valores no enumerados.



| Código devuelto                                                                                        | Descripción                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>             | Error.<br/>                                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>       | Argumento no válido.<br/>                                                      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>      | Memoria insuficiente Se devuelve cuando *el parámetro pVideoInfo* es **NULL.**<br/>   |
| <dl> <dt>**NOERROR**</dt> </dl>             | Correcto.<br/>                                                               |
| <dl> <dt>**VFW \_ E \_ NOT \_ PAUSED**</dt> </dl> | No se pudo realizar la operación porque el filtro no está en pausa.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta función miembro recupera la imagen del ejemplo y la copia en el búfer de salida. La sección de vídeo copiada en el búfer de salida refleja el rectángulo de origen establecido a través de la [**interfaz IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) No refleja el rectángulo de destino.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlVideo (clase)**](cbasecontrolvideo.md)
</dt> </dl>

 

 




