---
title: paso
description: Compara dos valores, devolviendo 0 o 1 según el valor que sea mayor.
ms.assetid: 1c1c4ec4-ae97-42ce-99af-71903e0b5edf
keywords:
- paso HLSL
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9c800e8d8c6f78386139f822f118163f3b431f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793294"
---
# <a name="step"></a>paso

Compara dos valores, devolviendo 0 o 1 según el valor que sea mayor.



| paso *RET* (*y*, *x*) |
|----------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span id="y"></span><span id="Y"></span>*sí*<br/> | \[en \] el primer valor de punto flotante que se va a comparar.<br/>  |
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] el segundo valor de punto flotante que se va a comparar.<br/> |



 

## <a name="return-value"></a>Valor devuelto

1 si el parámetro *x* es mayor o igual que el parámetro *y* ; de lo contrario, es 0.

## <a name="remarks"></a>Observaciones

Esta función usa la siguiente fórmula: (*x*  >=  *y*)? 1:0. La función devuelve 0 o 1, dependiendo de si el parámetro *x* es mayor que el parámetro *y* . Para calcular una interpolación suave entre 0 y 1, use la función intrínseca de HLSL [**smoothstep (**](dx-graphics-hlsl-smoothstep.md) .

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *x*   | igual que la entrada *y*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones como entrada *y* |
| *direcc* | igual que la entrada *y*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones como entrada *y* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible                   |
|------------------------------------------------------------------------------------|-----------------------------|
| Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos | sí                         |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí (vs \_ 1 \_ 1 y PS \_ 1 \_ 4) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

