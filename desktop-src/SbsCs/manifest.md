---
description: La propiedad Manifest se usa para establecer u obtener el contexto de activación activo.
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: Propiedad ActCtx.Manifest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.Manifest
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 77d45bd0dc97ed99ee976da4e262ed3d4819b0ec4c744a4e0a8d76b98f5bacd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977235"
---
# <a name="actctxmanifest-property"></a>Propiedad ActCtx.Manifest

La **propiedad Manifest** se usa para establecer u obtener el contexto de activación activo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Si se puede crear un contexto de activación con el archivo de manifiesto proporcionado, el siguiente script establece la propiedad Manifest y activa la constante de activación especificada por el manifiesto. Si no se puede crear un contexto de activación a partir del manifiesto, el contexto de activación permanece establecido en el contexto de activación activo actualmente.

ActCtxObj.Manifest = "<*nombre de archivo de* manifiesto>";

Si previamente se ha creado o activado un contexto de activación, el siguiente script establece la propiedad **Manifest** en el contexto de activación actual. Si no se ha creado o activado previamente un contexto de activación, se establece la propiedad **Manifest** en una cadena vacía.

"BSTR bstrManifest = ActCtxObj.Manifest"

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID IActCtx se define como \_ 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



 

 




