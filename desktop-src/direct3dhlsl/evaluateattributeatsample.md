---
title: EvaluateAttributeAtSample función)
description: Evalúa en la ubicación de ejemplo indizada.
ms.assetid: b5886004-5960-461d-a0d2-f4c3b0d09d94
keywords:
- EvaluateAttributeAtSample de función HLSL
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
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783677"
---
# <a name="evaluateattributeatsample-function"></a>EvaluateAttributeAtSample función)

Evalúa en la ubicación de ejemplo indizada.

## <a name="syntax"></a>Sintaxis

``` syntax
numeric EvaluateAttributeAtSample(
  in attrib numeric value,
  in uint sampleindex
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de de\]
</dt> <dd>

Tipo: **attrib Numeric**

Valor de entrada.

</dd> <dt>

*sampleindex* \[ de\]
</dt> <dd>

Tipo: **uint**

Ubicación de ejemplo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El modo de interpolación puede ser **lineal** o **lineal \_ sin \_ perspectiva** en la variable. Se omite el uso de **centroide** o **Sample** . También se permiten atributos con interpolación constante, en cuyo caso se omite el índice de ejemplo.

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




