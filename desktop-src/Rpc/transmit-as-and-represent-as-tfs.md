---
title: Transmit_as y Represent_as
description: Transmita como y represente como recurso compartido el mismo diseño, excepto para el token inicial; el token lee FC TRANSMIT AS o FC REPRESENT AS, pero el código subyacente \_ \_ es \_ \_ \_ \_ común.
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69267741536314c3e30e2270e7be61edfdb5caff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071406"
---
# <a name="transmit_as-and-represent_as"></a>Transmitir \_ como y representar \_ como

Transmita como y represente como recurso compartido el mismo diseño, excepto para el token inicial; el token lee FC TRANSMIT AS o FC REPRESENT AS, pero el código subyacente \_ \_ es \_ \_ \_ \_ común.

La descripción tiene el diseño siguiente:

``` syntax
FC_TRANSMIT_AS | FC_REPRESENT_AS
flags<1>
quintuple_index<2>
presented_type_memory_size<2>
transmitted_type_buffer_size<2>
transmitted_type_offset<2>
```

Las marcas<1> byte consta de la marca superior nibble y el nibble de alineación inferior.

El nibble de alineación mantiene la alineación de la conexión del tipo transmitido. Esto es necesario cuando se dimensiona el búfer y se usa el tamaño de tipo transmitido desde el código de formato.

La marca nibble puede tener las siguientes marcas:

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

La marca PRESENTED TYPE IS ARRAY marca un argumento de transmisión de nivel superior como (o representar como) como una matriz de algo y \_ un valor pasado por \_ \_ . El [**intérprete –Oi**](/windows/desktop/Midl/-oi) usa esta marca para superar este argumento (que en realidad es un puntero en la pila, no en la matriz). Las otras dos marcas también se usan solo en intérpretes anteriores para superar correctamente un tipo presentado en la pila.

El índice de la<2> es un índice de la rutina de devolución de llamada \_ de las funciones . La tabla es común para transmitir como y representar como y hay una asignación obvia para la posición de las rutinas, ya que el mismo servicio de puntos de entrada transmite como y representa como códigos. La asignación es de \_ local => a xmit, a local => from \_ \_ \_ xmit, free \_ inst => free \_ xmit, free \_ local => free \_ inst.

El tamaño de memoria de tipo presentado<2> siempre proporciona un tamaño para el tipo presentado o local, incluido el tipo \_ desconocido que se representa como \_ \_ tipos.

El tamaño de búfer de tipo transmitido<2> es cero, cuando el tamaño varía \_ o el tamaño fijo \_ \_ real. Se trata de una optimización que permite omitir algunas devoluciones de llamada al cambiar el tamaño del búfer.

El desplazamiento de tipo transmitido<2> es el desplazamiento de tipo relativo habitual a la \_ cadena de formato de tipo \_ transmitido.

 

 