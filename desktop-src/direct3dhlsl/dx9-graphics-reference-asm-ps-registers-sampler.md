---
title: Muestra (Direct3D 9 ASM-PS)
description: Una muestra es un pseudo registro de entrada para un sombreador de píxeles, que se usa para identificar la fase de muestreo.
ms.assetid: 37cc28ae-fbd0-4f81-9e8e-f9609980d84e
keywords:
- Muestra, tipo (Direct3D 9 ASM-PS)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77875eed0827ad6bcb6d89111b13b6a31232dd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077930"
---
# <a name="sampler-direct3d-9-asm-ps"></a>Muestra (Direct3D 9 ASM-PS)

Una muestra es un pseudo registro de entrada para un sombreador de píxeles, que se usa para identificar la fase de muestreo. Hay registros de fase de muestreo de sombreador de 16 píxeles: S0 a S15. Por lo tanto, se pueden leer hasta 16 superficies de textura en una sola fase de sombreador. Las instrucciones que usan un registro de muestra son texld y texldp.

La muestra debe declararse antes de usarse con la instrucción [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Muestra               |      |      |      |      | x    | x     | x    | x    | x     |



 

Los ejemplos son pseudo registros porque no se pueden leer ni escribir directamente en ellos.

Una unidad de muestreo corresponde a la fase de muestreo de textura, encapsulando el estado específico del muestreo proporcionado por [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate). Cada muestra identifica de forma única una superficie de textura única, que se establece en la muestra correspondiente mediante [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). Sin embargo, la misma superficie de textura se puede establecer en varios muestreadores.

En el momento de dibujar, no se puede establecer una textura simultáneamente como un destino de representación y una textura en una fase.

Una muestra puede aparecer como el único argumento de la instrucción de carga de textura: [texldl-PS](texldl---ps.md).

En PS \_ 3 \_ 0, si se usa una muestra, debe declararse al principio del programa del sombreador mediante la instrucción [DCL \_ samplerType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .

El muestreo de una textura con una dimensión superior a la que se encuentra en las coordenadas de textura no es válido. El muestreo de una textura con una dimensión inferior a la que se encuentra en las coordenadas de textura omitirá las coordenadas de texturas adicionales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registra](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 