---
title: Controls.currentAudioLanguageIndex
description: La propiedad currentAudioLanguageIndex especifica o recupera el índice basado en uno que corresponde al idioma de audio para la reproducción.
ms.assetid: 9a1ae887-4e64-4758-a8a2-bf2e10a7a5c7
keywords:
- Controls.currentAudioLanguageIndex Reproductor de Windows Media
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
ms.openlocfilehash: e783d42b957df40320b7c26814f7f05e93b94030518f45dc4b40d76f9ed32bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763875"
---
# <a name="controlscurrentaudiolanguageindex"></a>Controls.currentAudioLanguageIndex

La **propiedad currentAudioLanguageIndex** especifica o recupera el índice basado en uno que corresponde al idioma de audio para la reproducción.

``` syntax
player.controls.currentAudioLanguageIndex
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de **lectura** y escritura (**long**).

## <a name="remarks"></a>Comentarios

Para Windows contenido basado en multimedia, las propiedades y los métodos relacionados con la selección de idioma solo admiten una única salida.

Use la **propiedad audioLanguageCount** para obtener el número de idiomas de audio admitidos.

**Reproductor de Windows Media 10 Mobile:** Esta propiedad solo acepta o devuelve 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Controls.audioLanguageCount**](controls-audiolanguagecount.md)
</dt> <dt>

[**Controls.currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Controls.getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls.getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls.getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





