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
ms.openlocfilehash: a9b09804b2ee6ad9fbda394a7fb8f9f188b46453
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273103"
---
# <a name="cimagepalettepreparepalette-method"></a>Método CImagePalette.PreparePalette

El `PreparePalette` método configura una paleta, en función de un tipo de medio del filtro propietario.

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

Puntero a una cadena que contiene el nombre del dispositivo para mostrar, tal y como devuelve la función **EnumDisplayDevices de** GDI. Para usar el dispositivo de visualización principal, establezca este parámetro en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se actualizó la paleta o S \_ FALSE si la paleta no cambió.

## <a name="remarks"></a>Observaciones

Si es necesario actualizar la paleta, este método realiza las siguientes acciones:

-   Llama [**a CImagePalette::MakePalette para**](cimagepalette-makepalette.md) crear una nueva paleta lógica.
-   Envía un [**evento EC \_ PALETTE \_ CHANGED**](ec-palette-changed.md) al Administrador de Graph Filtros.
-   Llama [**a CBaseWindow::SetPalette en**](cbasewindow-setpalette.md) el objeto **CBaseWindow.**
-   Llama [**a CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) en el **objeto CDrawImage.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CImagePalette (clase)**](cimagepalette.md)
</dt> </dl>

 

 




