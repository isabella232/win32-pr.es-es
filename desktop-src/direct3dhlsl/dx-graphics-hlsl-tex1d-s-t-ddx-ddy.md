---
title: 'tex1D (referencia HLSL): seleccione el nivel de mip'
description: Muestrea una textura 1D mediante un degradado para seleccionar el nivel de mip. | tex1D (referencia hlsl)
ms.assetid: 1fa01f39-1c01-4a2e-9f7d-ca8e887b00bb
keywords:
- tex1D HLSL
topic_type:
- apiref
api_name:
- tex1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9700f3e70c57a8ccd96d0a88d12a88bdfcbbcabb85a79d65f2b658b35d40552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489665"
---
# <a name="tex1d-hlsl-reference---select-the-mip-level"></a>tex1D (referencia HLSL): seleccione el nivel de mip

Muestrea una textura 1D mediante un degradado para seleccionar el nivel de mip.



| ret tex1D(s, t, ddx, ddy) |
|---------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                         | Descripción                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/>       | \[en \] el estado del muestreador.<br/>                                         |
| <span id="t"></span><span id="T"></span>*T*<br/>       | \[en \] la coordenada de textura.<br/>                                    |
| <span id="ddx"></span><span id="DDX"></span>*Ddx*<br/> | \[en \] Velocidad de cambio de la geometría de la superficie en la dirección x.<br/> |
| <span id="ddy"></span><span id="DDY"></span>*ddy*<br/> | \[en \] Velocidad de cambio de la geometría de la superficie en la dirección y.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor de los datos de textura.

## <a name="type-description"></a>Descripción del tipo



| Nombre | Entrada o salida | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**object**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler1D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| Ddx  | in     | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| ddy  | in     | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| Ret  | out    | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible                |
|-----------------------------------------------------------|--------------------------|
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | sí (solo sombreador de píxeles)  |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | sí (solo sombreador de píxeles) |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | sí (solo sombreador de píxeles) |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No                       |



 

1.  Se realiza una reordenación significativa del código para mover los cálculos de degradado fuera del control de flujo.
2.  Si el límite D3DPSHADERCAPS2 0 se establece con \_ D3DD3DPSHADERCAPS2 \_ 0 GRADIENTINSTRUCTIONS, el compilador asigna esta función a \_ texldd.

## <a name="remarks"></a>Comentarios

Cuando el control de flujo está presente en un sombreador, el resultado de un cálculo de degradado solicitado dentro de una ruta de acceso de rama determinada es ambiguo cuando los píxeles adyacentes pueden bajar rutas de control de flujo independientes. Por lo tanto, se considera que no es posible usar cualquier operación de sombreador de píxeles que solicite que se produzca un cálculo de degradado en una ubicación que se encuentra dentro de una construcción de control de flujo que podría variar en píxeles para una primitiva determinada que se está rasterizando. Si cualquiera de los lados de una **instrucción if** con el atributo branch usa una función de degradado, se puede generar un error del compilador. Vea [la instrucción if (DirectX HLSL).](dx-graphics-hlsl-if.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

