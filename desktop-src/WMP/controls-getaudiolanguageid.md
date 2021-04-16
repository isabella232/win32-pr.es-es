---
title: Controls. getAudioLanguageID (método)
description: El método getAudioLanguageID recupera el identificador de configuración regional (LCID) para un índice de idioma de audio especificado.
ms.assetid: 8134a7ce-bdc7-46b2-b10e-2bf1215b0de1
keywords:
- método getAudioLanguageID de Windows Media Player
- método getAudioLanguageID Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método getAudioLanguageID
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab27e95edfc74fa7a9f57d2010bf86299c55dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699512"
---
# <a name="controlsgetaudiolanguageid-method"></a>Controls. getAudioLanguageID (método)

El método **getAudioLanguageID** recupera el identificador de configuración regional (LCID) para un índice de idioma de audio especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Controls.getAudioLanguageID(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

**Número** (**largo**) que especifica el índice del idioma de audio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **número** (**Long**).

## <a name="remarks"></a>Observaciones

Un LCID identifica de forma única un dialecto de lenguaje determinado, denominado configuración regional.

En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.

**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve el LCID independiente del idioma (0).

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

[**Controls. getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls. getLanguageName**](controls-getlanguagename.md)
</dt> </dl>

 

 





