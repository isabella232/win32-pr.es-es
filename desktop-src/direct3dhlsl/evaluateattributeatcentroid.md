---
title: EvaluateAttributeAtCentroid función)
description: Evalúa en el píxel centroide.
ms.assetid: 6735b3f4-765f-4cd9-9f38-326a52709021
keywords:
- EvaluateAttributeAtCentroid de función HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeAtCentroid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ee95c7f2f202dfd0065e5e9c30003cc46fd29281
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419574"
---
# <a name="evaluateattributeatcentroid-function"></a>EvaluateAttributeAtCentroid función)

Evalúa en el píxel centroide.

## <a name="syntax"></a>Sintaxis

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de de\]
</dt> <dd>

Tipo: **attrib Numeric**

Valor de entrada.

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

 

 




