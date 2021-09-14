---
title: Función EvaluateAttributeAtCentroid
description: Se evalúa en el centroide de píxeles.
ms.assetid: 6735b3f4-765f-4cd9-9f38-326a52709021
keywords:
- Función EvaluateAttributeAtCentroid HLSL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974682"
---
# <a name="evaluateattributeatcentroid-function"></a>Función EvaluateAttributeAtCentroid

Se evalúa en el centroide de píxeles.

## <a name="syntax"></a>Sintaxis

``` syntax
numeric EvaluateAttributeAtCentroid(
  in attrib numeric value
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ En\]
</dt> <dd>

Tipo: **attrib numeric**

Valor de entrada.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El modo de interpolación puede **ser lineal** o lineal **sin \_ \_ perspectiva** en la variable. Se omite **el uso de centroid** **o** sample. También se permiten atributos con interpolación constante, en cuyo caso se omite el índice de ejemplo.

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                | Compatible |
|-----------------------------------------------------------------------------|-----------|
| [Modelos de sombreador 5](d3d11-graphics-reference-sm5.md) y superiores | sí       |



 

Esta función se admite en los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader Model 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




