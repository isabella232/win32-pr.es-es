---
title: texCUBEgrad
description: Muestrea una textura de cubo mediante un degradado para seleccionar el nivel de mip. | texCUBEgrad
ms.assetid: ebc5e38a-e314-43b0-9a00-7e4147e24bf0
keywords:
- hlsl degrad
topic_type:
- apiref
api_name:
- texCUBEgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 831cfafcdc970a785bb702cabeac5b7ef881526421ef5ada9cb05cd1b407ce6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119889"
---
# <a name="texcubegrad"></a>texCUBEgrad

Muestrea una textura de cubo mediante un degradado para seleccionar el nivel de mip.



| ret texCUBEgrad(s, t, ddx, ddy) |
|---------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                         | Descripción                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/>       | \[en \] el estado sampler.<br/>                                         |
| <span id="t"></span><span id="T"></span>*T*<br/>       | \[en \] la coordenada de textura.<br/>                                    |
| <span id="ddx"></span><span id="DDX"></span>*Ddx*<br/> | \[en \] Velocidad de cambio de la geometría de la superficie en la dirección x.<br/> |
| <span id="ddy"></span><span id="DDY"></span>*ddy*<br/> | \[en \] Velocidad de cambio de la geometría de la superficie en la dirección y.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor de los datos de textura.

## <a name="type-description"></a>Descripción del tipo



| Nombre | Entrada o salida | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**object**](dx-graphics-hlsl-intrinsic-functions.md) | [samplerCUBE](dx-graphics-hlsl-sampler.md)                    | 1    |
| t    | in     | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| Ddx  | in     | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| ddy  | in     | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| Ret  | out    | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible                |
|-----------------------------------------------------------|--------------------------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí (solo sombreador de píxeles)  |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | sí (solo sombreador de píxeles) |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | sí (solo sombreador de píxeles) |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No                       |



 

1.  Se realiza una reordenación significativa del código para mover los cálculos de degradado fuera del control de flujo.
2.  Si el límite D3DPSHADERCAPS2 0 se establece con \_ D3DD3DPSHADERCAPS2 \_ 0 GRADIENTINSTRUCTIONS, el compilador asigna esta función \_ aldd.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

