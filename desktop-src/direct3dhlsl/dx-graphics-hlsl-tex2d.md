---
title: tex2D (referencia hlsl)
description: Muestrea una textura 2D.
ms.assetid: 9f4cbca8-c3de-42ed-89d9-5e86e47d12e5
keywords:
- hlsl de texas2D
topic_type:
- apiref
api_name:
- tex2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5fd0b3e8e007eff5ce85124a1108db757d51d1d8f483e83c46610556724a2b9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090506"
---
# <a name="tex2d-hlsl-reference"></a>tex2D (referencia hlsl)

Muestrea una textura 2D.



| ret tex2D(s, t) |
|-----------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/> | \[en \] el estado sampler.<br/>      |
| <span id="t"></span><span id="T"></span>*T*<br/> | \[en \] La coordenada de textura.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor de los datos de textura.

## <a name="type-description"></a>Descripción del tipo



| Nombre | Entrada o salida | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**object**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**Flotador**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| Ret  | out    | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí (solo sombreador de píxeles), pero debe usar la [opción de compilación heredada](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) al compilar. |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | sí (solo sombreador de píxeles)                                                                                                           |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | sí (solo sombreador de píxeles)                                                                                                           |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | sí (solo sombreador de píxeles)                                                                                                           |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

