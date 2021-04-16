---
title: Controls. currentAudioLanguageIndex
description: La propiedad currentAudioLanguageIndex especifica o recupera el índice basado en uno que corresponde al lenguaje de audio para la reproducción.
ms.assetid: 9a1ae887-4e64-4758-a8a2-bf2e10a7a5c7
keywords:
- Media Player de Windows Controls. currentAudioLanguageIndex
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguageIndex
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1eb87873170c486782368f431f4fa8e3597b20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699933"
---
# <a name="controlscurrentaudiolanguageindex"></a>Controls. currentAudioLanguageIndex

La propiedad **currentAudioLanguageIndex** especifica o recupera el índice basado en uno que corresponde al lenguaje de audio para la reproducción.

``` syntax
player.controls.currentAudioLanguageIndex
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de lectura y escritura (**Long**).

## <a name="remarks"></a>Observaciones

En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.

Use la propiedad **audioLanguageCount** para obtener el número de idiomas de audio admitidos.

**Windows Media Player 10 Mobile:** Esta propiedad solo acepta o devuelve 0.

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

[**Controls. currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Controls. getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





