---
title: determinante
description: Devuelve el determinante de la matriz cuadrada de punto flotante especificada.
ms.assetid: 9062b6f1-8518-4ee4-8d57-5aa9e2176d05
keywords:
- HLSL determinante
topic_type:
- apiref
api_name:
- determinant
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb010a0c0d0868afcb3dff488daf7926ec6c5e03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984018"
---
# <a name="determinant"></a>determinante

Devuelve el determinante de la matriz cuadrada de punto flotante especificada.



| determinante *RET* (*m*) |
|------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="m"></span><span id="M"></span>*f*<br/> | \[en \] el valor especificado.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor escalar y de punto flotante que representa el factor determinante del parámetro *m* .

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                                     |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------|
| *m*   | [**matrices**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | any (número de filas = número de columnas) |
| *direcc* | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1                                        |



 

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

 

