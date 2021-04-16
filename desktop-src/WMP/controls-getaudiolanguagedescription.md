---
title: Controls. getAudioLanguageDescription (método)
description: El método getAudioLanguageDescription recupera la descripción del idioma de audio correspondiente al índice basado en uno especificado.
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- método getAudioLanguageDescription de Windows Media Player
- método getAudioLanguageDescription Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método getAudioLanguageDescription
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699513"
---
# <a name="controlsgetaudiolanguagedescription-method"></a>Controls. getAudioLanguageDescription (método)

El método **getAudioLanguageDescription** recupera la descripción del idioma de audio correspondiente al índice basado en uno especificado.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

**Número** (**largo**) que especifica el índice de idioma de audio basado en uno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un valor de **cadena** .

## <a name="remarks"></a>Observaciones

En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.

Use la propiedad **audioLanguageCount** para obtener el número de idiomas de audio admitidos y, a continuación, acceda a un idioma de audio individualmente mediante un índice basado en uno.

**Windows Media Player 10 Mobile:** Este método no se admite.

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

[**Controls. currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls. getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> <dt>

[**Controls. getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





