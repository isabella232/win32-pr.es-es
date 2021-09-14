---
description: El método MakePalette crea una paleta lógica a partir de la tabla de colores en formato de vídeo.
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: Método CImagePalette.MakePalette (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20c4484b2666b25b5d713ede450a9a5a99f93348
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273116"
---
# <a name="cimagepalettemakepalette-method"></a>Método CImagePalette.MakePalette

El `MakePalette` método crea una paleta lógica a partir de la tabla de colores en formato de vídeo.

## <a name="syntax"></a>Sintaxis


```C++
HPALETTE MakePalette(
   const VIDEOINFOHEADER *pVideoInfo,
         LPSTR           szDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Puntero a una [**estructura VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contiene la tabla de colores.

</dd> <dt>

*szDevice* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del dispositivo para mostrar, tal y como devuelve la función **EnumDisplayDevices de** GDI. Para usar el dispositivo de visualización principal, establezca este parámetro en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, devuelve un identificador a la paleta. De lo contrario, devuelve **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CImagePalette (clase)**](cimagepalette.md)
</dt> </dl>

 

 




