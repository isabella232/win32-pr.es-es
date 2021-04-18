---
description: Las expresiones son instrucciones matemáticas o lógicas que se usan en el lado derecho de un signo igual. Hay muchos tipos de expresiones.
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: Expresiones (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa574069094853eb506f7a1b38cdb6cd4379d3b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677039"
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

    

    Los valores escalares deben ser valores escalares literales.

    El número de inicializadores debe ser compatible con la variable (State) en el lado izquierdo del signo igual.

6.  Expresión OR

    ```
    token [ | token ... ]
    ```

    

    Los tokens deben ser compatibles con la variable (State) en el lado izquierdo del signo igual.

    Los tokens no distinguen mayúsculas de minúsculas.

7.  NULL

    ```
    NULL
    ```

    

    NULL solo se puede asignar a un sombreador, un muestreador o un objeto de textura.

8.  Bloque de ensamblado

    ```
    asm { code }
    ```

    

    Los bloques de ensamblado de PS deben asignarse al estado u.

    Los bloques de ensamblado de VS deben asignarse al estado VERTEXSHADER.

9.  Bloque de estado de muestra

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    Los bloques de estado de muestra son secuencias de estado de la fase de muestra sin indexar o asignaciones de textura.

    Los bloques de estado de muestra se deben asignar al estado de efecto de la muestra.

10. Bloque de estado de estado de efecto

    ```
    stateblock_state { [ state [ [index] ] = expression; 
        [ state [ [index] ] = ... ] ] }
    ```

    

    Los bloques de estado son secuencias de estado general. Los bloques de estado pueden estar anidados, pero no pueden contener referencias circulares.

    Los bloques de estado deben estar asignados al estado de efecto de STATEBLOCK.

11. Compilación de HLSL

    ```
    compile target entrypoint ( [ arguments ] )
    ```

    

    El destino de sombreador de vértices + \_ m n indica la versión de \_ D3DVS \_ (m, n) versión del sombreador de vértices. El destino del sombreador de píxeles PS \_ m \_ n indica la versión \_ del sombreador de píxeles de la versión de D3DPS (m, n).

    Las expresiones de compilación del lenguaje de alto nivel del sombreador de vértices solo se pueden asignar al estado del efecto VERTEXSHADER. Las expresiones de compilación del lenguaje de alto nivel del sombreador de píxeles solo se pueden asignar al estado del efecto u.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



