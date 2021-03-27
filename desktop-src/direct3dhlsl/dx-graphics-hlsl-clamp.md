---
title: Sujet
description: Fija el valor especificado en el intervalo mínimo y máximo especificado.
ms.assetid: bcfafcec-3f9c-4b65-950c-da34184d5cdb
keywords:
- HLSL de abrazadera
topic_type:
- apiref
api_name:
- clamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5d6b0a3e83c0b1a5e511aba96df03b828b90c11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793306"
---
# <a name="clamp"></a>Sujet

Fija el valor especificado en el intervalo mínimo y máximo especificado.



| abrazadera *RET* (*x*, *min*, *Max*) |
|--------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                         | Descripción                                    |
|--------------------------------------------------------------|------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/>       | \[en \] un valor para la abrazadera.<br/>            |
| <span id="min"></span><span id="MIN"></span>*minuto*<br/> | \[en \] el intervalo mínimo especificado.<br/> |
| <span id="max"></span><span id="MAX"></span>*máx.*<br/> | \[en \] el intervalo máximo especificado.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor de la abrazadera del parámetro *x* .

## <a name="remarks"></a>Observaciones

En el caso de los valores de-INF o INF, la abrazadera se comportará de la manera esperada. Sin embargo, para los valores NaN, los resultados son indefinidos.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Tamaño                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | cualquiera                            |
| *min* | igual que la entrada *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mismas dimensiones que la entrada *x* |
| *max* | igual que la entrada *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mismas dimensiones que la entrada *x* |
| *direcc* | igual que la entrada *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible             |
|------------------------------------------------------------------------------------|-----------------------|
| Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos | sí                   |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 y PS \_ 1 \_ 4 |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

