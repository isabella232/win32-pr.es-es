---
title: fmod (Corecrt, \_ Math. h)
description: Devuelve el resto de punto flotante de x/y.
ms.assetid: bb940548-c4c5-4109-a488-4ea7295c7213
keywords:
- HLSL de fmod
topic_type:
- apiref
api_name:
- fmod
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9dc4367e3aa80484098e88926567953fc8e9a90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362547"
---
# <a name="fmod"></a>fmod

Devuelve el resto de punto flotante de x/y.



| *RET* FMOD (*x*, *y*) |
|----------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                    |
|--------------------------------------------------------|------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] el dividendo de punto flotante.<br/> |
| <span id="y"></span><span id="Y"></span>*sí*<br/> | \[en \] el divisor de punto flotante.<br/>  |



 

## <a name="return-value"></a>Valor devuelto

El resto de punto flotante del parámetro *x* dividido por el parámetro *y* .

## <a name="remarks"></a>Observaciones

El resto de punto flotante se calcula de forma que x = i \* y + f, donde i es un entero, f tiene el mismo signo que x y el valor absoluto de f es menor que el valor absoluto de y.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *y*   | igual que la entrada *x*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *x* |
| *direcc* | igual que la entrada *x*                                                                                              | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos | sí       |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

