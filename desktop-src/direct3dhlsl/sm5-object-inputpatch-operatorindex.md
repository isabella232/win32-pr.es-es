---
title: 'InputPatch:: Operator (función)'
description: 'Devuelve el n punto de control de la revisión. | InputPatch:: Operator (función)'
ms.assetid: 2c1eda6b-a9c1-40d3-be91-7a2e8f1da9fc
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
ms.openlocfilehash: 5d95cb8adae6e7a91629614e0ae10b4161dbac3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280024"
---
# <a name="inputpatchoperator--function"></a>InputPatch:: Operator (función)

Devuelve el punto <sup>de control</sup> *n* de la revisión.

## <a name="syntax"></a>Sintaxis

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*n* \[ in\]
</dt> <dd>

Tipo: **uint**

Índice de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **T**

Punto <sup>de control</sup> n.

## <a name="remarks"></a>Observaciones

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[InputPatch](sm5-object-inputpatch.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




