---
title: gather4 (SM 4.1-ASM)
description: Recopila las cuatro textura que se utilizarían en una operación de filtrado bilineal y las empaqueta en un solo registro. | gather4 (SM 4.1-ASM)
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84387bfe027e30b338b4701ec941a9d4e1b5e242
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986439"
---
# <a name="gather4-sm41---asm"></a>gather4 (SM 4.1-ASM)

Recopila las cuatro textura que se utilizarían en una operación de filtrado bilineal y las empaqueta en un solo registro.



| gather4 \[ \_ aoffimmi (u, v) \] dest \[ . Mask \] , srcAddress \[ . swizzle \] , srcResource \[ . swizzle \] srcSampler. r |
|--------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descripción                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[en \] la dirección del resultado de la operación.<br/>                                                                                                       |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[en \] contiene las coordenadas de textura. <br/>                                                                                                                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[en \] un registro de recursos. <br/> Swizzle permite que los valores devueltos se swizzled arbitrariamente antes de que se escriban en el *destino*. <br/>            |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>     | \[en \] un registro de muestra.<br/> Este parámetro debe tener un swizzle. r (rojo), que indica que el valor del canal de R se copia en el *destino*. <br/> |



 

## <a name="remarks"></a>Observaciones

Esta operación solo funciona con texturas 2D o mapa de canal único. Para las texturas 2D solo se usan los modos de direccionamiento de la muestra y se usa el nivel superior de cualquier pirámide MIP.

Esta instrucción se comporta como la instrucción de [ejemplo](sample--sm4---asm-.md) , pero no se genera un ejemplo filtrado. Las cuatro muestras que contribuirían al filtrado se colocan en xyzw en el orden en el sentido contrario a las agujas del reloj, empezando por el ejemplo situado en la parte inferior izquierda de la ubicación consultada. Esto es lo mismo que el muestreo de puntos con diferencias de coordenadas de textura (u, v) en las siguientes ubicaciones: (-, +), (+, +), (+,-), (-,-), donde la magnitud de los deltas siempre es la mitad de un textura.

En el caso de las texturas de mapa cuando se usa una superficie bilineal, se utiliza un textura de borde de la superficie adyacente. Las esquinas usan las mismas reglas que la instrucción de **ejemplo** ; es decir, la esquina desconocida se considera el promedio de las tres esquinas de la esfera en la que se está haciendo ping.

Las restricciones de formato de textura que se aplican a las instrucciones de **ejemplo** también se aplican a la instrucción **gather4** .

En el caso de las implementaciones de hardware, las optimizaciones en el filtrado bilineal tradicional que detectan muestras directamente en textura y omiten la lectura de textura que tendrían el peso 0 no se pueden aprovechar con **gather4**. **gather4** siempre devuelve todos los textura solicitados.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





