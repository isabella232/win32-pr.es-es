---
title: Referencia del sombreador de ASM
description: Los sombreadores controlan la canalización programable de gráficos.
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2941f4c32d03187ce08266bf1382cd1d94301ce0
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2019
ms.locfileid: "104983931"
---
# <a name="asm-shader-reference"></a>Referencia del sombreador de ASM

Los sombreadores controlan la canalización programable de gráficos.

## <a name="vertex-shader-reference"></a>Referencia del sombreador de vértices

-   [vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-1-1.md)
-   [vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-2-0.md)
-   [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md)
-   [vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-3-0.md)

Las [diferencias del sombreador de vértices](dx9-graphics-reference-asm-vs-differences.md) resumen las diferencias entre las versiones del sombreador de vértices.

## <a name="pixel-shader-reference"></a>Referencia del sombreador de píxeles

-   [PS \_ 1 \_ , PS \_ 1 \_ 2, PS 1 \_ \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-1-x.md)
-   [PS \_ 2 \_ 0](dx9-graphics-reference-asm-ps-2-0.md)
-   [PS \_ 2 \_ x](dx9-graphics-reference-asm-ps-2-x.md)
-   [PS \_ 3 \_ 0](dx9-graphics-reference-asm-ps-3-0.md)

Las [diferencias del sombreador de píxeles](dx9-graphics-reference-asm-ps-differences.md) resumen las diferencias entre las versiones del sombreador de píxeles.

## <a name="shader-model-4-and-5-reference"></a>Referencia del modelo de sombreador 4 y 5

Las secciones del ensamblado del modelo de [sombreador 4](dx-graphics-hlsl-sm4-asm.md) y del [modelo de sombreador modelo 5](shader-model-5-assembly--directx-hlsl-.md) describen las instrucciones que admiten el modelo de sombreador 4 y 5.

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a>Comportamiento de registros constantes en sombreadores de ensamblados

Hay dos maneras de establecer registros constantes en un sombreador de ensamblado:

-   Declare una constante de sombreador en el código de ensamblado mediante una de las instrucciones de Def \* .
-   Use uno de los métodos set de la \* \* \* API de ShaderConstant \* .

### <a name="direct3d-9-shader-constants"></a>Constantes de sombreador de Direct3D 9

En Direct3D 9, la duración de las constantes definidas en un sombreador determinado se limita solo a la ejecución de ese sombreador (y no es reemplazable). Las constantes definidas en Direct3D 9 no tienen efectos secundarios fuera del sombreador.

Este es un ejemplo de uso de Direct3D 9:


```
Given: 
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1:
    Call Set***Shader shader1
    Call Set***ShaderConstant* to set c4
    Call Draw
    Result: The shader will see the def'd value in c4

    
Given: 
    Scenario 1 has just completed
    Create shader2 (which references c4 but does not use the def instruction
      to define it) 

Scenario 2: 
    Call Set***Shader shader2
    Call Draw
    Result: The shader will see the value last set in c4 by 
     Set***ShaderConstant* in scenario 1. This is because shader 2 
     didn't def c4.
```



En Direct3D 9, al llamar a get \* \* \* ShaderConstant \* solo se recuperarán los valores constantes establecidos mediante set \* \* \* ShaderConstant \* .

### <a name="direct3d-8-shader-constants"></a>Constantes de sombreador de Direct3D 8

Este comportamiento es diferente en Direct3D 8. x.


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



En Direct3D 8. x Set \* \* \* ShaderConstant surte efecto inmediatamente. Considere el escenario siguiente:


```
Given:
    Create shader1 which references c4 and defines it with the def instruction
    
Scenario 3:
    Call Set***Shader with shader1
    Call Draw
    Result: The shader will see the def'd value in c4

Given:
    Scenario 3 has just completed
    Create shader2 (which references c4 but does not use the def instruction 
      to define it)     
    
Scenario 4 :    
    Call Set***Shader with shader2
    Call Draw
    Result: The shader will see the def'd value in c4 (set by def in shader 1)
```



El resultado no deseado es que el orden en el que se establecen los sombreadores podría afectar al comportamiento observado de los sombreadores individuales.

## <a name="shader-driver-model-requirements"></a>Requisitos del modelo del controlador del sombreador

Las interfaces de Direct3D 9 están restringidas a los controladores de la interfaz de controlador de dispositivo (DDI) que son DirectX 7 y versiones posteriores. Para comprobar el nivel de DDI, ejecute la [herramienta de diagnóstico de DirectX](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) y examine el archivo de texto guardado.

Como referencia, las interfaces de Direct3D 8 solo funcionan en los controladores DDI que son DirectX de nivel 6 y versiones posteriores.

## <a name="shader-binary-format"></a>Formato binario del sombreador

El diseño bit a bit de la secuencia de instrucciones del sombreador se define en D3d9types. h. Si quiere diseñar sus propias herramientas de construcción o compilador de sombreador y desea obtener más información sobre el flujo de tokens del sombreador, consulte el kit de desarrollo de controladores (DDK) de Direct3D 9.

## <a name="c-like-shader-language"></a>Lenguaje de sombreador de tipo C

Consulte [referencia de HLSL](dx-graphics-hlsl-reference.md) para experimentar un lenguaje de sombreador similar a C.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




