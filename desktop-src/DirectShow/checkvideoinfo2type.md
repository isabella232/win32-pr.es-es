---
description: La función CheckVideoInfo2Type comprueba un tipo de medio que contenga una estructura de formato VIDEOINFOHEADER2 para algunos errores comunes que pueden producir desbordamientos de búfer o desbordamientos de enteros.
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: Función CheckVideoInfo2Type (Checkbmi. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680517"
---
# <a name="checkvideoinfo2type-function"></a>CheckVideoInfo2Type función)

La `CheckVideoInfo2Type` función comprueba un tipo de medio que contiene una estructura de formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) para algunos errores comunes que pueden producir desbordamientos de búfer o desbordamientos de enteros.

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

*p.p.* 
</dt> <dd>

Puntero a la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que se va a validar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** .



| Código devuelto                                                                                                | Descripción                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | Correcto<br/>                |
| <dl> <dt>**\_puntero E**</dt> </dl>                  | Valor de puntero **nulo**<br/> |
| <dl> <dt>**\_tipo VFW \_ E \_ no \_ aceptado**</dt> </dl> | Tipo de medio no válido<br/>     |



 

## <a name="remarks"></a>Observaciones

Esta función llama a [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) para validar la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) en el tipo de medio. Si el tipo de formato no tiene el **formato \_ VideoInfo2**, la función devuelve el **\_ tipo VFW E \_ \_ no \_ aceptado**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Checkbmi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de vídeo e imagen](video-and-image-functions.md)
</dt> </dl>

 

 




