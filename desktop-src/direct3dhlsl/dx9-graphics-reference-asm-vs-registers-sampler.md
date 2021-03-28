---
title: Muestra (Direct3D 9 ASM-vs)
description: Una muestra es un pseudo registro de entrada para un sombreador de vértices, que se usa para identificar la fase de muestreo. Hay cuatro muestreadores de sombreador de vértices S0 a S3. Se pueden leer cuatro superficies de textura en una sola fase de sombreador.
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- Muestra, tipo (Direct3D 9 ASM-vs)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 685f261da9d56dc29c0632d01cabbf29cd13a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421353"
---
# <a name="sampler-direct3d-9-asm-vs"></a>Muestra (Direct3D 9 ASM-vs)

Una muestra es un pseudo registro de entrada para un sombreador de vértices, que se usa para identificar la fase de muestreo. Hay cuatro muestreadores de sombreador de vértices: S0 a S3. Se pueden leer cuatro superficies de textura en una sola fase de sombreador.

El muestreador (Direct3D 9 ASM-vs) es un pseudo registro porque no se puede leer ni escribir directamente en ellos.

Una unidad de muestreo corresponde a la fase de muestreo de textura, encapsulando el estado específico del muestreo proporcionado por [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate). Cada muestra identifica de forma única una superficie de textura única, que se establece en la muestra correspondiente mediante [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). Sin embargo, la misma superficie de textura se puede establecer en varios muestreadores.

En el momento de dibujar, no se puede establecer una textura simultáneamente como un destino de representación y una textura en una fase.

Dado que hay cuatro muestras, se pueden leer hasta cuatro superficies de textura desde en una única fase del sombreador. Una muestra puede aparecer como el único argumento de la instrucción de carga de textura: [texldl-vs](texldl---vs.md).

En vs \_ 3 \_ 0, si se usa una muestra, debe declararse al principio del programa del sombreador mediante la instrucción [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md) .



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Muestra                |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[Texturas de vértices en vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 