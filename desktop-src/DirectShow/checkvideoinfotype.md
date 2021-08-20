---
description: La función CheckVideoInfoType comprueba un tipo de medio que contiene una estructura de formato VIDEOINFOHEADER para ver si hay determinados errores comunes que pueden provocar saturaciones del búfer o desbordamientos de enteros.
ms.assetid: 7ffca7de-26f9-4d8d-b70e-231eca462211
title: Función CheckVideoInfoType (Checkbmi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfoType
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 4463a1edb2002f64e983a38eb4a0ace5b5289b4d47ac43c8ea27bf165138ff95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539545"
---
# <a name="checkvideoinfotype-function"></a>Función CheckVideoInfoType

La función comprueba un tipo de medio que contiene una estructura de formato VIDEOINFOHEADER para ver si hay determinados errores comunes que pueden provocar saturaciones del búfer o `CheckVideoInfoType` desbordamientos de [](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) enteros.

> [!Note]  
> Esta función no garantiza que el tipo de medio sea válido o que el código que usa la estructura sea seguro.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckVideoInfoType(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntero a la [**estructura AM MEDIA TYPE \_ \_ que**](/windows/win32/api/strmif/ns-strmif-am_media_type) se validará

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT.**



| Código devuelto                                                                                                | Descripción                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Correcto.<br/>                |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>                  | **Valor de** puntero NULL.<br/> |
| <dl> <dt>**TIPO VFW \_ E \_ NO \_ \_ ACEPTADO**</dt> </dl> | Tipo de medio no válido.<br/>     |



 

## <a name="remarks"></a>Comentarios

Esta función llama [**a ValidateBitmapInfoHeader para**](validatebitmapinfoheader.md) validar la [**estructura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) en el tipo de medio. Si el tipo de formato no es FORMAT \_ VideoInfo, la función devuelve VFW \_ E TYPE NOT \_ \_ \_ ACCEPTED.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Checkbmi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de vídeo e imagen](video-and-image-functions.md)
</dt> </dl>

 

 




