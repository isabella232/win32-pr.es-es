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
ms.openlocfilehash: 81c768d138f6ee1853f9930a56f1a1864b468e8be9ff421f4dba1698b790053c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986035"
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

## <a name="remarks"></a>Comentarios

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[InputPatch](sm5-object-inputpatch.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




