---
title: Método Controls.getLanguageName
description: El método getLanguageName recupera el nombre del idioma de audio con el identificador de configuración regional (LCID) especificado.
ms.assetid: 9e142c89-92bf-476f-bae7-b94f5b5ebe01
keywords:
- Método getLanguageName Reproductor de Windows Media
- Método getLanguageName Reproductor de Windows Media , clase Controls
- Clase Controls Reproductor de Windows Media , método getLanguageName
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
ms.openlocfilehash: 798a6b22f344953df716e4df4ed8a9a0daff2a7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967700"
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

## <a name="remarks"></a>Observaciones

Un LCID identifica de forma única un dialecto de idioma determinado, denominado configuración regional.

Para Windows contenido basado en medios, las propiedades y los métodos relacionados con la selección de idioma solo admiten una única salida.

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

[**Controls.getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
</dt> <dt>

[**Controls.getAudioLanguageID**](controls-getaudiolanguageid.md)
</dt> </dl>

 

 





