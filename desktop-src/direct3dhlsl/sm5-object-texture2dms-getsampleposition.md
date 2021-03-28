---
title: 'Texture2DMS:: GetSamplePosition (función)'
description: Devuelve la posición de ejemplo para el índice de ejemplo proporcionado.
ms.assetid: b7821112-9b40-4302-b5c1-03bab531a0ab
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
ms.openlocfilehash: 532411e333023ff61df0b7f9fbf0336dc11d1586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533711"
---
# <a name="texture2dmsgetsampleposition-function"></a>Texture2DMS:: GetSamplePosition (función)

Devuelve la posición de ejemplo para el índice de ejemplo proporcionado.

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

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
