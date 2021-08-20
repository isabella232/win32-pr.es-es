---
title: gather4_po (sm5 - asm)
description: Variante de gather4, pero en lugar de admitir un desplazamiento inmediato \ -8..7\, el desplazamiento viene como un parámetro para la instrucción y también tiene un intervalo mayor de \ -32..31\.
ms.assetid: A77A32B4-BD4F-46E7-9999-13EAA8A26974
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e18859c2df7b26511f89e6e791573fe74a69f6bd548706ac65e6b268ca08e2be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089895"
---
# <a name="gather4_po-sm5---asm"></a>gather4 \_ po (sm5 - asm)

Variante de [gather4](gather4--sm5---asm-.md), pero en lugar de admitir un desplazamiento inmediato -8..7 , el desplazamiento viene como un parámetro para la instrucción y también tiene un intervalo mayor de \[ \] \[ -32..31 \] .



| gather4 \_ po dest \[ .mask , \] srcAddress \[ .swzzle \] , srcOffset \[ .swzzle \] , srcResource \[ .swlinole \] , srcSampler \[ .select \_ component\] |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                   |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[en \] La dirección del resultado de la operación.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] Un conjunto de coordenadas de textura.<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*<br/>         | \[en \] Desplazamiento.<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] Un registro de textura.<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[en \] Un registro de sampler.<br/>                         |



 

## <a name="remarks"></a>Comentarios

Los dos primeros componentes del parámetro de desplazamiento de 4 vectores suministran desplazamientos enteros de 32 bits. Los demás componentes de este parámetro se omiten.

Los 6 bits menos significativos de cada valor de desplazamiento se respetan como un valor con firma, lo que produce \[ un intervalo de -32,31. \]

Esta instrucción solo funciona con texturas 2D, a diferencia de **gather4**, que también funciona con TextureCubes.

Los únicos modos que se respetan en el muestreador son los modos de direccionamiento. Solo se usa el mip más detallado en la vista de recursos.

Si la dirección se encuentra en un centro de textura, esto no significa que los demás elementos de textura se puedan establecer en cero.

El *parámetro srcSampler* incluye el componente .select , lo que permite recuperar cualquier componente único de una textura, incluida la devolución de valores predeterminados para los \[ componentes que \_ \] faltan.

Para los formatos con componentes float32, si el valor que se captura está normalizado, desnormalizado, +-0 o +-INF, se devuelve al sombreador sin modificar. NaN se devuelve como NaN, pero se puede cambiar la representación de bits exacta del NaN. Para TextureCubes, se debe producir alguna síntesis del 4.º texel que falta en las esquinas, por lo que no se aplica la noción de devolver bits sin modificar para el texel sintetizado y se podrían vaciar los desnormados.

Use esta instrucción para ampliar el intervalo de desplazamiento **de gather4** para que sea mayor y programable. El sufijo "po" del nombre significa "desplazamiento programable".

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





