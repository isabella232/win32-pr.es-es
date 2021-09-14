---
title: Abrazadera
description: Fija el valor especificado al intervalo mínimo y máximo especificado.
ms.assetid: bcfafcec-3f9c-4b65-950c-da34184d5cdb
keywords:
- clamp HLSL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888353"
---
# <a name="clamp"></a>Abrazadera

Fija el valor especificado al intervalo mínimo y máximo especificado.



| *ret* clamp(*x,* *min*, *max*) |
|--------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                         | Descripción                                    |
|--------------------------------------------------------------|------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/>       | \[en \] Un valor que se debe fijar.<br/>            |
| <span id="min"></span><span id="MIN"></span>*Min*<br/> | \[en \] El intervalo mínimo especificado.<br/> |
| <span id="max"></span><span id="MAX"></span>*máximo*<br/> | \[en \] El intervalo máximo especificado.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor de fijación para el *parámetro x.*

## <a name="remarks"></a>Observaciones

Para los valores de -INF o INF, la fijación se comportará según lo previsto. Sin embargo, para los valores de NaN, los resultados no están definidos.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | cualquiera                            |
| *min* | igual que la entrada *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | las mismas dimensiones que la entrada *x* |
| *max* | igual que la entrada *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | las mismas dimensiones que la entrada *x* |
| *Ret* | igual que la entrada *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | las mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible             |
|------------------------------------------------------------------------------------|-----------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | sí                   |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 y ps \_ 1 \_ 4 |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

