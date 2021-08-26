---
title: Enrutamiento de solicitudes entrantes
description: La API del servidor HTTP mantiene una base de datos de enrutamiento para determinar qué aplicación recibe una solicitud entrante.
ms.assetid: 7c613137-66bd-4375-93cb-b5562823bc12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e40feab96a913da895633bddd8e53697b6aeef959162da054da22aeeedef652a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829965"
---
# <a name="routing-incoming-requests"></a>Enrutamiento de solicitudes entrantes

La API del servidor HTTP mantiene una base de datos de enrutamiento para determinar qué aplicación recibe una solicitud entrante. La tabla de enrutamiento se ha creado a partir de la base de datos de reserva y contiene entradas de reserva, así como registros actuales. Cuando se realiza un registro o una reserva, se coloca en el cubo de la base de datos de enrutamiento que corresponde al tipo de host como se muestra a continuación:

-   \+ : los registros de puertos se colocan en el cubo "Carácter comodín fuerte".

-   host: los registros de puerto se colocan en el cubo "Explícito".

-   IP: los registros de puertos se colocan en el cubo "Carácter comodín débil enlazado a IP"

-   \* : los registros de puertos se colocan en el cubo "Carácter comodín débil".

Estos pasos también hacen referencia al orden en que se procesan las solicitudes HTTP entrantes. Primero se comprueban las reservas con caracteres comodín fuertes y, a continuación, se comprueba la reserva explícita seguida del carácter comodín débil enlazado a IP y el carácter comodín débil. La búsqueda se detiene cuando se encuentra una coincidencia para que no se busquen registros en ninguno de los cubos restantes.

El algoritmo de enrutamiento de API de servidor HTTP busca la mejor coincidencia para [UrlPrefix](urlprefix-strings.md) mediante la búsqueda de las entradas de registro y las entradas de reserva de la base de datos de enrutamiento, empezando por el depósito de caracteres comodín seguro y finalizando con el depósito de caracteres comodín débiles. La mejor coincidencia, dentro de un cubo, es la coincidencia más larga en la parte relativa del URI de UrlPrefix (suponiendo una coincidencia exacta para las partes host, puerto y esquema de la dirección URL). Una vez que se encuentra una coincidencia en un cubo, el algoritmo de enrutamiento detiene su búsqueda y omite todos los depósitos de prioridad inferior.

Por ejemplo, considere los registros siguientes (enumerados en orden descendente de prioridad en función de los tipos de cubo:

-   Registro: `https://+:80/vroot/` está registrado por la aplicación 1

-   Registro: `https://adatum.com:80/` está registrado por la aplicación 2

-   Registro: `https://\*:80/` está registrado por la aplicación 3

Una solicitud entrante para `https://adatum.com:80/vroot/subdir/file.htm/` se entrega a la aplicación 1. Una solicitud entrante para `https://adatum.com:80/default.htm/` se entrega a la aplicación 2. Se entrega una solicitud entrante `https://otheradatum.com:80/file.htm/` de a la aplicación 3.

Si la mejor coincidencia es una entrada de reserva, significa que la aplicación que debe recibir la solicitud no se está ejecutando. Por ejemplo, considere el registro y la reserva siguientes:

-   Registro: `https://\*:80/vroot/` está registrado por la aplicación 1, usuario A

-   Reserva: `https://adatum.com:80/` se ha reservado para el usuario B

No se entrega una solicitud entrante a la aplicación 1 porque la mejor coincidencia conduce a la entrada `https://adatum.com:80/vroot/file.htm/` de reserva del usuario B. En este caso, las reglas de precedencia se aplican a la reserva que tiene una prioridad más alta. Si no hay ningún proceso activo que esté autorizado y registrado en las solicitudes de servicio para la dirección URL recibida, la solicitud se rechazará con un código de estado 400 (solicitud no válida).

 

 




