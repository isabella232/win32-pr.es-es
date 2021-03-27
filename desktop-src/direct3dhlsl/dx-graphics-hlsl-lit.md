---
title: encender
description: Devuelve un vector de coeficiente de iluminación.
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- HLSL Lit
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dbf6f1e53218355ba1ee9ccf58dac6176007218
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904614"
---
# <a name="lit"></a>encender

Devuelve un vector de coeficiente de iluminación.



| *RET* Lit (*n \_ punto \_ l*, *n \_ punto \_ h*, *m*) |
|------------------------------------------|



 

Esta función devuelve un vector de coeficiente de iluminación (ambiente, difuso, especular, 1) donde:

-   ambiente = 1
-   difuso = n · l < 0? 0: n · CG
-   especular = n · l < 0 \| \| n · h < 0? 0: (n · h) ^ m

Donde el vector n es el vector normal, l es la dirección que se debe aclarar y h es el vector medio.

## <a name="parameters"></a>Parámetros



| Elemento                                                                       | Descripción                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ punto \_ l*<br/> | \[en \] el producto de punto de la superficie normalizada normal y el vector de luz.<br/> |
| <span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ punto \_ h*<br/> | \[en \] el producto de puntos del vector de medio ángulo y la superficie normal.<br/>       |
| <span id="m"></span><span id="M"></span>*f*<br/>                     | \[en \] un exponente especular.<br/>                                                   |



 

## <a name="return-value"></a>Valor devuelto

Vector de coeficiente de iluminación.

## <a name="type-description"></a>Descripción del tipo



| Nombre        | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *n \_ punto \_ l* | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *n \_ punto \_ h* | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *m*         | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *direcc*       | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible           |
|------------------------------------------------------------------------------------|---------------------|
| Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos | sí                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí ( \_ solo vs 1 \_ 1) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

