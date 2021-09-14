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
ms.openlocfilehash: b183f86599d08a6892e33c169b938dc09a2b55de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359013"
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

## <a name="remarks"></a>Observaciones

El modo de interpolación puede **ser lineal** o lineal **sin \_ \_ perspectiva** en la variable. Se omite **el uso de centroide** **o** de ejemplo. También se permiten atributos con interpolación constante, en cuyo caso se omite el índice de ejemplo.

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) y modelos de sombreador posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




