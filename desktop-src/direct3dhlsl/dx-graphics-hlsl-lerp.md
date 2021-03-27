---
title: lerp
description: Realiza una interpolación lineal.
ms.assetid: e369f182-b5bd-4b7f-aa77-9cfe11033bc4
keywords:
- HLSL de lerp
topic_type:
- apiref
api_name:
- lerp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c7a5251aaf410d7224b87b9ee9a8f0e8a0c947e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997084"
---
# <a name="lerp"></a>lerp

Realiza una interpolación lineal.



| *RET* lerp (*x*, *y*, *s*) |
|---------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] el primer valor de punto flotante.<br/>                                                     |
| <span id="y"></span><span id="Y"></span>*sí*<br/> | \[en \] el segundo valor de punto flotante.<br/>                                                    |
| <span id="s"></span><span id="S"></span>*seg*<br/> | \[en \] un valor que se interpola linealmente entre el parámetro *x* y el parámetro *y* .<br/> |



 

## <a name="return-value"></a>Valor devuelto

Resultado de la interpolación lineal.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *y*   | igual que la entrada *x*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *x* |
| *s*   | igual que la entrada *x*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *x* |
| *direcc* | igual que la entrada *x*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *x* |



 

## <a name="remarks"></a>Observaciones

La interpolación lineal se basa en la fórmula siguiente: x \* (1-s) + y, \* que se puede escribir de forma equivalente como x + s (y-x).

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible                   |
|------------------------------------------------------------------------------------|-----------------------------|
| Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos | sí                         |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí (vs \_ 1 1 \_ y PS \_ 1 \_ 1) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

