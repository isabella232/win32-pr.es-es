---
title: Texture2D::mips. Función de operador
description: Devuelve una variable de recurso de solo lectura. | Texture2D::mips. Función de operador
ms.assetid: 201996a7-741f-4457-ab77-9cd653f3682b
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
ms.openlocfilehash: 0d8c915c340e69eedc8b66a1665b6e600c0134b66cb6cd81fe6b803681e5fdeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789501"
---
# <a name="texture2dmipsoperator----function"></a>Texture2D::mips. Función de operador

Devuelve una variable de recurso de solo lectura.

## <a name="syntax"></a>Sintaxis

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint2 pos
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

Tipo: **uint2**

Posición del índice. Contiene las coordenadas (x, y).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Una variable de recurso de solo lectura.

## <a name="remarks"></a>Comentarios

### <a name="usage-example"></a>Ejemplo de uso


```
Texture2D<float4> tex;
uint mip = 2;
uint2 pos_xy = {123, 456};
float4 f = tex.mips[mip][pos_xy];
        
```



Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Texture2D](sm5-object-texture2d.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




