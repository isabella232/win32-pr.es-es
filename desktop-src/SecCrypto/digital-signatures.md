---
description: Las firmas digitales se pueden usar para distribuir un mensaje en formato de texto no cifrado cuando los destinatarios deben identificar y comprobar el remitente del mensaje.
ms.assetid: 10c33787-72d3-4e5d-b4dd-633b3fd29903
title: Firmas digitales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76dfbf31de87edb2f62531266ee62378cadefa437ebd79913ac66bfc718d612d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875391"
---
# <a name="digital-signatures"></a>Firmas digitales

[*Las firmas digitales*](../secgloss/d-gly.md) se pueden usar para distribuir un mensaje en formato de [*texto*](../secgloss/p-gly.md) no cifrado cuando los destinatarios deben identificar y comprobar el remitente del mensaje. La firma de un mensaje no modifica el mensaje; simplemente genera una cadena de firma digital que puede agrupar con el mensaje o transmitir por separado. Una firma digital es un fragmento corto de datos que se cifra con la clave privada [*del remitente.*](../secgloss/p-gly.md) Descifrar los datos de firma [](../secgloss/p-gly.md) mediante la clave pública del remitente demuestra que los datos los cifra el remitente o alguien que tenía acceso a la clave privada del remitente.

Las firmas digitales se generan mediante algoritmos [*de firma*](../secgloss/p-gly.md) de clave pública. Una [*clave privada*](../secgloss/p-gly.md) genera la firma y la clave pública correspondiente debe usarse para validar la firma. Este proceso se muestra en la ilustración siguiente.

![generación de una firma digital](images/capi02.png)

Hay dos pasos que se deben seguir para crear una firma digital a partir de un mensaje. El primer paso implica la creación de un [*valor hash*](../secgloss/h-gly.md) (también conocido como resumen [*del mensaje)*](../secgloss/m-gly.md)a partir del mensaje. A continuación, este valor hash se firma mediante la clave privada del firmante. A continuación se muestra una ilustración de los pasos necesarios para crear una firma digital.

![crear una firma digital a partir de un mensaje](images/capi06.png)

Para comprobar una firma, se requieren tanto el mensaje como la firma. En primer lugar, se debe crear un valor hash a partir del mensaje de la misma manera que se creó la firma. A continuación, este valor hash se comprueba con la firma mediante la clave pública del firmante. Si el valor hash y la firma coinciden, puede estar seguro de que el mensaje es realmente el que el firmante firmó originalmente y que no se ha alterado. En el diagrama siguiente se muestra el proceso implicado en la comprobación de una firma digital.

![comprobar una firma digital](images/capi07.png)

Un valor hash consta de una pequeña cantidad de datos binarios, normalmente alrededor de 160 bits. Esto se genera mediante un [*algoritmo hash*](../secgloss/h-gly.md). Más adelante en esta sección se enumeran varios de estos algoritmos.

Todos los valores hash comparten las siguientes propiedades, independientemente del algoritmo utilizado:

-   La longitud del valor hash viene determinada por el tipo de algoritmo utilizado y su longitud no varía con el tamaño del mensaje. Las longitudes de valor hash más comunes son 128 o 160 bits.
-   Cada par de mensajes no idénticos se traduce en un valor hash completamente diferente, incluso si los dos mensajes solo difieren en un solo bit. Con la tecnología actual, no es factible detectar un par de mensajes que se traducen en el mismo valor hash sin romper el algoritmo hash.
-   Cada vez que se aplica un algoritmo hash a un mensaje determinado con el mismo algoritmo, se genera el mismo valor hash.
-   Todos los algoritmos hash son un solo sentido. Dado un valor hash, no es posible recuperar el mensaje original. De hecho, ninguna de las propiedades del mensaje original se puede determinar teniendo en cuenta solo el valor hash.

 

 
