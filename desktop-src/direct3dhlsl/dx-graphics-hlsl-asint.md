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
ms.openlocfilehash: 492e0b5e400adc4e5c847f12880a668fb5e3b98f683a0f64dbe32ec98f28a93c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789865"
---
# <a name="asint"></a>asint

Interpreta el patrón de bits de *x* como un entero.



| ret asint(*x*) |
|----------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] El valor de entrada.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Entrada interpretada como un entero.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                  | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **uint**](/windows/desktop/WinProg/windows-data-types) | cualquiera                            |
| *Ret* | igual que la entrada *x*                                                                                              | [**int**](/windows/desktop/WinProg/windows-data-types)                                           | las mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| [Modelos de sombreador 4](dx-graphics-hlsl-sm4.md) y superiores | Sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | No        |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

