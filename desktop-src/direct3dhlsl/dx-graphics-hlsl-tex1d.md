---
title: tex1D (referencia de HLSL)
description: Muestrea una textura 1D.
ms.assetid: 587be0fd-af12-4bf0-862b-84988435e90e
keywords:
- HLSL de tex1D
topic_type:
- apiref
api_name:
- tex1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dec5cc8a35b18c35076f99443ad3c1166fcf410
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792303"
---
# <a name="tex1d-hlsl-reference"></a>tex1D (referencia de HLSL)

Muestrea una textura 1D.



| RET tex1D (s, t) |
|-----------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*seg*<br/> | \[en \] el estado de la muestra.<br/>      |
| <span id="t"></span><span id="T"></span>*h*<br/> | \[en \] la coordenada de textura.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor de los datos de textura.

## <a name="type-description"></a>Descripción del tipo



| Nombre | Entrada o salida | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**object**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler1D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| direcc  | out    | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí (solo sombreador de píxeles), pero debe utilizar la [opción de compilación heredada](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) al compilar. |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | sí (solo sombreador de píxeles)                                                                                                           |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | sí (solo sombreador de píxeles)                                                                                                           |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | sí (solo sombreador de píxeles)                                                                                                           |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

