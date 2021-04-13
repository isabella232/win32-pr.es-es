---
title: Enrutamiento de solicitudes entrantes
description: La API del servidor HTTP mantiene una base de datos de enrutamiento para determinar qué aplicación recibe una solicitud entrante.
ms.assetid: 7c613137-66bd-4375-93cb-b5562823bc12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da483030441f3a9239eef153da59212166bce9eb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104421586"
---
# <a name="routing-incoming-requests"></a>Enrutamiento de solicitudes entrantes

La API del servidor HTTP mantiene una base de datos de enrutamiento para determinar qué aplicación recibe una solicitud entrante. La tabla de enrutamiento se genera a partir de la base de datos de reserva y contiene entradas de reserva, así como registros actuales. Cuando se realiza un registro o una reserva, se coloca en el cubo de la base de datos de enrutamiento que corresponde al tipo de host de la siguiente manera:

-   \+ : los registros de puerto se colocan en el cubo "comodín seguro".

-   host: los registros de puerto se colocan en el cubo "explícito"

-   IP: los registros de puerto se colocan en el cubo "comodín débil de IP enlazada"

-   \* : los registros de puerto se colocan en el cubo "comodín débil"

Estos pasos también hacen referencia al orden en que se procesan las solicitudes HTTP entrantes. En primer lugar, se comprueban las reservas de caracteres comodín seguros y, a continuación, se comprueba la reserva explícita seguida del carácter comodín débil y el carácter comodín débil. La búsqueda se detiene cuando se encuentra una coincidencia para que no se encuentren los registros en ninguno de los cubos restantes.

El algoritmo de enrutamiento de la API del servidor HTTP localiza la mejor coincidencia para [UrlPrefix](urlprefix-strings.md) mediante la búsqueda de las entradas de registro y de las entradas de reserva de la base de datos de enrutamiento, comenzando por el depósito de comodín seguro y finalizando con el depósito de comodín débil. La mejor coincidencia, dentro de un depósito, es la coincidencia más larga en la parte del URI relativo de UrlPrefix (suponiendo que haya una coincidencia exacta para las partes de host, puerto y esquema de la dirección URL). Una vez que se encuentra una coincidencia en un depósito, el algoritmo de enrutamiento detiene su búsqueda y omite todos los depósitos de menor prioridad.

Por ejemplo, considere los siguientes registros (en orden descendente de prioridad en función de los tipos de cubos:

-   Registro: `https://+:80/vroot/` está registrado por la aplicación 1

-   Registro: `https://adatum.com:80/` está registrado por la aplicación 2

-   Registro: `https://\*:80/` está registrado por la aplicación 3

Una solicitud entrante para `https://adatum.com:80/vroot/subdir/file.htm/` se entrega a la aplicación 1. Una solicitud entrante para `https://adatum.com:80/default.htm/` se entrega a la aplicación 2. Una solicitud entrante para `https://otheradatum.com:80/file.htm/` se entrega a la aplicación 3.

Si la mejor coincidencia es una entrada de reserva, significa que la aplicación que debe recibir la solicitud no se está ejecutando. Por ejemplo, considere el registro y la reserva siguientes:

-   Registro: `https://\*:80/vroot/` está registrado por la aplicación 1, el usuario A

-   Reserva: se `https://adatum.com:80/` ha reservado para el usuario B

Una solicitud entrante para `https://adatum.com:80/vroot/file.htm/` no se entrega a la aplicación 1 porque la mejor coincidencia conduce a la entrada de reserva para el usuario B. Las reglas de prioridad se aplican en este caso a la reserva que tiene una prioridad más alta. Si no hay ningún proceso activo que esté autorizado y registrado en las solicitudes de servicio de la dirección URL recibida, la solicitud se rechazará con un código de estado 400 (solicitud incorrecta).

 

 




