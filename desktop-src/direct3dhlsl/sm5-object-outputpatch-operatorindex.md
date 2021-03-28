---
title: 'OutputPatch:: Operator (función)'
description: 'Devuelve el n punto de control de la revisión. | OutputPatch:: Operator (función)'
ms.assetid: 3ac15fe8-8bab-46a2-8826-61ade927c99e
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
ms.openlocfilehash: 8194713dc4967151991fab95000fa70c40122f26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362141"
---
# <a name="outputpatchoperator--function"></a>OutputPatch:: Operator (función)

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
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[OutputPatch](sm5-object-outputpatch.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




