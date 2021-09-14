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
ms.openlocfilehash: 2ebc671bbfcdfc951343e7f92cc0385ace43997e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073808"
---
# <a name="actctxmanifest-property"></a>Propiedad ActCtx.Manifest

La **propiedad Manifest** se usa para establecer u obtener el contexto de activación activo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Si se puede crear un contexto de activación con el archivo de manifiesto proporcionado, el siguiente script establece la propiedad Manifest y activa la constante de activación especificada por el manifiesto. Si no se puede crear un contexto de activación a partir del manifiesto, el contexto de activación permanece establecido en el contexto de activación activo actualmente.

ActCtxObj.Manifest = "<*nombre de archivo de manifiesto*>";

Si previamente se ha creado o activado un contexto de activación, el siguiente script establece la propiedad **Manifest** en el contexto de activación actual. Si no se ha creado o activado previamente un contexto de activación, se establece la propiedad **Manifest** en una cadena vacía.

"BSTR bstrManifest = ActCtxObj.Manifest"

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID IActCtx se define como \_ 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



 

 




