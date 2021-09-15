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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568357"
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
| *Ret* | igual que la entrada *x*                                                                                              | [**Int**](/windows/desktop/WinProg/windows-data-types)                                           | las mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                        | Compatible |
|---------------------------------------------------------------------|-----------|
| [Modelos de sombreador 4](dx-graphics-hlsl-sm4.md) y superiores | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | No        |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

