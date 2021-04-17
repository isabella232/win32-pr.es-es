---
title: Controls. currentAudioLanguage
description: La propiedad currentAudioLanguage especifica o recupera el identificador de configuración regional (LCID) del idioma de audio para la reproducción.
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- Media Player de Windows Controls. currentAudioLanguage
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
ms.openlocfilehash: f1bc84c7d4c14bb742a6db37feca59fb9d0db0e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699934"
---
# <a name="controlscurrentaudiolanguage"></a>Controls. currentAudioLanguage

La propiedad **currentAudioLanguage** especifica o recupera el identificador de configuración regional (LCID) del idioma de audio para la reproducción.

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de lectura y escritura (**Long**).

## <a name="remarks"></a>Observaciones

Un LCID identifica de forma única un dialecto de lenguaje determinado, denominado configuración regional.

En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.

Al trabajar con contenido de DVD, si se especifica un LCID, se seleccionará la primera pista de audio disponible que tenga el identificador de idioma especificado.

**Windows Media Player 10 Mobile:** Esta propiedad solo acepta o devuelve el LCID independiente del idioma (0).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Controls. audioLanguageCount**](controls-audiolanguagecount.md)
</dt> <dt>

[**Controls. currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls. getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





