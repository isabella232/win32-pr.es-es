---
title: grad3Dgrad
description: Muestrea una textura 3D mediante un degradado para seleccionar el nivel de mip. | grad3Dgrad
ms.assetid: 230c42cc-31b7-4f57-ade4-14f069094d46
keywords:
- hlSL de grado 3D
topic_type:
- apiref
api_name:
- tex3Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cd8188b7f39cc2b79eb2e961857732cd8dae9f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072722"
---
# <a name="tex3dgrad"></a>grad3Dgrad

Muestrea una textura 3D mediante un degradado para seleccionar el nivel de mip.



| ret tex3Dgrad(s, t, ddx, ddy) |
|-------------------------------|



 

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
| s    | in     | [**Objeto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler3D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| Ddx  | in     | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| ddy  | in     | [**Vector**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
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

## <a name="remarks"></a>Observaciones

Cuando el control de flujo está presente en un sombreador, el resultado de un cálculo de degradado solicitado dentro de una ruta de acceso de rama determinada es ambiguo cuando los píxeles adyacentes pueden bajar por rutas de control de flujo independientes. Por lo tanto, se considera no seguro usar cualquier operación de sombreador de píxeles que solicite que se produzca un cálculo de degradado en una ubicación que se encuentra dentro de una construcción de control de flujo que podría variar en píxeles para una primitiva determinada que se está rasterizar. Si cualquiera de los lados de una **instrucción if** con el atributo de rama usa una función de degradado, se puede generar un error del compilador. Vea [la instrucción if (DirectX HLSL).](dx-graphics-hlsl-if.md)

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

