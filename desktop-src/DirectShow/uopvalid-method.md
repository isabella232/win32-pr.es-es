---
description: El método UOPValid recupera un valor que indica si la operación de usuario especificada (UOP) es válida actualmente.
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: Método UOPValid (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3051ad20c496713880407270c7054839520ce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690227"
---
# <a name="uopvalid-method"></a>Método UOPValid

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `UOPValid` método recupera un valor que indica si la operación de usuario especificada (UOP) es válida actualmente.

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*
</dt> <dd>

Especifica la operación de usuario (UOP) como un entero.



| Value | Descripción                                                                                                                                                                                                              |
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
| 10    | [**Showmenu**](showmenu-method.md) con un valor de parámetro de 2 ( \_ título de menú de DVD \_ )                                                                                                                                       |
| 11    | [**Showmenu**](showmenu-method.md) con un valor de parámetro de 3 ( \_ raíz de menú de DVD \_ )                                                                                                                                        |
| 12    | [**Showmenu**](showmenu-method.md) con un valor de parámetro de 4 ( \_ subimagen de menú de DVD \_ )                                                                                                                                  |
| 13    | [**Showmenu**](showmenu-method.md) con un valor de parámetro de 5 ( \_ audio de menú de DVD \_ )                                                                                                                                       |
| 14    | [**Showmenu**](showmenu-method.md) con un valor de parámetro de 6 ( \_ ángulo de menú de DVD \_ )                                                                                                                                       |
| 15    | [**Showmenu**](showmenu-method.md) con un valor de parámetro de 7 ( \_ capítulo de menú de DVD \_ )                                                                                                                                     |
| 16    | [**Reanudar**](resume-method.md)                                                                                                                                                                                          |
| 17    | [**SelectLeftButton**](selectleftbutton-method.md), [**SelectRightButton**](selectrightbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md) |
| 18    | [**StillOff**](stilloff-method.md)                                                                                                                                                                                      |
| 19    | [**Pausar**](pause-method.md)                                                                                                                                                                                            |
| 20    | [**CurrentAudioStream**](currentaudiostream-property.md)                                                                                                                                                                |
| 21    | [**CurrentSubpictureStream**](currentsubpicturestream-property.md)                                                                                                                                                      |
| 22    | [**CurrentAngle**](currentangle-property.md), [ **SelectParentalLevel**](selectparentallevel-method.md)                                                                                                                 |
| 23    | [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| 24    | Seleccione Preferencias del modo de vídeo.                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor booleano que indica si el control UOP permite la operación especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Segmento. h</dt> </dl> |



 

 




