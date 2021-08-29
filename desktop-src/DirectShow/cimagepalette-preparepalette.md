---
description: El método PreparePalette configura una paleta, basada en un tipo de medio del filtro propietario.
ms.assetid: cb012391-39ab-4ad1-aeb7-ec25010ac64a
title: Método CImagePalette.PreparePalette (Winutil.h)
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
ms.openlocfilehash: 5cc0abd9847c535ca9851355a593bdbd3495b594669e326c73a0bf986b8f75e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916045"
---
# <a name="cimagepalettepreparepalette-method"></a>Método CImagePalette.PreparePalette

El `PreparePalette` método configura una paleta, basada en un tipo de medio del filtro propietario.

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

Puntero al nuevo tipo de medio. El bloque de formato debe ser una [**estructura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)

</dd> <dt>

*pmtOld* 
</dt> <dd>

Puntero al tipo de medio anterior. Si el tipo de medio se establece por primera vez, este parámetro puede ser un tipo vacío sin bloque de formato. De lo contrario, el bloque de formato debe ser **una estructura VIDEOINFOHEADER.**

</dd> <dt>

*szDevice* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del dispositivo para mostrar, tal como lo devuelve la función **EnumDisplayDevices de** GDI. Para usar el dispositivo de pantalla principal, establezca este parámetro en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se actualizó la paleta o S \_ FALSE si la paleta no cambió.

## <a name="remarks"></a>Comentarios

Si es necesario actualizar la paleta, este método realiza las siguientes acciones:

-   Llama [**a CImagePalette::MakePalette**](cimagepalette-makepalette.md) para crear una nueva paleta lógica.
-   Envía un [**evento EC \_ PALETTE \_ CHANGED**](ec-palette-changed.md) al Administrador de Graph filtros.
-   Llama [**a CBaseWindow::SetPalette**](cbasewindow-setpalette.md) en el **objeto CBaseWindow.**
-   Llama [**a CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) en el **objeto CDrawImage.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImagePalette (clase)**](cimagepalette.md)
</dt> </dl>

 

 




