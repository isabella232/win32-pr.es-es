---
title: fwidth
description: Devuelve el valor absoluto de los derivados parciales del valor especificado.
ms.assetid: 7184c3b4-1720-4176-a494-7f73322a918e
keywords:
- HLSL de fwidth
topic_type:
- apiref
api_name:
- fwidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf2d5a34e1f387aadb3b044ddd1264616a61109b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149476"
---
# <a name="fwidth"></a>fwidth

Devuelve el valor absoluto de los derivados parciales del valor especificado.



| *RET* fwidth (*x*) |
|-------------------|



 

Esta función calcula lo siguiente: [**ABS**](dx-graphics-hlsl-abs.md)([**DDX**](dx-graphics-hlsl-ddx.md)(*x*)) + [**ABS**](dx-graphics-hlsl-abs.md)([**DDY**](dx-graphics-hlsl-ddy.md)(*x*)).

Esta función solo se admite en sombreadores de píxeles.

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] el valor especificado.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor absoluto de los derivados parciales del parámetro *x* .

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *direcc* | igual que la entrada *x*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible           |
|------------------------------------------------------------------------------------|---------------------|
| Modelador [modelo 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) y modelos de sombreador más altos | sí                 |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | sí ( \_ solo PS 2 \_ x) |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | No                  |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

