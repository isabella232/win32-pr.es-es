---
title: Controls. audioLanguageCount
description: La propiedad audioLanguageCount recupera el número de idiomas de audio admitidos.
ms.assetid: a6dda8bf-db8c-4e97-9277-5a23dfa93156
keywords:
- Media Player de Windows Controls. audioLanguageCount
topic_type:
- apiref
api_name:
- Controls.audioLanguageCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09193eb19580d9456f25ea336fe68b8d21e06bae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699936"
---
# <a name="controlsaudiolanguagecount"></a>Controls. audioLanguageCount

La propiedad **audioLanguageCount** recupera el número de idiomas de audio admitidos.

``` syntax
player.controls.audioLanguageCount
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura (**Long**).

## <a name="remarks"></a>Observaciones

En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.

**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Controls. currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Controls. currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls. getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





