---
title: Controls.currentAudioLanguage
description: La propiedad currentAudioLanguage especifica o recupera el identificador de configuración regional (LCID) del idioma de audio para la reproducción.
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- Controls.currentAudioLanguage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguage
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63c5eb53c9f408a9d50a7f738434e5dcd30fc804970b3e1ea95c985c90d62063
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750617"
---
# <a name="controlscurrentaudiolanguage"></a>Controls.currentAudioLanguage

La **propiedad currentAudioLanguage** especifica o recupera el identificador de configuración regional (LCID) del idioma de audio para la reproducción.

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de lectura y **escritura** (**long**).

## <a name="remarks"></a>Comentarios

Un LCID identifica de forma única un dialecto de idioma determinado, denominado configuración regional.

Para Windows contenido basado en medios, las propiedades y los métodos relacionados con la selección de idioma solo admiten una única salida.

Al trabajar con contenido de DVD, la especificación de un LCID hará que se seleccione la primera pista de audio disponible con el identificador de idioma especificado.

**Reproductor de Windows Media 10 Mobile:** Esta propiedad solo acepta o devuelve el LCID neutro del idioma (0).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Controls.audioLanguageCount**](controls-audiolanguagecount.md)
</dt> <dt>

[**Controls.currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls.getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls.getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls.getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





