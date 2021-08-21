---
title: fwidth
description: Devuelve el valor absoluto de los derivados parciales del valor especificado.
ms.assetid: 7184c3b4-1720-4176-a494-7f73322a918e
keywords:
- fwidth HLSL
topic_type:
- apiref
api_name:
- fwidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: feee9a017664e71c9c96f19fda5106870c04b947dc2b668e67f376626f7ea38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120179"
---
# <a name="fwidth"></a>fwidth

Devuelve el valor absoluto de los derivados parciales del valor especificado.



| *ret* fwidth(*x*) |
|-------------------|



 

Esta función calcula lo siguiente: [**abs**](dx-graphics-hlsl-abs.md)([**ddx**](dx-graphics-hlsl-ddx.md)(*x*)) + [**abs**](dx-graphics-hlsl-abs.md)([**ddy**](dx-graphics-hlsl-ddy.md)(*x*)).

Esta función solo se admite en sombreadores de píxeles.

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] El valor especificado.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor absoluto de los derivados parciales del *parámetro x.*

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *Ret* | igual que la entrada *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible           |
|------------------------------------------------------------------------------------|---------------------|
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) y modelos de sombreador superiores | Sí                 |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | sí (solo ps \_ 2 \_ x) |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | No                  |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

