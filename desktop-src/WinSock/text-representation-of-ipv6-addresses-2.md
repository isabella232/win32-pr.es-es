---
description: Esta sección se copia desde &\# 0034; arquitectura de direccionamiento IPv6&\# 0034; por R.
ms.assetid: 52faecb9-0d7a-40fa-a021-3cc6816a4db8
title: Representación de texto de direcciones IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df97c1c8933f3708fee56e34e05f918d531d2a13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715852"
---
# <a name="text-representation-of-ipv6-addresses"></a>Representación de texto de direcciones IPv6

R. Hinden y S. Deering copian esta sección de "arquitectura de direccionamiento IPv6". Hay tres formas convencionales para representar direcciones IPv6 como cadenas de texto:

-   La forma preferida es x:x: x:x: x:x: x:x, donde ' x ' son los valores hexadecimales de las partes de 8 16 bits de la dirección.

    Ejemplos:

    <dl> FEDC:BA98:7654:3210:FEDC:BA98:7654:3210  
    1080:0: 0:0: 8:800:200C: 417A  
    </dl>

> [!Note]  
> No es necesario escribir los ceros a la izquierda en un campo individual, pero debe haber al menos un número en cada campo (excepto en el caso descrito en el segundo formulario).

 

-   Debido al método de asignación de determinados estilos de direcciones IPv6, es habitual que las direcciones contengan cadenas largas de cero bits. Con el fin de facilitar la escritura de direcciones que contienen cero bits, hay una sintaxis especial disponible para comprimir los ceros. El uso de dos puntos dobles ("::") indica varios grupos de 16 bits de ceros.

    Por ejemplo, la dirección de multidifusión

    <dl> FF01:0: 0:0: 0:0: 0:43  
    </dl>

    se puede representar como:

    <dl> FF01:: 43  
    </dl>

    Las comillas dobles ("::") solo pueden aparecer una vez en una dirección. Se pueden usar para comprimir ceros iniciales o finales en una dirección.

-   Una forma alternativa que puede ser más conveniente cuando se trabaja con un entorno mixto de nodos IPv4 e IPv6 es x:x: x:x: x:x: d. d. d. d, donde ' x ' son los valores hexadecimales de los seis elementos de 16 bits de orden superior de la dirección, y los de la ' d ' son los valores decimales de las cuatro partes de 8 bits de orden inferior de la dirección (representación IPv4 estándar).

    Ejemplos:

    <dl> 0:0: 0:0: 0:0: 13.1.68.3  
    0:0: 0:0: FFFF: 129.144.52.38  
    </dl>

    o en formato comprimido:

    <dl> ::13.1.68.3  
    :: FFFF: 129.144.52.38  
    </dl>

 

 



