---
title: InputPatch::Operator (Función)
description: Devuelve el enésimo punto de control de la revisión. | InputPatch::Operator (Función)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963600"
---
# <a name="inputpatchoperator--function"></a>InputPatch::Operator (Función)

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
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[InputPatch](sm5-object-inputpatch.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




