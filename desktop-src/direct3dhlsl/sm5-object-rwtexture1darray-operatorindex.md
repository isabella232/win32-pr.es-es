---
title: RWTexture1DArray::Operator (Función)
description: Devuelve una variable de recurso. | RWTexture1DArray::Operator (Función)
ms.assetid: 7047e670-dd78-4b73-8d80-5575e458f27c
keywords:
- Función de operador HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f8623ab25b42f6865e401c5b263a1774206c752
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126884113"
---
# <a name="rwtexture1darrayoperator--function"></a>RWTexture1DArray::Operator (Función)

Devuelve una variable de recurso.

## <a name="syntax"></a>Sintaxis

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* \[ En\]
</dt> <dd>

Tipo: **uint2**

Posición del índice. El primer componente contiene la coordenada x. El segundo componente indica el segmento de matriz deseado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Variable de recurso.

## <a name="remarks"></a>Observaciones

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[RWTexture1DArray](sm5-object-rwtexture1darray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




