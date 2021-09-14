---
title: Uniones RPC
description: Uniones encapsuladas y nocapsuladas y su formato con llamada a procedimiento remoto (RPC).
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f35f0ff23132705330bf1f8566443ac8aa81d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071388"
---
# <a name="rpc-unions"></a>Uniones RPC

Tanto las uniones encapsuladas como las nocapsuladas comparten un selector de arm de \_ \_ unión común<> formato:

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

Los dos \_<de> de unión constan de dos partes. Si la unión es una unión de estilo MIDL 1.0, los 4 bits superiores contienen la alineación del arm de unión (alineación del mayor arm alineado). De lo contrario, los 4 bits superiores son cero. Los 12 bits inferiores contienen el número de manos en la unión. En otras palabras:

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

La descripción de desplazamiento a arm<2 campos> contienen un desplazamiento con firma relativa con respecto a la \_ descripción de tipo del \_ \_ arm. Sin embargo, el campo está sobrecargado con optimización para tipos simples. Para estos, el byte superior de este campo de desplazamiento es FC \_ MAGIC \_ UNION BYTE (0x80) y el byte inferior del short es el tipo de carácter de formato real \_ del arm. Por lo tanto, hay dos intervalos para los valores de desplazamiento: "80 *xx"* significa que *xx* es una cadena de formato de tipo; y todo lo demás dentro del intervalo (80 FF . 7f FF) significa un desplazamiento real. Esto realiza desplazamientos del intervalo <80 00 .. 80 FF > disponible como desplazamientos. El compilador lo comprueba a partir de la versión 5.1.164 de MIDL.

La descripción de arm predeterminada<campo 2> indica el tipo de arm de unión para el arm \_ \_ predeterminado, si lo hay. Si no se especifica ningún arm predeterminado para la unión, el campo predeterminado arm description<2> es 0xFFFF y se produce una excepción si el valor de switch es no coincide con ninguno de los valores de arm \_ \_ \_ case. Si se especifica el arm predeterminado pero está vacío, la descripción predeterminada del<2> \_ \_ campo es cero. De lo contrario, la descripción predeterminada del<2> campo tiene la misma semántica que el desplazamiento para la descripción de arm<\_ \_ \_ \_ \_ 2> campos.

A continuación se muestra un resumen:

-   0: valor predeterminado vacío
-   FFFF: sin valor predeterminado
-   80xx: tipo simple
-   other: desplazamiento relativo

## <a name="encapsulated-unions"></a>Uniones encapsuladas

Una unión encapsulada procede de una sintaxis de unión especial en IDL. De hecho, una unión encapsulada es una estructura de agrupación con un campo discriminante al principio de la estructura y la unión como el único miembro.

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

El tipo de modificador de una unión \_ encapsulada<1> campo tiene dos partes. El nibble inferior proporciona el tipo de modificador real, y el nibble superior proporciona el incremento de memoria para ir paso a paso, que es una cantidad que el puntero de memoria debe incrementarse para omitir más allá del campo switch is, que incluye cualquier relleno entre el campo switch is() de la estructura construida con código auxiliar y el \_ \_ campo de unión real.

El tamaño de memoria<2> campo es el tamaño de la unión solo y es idéntico a las uniones \_ nocapsuladas. Para obtener el tamaño total de la estructura que contiene la unión, agregue el tamaño de memoria<2> al incremento de memoria para ir paso a paso por instrucciones, es decir, al nibble superior del tipo de conmutador<1 campo> y, a continuación, alinee por la alineación correspondiente \_ \_ al incremento.

## <a name="nonencapsulated-unions"></a>Uniones no superadas

Una unión no superada es una situación típica en la que una unión es un argumento o campo y el modificador es otro argumento o campo, respectivamente.

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

Donde:

El tipo \_ de modificador<1> campo es un carácter de formato para el discriminador.

El modificador es descriptor<> campo es un descriptor de correlación y tiene 4 o 6 bytes, dependiendo de \_ \_ si se usa [**/robust.**](/windows/desktop/Midl/-robust) Sin embargo, para el modificador es description<>, si la unión está incrustada en una estructura, el campo de desplazamiento del modificador es description<> es el desplazamiento al modificador es field desde la posición de la unión en la estructura (no desde el principio de \_ \_ la \_ \_ \_ estructura).

El desplazamiento al tamaño y la descripción del arm<el campo 2> proporciona el desplazamiento al tamaño de la unión y la descripción del arm, que es idéntico al de las uniones encapsuladas y se comparte con todas las uniones \_ \_ \_ \_ nocapsuladas del mismo \_ tipo:

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 