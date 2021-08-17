---
title: lerp
description: Realiza una interpolación lineal.
ms.assetid: e369f182-b5bd-4b7f-aa77-9cfe11033bc4
keywords:
- lerp HLSL
topic_type:
- apiref
api_name:
- lerp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6981ef4134bbce17cbc7fa1e17de4d55de198572716ac39cbdd44b5e552e7f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791641"
---
# <a name="lerp"></a>lerp

Realiza una interpolación lineal.



| *ret* lerp(*x*, *y*, *s*) |
|---------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[en \] el primer valor de punto flotante.<br/>                                                     |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[en \] el segundo valor de punto flotante.<br/>                                                    |
| <span id="s"></span><span id="S"></span>*s*<br/> | \[en \] Un valor que interpola linealmente entre el parámetro *x* y el *parámetro y* .<br/> |



 

## <a name="return-value"></a>Valor devuelto

Resultado de la interpolación lineal.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *y*   | igual que la entrada *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |
| *s*   | igual que la entrada *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |
| *Ret* | igual que la entrada *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |



 

## <a name="remarks"></a>Comentarios

La interpolación lineal se basa en la siguiente fórmula: x (1-s) + y s que se pueden escribir equivalentemente como \* \* x + s(y-x).

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | Sí                         |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí (frente \_ a \_ 1 1 y ps \_ \_ 1 1) |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

