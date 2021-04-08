---
title: Transmit_as y Represent_as
description: Transmitir \_ como y representan \_ como recursos compartidos del mismo diseño, excepto el token inicial; el token lee la \_ transmisión \_ de FC como o FC \_ \_ como, pero el código subyacente es común.
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69267741536314c3e30e2270e7be61edfdb5caff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995296"
---
# <a name="transmit_as-and-represent_as"></a>Transmitir \_ como y representar \_ como

Transmitir \_ como y representan \_ como recursos compartidos del mismo diseño, excepto el token inicial; el token lee la \_ transmisión \_ de FC como o FC \_ \_ como, pero el código subyacente es común.

La descripción tiene el siguiente diseño:

``` syntax
FC_TRANSMIT_AS | FC_REPRESENT_AS
flags<1>
quintuple_index<2>
presented_type_memory_size<2>
transmitted_type_buffer_size<2>
transmitted_type_offset<2>
```

Las marcas<1> byte están formadas por el recorte superior de la marca y el recorte de alineación inferior.

El recorte de la alineación mantiene la alineación del cable del tipo transmitido. Esto es necesario cuando se cambia el tamaño del búfer y se usa el tamaño del tipo transmitido desde el código de formato.

La marca de recorte puede tener las marcas siguientes:

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

El \_ tipo presentado \_ es \_ una marca de matriz marca un argumento transmitir como (o representar como) de nivel superior como una matriz de algo y un valor pasado por. El intérprete [**– OI**](/windows/desktop/Midl/-oi) usa esta marca para depurar este tipo de argumento (que en realidad es un puntero en Stack, no en la matriz). Las otras dos marcas también se usan solo en intérpretes anteriores para ir correctamente sobre un tipo presentado en la pila.

El \_ Índice quíntuplo<2> es un índice de la rutina de devolución de llamada quíntuplo (es realmente un cuádruple) de funciones. La tabla es común para transmitir como y representar como y hay una asignación obvia para la posición de las rutinas, ya que el mismo servicio de puntos de entrada transmite como y representan códigos. La asignación es de \_ local => a la \_ transmisión, a \_ local => desde \_ transmisión, \_ inst. inst => transmisión gratuita \_ , local gratis \_ => \_ inst.

El \_ \_ \_ tamaño de memoria de tipo presentado<2> siempre proporciona un tamaño para el tipo presentado/local, incluidos los tipos de representación desconocidos.

El tamaño del búfer de tipo transmitido \_ \_ \_<2> es cero, cuando el tamaño es variable o el tamaño fijo real. Se trata de una optimización que permite omitir algunas devoluciones de llamada al cambiar el tamaño del búfer.

El desplazamiento de tipo transmitido \_ \_<2> es el desplazamiento de tipo relativo habitual a la cadena de formato de tipo transmitido.

 

 