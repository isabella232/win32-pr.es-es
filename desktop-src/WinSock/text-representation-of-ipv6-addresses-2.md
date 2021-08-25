---
description: Esta sección se copia de &\# 0034;IPv6 Addressing Architecture&\# 0034; by R.
ms.assetid: 52faecb9-0d7a-40fa-a021-3cc6816a4db8
title: Representación de texto de direcciones IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d71ad1f98652a0f00e4f14f957bcedc27316444ceabc3e5c35ee2bcf81b5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733355"
---
# <a name="text-representation-of-ipv6-addresses"></a>Representación de texto de direcciones IPv6

R. Hinden y S. Deering copian esta sección de "Arquitectura de direccionamiento IPv6". Hay tres formas convencionales para representar direcciones IPv6 como cadenas de texto:

-   La forma preferida es x:x:x:x:x:x:x:x:x, donde las "x" son los valores hexadecimales de las ocho partes de 16 bits de la dirección.

    Ejemplos:

    <dl> FEDC:BA98:7654:3210:FEDC:BA98:7654:3210  
    1080:0:0:0:8:800:200C:417A  
    </dl>

> [!Note]  
> No es necesario escribir los ceros iniciales en un campo individual, pero debe haber al menos un número en cada campo (excepto en el caso descrito en el segundo formulario).

 

-   Debido al método de asignación de determinados estilos de direcciones IPv6, es habitual que las direcciones contengan cadenas largas de cero bits. Para facilitar la escritura de direcciones que contienen cero bits, hay disponible una sintaxis especial para comprimir los ceros. El uso de dos puntos dobles ("::") indica varios grupos de 16 bits de ceros.

    Por ejemplo, la dirección de multidifusión

    <dl> FF01:0:0:0:0:0:0:43  
    </dl>

    se puede representar como:

    <dl> FF01::43  
    </dl>

    Las comillas dobles ("::") solo pueden aparecer una vez en una dirección. Se pueden usar para comprimir ceros iniciales o finales en una dirección.

-   Una forma alternativa que puede ser más conveniente cuando se trabaja con un entorno mixto de nodos IPv4 e IPv6 es x:x:x:x:x:x:d.d.d.d, donde las "x" son los valores hexadecimales de las seis partes de 16 bits de orden alto de la dirección y las "d" son los valores decimales de las cuatro partes de 8 bits de orden bajo de la dirección (representación estándar de IPv4).

    Ejemplos:

    <dl> 0:0:0:0:0:0:13.1.68.3  
    0:0:0:0:0:FFFF:129.144.52.38  
    </dl>

    o en formato comprimido:

    <dl> ::13.1.68.3  
    ::FFFF:129.144.52.38  
    </dl>

 

 



