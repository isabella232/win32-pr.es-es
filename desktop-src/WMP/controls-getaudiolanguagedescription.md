---
title: Método Controls.getAudioLanguageDescription
description: El método getAudioLanguageDescription recupera la descripción del idioma de audio correspondiente al índice basado en uno especificado.
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- Método getAudioLanguageDescription Reproductor de Windows Media
- Método getAudioLanguageDescription Reproductor de Windows Media , clase Controls
- Clase Controls Reproductor de Windows Media método , getAudioLanguageDescription
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageDescription
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d28e82648a1047252402694f4948d2a2734f344
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967699"
---
# <a name="controlsgetaudiolanguagedescription-method"></a>Método Controls.getAudioLanguageDescription

El **método getAudioLanguageDescription** recupera la descripción del idioma de audio correspondiente al índice basado en uno especificado.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

**Number** (**long**) que especifica el índice de idioma de audio basado en uno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor String.**

## <a name="remarks"></a>Observaciones

Para Windows contenido basado en medios, las propiedades y los métodos relacionados con la selección de idioma solo admiten una única salida.

Use la **propiedad audioLanguageCount** para obtener el número de idiomas de audio admitidos y, a continuación, acceda a un idioma de audio individualmente mediante un índice basado en uno.

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Controls.audioLanguageCount**](controls-audiolanguagecount.md)
</dt> <dt>

[**Controls.currentAudioLanguage**](controls-currentaudiolanguage.md)
</dt> <dt>

[**Controls.currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls.getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls.getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





