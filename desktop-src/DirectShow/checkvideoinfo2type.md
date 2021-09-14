---
description: La función CheckVideoInfo2Type comprueba un tipo de medio que contiene una estructura de formato VIDEOINFOHEADER2 para ver si hay determinados errores comunes que pueden provocar saturaciones del búfer o desbordamientos de enteros.
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: Función CheckVideoInfo2Type (Checkbmi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfo2Type
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 5ec092bdea1e3dd00de36893d1816f70ca6d7945
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255519"
---
# <a name="checkvideoinfo2type-function"></a>Función CheckVideoInfo2Type

La función comprueba un tipo de medio que contiene una estructura de formato VIDEOINFOHEADER2 para ver si hay determinados errores comunes que pueden provocar saturaciones del búfer o `CheckVideoInfo2Type` desbordamientos de [](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) enteros.

> [!Note]  
> Esta función no garantiza que el tipo de medio sea válido o que el código que usa la estructura sea seguro.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckVideoInfo2Type(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntero a la [**estructura \_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que se validará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT.**



| Código devuelto                                                                                                | Descripción                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Correcto<br/>                |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>                  | **Valor de** puntero NULL<br/> |
| <dl> <dt>**TIPO VFW \_ E \_ NO \_ \_ ACEPTADO**</dt> </dl> | Tipo de medio no válido<br/>     |



 

## <a name="remarks"></a>Observaciones

Esta función llama [**a ValidateBitmapInfoHeader para**](validatebitmapinfoheader.md) validar la [**estructura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) en el tipo de medio. Si el tipo de formato no es **FORMAT \_ VideoInfo2,** la función devuelve **VFW \_ E TYPE \_ NOT \_ \_ ACCEPTED**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Checkbmi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de vídeo e imagen](video-and-image-functions.md)
</dt> </dl>

 

 




