---
description: La función ConvertVideoInfoToVideoInfo2 convierte un tipo de medio que usa VIDEOINFOHEADER en uno que usa VIDEOINFOHEADER2.
ms.assetid: d938bfc0-a5ae-475b-b183-56ff39b4bae1
title: Función ConvertVideoInfoToVideoInfo2 (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertVideoInfoToVideoInfo2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54611c83c30ad65a806a077dc51c933a9f881636
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161560"
---
# <a name="convertvideoinfotovideoinfo2-function"></a>Función ConvertVideoInfoToVideoInfo2

La `ConvertVideoInfoToVideoInfo2` función convierte un tipo de medio que usa [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) en uno que [**usa VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDAPI ConvertVideoInfoToVideoInfo2(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntero a la [**estructura AM MEDIA TYPE \_ \_ que**](/windows/win32/api/strmif/ns-strmif-am_media_type) se convertirá. La estructura debe tener el tipo de formato FORMAT \_ VideoInfo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK o E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Esta función asigna una nueva estructura **VIDEOINFOHEADER2,** copia los miembros de la estructura **VIDEOINFOHEADER** en ella y reemplaza la estructura anterior por la nueva estructura en el bloque de formato del tipo de medio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de vídeo e imagen](video-and-image-functions.md)
</dt> </dl>

 

 




