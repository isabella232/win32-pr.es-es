---
title: asint
description: Interpreta el patrón de bits de x como un entero.
ms.assetid: e17e0a11-ef52-4b23-94b8-5db0b18aff4d
keywords:
- asint HLSL
topic_type:
- apiref
api_name:
- asint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce1b0ca7e1c7b3716be1a3029c5478f96e261ce5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078142"
---
# <a name="asint"></a>asint

Interpreta el patrón de bits de *x* como un entero.



| RET Asin (*x*) |
|----------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] el valor de entrada.<br/> |



 

## <a name="return-value"></a>Valor devuelto

La entrada se interpreta como un entero.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                  | Tamaño                           |
|-------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **uint**](/windows/desktop/WinProg/windows-data-types) | cualquiera                            |
| *direcc* | igual que la entrada *x*                                                                                              | [**int**](/windows/desktop/WinProg/windows-data-types)                                           | mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| Modelos de sombreador [modelo 4](dx-graphics-hlsl-sm4.md) y versiones posteriores | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | No        |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

