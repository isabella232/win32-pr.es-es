---
title: Modificadores para ps_1_X
description: Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbc8a9b13f7ffc29cf84bc839409f29bea6c8c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903881"
---
# <a name="modifiers-for-ps_1_x"></a>Modificadores para PS \_ 1 \_ X

Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino. Por ejemplo, úselos para multiplicar o dividir el resultado por un factor de dos, o para fijar el resultado entre cero y uno. Los modificadores de instrucción se aplican después de que se ejecute la instrucción, pero antes de escribir el resultado en el registro de destino.

A continuación se muestra una lista de los modificadores.



| Modificador | Descripción                   | Sintaxis           | Versión |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | 1\_1    | 1\_2 | 1 \_ 3 | 1\_4 |
| \_RCA     | Multiplicar por 2                 | instrucción \_ x2  | X       | X    | X    | X    |
| \_x4     | Multiplicar por 4                 | instrucción \_ x4  | X       | X    | X    | X    |
| \_canal     | Multiplicar por 8                 | instrucción \_ x8  |         |      |      | X    |
| \_D2     | Dividir por 2                   | instrucción \_ D2  | X       | X    | X    | X    |
| \_D4     | Dividir por 4                   | instrucción \_ D4  |         |      |      | X    |
| \_D8     | Dividir por 8                   | instrucción \_ D8  |         |      |      | X    |
| \_sábado    | Saturación (Clamp de 0 y 1) | instrucción \_ SAT | X       | X    | X    | X    |



 

-   El modificador Multiply multiplica los datos de registro por una potencia de dos después de leerlos. Es lo mismo que un desplazamiento a la izquierda.
-   El modificador de división divide los datos de registro por una potencia de dos después de leerlos. Es lo mismo que un desplazamiento a la derecha.
-   El modificador satura el intervalo de valores de registro de cero a uno.

Los modificadores de instrucción se pueden utilizar en Instrucciones aritméticas. No se pueden usar en instrucciones de dirección de textura.

Multiply (modificador)

En este ejemplo se carga el registro de destino (DEST) con la suma de los dos colores de los operandos de origen (src0 y SRC1) y se multiplica el resultado por dos.


```
add_x2 dest, src0, src1
```



En este ejemplo se combinan dos modificadores de instrucción. En primer lugar, se agregan dos colores en los operandos de origen (src0 y SRC1). El resultado se multiplica por dos y se fija entre 0,0 y 1,0 para cada componente. El resultado se guarda en el registro de destino.


```
add_x2_sat dest, src0, src1
```



Divide (modificador)

En este ejemplo se carga el registro de destino (DEST) con la suma de los dos colores de los operandos de origen (src0 y SRC1) y se divide el resultado entre dos.


```
add_d2 dest, src0, src1
```



Modificador de saturación

En el caso de las instrucciones aritméticas, el modificador de saturación fija el resultado de esta instrucción en el intervalo de 0,0 a 1,0 para cada componente. En el ejemplo siguiente se muestra cómo usar este modificador de instrucciones.


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



Esta operación se produce después de cualquier modificador de instrucción Multiply o de división. \_SAT se usa con más frecuencia para Clamp los resultados de los productos de punto. Sin embargo, también permite la emulación coherente de los métodos de Multipass en los que el búfer de fotogramas siempre está en el intervalo comprendido entre 0 y 1, y con la sintaxis multitexture de DirectX 6 y 7,0, en la que se define la saturación para que se produzca en cada fase.

En este ejemplo se carga el registro de destino (DEST) con la suma de los dos colores de los operandos de origen (src0 y SRC1) y se divide el resultado en el intervalo de 0,0 a 1,0 para cada componente.


```
add_sat dest, src0, src1
```



En este ejemplo se combinan dos modificadores de instrucción. En primer lugar, se agregan dos colores en los operandos de origen (src0 y SRC1). El resultado se multiplica por dos y se fija entre 0,0 y 1,0 para cada componente. El resultado se guarda en el registro de destino.


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




