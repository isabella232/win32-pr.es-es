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
ms.openlocfilehash: e27ebe7d908c473890ac5b851eac3e0bc840c859
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903263"
---
# <a name="common-shader-core"></a>Common-Shader Core

En el modelo de sombreador 4, todas las fases del sombreador implementan la misma funcionalidad base mediante un núcleo común de sombreador. Además, cada una de las tres fases del sombreador (vértice, geometría y píxel) ofrecen una funcionalidad única para cada fase, como la capacidad de generar nuevos primitivos desde la fase del sombreador de geometría o para descartar un píxel específico en la fase del sombreador de píxeles. En el diagrama siguiente se muestra cómo fluyen los datos a través de una fase del sombreador y la relación entre el núcleo común del sombreador y los recursos de la memoria del sombreador.

![diagrama del flujo de datos en una fase del sombreador](images/d3d10-shader-unit.png)

-   **Datos de entrada**: un sombreador de vértices recibe sus entradas de la etapa ensamblador de entrada; los sombreadores de píxeles y de geometría reciben sus entradas de la fase del sombreador anterior. Entre las entradas adicionales se incluyen la [semántica de valores del sistema](dx-graphics-hlsl-semantics.md), que son consumibles por la primera unidad de la canalización a la que se aplican.
-   **Datos de salida**: los sombreadores generan resultados de salida que se van a pasar a la fase siguiente de la canalización. En el caso de un sombreador de geometría, la cantidad de datos de salida de una única invocación puede variar. Algunos resultados son interpretados por el núcleo del sombreador común (como la posición del vértice y el índice de representación-destino-matriz); otros están diseñados para ser interpretados por una aplicación.
-   **Código del sombreador**: los sombreadores pueden leer de la memoria, realizar operaciones aritméticas de punto flotante y de entero de Vector, o operaciones de control de flujo. No hay ningún límite en el número de instrucciones que se pueden implementar en un sombreador.
-   **Muestreadores**: los muestreadores definen cómo se muestra y filtra las texturas. Hasta 16 muestras se pueden enlazar a un sombreador simultáneamente.
-   **Texturas**: las texturas se pueden filtrar mediante muestreadores o leer por cada textura directamente con la función de [carga](dx-graphics-hlsl-to-load.md) intrínseca.
-   **Búferes**: los búferes nunca se filtran, pero se pueden leer de la memoria por elemento directamente con la función de [carga](dx-graphics-hlsl-to-load.md) intrínseca. Como máximo 128, se pueden enlazar varios recursos de búfer y textura (combinados) a un sombreador simultáneamente.
-   **Búferes de constantes**: los búferes de constantes están optimizados para las variables de constantes de sombreador. Hasta 16 búferes de constantes se pueden enlazar a una fase de sombreador simultáneamente. Están diseñados para una actualización más frecuente de la CPU; por lo tanto, tienen restricciones de acceso, diseño y tamaño adicionales.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 10:<br/> En Direct3D 9, cada unidad de sombreador tenía un único archivo de registro constante pequeño para almacenar todas las variables de sombreador constantes. Acomodar todos los sombreadores con este espacio constante limitado requería el reciclaje frecuente de constantes por la CPU.<br/> En Direct3D 10, las constantes se almacenan en búferes inmutables en la memoria y se administran como cualquier otro recurso. No hay ningún límite en el número de búferes de constantes que puede crear una aplicación. Mediante la organización de constantes en búferes por frecuencia de actualización y uso, la cantidad de ancho de banda necesaria para actualizar las constantes de forma que quepan todos los sombreadores se puede reducir considerablemente.<br/> |



 

## <a name="integer-and-bitwise-support"></a>Compatibilidad con enteros y bit a bit

El núcleo de sombreador común proporciona un conjunto completo de operaciones bit a bit y de enteros de 32 bits compatibles con IEEE. Estas operaciones habilitan una nueva clase de algoritmos en los ejemplos de hardware de gráficos incluyen técnicas de compresión y empaquetado, FFTs y control de flujo de programa de bits de bits.

Los tipos de datos **int** y **uint** de Direct3D 10 HLSL se asignan a enteros de 32 bits en hardware.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 10:<br/> En Direct3D 9, las entradas de flujo marcadas como enteros en HLSL se interpretaban como punto flotante. En Direct3D 10, las entradas de secuencia marcadas como Integer se interpretan como un entero de 32 bits.<br/> Además, los valores booleanos son ahora todos los bits establecidos o todos los bits no se establecen. Los datos convertidos en **bool** se interpretarán como true si el valor no es igual a 0,0 f (los cero positivos y negativos pueden ser false) y false en caso contrario.<br/> |



 

## <a name="bitwise-operators"></a>Operadores bit a bit

Common Shader Core admite los siguientes operadores bit a bit:



| Operador  | Función          |
|-----------|-------------------|
| ~         | Not lógico       |
| <<  | Desplazamiento a la izquierda        |
| >>  | Desplazamiento a la derecha       |
| &         | Logical And       |
| \|        | Or lógico.        |
| ^         | XOR lógico       |
| <<= | Igual a la izquierda  |
| >>= | Desplazamiento a la derecha |
| &=        | Y igual         |
| \|=       | O igual          |
| ^=        | XOR igual         |



 

Los operadores bit a bit se definen para funcionar solo en los tipos de datos **int** y **uint** . Si se intenta usar operadores bit a bit en tipos de datos **float** o **struct** , se producirá un error. Los operadores bit a bit siguen la misma precedencia que C con respecto a otros operadores.

## <a name="binary-casts"></a>Conversiones binarias

La conversión entre un entero y un tipo de punto flotante convertirá el valor numérico después de las reglas de truncamiento de C. Convertir un valor de **float** a **int** y volver a un valor **float** es una conversión de pérdida que depende de la precisión del tipo de datos de destino. Estas son algunas de las funciones de conversión: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**Asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).

Las conversiones binarias también se pueden realizar mediante las funciones intrínsecas de HLSL. Esto hace que el compilador reinterprete la representación de bits de un número en el tipo de datos de destino.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





