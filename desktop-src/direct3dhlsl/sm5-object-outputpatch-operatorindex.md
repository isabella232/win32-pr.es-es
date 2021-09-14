---
title: OutputPatch::Operator (Función)
description: Devuelve el enésimo punto de control de la revisión. | OutputPatch::Operator (Función)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963591"
---
# <a name="outputpatchoperator--function"></a>OutputPatch::Operator (Función)

Devuelve el<sup>n.º</sup> punto de control de la revisión. 

## <a name="syntax"></a>Sintaxis

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*n* \[ en\]
</dt> <dd>

Tipo: **uint**

Índice de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **T**

El <sup>n.º</sup> punto de control.

## <a name="remarks"></a>Observaciones

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[OutputPatch](sm5-object-outputpatch.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




