---
title: 'tex2D (referencia de HLSL): seleccionar el nivel de MIP'
description: Muestrea una textura 2D con un degradado para seleccionar el nivel de MIP. | tex2D (referencia de HLSL)
ms.assetid: 0e8c32ed-d174-4045-9cbf-6c04586ea5bb
keywords:
- HLSL de tex2D
topic_type:
- apiref
api_name:
- tex2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5a642a92756f3f0774e5719aa1fcf9ec302eecb5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987312"
---
# <a name="tex2d-hlsl-reference---select-the-mip-level"></a>tex2D (referencia de HLSL): seleccionar el nivel de MIP

Muestrea una textura 2D con un degradado para seleccionar el nivel de MIP.



| RET tex2D (s, t, DDX, DDY) |
|---------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                         | Descripción                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*seg*<br/>       | \[en \] el estado de la muestra.<br/>                                         |
| <span id="t"></span><span id="T"></span>*h*<br/>       | \[en \] las coordenadas de textura.<br/>                                   |
| <span id="ddx"></span><span id="DDX"></span>*DDX*<br/> | \[en \] la velocidad de cambio de la geometría de la superficie en la dirección x.<br/> |
| <span id="ddy"></span><span id="DDY"></span>*ddy*<br/> | \[en \] la velocidad de cambio de la geometría de la superficie en la dirección y.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Valor de los datos de textura.

## <a name="type-description"></a>Descripción del tipo



| Nombre | Entrada o salida | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**object**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| DDX  | in     | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| ddy  | in     | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**flot**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| direcc  | out    | [**medios**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible                |
|-----------------------------------------------------------|--------------------------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí (solo sombreador de píxeles)  |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | sí (solo sombreador de píxeles) |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | sí (solo sombreador de píxeles) |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no                       |



 

1.  Se realiza una reordenación importante del código para trasladar los cálculos de degradado fuera del control de flujo.
2.  Si el extremo de D3DPSHADERCAPS2 \_ 0 se establece con D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS, el compilador asigna esta función a texldd.

## <a name="remarks"></a>Observaciones

Cuando el control de flujo está presente en un sombreador, el resultado de un cálculo de degradado solicitado dentro de una ruta de acceso de rama determinada es ambiguo cuando los píxeles adyacentes pueden reducir las rutas de acceso de control de flujo independientes. Por lo tanto, se considera que no es válido usar cualquier operación de sombreador de píxeles que solicite que se produzca un cálculo de degradado en una ubicación que se encuentre dentro de una construcción de control de flujo que podría variar en píxeles para que se rasterizase un primitivo determinado. Si uno de los lados de una instrucción **If** con el atributo Branch usa una función de degradado, puede generarse un error del compilador. Vea la [instrucción if (DirectX HLSL)](dx-graphics-hlsl-if.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

