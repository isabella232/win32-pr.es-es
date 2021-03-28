---
title: distancia
description: Devuelve un escalar de distancia entre dos vectores.
ms.assetid: dda8dc39-fd72-4e92-bf9d-e700db0ede9e
keywords:
- HLSL de distancia
topic_type:
- apiref
api_name:
- distance
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0f3a64778666ac8f7de16b91eed202e36e90ed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359124"
---
# <a name="distance"></a>distancia

Devuelve un escalar de distancia entre dos vectores.



| distancia *RET* (*x*, *y*) |
|--------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                                    |
|--------------------------------------------------------|----------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x1*<br/> | \[en \] el primer vector de punto flotante que se va a comparar.<br/>  |
| <span id="y"></span><span id="Y"></span>*sí*<br/> | \[en \] el segundo vector de punto flotante que se va a comparar.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Un valor escalar y de punto flotante que representa la distancia entre el parámetro *x* y el parámetro *y* .

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *y*   | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *x* |
| *direcc* | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible |
|------------------------------------------------------------------------------------|-----------|
| Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos | sí       |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

