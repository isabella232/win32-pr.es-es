---
description: La clase CImageDisplay es una clase auxiliar para que los representadores de vídeo GDI administren el formato de presentación.
ms.assetid: c9221e5c-30c6-489a-89d7-132203314dc8
title: Clase CImageDisplay (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a7cbb28c53d8ff357d4e5174d24f92ba2d0cad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681008"
---
# <a name="cimagedisplay-class"></a>Clase CImageDisplay

![cimagedisplayclasshierarchy](images/wutil06.png)

La `CImageDisplay` clase es una clase auxiliar para que los representadores de vídeo GDI administren el formato de presentación. El objeto almacena una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que describe el modo de presentación actual, que se inicializa en el método de constructor del objeto. El método **CheckMediaType** del objeto comprueba si un tipo de medio propuesto se puede representar de forma eficaz mediante GDI.



| Variables de miembro protegidas                                       | Descripción                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ Mostrar**](cimagedisplay-m-display.md)                    | Estructura de **videoinfo** que describe el formato de presentación actual.                     |
| Métodos protegidos                                                | Descripción                                                                            |
| [**CheckBitFields**](cimagedisplay-checkbitfields.md)           | Valida las máscaras de color de una estructura de **videoinfo** .                                |
| [**CountPrefixBits**](cimagedisplay-countprefixbits.md)         | Calcula el número de bits cero al principio de un campo de bits especificado.              |
| [**CountSetBits**](cimagedisplay-countsetbits.md)               | Devuelve el número de bits establecidos en 1 en un campo de bits especificado.                          |
| Métodos públicos                                                   | Descripción                                                                            |
| [**CheckHeaderValidity**](cimagedisplay-checkheadervalidity.md) | Valida una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .                    |
| [**CheckMediaType**](cimagedisplay-checkmediatype.md)           | Determina si un tipo de medio propuesto es compatible con el formato de presentación.        |
| [**CheckPaletteHeader**](cimagedisplay-checkpaletteheader.md)   | Valida las entradas de la paleta en una estructura de **videoinfo** .                            |
| [**CheckVideoType**](cimagedisplay-checkvideotype.md)           | Comprueba si un formato de **videoinfo** especificado es compatible con el formato de presentación. |
| [**CImageDisplay**](cimagedisplay-cimagedisplay.md)             | Método de constructor.                                                                    |
| [**GetBitMasks**](cimagedisplay-getbitmasks.md)                 | Recupera las máscaras de color para un formato de **videoinfo** especificado.                        |
| [**GetColourMask**](cimagedisplay-getcolourmask.md)             | Recupera las máscaras de color para el formato de presentación actual.                              |
| [**GetDisplayDepth**](cimagedisplay-getdisplaydepth.md)         | Recupera la profundidad de bits del modo de presentación actual.                                   |
| [**GetDisplayFormat**](cimagedisplay-getdisplayformat.md)       | Recupera un formato de vídeo que describe el modo de presentación actual.                      |
| [**IsPalettised**](cimagedisplay-ispalettised.md)               | Retermines si el formato de presentación actual es de paleta.                           |
| [**RefreshDisplayType**](cimagedisplay-refreshdisplaytype.md)   | Actualiza el formato de vídeo del objeto para que coincida con la presentación especificada.                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




