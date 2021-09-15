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
ms.openlocfilehash: 6dbf6f1e53218355ba1ee9ccf58dac6176007218
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573061"
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
| <span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ punto \_ h*<br/> | \[en \] El producto de puntos del vector de ángulo medio y la superficie normal.<br/>       |
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
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | sí                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí (solo \_ frente a \_ 1 1) |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

