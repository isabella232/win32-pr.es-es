---
title: Función Texture2DMS::GetSamplePosition
description: Devuelve la posición del ejemplo para el índice de ejemplo proporcionado.
ms.assetid: b7821112-9b40-4302-b5c1-03bab531a0ab
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
ms.openlocfilehash: 0e43882db0388bd8c7c9b53df571093d93384487121c72c0bc8a72cbae7950f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905232"
---
# <a name="texture2dmsgetsampleposition-function"></a>Función Texture2DMS::GetSamplePosition

Devuelve la posición del ejemplo para el índice de ejemplo proporcionado.

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

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
