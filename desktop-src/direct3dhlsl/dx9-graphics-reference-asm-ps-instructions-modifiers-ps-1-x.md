---
title: Modificadores para ps_1_X
description: Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino. Obtenga información sobre los modificadores ps_1_X.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9291d818252c95bc11fae72bd3311ec733a45fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264076"
---
# <a name="modifiers-for-ps_1_x"></a>Modificadores para ps \_ 1 \_ X

Los modificadores de instrucción afectan al resultado de la instrucción antes de que se escriba en el registro de destino. Por ejemplo, úsenlos para multiplicar o dividir el resultado por un factor de dos, o para fijar el resultado entre cero y uno. Los modificadores de instrucción se aplican después de que se ejecute la instrucción, pero antes de escribir el resultado en el registro de destino.

A continuación se muestra una lista de los modificadores.



| Modificador | Descripción                   | Sintaxis           | Versión 1 \_ 1 | Versión 1 \_ 2     |Versión 1 \_ 3    | Versión 1 \_ 4    |
|----------|-------------------------------|------------------|---------|------|------|------|
| \_x2     | Multiplicar por 2                 | instrucción \_ x2  | X       | X    | X    | X    |
| \_x4     | Multiplicar por 4                 | instrucción \_ x4  | X       | X    | X    | X    |
| \_x8     | Multiplicar por 8                 | instrucción \_ x8  |         |      |      | X    |
| \_d2     | Dividir por 2                   | instrucción \_ d2  | X       | X    | X    | X    |
| \_d4     | Dividir entre 4                   | instrucción \_ d4  |         |      |      | X    |
| \_d8     | Dividir entre 8                   | instrucción \_ d8  |         |      |      | X    |
| \_Sentado    | Saturación (fijación de 0 y 1) | instrucción \_ sat | X       | X    | X    | X    |



 

-   El modificador de multiplicación multiplica los datos de registro por una potencia de dos después de leerse. Esto es lo mismo que un desplazamiento a la izquierda.
-   El modificador de división divide los datos de registro entre una potencia de dos después de leerlos. Esto es lo mismo que un desplazamiento a la derecha.
-   El modificador saturate fija el intervalo de valores de registro de cero a uno.

Los modificadores de instrucción se pueden usar en instrucciones aritméticas. No se pueden usar en las instrucciones de dirección de textura.

Multiplicación del modificador

En este ejemplo se carga el registro de destino (dest) con la suma de los dos colores de los operandos de origen (src0 y src1) y se multiplica el resultado por dos.


```
add_x2 dest, src0, src1
```



En este ejemplo se combinan dos modificadores de instrucción. En primer lugar, se agregan dos colores en los operandos de origen (src0 y src1). A continuación, el resultado se multiplica por dos y se fija entre 0,0 y 1,0 para cada componente. El resultado se guarda en el registro de destino.


```
add_x2_sat dest, src0, src1
```



Modificador De división

En este ejemplo se carga el registro de destino (dest) con la suma de los dos colores de los operandos de origen (src0 y src1) y se divide el resultado entre dos.


```
add_d2 dest, src0, src1
```



Modificador Saturate

Para las instrucciones aritméticas, el modificador de saturación fija el resultado de esta instrucción en el intervalo de 0,0 a 1,0 para cada componente. En el ejemplo siguiente se muestra cómo usar este modificador de instrucción.


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



Esta operación se produce después de cualquier modificador de instrucción de multiplicación o división. \_sat se usa con más frecuencia para fijar los resultados del producto por puntos. Sin embargo, también permite la emulación coherente de métodos multipass donde el búfer de fotogramas siempre está en el intervalo de 0 a 1, y de la sintaxis multitexture de DirectX 6 y 7.0, en la que se define la saturación para que se produzca en cada fase.

En este ejemplo se carga el registro de destino (dest) con la suma de los dos colores de los operandos de origen (src0 y src1) y se fija el resultado en el intervalo de 0,0 a 1,0 para cada componente.


```
add_sat dest, src0, src1
```



En este ejemplo se combinan dos modificadores de instrucción. En primer lugar, se agregan dos colores en los operandos de origen (src0 y src1). El resultado se multiplica por dos y se fija entre 0,0 y 1,0 para cada componente. El resultado se guarda en el registro de destino.


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




