---
title: Encendido
description: Devuelve un vector de coeficiente de iluminación.
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- lit HLSL
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d3f941fe3aad52f352f5a36d3642141b31e08ef00c25dd8687c8fc7a8ed2de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791631"
---
# <a name="lit"></a>Encendido

Devuelve un vector de coeficiente de iluminación.



| *ret* lit(*n dot \_ \_ l*, *n dot \_ \_ h*, *m*) |
|------------------------------------------|



 

Esta función devuelve un vector de coeficiente de iluminación (ambiente, difuso, especular, 1) donde:

-   ambient = 1
-   difuso = n · l < 0 ? 0 : n · L
-   specular = n · l < 0 \| \| n · h < 0 ? 0 : (n · h) ^ m

Donde el vector n es el vector normal, l es la dirección a la luz y h es el vector medio.

## <a name="parameters"></a>Parámetros



| Elemento                                                                       | Descripción                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ punto \_ l*<br/> | \[en \] El producto de puntos de la superficie normalizada normal y el vector de luz.<br/> |
| <span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ punto \_ h*<br/> | \[en \] Producto de puntos del vector de medio ángulo y normal de la superficie.<br/>       |
| <span id="m"></span><span id="M"></span>*M*<br/>                     | \[en \] Un exponente especular.<br/>                                                   |



 

## <a name="return-value"></a>Valor devuelto

Vector de coeficiente de iluminación.

## <a name="type-description"></a>Descripción del tipo



| Nombre        | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *n \_ punto \_ l* | [**Escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *n \_ punto \_ h* | [**Escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *m*         | [**Escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *Ret*       | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible           |
|------------------------------------------------------------------------------------|---------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | Sí                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí (solo \_ frente a \_ 1 1) |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

