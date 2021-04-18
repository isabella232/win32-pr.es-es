---
description: El método GetImageSize recupera información de tamaño de imagen de vídeo.
ms.assetid: a6d7f949-c6a9-49e9-b10a-f6f5bd73dc00
title: Método CBaseControlVideo. GetImageSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed7795e3998bc101e907bce87c9981e86f51fcb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691099"
---
# <a name="cbasecontrolvideogetimagesize-method"></a>CBaseControlVideo. GetImageSize, método

El `GetImageSize` método recupera información de tamaño de imagen de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetImageSize(
   VIDEOINFOHEADER *pVideoInfo,
   long            *pBufferSize,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Puntero a una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que se va a rellenar.

</dd> <dt>

*pBufferSize* 
</dt> <dd>

Puntero al tamaño del búfer de vídeo.

</dd> <dt>

*pSourceRect* 
</dt> <dd>

Puntero a las dimensiones del rectángulo del vídeo de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** que depende de la implementación; puede ser uno de los valores siguientes u otros valores que no estén en la lista.



| Código devuelto                                                                                  | Descripción                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Error.<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento no válido. El formato de datos no es compatible.<br/>           |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Se ha producido un error inesperado. Uno o más argumentos son **null**.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>       | Correcto.<br/>                                                       |



 

## <a name="remarks"></a>Observaciones

Esta función miembro es una función auxiliar que se usa para crear representaciones de imágenes de memoria de imágenes DIB. Se llama desde la implementación de la clase base de [**CBaseControlVideo:: GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) cuando se pasa un parámetro _pVideoImage_ **nulo** a esa función miembro. Como resultado, esta función miembro crea y devuelve una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , usando la información de *pBufferSize* y *pSourceRect*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




