---
title: Método Controls.getLanguageName
description: El método getLanguageName recupera el nombre del idioma de audio con el identificador de configuración regional (LCID) especificado.
ms.assetid: 9e142c89-92bf-476f-bae7-b94f5b5ebe01
keywords:
- Método getLanguageName Reproductor de Windows Media
- Método getLanguageName Reproductor de Windows Media , clase Controls
- Clase Controls Reproductor de Windows Media método , getLanguageName
topic_type:
- apiref
api_name:
- Controls.getLanguageName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e747860c60313a66eecf8b7d6bd289ffb47f282c8c8d7633716e5c4e60ca7674
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997485"
---
# <a name="controlsgetlanguagename-method"></a>Método Controls.getLanguageName

El **método getLanguageName** recupera el nombre del idioma de audio con el identificador de configuración regional (LCID) especificado.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = Controls.getLanguageName(
  LCID
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LCID* \[ en\]
</dt> <dd>

**Number** (**long**) que especifica el LCID.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena**.

## <a name="remarks"></a>Comentarios

Un LCID identifica de forma única un dialecto de idioma determinado, denominado configuración regional.

Para Windows contenido basado en medios, las propiedades y los métodos relacionados con la selección de idioma solo admiten una única salida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**Controls.currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
</dt> <dt>

[**Controls.getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls.getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> </dl>

 

 





