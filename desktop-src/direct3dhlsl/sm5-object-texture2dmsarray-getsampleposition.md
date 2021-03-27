---
title: 'Texture2DMSArray:: GetSamplePosition (función)'
description: 'Obtiene la posición del ejemplo especificado. | Texture2DMSArray:: GetSamplePosition (función)'
ms.assetid: e04717be-58b0-4242-87dd-d769834ae1c2
keywords:
- GetSamplePosition de función HLSL
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ea4d45ef5523c5fa4c9ef080bba6286a050aa12c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280186"
---
# <a name="texture2dmsarraygetsampleposition-function"></a>Texture2DMSArray:: GetSamplePosition (función)

Obtiene la posición del ejemplo especificado.

## <a name="syntax"></a>Sintaxis

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*sampleindex* \[ de\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Índice de base cero de una ubicación de ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **float2**

Una ubicación de ejemplo.

## <a name="remarks"></a>Observaciones

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
