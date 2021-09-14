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
ms.openlocfilehash: 6c80802c41f076a2b1c0b320b591bc591da8546e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158462"
---
# <a name="errorlanguage-property"></a>Error.Language, propiedad

La propiedad **Language de solo** lectura del [**objeto Error**](error-object.md) devuelve el **LANGID** del error actual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Error.Language
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

El valor de la **propiedad Language** es -1 a menos que el error sea de tipo msmErrorLanguageUnsupported o msmErrorLanguageFailed. Puede determinar el tipo de error llamando a la [**propiedad Type**](error-type.md) del [**objeto Error.**](error-object.md)

### <a name="c"></a>C++

Vea [**get Language Function \_ (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 1.0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

