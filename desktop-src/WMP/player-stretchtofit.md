---
title: Player.stretchToFit
description: La propiedad stretchToFit especifica o recupera un valor que indica si el vídeo mostrado por el control Reproductor de Windows Media cambia automáticamente de tamaño para ajustarse a la ventana de vídeo, cuando la ventana de vídeo es mayor que las dimensiones de la imagen de vídeo.
ms.assetid: 9ea02959-602e-4bac-a8aa-dce502d1bb54
keywords:
- Player.stretchToFit Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Player.stretchToFit
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570d0b9bf7e266af769944b675a85c0ac1518c321d11038ff94cab035dfb316c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995845"
---
# <a name="playerstretchtofit"></a>Player.stretchToFit

La propiedad **stretchToFit** especifica o recupera un valor que indica si el vídeo mostrado por el control Reproductor de Windows Media cambia automáticamente de tamaño para ajustarse a la ventana de vídeo, cuando la ventana de vídeo es mayor que las dimensiones de la imagen de vídeo.

## <a name="syntax"></a>Syntax

*player*. **stretchToFit**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un booleano de lectura **y escritura.**



| Value | Descripción                                            |
|-------|--------------------------------------------------------|
| true  | El vídeo se ajustará para ajustarse a la ventana.              |
| false | Predeterminada. El vídeo no se ajustará para ajustarse a la ventana. |



 

## <a name="remarks"></a>Comentarios

Cuando **stretchToFit** se establece en true, el control Reproductor de Windows Media mantiene la relación de aspecto original del vídeo. Si la relación de aspecto del vídeo no coincide con la relación de aspecto de la ventana de vídeo, las áreas de máscara negra pueden aparecer en la parte superior e inferior, o en la izquierda y derecha, de la imagen de vídeo.

Esta propiedad se aplica al control Reproductor de Windows Media solo cuando se inserta en una página web.

**Reproductor de Windows Media 10 Mobile:** Esta propiedad no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.1 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





