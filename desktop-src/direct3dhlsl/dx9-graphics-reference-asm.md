---
title: Referencia de sombreador de Asm
description: Los sombreadores impulsan la canalización de gráficos programables.
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9dbeb680b7131581b3891e59bb6bd2db0d6e5c19eb6279c47b83d22f01b5000e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119549"
---
# <a name="asm-shader-reference"></a>Referencia de sombreador de Asm

Los sombreadores impulsan la canalización de gráficos programables.

## <a name="vertex-shader-reference"></a>Referencia del sombreador de vértices

-   [vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-1-1.md)
-   [vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-2-0.md)
-   [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md)
-   [vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-3-0.md)

[Diferencias del sombreador de](dx9-graphics-reference-asm-vs-differences.md) vértices resume las diferencias entre las versiones del sombreador de vértices.

## <a name="pixel-shader-reference"></a>Referencia del sombreador de píxeles

-   [ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4](dx9-graphics-reference-asm-ps-1-x.md)
-   [ps \_ 2 \_ 0](dx9-graphics-reference-asm-ps-2-0.md)
-   [ps \_ 2 \_ x](dx9-graphics-reference-asm-ps-2-x.md)
-   [ps \_ 3 \_ 0](dx9-graphics-reference-asm-ps-3-0.md)

[Diferencias del sombreador de](dx9-graphics-reference-asm-ps-differences.md) píxeles resume las diferencias entre las versiones del sombreador de píxeles.

## <a name="shader-model-4-and-5-reference"></a>Referencia del modelo de sombreador 4 y 5

Las secciones Ensamblado del modelo de sombreador [4](dx-graphics-hlsl-sm4-asm.md) y Ensamblado del modelo de sombreador [5](shader-model-5-assembly--directx-hlsl-.md) describen las instrucciones que admiten los modelos de sombreador 4 y 5.

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a>Comportamiento de los registros constantes en sombreadores de ensamblados

Hay dos maneras de establecer registros constantes en un sombreador de ensamblados:

-   Declare una constante de sombreador en el código de ensamblado mediante una de las instrucciones \* def.
-   Use uno de los métodos set \* \* \* ShaderConstant \* API.

### <a name="direct3d-9-shader-constants"></a>Constantes de sombreador de Direct3D 9

En Direct3D 9, la duración de las constantes definidas en un sombreador determinado se limita solo a la ejecución de ese sombreador (y no se puede invalidar). Las constantes definidas en Direct3D 9 no tienen efectos secundarios fuera del sombreador.

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



En Direct3D 9, al llamar a Get ShaderConstant solo se recuperarán los valores constantes establecidos \* \* \* mediante \* Set \* \* \* ShaderConstant \* .

### <a name="direct3d-8-shader-constants"></a>Constantes de sombreador de Direct3D 8

Este comportamiento es diferente en Direct3D 8.x.


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



En Direct3D 8.x, Establecer \* \* \* sombreadorConstant entra en vigor inmediatamente. Considere el escenario siguiente:


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



El resultado no deseado es que el orden en el que se establecen los sombreadores podría afectar al comportamiento observado de sombreadores individuales.

## <a name="shader-driver-model-requirements"></a>Requisitos del modelo de controlador de sombreador

Las interfaces de Direct3D 9 están restringidas a los controladores de la interfaz de controlador de dispositivo (DDI) que son de nivel 7 de DirectX y superiores. Para comprobar el nivel de DDI, ejecute la herramienta [de diagnóstico de DirectX](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) y examine el archivo de texto guardado.

Como referencia, las interfaces de Direct3D 8 solo funcionan en controladores DDI de nivel 6 y superiores de DirectX.

## <a name="shader-binary-format"></a>Formato binario del sombreador

El diseño bit a bit del flujo de instrucciones del sombreador se define en D3d9types.h. Si desea diseñar su propio compilador de sombreador o herramientas de construcción y desea obtener más información sobre el flujo de tokens de sombreador, consulte el Kit de desarrollo de controladores (DDK) de Direct3D 9.

## <a name="c-like-shader-language"></a>Lenguaje de sombreador de tipo C

Consulte [Referencia de HLSL para](dx-graphics-hlsl-reference.md) experimentar un lenguaje de sombreador de tipo C.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




