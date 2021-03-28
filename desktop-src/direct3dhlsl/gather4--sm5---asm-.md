---
title: gather4 (SM5-ASM)
description: Recopila las cuatro textura que se utilizarían en una operación de filtrado bilineal y las empaqueta en un solo registro. | gather4 (SM5-ASM)
ms.assetid: 5F93BB70-7696-48E4-BCD3-91D5D42FF63E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5657265738f12331afc7596286f02170de2a635
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280012"
---
# <a name="gather4-sm5---asm"></a>gather4 (SM5-ASM)

Recopila las cuatro textura que se utilizarían en una operación de filtrado bilineal y las empaqueta en un solo registro. Esta instrucción solo funciona con texturas 2D o mapa, incluidas las matrices. Solo se usan los modos de direccionamiento de la muestra y se usa el nivel superior de cualquier pirámide de MIP.



| gather4 \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] , srcSampler \[ . Select ( \_ componente)\] |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[en \] la dirección de los resultados de la operación.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] un conjunto de coordenadas de textura.<br/>                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] un registro de textura.<br/>                          |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[en \] un registro de muestra.<br/>                          |



 

## <a name="remarks"></a>Observaciones

Esta instrucción se comporta como la instrucción de [**ejemplo**](sample--sm4---asm-.md) , pero no se genera un ejemplo filtrado. Las cuatro muestras que contribuirían al filtrado se colocan en xyzw en el orden en el sentido contrario a las agujas del reloj, empezando por el ejemplo situado en la parte inferior izquierda de la ubicación consultada. Esto es lo mismo que el muestreo de puntos con diferencias de coordenadas de textura (u, v) en las siguientes ubicaciones: (-, +), (+, +), (+,-), (-,-), donde la magnitud de los deltas siempre es la mitad de un textura.

En el caso de las texturas de mapa, cuando una superficie bilineal abarca un borde, se usan textura desde la superficie adyacente. Las esquinas usan las mismas reglas que la instrucción de [**ejemplo**](sample--sm4---asm-.md) ; es decir, la esquina desconocida se considera el promedio de las tres esquinas de la esfera en la que se está haciendo ping.

Hay restricciones de formato de textura que se aplican a **gather4** , que se expresan en la lista de formatos.

Swizzle en *srcResource* permite que los valores devueltos se swizzled arbitrariamente antes de que se escriban en el destino.

El componente. Select \_ de *srcSampler* elige qué componente de la textura de origen (r/g/b/a) se leerá 4 textura.

En el caso de los formatos con componentes float32, si el valor que se va a capturar es normalizado, desnormalizado, +-0 o +-INF, se devuelve al sombreador sin modificar. NaN se devuelve como NaN, pero se puede cambiar la representación de bits exacta del NaN. En el caso de TextureCubes, algunas síntesis de la cuarta textura que faltan deben aparecer en las esquinas, por lo que no se aplican los bits que no han cambiado para la textura sintetizada, y se pueden vaciar las denormalidades.

En el caso de las implementaciones de hardware, las optimizaciones en el filtrado bilineal tradicional que detectan los ejemplos directamente en textura y omiten la lectura de textura que tendrían el peso 0 no se pueden aprovechar con esta instrucción. *gather4* siempre devuelve todos los textura solicitados.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta instrucción es compatible con los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





