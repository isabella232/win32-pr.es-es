---
title: 'RWTexture1DArray:: Operator (función)'
description: 'Devuelve una variable de recurso. | RWTexture1DArray:: Operator (función)'
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
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986515"
---
# <a name="rwtexture1darrayoperator--function"></a>RWTexture1DArray:: Operator (función)

Devuelve una variable de recurso.

## <a name="syntax"></a>Sintaxis

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*PDV* \[ de de\]
</dt> <dd>

Tipo: **uint2**

Posición de índice. El primer componente contiene la coordenada x. El segundo componente indica el segmento de matriz deseado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **R**

Variable de recurso.

## <a name="remarks"></a>Observaciones

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[RWTexture1DArray](sm5-object-rwtexture1darray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




