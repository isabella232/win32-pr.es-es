---
description: La propiedad manifest se usa para establecer u obtener el contexto de activación activo.
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: Propiedad ActCtx. manifest
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001063"
---
# <a name="actctxmanifest-property"></a>Propiedad ActCtx. manifest

La propiedad **manifest** se usa para establecer u obtener el contexto de activación activo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Si se puede crear un contexto de activación con el archivo de manifiesto proporcionado, el siguiente script establece la propiedad manifest y activa la constante de activación especificada por el manifiesto. Si no se puede crear un contexto de activación a partir del manifiesto, el contexto de activación permanece establecido en el contexto de activación actualmente activo.

ActCtxObj. manifest = " *nombre de archivo de manifiesto* de <>";

Si un contexto de activación se ha creado o activado previamente, el siguiente script establece la propiedad **manifest** en el contexto de activación actual. Si un contexto de activación no se ha creado o activado previamente, establece la propiedad **manifest** en una cadena vacía.

"BSTR bstrManifest = ActCtxObj. manifest"

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx se define como 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



 

 




