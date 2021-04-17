---
description: El método PreparePalette configura una paleta basándose en un tipo de medio del filtro propietario.
ms.assetid: cb012391-39ab-4ad1-aeb7-ec25010ac64a
title: Método CImagePalette. PreparePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.PreparePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9b09804b2ee6ad9fbda394a7fb8f9f188b46453
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670493"
---
# <a name="cimagepalettepreparepalette-method"></a>CImagePalette. PreparePalette, método

El `PreparePalette` método configura una paleta, basándose en un tipo de medio del filtro propietario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PreparePalette(
   const CMediaType *pmtNew,
   const CMediaType *pmtOld,
         LPSTR      szDevice
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pmtNew* 
</dt> <dd>

Puntero al nuevo tipo de archivo multimedia. El bloque de formato debe ser una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .

</dd> <dt>

*pmtOld* 
</dt> <dd>

Puntero al tipo de medio anterior. Si el tipo de medio se establece por primera vez, este parámetro puede ser un tipo vacío sin bloque de formato. De lo contrario, el bloque de formato debe ser una estructura **VIDEOINFOHEADER** .

</dd> <dt>

*szDevice* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del dispositivo de pantalla, devuelto por la función **EnumDisplayDevices** de GDI. Para usar el dispositivo de pantalla principal, establezca este parámetro en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se actualizó la paleta o S \_ false si no ha cambiado la paleta.

## <a name="remarks"></a>Observaciones

Si es necesario actualizar la paleta, este método realiza las acciones siguientes:

-   Llama a [**CImagePalette:: MakePalette**](cimagepalette-makepalette.md) para crear una nueva paleta lógica.
-   Envía un evento de la [**paleta de EC \_ \_ cambiada**](ec-palette-changed.md) al administrador de gráficos de filtro.
-   Llama a [**CBaseWindow:: SetPalette**](cbasewindow-setpalette.md) en el objeto **CBaseWindow** .
-   Llama a [**CDrawImage:: IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) en el objeto **CDrawImage** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




