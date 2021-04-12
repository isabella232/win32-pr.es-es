---
title: Uniones RPC
description: Uniones encapsuladas y no encapsuladas y su formato con la llamada a procedimiento remoto (RPC).
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f35f0ff23132705330bf1f8566443ac8aa81d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487743"
---
# <a name="rpc-unions"></a>Uniones RPC

Tanto las uniones encapsuladas como las no encapsuladas comparten el \_ formato de<> selector de ARM de la Unión común \_ :

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

El campo Union de la Unión \_<2> consta de dos partes. Si la Unión es una Unión de estilo MIDL 1,0, los 4 bits superiores contienen la alineación del brazo de la Unión (alineación de la ARM más alineada). De lo contrario, los cuatro bits superiores son cero. Los 12 bits inferiores contienen el número de ramas de la Unión. En otras palabras:

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

El desplazamiento \_ a la \_ Descripción de ARM \_<2> campos contienen un desplazamiento con signo relativo a la descripción del tipo de ARM. Sin embargo, el campo se sobrecarga con optimización para tipos simples. Para estos, el byte superior de este campo de desplazamiento es \_ el byte de Unión mágica de FC \_ \_ (0x80) y el byte inferior del Short es el tipo de carácter de formato real del brazo. Como tal, hay dos intervalos para los valores de desplazamiento: "80 *XX*" significa que *XX* es una cadena de formato de tipo; y todo lo demás dentro del intervalo (80 FF.. 7F FF) significa un desplazamiento real. Esto hace que los desplazamientos del intervalo <80 00.. 80 FF > no disponible como desplazamiento. El compilador comprueba que a partir de la versión de MIDL 5.1.164.

La descripción predeterminada de \_ arm \_<2> campo indica el tipo de ARM de Unión para el ARM predeterminado, si existe. Si no hay ningún brazo predeterminado especificado para la Unión, el \_ campo Descripción predeterminada de arm \_<2> es 0xFFFF y se produce una excepción si el valor del modificador \_ es no coincide con ninguno de los valores de caso ARM. Si se especifica el ARM predeterminado pero está vacío, el \_ campo Descripción predeterminada de arm \_<2> es cero. De lo contrario, el \_ campo Descripción predeterminada de arm \_<2> tiene la misma semántica que el desplazamiento \_ para la descripción de \_ ARM \_<2> campos.

El siguiente es un resumen:

-   0: valor predeterminado vacío
-   FFFF: sin valor predeterminado
-   80xx-tipo simple
-   otro desplazamiento relativo

## <a name="encapsulated-unions"></a>Uniones encapsuladas

Una Unión encapsulada proviene de una sintaxis de Unión especial en IDL. De hecho, una Unión encapsulada es una estructura de agrupación con un campo discriminante al principio de la estructura y la Unión como el único miembro.

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

El tipo de conmutador de una Unión encapsulada \_<1> campo tiene dos partes. El recorte inferior proporciona el tipo de modificador real y el recorte superior proporciona el incremento de memoria para depurar, que es una cantidad que el puntero de memoria debe incrementarse para omitir el \_ campo, que incluye cualquier relleno entre el campo \_ () de la estructura construida por código auxiliar y el campo de unión real.

El \_ campo tamaño de memoria<2> es el tamaño de la Unión únicamente y es idéntico a las uniones no encapsuladas. Para obtener el tamaño total de la estructura que contiene la Unión, agregue el \_ tamaño de memoria<2> al incremento de memoria que se va a depurar, es decir, al recorte superior del tipo de modificador \_<1> campo y, a continuación, alinearse mediante la alineación correspondiente al incremento.

## <a name="nonencapsulated-unions"></a>Uniones no encapsuladas

Una Unión no encapsulada es una situación típica en la que una Unión es un argumento o un campo y el modificador es otro argumento o campo, respectivamente.

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

Donde:

El \_ tipo de modificador<1> campo es un carácter de formato para discriminante.

El modificador \_ es \_ un descriptor<> campo es un descriptor de correlación y tiene 4 o 6 bytes dependiendo de si se usa [**/Robust**](/windows/desktop/Midl/-robust) . Sin embargo, para el modificador \_ es \_ una descripción<>, si la Unión está incrustada en una estructura, el campo de desplazamiento del modificador \_ es \_ Description<> es el desplazamiento al modificador en el \_ campo de la posición de la Unión en la estructura (no desde el principio de la estructura).

El \_ campo desplazamiento a \_ tamaño \_ y descripción de \_ ARM \_<2> proporciona el desplazamiento al tamaño y la descripción de ARM de la Unión, que es idéntico al de las uniones encapsuladas y lo comparten todas las uniones no encapsuladas del mismo tipo:

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 