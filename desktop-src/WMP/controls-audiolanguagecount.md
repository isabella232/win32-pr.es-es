---
title: Controls.audioLanguageCount
description: La propiedad audioLanguageCount recupera el recuento de idiomas de audio admitidos.
ms.assetid: a6dda8bf-db8c-4e97-9277-5a23dfa93156
keywords:
- Controls.audioLanguageCount Reproductor de Windows Media
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
ms.openlocfilehash: 8e4bb89c9e9af4218daf1491b53c59f252d50931995da3df9d5f84ef8e8481b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997565"
---
# <a name="controlsaudiolanguagecount"></a>Controls.audioLanguageCount

La **propiedad audioLanguageCount** recupera el recuento de idiomas de audio admitidos.

``` syntax
player.controls.audioLanguageCount
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Comentarios

Para Windows contenido basado en medios, las propiedades y los métodos relacionados con la selección de idioma solo admiten una única salida.

**Reproductor de Windows Media 10 Mobile:** Esta propiedad siempre devuelve 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Controls.currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Controls.currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls.getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls.getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls.getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





