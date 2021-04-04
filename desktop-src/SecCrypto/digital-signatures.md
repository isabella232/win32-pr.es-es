---
description: Las firmas digitales se pueden usar para distribuir un mensaje en formato de texto no cifrado cuando los destinatarios deben identificar y comprobar el remitente del mensaje.
ms.assetid: 10c33787-72d3-4e5d-b4dd-633b3fd29903
title: Firmas digitales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d84d1a1c71b6b6d709dbe67b4fa2c81f4b54e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154082"
---
# <a name="digital-signatures"></a>Firmas digitales

Las [*firmas digitales*](../secgloss/d-gly.md) se pueden usar para distribuir un mensaje en formato de [*texto no cifrado*](../secgloss/p-gly.md) cuando los destinatarios deben identificar y comprobar el remitente del mensaje. La firma de un mensaje no modifica el mensaje; simplemente genera una cadena de firma digital que puede agrupar con el mensaje o transmitir por separado. Una firma digital es una pequeña parte de los datos cifrados con la [*clave privada*](../secgloss/p-gly.md)del remitente. Descifrar los datos de la firma mediante la [*clave pública*](../secgloss/p-gly.md) del remitente demuestra que los datos se cifraron por el remitente o por alguien que tenía acceso a la clave privada del remitente.

Las firmas digitales se generan mediante algoritmos de firma de [*clave pública*](../secgloss/p-gly.md) . Una [*clave privada*](../secgloss/p-gly.md) genera la firma y la clave pública correspondiente debe usarse para validar la firma. Este proceso se muestra en la siguiente ilustración.

![generar una firma digital](images/capi02.png)

Hay dos pasos que se deben seguir para crear una firma digital a partir de un mensaje. El primer paso implica la creación de un valor [*hash*](../secgloss/h-gly.md) (también conocido como [*síntesis del mensaje*](../secgloss/m-gly.md)) del mensaje. A continuación, este valor hash se firma con la clave privada del firmante. A continuación se ilustran los pasos necesarios para crear una firma digital.

![crear una firma digital a partir de un mensaje](images/capi06.png)

Para comprobar una firma, se requieren tanto el mensaje como la firma. En primer lugar, se debe crear un valor hash a partir del mensaje de la misma manera que se creó la firma. A continuación, este valor hash se comprueba con la firma mediante la clave pública del firmante. Si el valor hash y la firma coinciden, puede estar seguro de que el mensaje es realmente el firmante firmado originalmente y que no se ha alterado. En el diagrama siguiente se ilustra el proceso implicado en la comprobación de una firma digital.

![comprobar una firma digital](images/capi07.png)

Un valor hash consta de una pequeña cantidad de datos binarios, normalmente alrededor de 160 bits. Esto se genera mediante un [*algoritmo hash*](../secgloss/h-gly.md). Más adelante en esta sección se enumeran algunos de estos algoritmos.

Todos los valores hash comparten las siguientes propiedades, independientemente del algoritmo utilizado:

-   La longitud del valor hash viene determinada por el tipo de algoritmo utilizado y su longitud no varía en función del tamaño del mensaje. Las longitudes de los valores hash más comunes son 128 o 160 bits.
-   Cada par de mensajes no idénticos se convierte en un valor hash completamente diferente, incluso si los dos mensajes solo difieren en un solo bit. Con la tecnología de hoy en día, no es factible detectar un par de mensajes que se traduzcan al mismo valor hash sin interrumpir el algoritmo hash.
-   Cada vez que se aplica un algoritmo hash a un mensaje determinado mediante el mismo algoritmo, se genera el mismo valor hash.
-   Todos los algoritmos hash son unidireccionales. Dado un valor hash, no es posible recuperar el mensaje original. De hecho, ninguna de las propiedades del mensaje original se puede determinar a partir del valor hash por sí solo.

 

 
