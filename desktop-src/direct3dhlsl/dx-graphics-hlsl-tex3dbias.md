---
title: tex3Dbias
description: Muestrea una textura 3D después de sesgo del nivel de mip por t.w.
ms.assetid: 6a506036-90d1-420c-a712-a373068c8c16
keywords:
- tex3Dbias HLSL
topic_type:
- apiref
api_name:
- tex3Dbias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53fb0a196831a9dd9d7f7cbe7c34c56259f9a0e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072723"
---
# <a name="tex3dbias"></a>tex3Dbias

Muestrea una textura 3D después de sesgo del nivel de mip por t.w.



| ret tex3Dbias(s, t) |
|---------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                   | Descripción                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/> | \[en \] el estado del muestreador.<br/>      |
| <span id="t"></span><span id="T"></span>*T*<br/> | \[en \] la coordenada de textura.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor de los datos de textura.

## <a name="type-description"></a>Descripción del tipo



| Nombre | Entrada o salida | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Objeto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler3D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| Ret  | out    | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible               |
|-----------------------------------------------------------|-------------------------|
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | sí (solo sombreador de píxeles) |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | sí (solo sombreador de píxeles) |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | sí (solo sombreador de píxeles) |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No                      |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

