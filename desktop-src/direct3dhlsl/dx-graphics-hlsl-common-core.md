---
title: Common-Shader Core
description: Common-Shader Core
ms.assetid: f3cf2969-83a4-461f-8177-d336536194ba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c2d1851025cb051a21a997f5e3a4987d3b6309e148248b3ea55c6b9ca6ad31c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950485"
---
# <a name="common-shader-core"></a>Common-Shader Core

En El modelo de sombreador 4, todas las fases del sombreador implementan la misma funcionalidad base mediante un núcleo de sombreador común. Además, cada una de las tres fases del sombreador (vértice, geometría y píxel) ofrece una funcionalidad única para cada fase, como la capacidad de generar nuevas primitivas a partir de la fase del sombreador de geometría o descartar un píxel específico en la fase del sombreador de píxeles. En el diagrama siguiente se muestra cómo fluyen los datos a través de una fase del sombreador y la relación del núcleo de sombreador común con los recursos de memoria del sombreador.

![diagrama de flujo de datos en una fase de sombreador](images/d3d10-shader-unit.png)

-   **Datos de entrada:** un sombreador de vértices recibe sus entradas de la fase del ensamblador de entrada; Los sombreadores de geometría y píxel reciben sus entradas de la fase anterior del sombreador. Entre las entradas adicionales se [incluye la semántica de](dx-graphics-hlsl-semantics.md)valor del sistema, que se puede consumir mediante la primera unidad de la canalización a la que son aplicables.
-   **Datos de salida:** los sombreadores generan resultados de salida que se pasarán a la fase posterior de la canalización. Para un sombreador de geometría, la cantidad de datos de salida de una sola invocación puede variar. Algunas salidas se interpretan mediante el núcleo de sombreador común (como la posición del vértice y el índice de la matriz de destino de representación), mientras que otras están diseñadas para ser interpretadas por una aplicación.
-   **Código de sombreador:** los sombreadores pueden leer desde la memoria, realizar operaciones aritméticas de punto flotante y entero vectoriales o operaciones de control de flujo. No hay ningún límite en el número de instrucciones que se pueden implementar en un sombreador.
-   **Muestreadores:** los muestreadores definen cómo muestrear y filtrar texturas. Se pueden enlazar hasta 16 muestreadores a un sombreador simultáneamente.
-   **Texturas:** las texturas se pueden filtrar mediante muestreadores o leerse por elemento de textura directamente con la [función intrínseca de](dx-graphics-hlsl-to-load.md) carga.
-   **Búferes:** los búferes nunca se filtran, pero se pueden leer de la memoria por elemento directamente con la [función intrínseca de](dx-graphics-hlsl-to-load.md) carga. Se pueden enlazar simultáneamente hasta 128 recursos de textura y búfer (combinados) a un sombreador.
-   **Búferes constantes:** los búferes constantes están optimizados para las variables constantes del sombreador. Se pueden enlazar hasta 16 búferes constantes a una fase del sombreador simultáneamente. Están diseñados para una actualización más frecuente desde la CPU; por lo tanto, tienen restricciones de tamaño, diseño y acceso adicionales.


Diferencias entre Direct3D 9 y Direct3D 10:

- En Direct3D 9, cada unidad de sombreador tenía un único archivo de registro constante pequeño para almacenar todas las variables de sombreador constantes. La compatibilidad de todos los sombreadores con este espacio constante limitado requería el reciclaje frecuente de constantes por parte de la CPU.
- En Direct3D 10, las constantes se almacenan en búferes inmutables en memoria y se administran como cualquier otro recurso. No hay ningún límite en el número de búferes constantes que una aplicación puede crear. Al organizar las constantes en búferes por frecuencia de actualización y uso, se puede reducir considerablemente la cantidad de ancho de banda necesario para actualizar las constantes para dar cabida a todos los sombreadores.



 

## <a name="integer-and-bitwise-support"></a>Compatibilidad con enteros y bit a bit

El núcleo común del sombreador proporciona un conjunto completo de operaciones bit a bit y enteros de 32 bits compatibles con IEEE. Estas operaciones permiten una nueva clase de algoritmos en ejemplos de hardware gráfico, como técnicas de compresión y empaquetado, FFT y control de flujo de programa de campo de bits.

Los tipos de datos **int** y **uint** de Direct3D 10 HLSL se asignan a enteros de 32 bits en hardware.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 10:<br/> En Direct3D 9, las entradas de flujo marcadas como enteros en HLSL se interpretaron como de punto flotante. En Direct3D 10, las entradas de secuencia marcadas como entero se interpretan como un entero de 32 bits.<br/> Además, los valores booleanos ahora son todos los bits establecidos o todos los bits no establecidos. Los datos convertidos en **bool** se interpretarán como true si el valor no es igual a 0,0f (los ceros positivos y negativos pueden ser false) y false en caso contrario.<br/> |



 

## <a name="bitwise-operators"></a>Operadores bit a bit

El núcleo común del sombreador admite los siguientes operadores bit a bit:



| Operador  | Función          |
|-----------|-------------------|
| ~         | No lógico       |
| <<  | Desplazamiento a la izquierda        |
| >>  | Desplazamiento a la derecha       |
| &         | Logical And       |
| \|        | Or lógico.        |
| ^         | Xor lógico       |
| <<= | Desplazamiento a la izquierda Igual  |
| >>= | Desplazamiento a la derecha Igual |
| &=        | Y iguales         |
| \|=       | O igual          |
| ^=        | Xor Equal         |



 

Los operadores bit a bit se definen para funcionar solo en tipos de datos **int** **y uint.** Si intenta usar operadores bit a bit en tipos de datos **float** o **struct,** se producirá un error. Los operadores bit a bit tienen la misma prioridad que C con respecto a otros operadores.

## <a name="binary-casts"></a>Conversión binaria

La conversión entre un entero y un tipo de punto flotante convertirá el valor numérico después de las reglas de truncamiento de C. Convertir un valor **de** float a **int** y volver a **float** es una conversión de pérdida que depende de la precisión del tipo de datos de destino. Estas son algunas de las funciones de conversión: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL).**](dx-graphics-hlsl-asuint.md)

Las conversión binarias también se pueden realizar mediante funciones intrínsecas HLSL. Esto hace que el compilador reinterprete la representación de bits de un número en el tipo de datos de destino.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Shader Model 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





