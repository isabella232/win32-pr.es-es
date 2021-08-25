---
description: El método UOPValid recupera un valor que indica si la operación de usuario (UOP) especificada es válida actualmente.
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: Método UOPValid (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eee8f11fbcc51c982b2a619f35fdd56b0f0eebe86945e84f18d6ce62afa783b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078675"
---
# <a name="uopvalid-method"></a>UOPValid (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El método recupera un valor que indica si la operación de usuario `UOPValid` (UOP) especificada es válida actualmente.

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*
</dt> <dd>

Especifica la operación de usuario (UOP) como un entero.



| Valor | Descripción                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | [**PlayTitle**](playtitle-method.md), [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)                                                                                      |
| 1     | [**PlayChapter**](playchapter-method.md)                                                                                                                                                                                |
| 2     | [**PlayTitle**](playtitle-method.md)                                                                                                                                                                                    |
| 3     | [**Stop**](stop-method.md)                                                                                                                                                                                              |
| 4     | [**ReturnFromSubmenu**](returnfromsubmenu-method.md)                                                                                                                                                                    |
| 5     | [**PlayChapter**](playchapter-method.md)                                                                                                                                                                                |
| 6     | [**PlayPrevChapter**](playprevchapter-method.md), [ **ReplayChapter**](replaychapter-method.md)                                                                                                                         |
| 7     | [**PlayNextChapter**](playnextchapter-method.md)                                                                                                                                                                        |
| 8     | [**PlayForwards**](playforwards-method.md)                                                                                                                                                                              |
| 9     | [**PlayBackwards**](playbackwards-method.md)                                                                                                                                                                            |
| 10    | [**ShowMenu**](showmenu-method.md) con un valor de parámetro de 2 (TÍTULO \_ DEL MENÚ DE \_ DVD)                                                                                                                                       |
| 11    | [**ShowMenu**](showmenu-method.md) con un valor de parámetro de 3 (RAÍZ \_ DE MENÚ DE \_ DVD)                                                                                                                                        |
| 12    | [**ShowMenu**](showmenu-method.md) con un valor de parámetro de 4 \_ (subpicture DVD \_ MENU)                                                                                                                                  |
| 13    | [**ShowMenu**](showmenu-method.md) con un valor de parámetro de 5 (DVD \_ MENU \_ Audio)                                                                                                                                       |
| 14    | [**ShowMenu**](showmenu-method.md) con un valor de parámetro de 6 (DVD \_ MENU \_ Angle)                                                                                                                                       |
| 15    | [**ShowMenu**](showmenu-method.md) con un valor de parámetro de 7 (capítulo DVD \_ \_ MENU)                                                                                                                                     |
| 16    | [**Reanudar**](resume-method.md)                                                                                                                                                                                          |
| 17    | [**SelectLeftButton,**](selectleftbutton-method.md) [**SelectRightButton,**](selectrightbutton-method.md) [**SelectUpperButton**](selectupperbutton-method.md)y [**SelectLowerButton**](selectlowerbutton-method.md) |
| 18    | [**StillOff**](stilloff-method.md)                                                                                                                                                                                      |
| 19    | [**Pausar**](pause-method.md)                                                                                                                                                                                            |
| 20    | [**CurrentAudioStream**](currentaudiostream-property.md)                                                                                                                                                                |
| 21    | [**CurrentSubpictureStream**](currentsubpicturestream-property.md)                                                                                                                                                      |
| 22    | [**CurrentAngle**](currentangle-property.md), [ **SelectParentalLevel**](selectparentallevel-method.md)                                                                                                                 |
| 23    | [**AudioAudioPresentationMode**](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| 24    | Seleccione la preferencia del modo de vídeo.                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si el control UOP permite la operación especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Segment.h</dt> </dl> |



 

 




