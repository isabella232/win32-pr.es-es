---
title: 'Texture1D:: MIPS. Operador (función)'
description: Devuelve una variable de recurso de solo lectura o una Texture1D.
ms.assetid: 0b64f0d3-f9a1-474b-b229-d91d18922d5c
keywords:
- MIPS. Función de operador HLSL
topic_type:
- apiref
api_name:
- mips.Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4713fe20fa52e948113a220969229c413c5dc4d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359644"
---
# <a name="texture1dmipsoperator----function"></a>Texture1D:: MIPS. Operador (función)

Devuelve una variable de recurso de solo lectura o una [**Texture1D**](sm5-object-texture1d.md).

## <a name="syntax"></a>Sintaxis

``` syntax
R mips.Operator[][](
  in uint mipSlice,
  in uint pos
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*mipSlice* \[ de\]
</dt> <dd>

Tipo: **uint**

Índice del segmento MIP.

</dd> <dt>

*PDV* \[ de de\]
</dt> <dd>

Tipo: **uint**

Posición de índice. Contiene la coordenada x.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Variable de recurso de solo lectura.

## <a name="remarks"></a>Observaciones

### <a name="usage-example"></a>Ejemplo de uso


```
Texture1D<float4> tex;
uint mip = 2;
uint pos = 1234;
float4 f = tex.mips[mip][pos];
      
```



Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Texture1D](sm5-object-texture1d.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




