---
title: 'AppendStructuredBuffer:: Getdimensions ((función)'
description: 'Obtiene las dimensiones de recursos. | AppendStructuredBuffer:: Getdimensions ((función)'
ms.assetid: 41ed86d5-25c0-48bd-add9-792eb89605c3
keywords:
- Getdimensions (de función HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 93db905ae40f1bec7488eca292f4ea44d87950d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986207"
---
# <a name="appendstructuredbuffergetdimensions-function"></a>AppendStructuredBuffer:: Getdimensions ((función)

Obtiene las dimensiones de recursos.

## <a name="syntax"></a>Sintaxis

``` syntax
void GetDimensions(
  out uint numStructs,
  out uint stride
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*numStructs* \[ enuncia\]
</dt> <dd>

Tipo: **uint**

El número de estructuras.

</dd> <dt>

*STRIDE* \[ enuncia\]
</dt> <dd>

Tipo: **uint**

Número de bytes de cada elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[AppendStructuredBuffer](sm5-object-appendstructuredbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




