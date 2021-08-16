---
description: La propiedad Language de solo lectura del objeto Error devuelve el LANGID del error actual.
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
title: Propiedad Error.Language (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Language
- IMsmError.get_Language
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 966725be2378292215ffaad6c7fc96fb36fd305d2bb2b6053849816dd1fb3f70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082895"
---
# <a name="errorlanguage-property"></a>Error.Language, propiedad

La propiedad **Language** de solo lectura del [**objeto Error**](error-object.md) devuelve el **LANGID** del error actual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Error.Language
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

El valor de la **propiedad Language** es -1 a menos que el error sea de tipo msmErrorLanguageUnsupported o msmErrorLanguageFailed. Puede determinar el tipo de error llamando a la [**propiedad Type**](error-type.md) del [**objeto Error.**](error-object.md)

### <a name="c"></a>C++

Vea get Language Function (Error Object) ( Obtener función de [**\_ lenguaje [objeto de error]).**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

