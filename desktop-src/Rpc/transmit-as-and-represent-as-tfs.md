---
title: Transmit_as y Represent_as
description: Transmitir como y representar como compartir el mismo diseño excepto el token inicial; el token lee FC TRANSMIT AS o FC REPRESENT AS, pero el código subyacente \_ \_ es \_ \_ \_ \_ común.
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ada873ee6e928a08dfe1d9a93928e3b00835c9f2394bde3a5194b56cce58911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011223"
---
# <a name="transmit_as-and-represent_as"></a>Transmitir \_ como y Representar \_ como

Transmitir como y representar como compartir el mismo diseño excepto el token inicial; el token lee FC TRANSMIT AS o FC REPRESENT AS, pero el código subyacente \_ \_ es \_ \_ \_ \_ común.

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

El nibble de alineación mantiene la alineación de la conexión del tipo transmitido. Esto es necesario cuando el tamaño del búfer y el uso del tamaño de tipo transmitido del código de formato.

La marca nibble puede tener las siguientes marcas:

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

La marca PRESENTED TYPE IS ARRAY marca un argumento de transmisión de nivel superior como (o representar como) como una matriz de algo \_ \_ y un valor \_ pasado. El [**intérprete –Oi**](/windows/desktop/Midl/-oi) usa esta marca para superar este argumento (que es realmente un puntero en la pila, no en la matriz). Las otras dos marcas también se usan solo en intérpretes anteriores para ir correctamente sobre un tipo presentado en la pila.

El índice<2> es un índice de la rutina de devolución de llamada de las funciones . \_ La tabla es común para transmitir como y representar como y hay una asignación obvia para la posición de las rutinas, ya que el mismo servicio de puntos de entrada transmite como y representa como códigos. La asignación es de \_ local => a \_ xmit, \_ a local => from \_ xmit, free \_ inst => free \_ xmit, free \_ local => free \_ inst.

El tamaño de memoria de tipo presentado<2> siempre proporciona un tamaño para el tipo presentado o local, incluidos los tipos de \_ \_ representación \_ desconocidos.

El tamaño de búfer de tipo transmitido<2> es cero, cuando el tamaño varía \_ o el tamaño fijo \_ \_ real. Se trata de una optimización que permite omitir algunas devoluciones de llamada al cambiar el tamaño del búfer.

El desplazamiento de tipo transmitido<2> es el desplazamiento de tipo relativo habitual a la \_ cadena de formato de tipo \_ transmitido.

 

 