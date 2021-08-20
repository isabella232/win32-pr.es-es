---
title: Función Texture2DMSArray::GetSamplePosition
description: Obtiene la posición del ejemplo especificado. | Función Texture2DMSArray::GetSamplePosition
ms.assetid: e04717be-58b0-4242-87dd-d769834ae1c2
keywords:
- Función GetSamplePosition HLSL
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9da6727120dcb19d9dd51c83d62f85d842036edb2197d33e298259480b248642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508421"
---
# <a name="texture2dmsarraygetsampleposition-function"></a>Función Texture2DMSArray::GetSamplePosition

Obtiene la posición del ejemplo especificado.

## <a name="syntax"></a>Sintaxis

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*sampleindex* \[ En\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Índice de base cero de una ubicación de ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **float2**

Ubicación de ejemplo.

## <a name="remarks"></a>Comentarios

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
