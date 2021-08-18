---
description: Las expresiones son instrucciones matemáticas o lógicas que se usan en el lado derecho de un signo igual. Hay muchos tipos de expresiones.
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: Expresiones (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daeffeb09a2c2f496f73d492581cb2b51ac2e518e176bbbc848889bef5716b25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985705"
---
# <a name="expressions-direct3d-9"></a>Expresiones (Direct3D 9)

Las expresiones son instrucciones matemáticas o lógicas que se usan en el lado derecho de un signo igual. Hay muchos tipos de expresiones.

## <a name="expressions"></a>Expresiones

1.  Referencia de variables
    ```
    ( variable ) or<variable >
    ```

    

2.  Escalar numérico
    ```
    scalar 
    ```

    

3.  Expresión numérica

    ```
    ( numeric expression )
    ```

    

    Aquí se admiten todas las expresiones HLL numéricas estándar.

4.  Constructor
    ```
    type ( constructor arguments )
    ```

    

5.  Lista de inicializadores

    ```
    { scalar value [, scalar value ...  ] }
    
    ```

    

    Los escalares deben ser valores escalares literales.

    El número de inicializadores debe ser compatible con la variable (estado) del lado izquierdo del signo igual.

6.  Expresión OR

    ```
    token [ | token ... ]
    ```

    

    Los tokens deben ser compatibles con la variable (estado) del lado izquierdo del signo igual.

    Los tokens no distinguen mayúsculas de minúsculas.

7.  NULL

    ```
    NULL
    ```

    

    NULL solo se puede asignar a un sombreador, muestreador o un objeto de textura.

8.  Bloque de ensamblado

    ```
    asm { code }
    ```

    

    Los bloques de ensamblado ps deben asignarse al estado PIXELSHADER.

    Los bloques de ensamblado de VS deben asignarse al estado VERTEXSHADER.

9.  Sampler State Block

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    Los bloques de estado del muestreador son secuencias de asignaciones de estado de fase del muestreador sin indexar o de textura.

    Los bloques de estado del muestreador deben asignarse al estado de efecto SAMPLER.

10. Bloque de estado de efecto

    ```
    stateblock_state { [ state [ [index] ] = expression; 
        [ state [ [index] ] = ... ] ] }
    ```

    

    Los bloques de estado son secuencias de estado general. Los bloques de estado se pueden anidar, pero no pueden contener referencias circulares.

    Los bloques de estado deben asignarse al estado de efecto STATEBLOCK.

11. Compilación HLSL

    ```
    compile target entrypoint ( [ arguments ] )
    ```

    

    El sombreador de vértices frente al destino m n indica la versión del sombreador de \_ \_ vértices D3DVS \_ VERSION(m, n). El destino del sombreador de píxeles ps m n indica la versión del sombreador de \_ \_ píxeles D3DPS \_ VERSION(m, n).

    Las expresiones de compilación de lenguaje de alto nivel del sombreador de vértices solo se pueden asignar al estado de efecto VERTEXSHADER. Las expresiones de compilación de lenguaje de alto nivel del sombreador de píxeles solo se pueden asignar al estado de efecto PIXELSHADER.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



