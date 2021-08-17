---
title: Texture3D::mips. Función operator
description: Devuelve una variable de recurso de solo lectura. | Texture3D::mips. Función de operador
ms.assetid: d5f6cb3b-4163-44c2-8379-ac8a412b1aa6
keywords:
- Mips. Función de operador HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 18ad563041c8ad0b601240f4353dad5bbc44ef418c267f72d07f0f753d12d993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724505"
---
# <a name="texture3dmipsoperator----function"></a>Texture3D::mips. Función operator

Devuelve una variable de recurso de solo lectura.

## <a name="syntax"></a>Sintaxis

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint3 pos
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*mipSlice* \[ En\]
</dt> <dd>

Tipo: **uint**

Índice del segmento mip.

</dd> <dt>

*pos* \[ En\]
</dt> <dd>

Tipo: **uint3**

Posición del índice. Contiene las coordenadas (x, y, z).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Variable de recurso de solo lectura.

## <a name="remarks"></a>Comentarios

### <a name="usage-example"></a>Ejemplo de uso


```
Texture3D<float4> tex;
uint mip = 2;
uint3 pos_xyz = {123, 456, 789};
float4 f = tex.mips[mip][pos_xyz];
        
```



Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Texture3D](sm5-object-texture3d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




