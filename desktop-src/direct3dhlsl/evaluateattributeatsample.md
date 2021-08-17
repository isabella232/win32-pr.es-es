---
title: Función EvaluateAttributeAtSample
description: Se evalúa en la ubicación de ejemplo indizada.
ms.assetid: b5886004-5960-461d-a0d2-f4c3b0d09d94
keywords:
- Función EvaluateAttributeAtSample HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtSample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29191a3790afee2d37fee3d2ee8fb58673ff487af178bd8b1e2b33f26f1ec44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982485"
---
# <a name="evaluateattributeatsample-function"></a>Función EvaluateAttributeAtSample

Se evalúa en la ubicación de ejemplo indizada.

## <a name="syntax"></a>Sintaxis

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ En\]
</dt> <dd>

Tipo: **attrib numeric**

Valor de entrada.

</dd> <dt>

*sampleindex* \[ En\]
</dt> <dd>

Tipo: **uint**

Ubicación de ejemplo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El modo de interpolación puede **ser lineal** o lineal **sin \_ \_ perspectiva** en la variable. Se omite **el uso de centroide** **o** de ejemplo. También se permiten atributos con interpolación constante, en cuyo caso se omite el índice de ejemplo.

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | Sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




