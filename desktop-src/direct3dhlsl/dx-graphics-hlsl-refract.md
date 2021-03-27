---
title: refract
description: Devuelve un vector de refracción mediante un rayo de entrada, una normal de superficie y un índice de refracción.
ms.assetid: 9f9467d7-dd9b-472a-bbdc-752394d382c6
keywords:
- HLSL de refract
topic_type:
- apiref
api_name:
- refract
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e499d078a020ade1ff9ff2566c3fd15b2a820d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997152"
---
# <a name="refract"></a>refract

Devuelve un vector de refracción mediante un rayo de entrada, una normal de superficie y un índice de refracción.



| *RET* refract (*i*, *n*,?) |
|----------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                                                  |
|--------------------------------------------------------|--------------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*Configur*<br/> | \[en \] un vector de dirección de rayo de punto flotante.<br/>    |
| <span id="n"></span><span id="N"></span>*n*<br/> | \[en \] un vector normal de superficie de punto flotante.<br/>   |
| *?*<br/>                                         | \[en \] un punto flotante, el índice de refracción es escalar.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Un vector de refracción de punto flotante. Si el ángulo entre la entrada del rayo i y la superficie normal n es demasiado grande para un índice de refracción determinado, el valor devuelto es (0, 0, 0).

## <a name="type-description"></a>Descripción del tipo



| Nombre              | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                           |
|-------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*               | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *n*               | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *i* |
| ?                 | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |
| Vector de refracción | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | mismas dimensiones que la entrada *i* |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible           |
|------------------------------------------------------------------------------------|---------------------|
| Modelador [modelo 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador más altos | sí                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí ( \_ solo vs 1 \_ 1) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

