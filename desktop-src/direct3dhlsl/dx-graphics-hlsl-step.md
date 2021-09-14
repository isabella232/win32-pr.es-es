---
title: paso
description: Compara dos valores y devuelve 0 o 1 en función del valor mayor.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072754"
---
# <a name="step"></a>paso

Compara dos valores y devuelve 0 o 1 en función del valor mayor.



| *ret* step(*y*, *x*) |
|----------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[en \] El primer valor de punto flotante que se comparará.<br/>  |
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] El segundo valor de punto flotante que se comparará.<br/> |



 

## <a name="return-value"></a>Valor devuelto

1 si el *parámetro x* es mayor o igual que el *parámetro y;* de lo contrario, 0.

## <a name="remarks"></a>Observaciones

Esta función usa la fórmula siguiente: (*x*  >=  *y*) ? 1 : 0. La función devuelve 0 o 1 dependiendo de si el parámetro *x* es mayor que *el parámetro y.* Para calcular una interpolación sin problemas entre 0 y 1, use la función intrínseca HLSL [**smoothstep.**](dx-graphics-hlsl-smoothstep.md)

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**float**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *x*   | igual que la entrada *y*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *y* |
| *Ret* | igual que la entrada *y*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *y* |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | sí                         |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí (frente \_ a \_ 1 1 y ps \_ 1 \_ 4) |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

