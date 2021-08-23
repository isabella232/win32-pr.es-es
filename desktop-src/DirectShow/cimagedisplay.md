---
description: La clase CImageDisplay es una clase auxiliar para que los representadores de vídeo GDI administren el formato de presentación.
ms.assetid: c9221e5c-30c6-489a-89d7-132203314dc8
title: CImageDisplay (clase, Winutil.h)
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
ms.openlocfilehash: 551650e7c8b6b0f830a84aee37bf671bbc300224c9e300a3f6f841ef503a504d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428954"
---
# <a name="cimagedisplay-class"></a>CImageDisplay (clase)

![cimagedisplayclasshierarchy](images/wutil06.png)

La `CImageDisplay` clase es una clase auxiliar para que los representadores de vídeo GDI administren el formato de presentación. El objeto almacena una [**estructura VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que describe el modo de presentación actual, que se inicializa en el método constructor del objeto. El método **CheckMediaType del** objeto comprueba si un tipo de medio propuesto se puede representar de forma eficaz mediante GDI.



| Variables miembro protegidas                                       | Descripción                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ Display**](cimagedisplay-m-display.md)                    | **Estructura VIDEOINFO** que describe el formato de presentación actual.                     |
| Métodos protegidos                                                | Descripción                                                                            |
| [**CheckBitFields**](cimagedisplay-checkbitfields.md)           | Valida las máscaras de color de una **estructura VIDEOINFO.**                                |
| [**CountPrefixBits**](cimagedisplay-countprefixbits.md)         | Calcula el número de cero bits al principio de un campo de bits especificado.              |
| [**CountSetBits**](cimagedisplay-countsetbits.md)               | Devuelve el número de bits establecido en 1 en un campo de bits especificado.                          |
| Métodos públicos                                                   | Descripción                                                                            |
| [**CheckHeaderValidity**](cimagedisplay-checkheadervalidity.md) | Valida una [**estructura BITMAPINFOHEADER.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)                    |
| [**CheckMediaType**](cimagedisplay-checkmediatype.md)           | Determina si un tipo de medio propuesto es compatible con el formato de presentación.        |
| [**CheckPaletteHeader**](cimagedisplay-checkpaletteheader.md)   | Valida las entradas de la paleta en una **estructura VIDEOINFO.**                            |
| [**CheckVideoType**](cimagedisplay-checkvideotype.md)           | Comprueba si un formato **VIDEOINFO** especificado es compatible con el formato de presentación. |
| [**CImageDisplay**](cimagedisplay-cimagedisplay.md)             | Método constructor.                                                                    |
| [**GetBitMasks**](cimagedisplay-getbitmasks.md)                 | Recupera las máscaras de color para un formato **VIDEOINFO** especificado.                        |
| [**GetColourMask**](cimagedisplay-getcolourmask.md)             | Recupera las máscaras de color para el formato de presentación actual.                              |
| [**GetDisplayDepth**](cimagedisplay-getdisplaydepth.md)         | Recupera la profundidad de bits del modo de presentación actual.                                   |
| [**GetDisplayFormat**](cimagedisplay-getdisplayformat.md)       | Recupera un formato de vídeo que describe el modo de presentación actual.                      |
| [**IsPalettsed**](cimagedisplay-ispalettised.md)               | Vuelve a determinar si el formato de presentación actual está sobresaltado.                           |
| [**RefreshDisplayType**](cimagedisplay-refreshdisplaytype.md)   | Actualiza el formato de vídeo del objeto para que coincida con la pantalla especificada.                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




