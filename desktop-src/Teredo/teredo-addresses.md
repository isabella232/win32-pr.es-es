---
title: Direcciones Teredo
ms.assetid: e2e185c2-e53d-471d-aedb-54d75f9db0bb
description: 'Más información acerca de: direcciones Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc08a53da2f710423d948e9479df2aeb08f20178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361528"
---
# <a name="teredo-addresses"></a>Direcciones Teredo

Una dirección Teredo consta de lo siguiente:

-   **Prefijo Teredo**

    Los primeros 32 bits son para el prefijo Teredo, que es el mismo para todas las direcciones Teredo. Windows XP y Windows Server 2003 inicialmente usaban el prefijo de Teredo 3FFE: 831F::/32. El prefijo definido para Teredo en RFC 4380 es 2001::/32 y es el prefijo usado por Teredo en Windows Vista y Windows Server 2008. Los equipos que ejecutan Windows XP y Windows Server 2003 usarán el prefijo de Teredo 2001::/32 cuando se actualicen con el boletín de seguridad de Microsoft MS06-064.

-   **Dirección IPv4 del servidor Teredo**

    Los siguientes 32 bits contienen la dirección IPv4 pública del servidor Teredo que ayudó a configurar esta dirección Teredo. Para obtener más información, consulte "configuración inicial para clientes Teredo" en este artículo.

-   **Marcas**

    Los 16 bits siguientes para están reservados para las marcas de Teredo. En el caso de los clientes Teredo basados en Windows XP, la única marca definida es el bit de orden superior conocido como marca cónica. La marca cónica se establece cuando el cliente Teredo está detrás de un NAT cónico. La determinación de si el NAT conectado a Internet es una NAT cónica que se produce durante la configuración inicial del cliente Teredo. Para obtener más información, consulte "configuración inicial para clientes Teredo" en este artículo.

    En el caso de los clientes Teredo basados en Windows Vista y Windows Server 2008, los bits no usados dentro del campo marcas proporcionan un nivel de protección de los exámenes de direcciones por parte de usuarios malintencionados. Los 16 bits del campo Flags para los clientes Teredo basados en Windows Vista y Windows Server 2008 se componen de lo siguiente: CRAAAAUG AAAAAAAA. El bit C es para la marca de cono. El bit R está reservado para un uso futuro. El bit U es para la marca universal/local (establecido en 0). El bit G es una marca individual o de grupo (establecida en 0). Los bits A se establecen en un número generado aleatoriamente de 12 bits. Mediante el uso de un número aleatorio para los bits A, un usuario malintencionado que ha determinado el resto de la dirección Teredo mediante la captura del intercambio de configuración inicial de paquetes entre el cliente Teredo y el servidor Teredo tendrá que probar hasta 4.096 (212) diferentes direcciones para determinar la dirección de un cliente Teredo durante un examen de direcciones.

-   **Puerto externo oculto**

    Los 16 bits siguientes almacenan una versión oculta del puerto UDP externo correspondiente a todo el tráfico Teredo de este cliente Teredo. Cuando el cliente Teredo envía su paquete inicial a un servidor Teredo, el puerto UDP de origen del paquete se asigna mediante NAT a un puerto UDP externo diferente. El cliente Teredo mantiene esta asignación de puerto para que permanezca en la tabla de traducción de NAT. Por lo tanto, todo el tráfico Teredo del host utiliza el mismo puerto UDP asignado externo. El puerto UDP externo viene determinado por el servidor Teredo del puerto UDP de origen del paquete inicial entrante enviado por el cliente Teredo y enviado de vuelta al cliente Teredo.

    El puerto externo está oculto XORing el puerto externo con 0xFFFF. Por ejemplo, la versión oculta del puerto externo 5000 en formato hexadecimal es EC77 (5000 = 0x1388, 0x1388 XOR 0xFFFF = 0xEC77). La ocultación del puerto externo impide que los NAT contengan el puerto externo dentro de la carga de los paquetes que se reenvían.

-   **Dirección externa oculta**

    Los últimos 32 bits almacenan una versión oculta de la dirección IPv4 externa correspondiente a todo el tráfico Teredo de este cliente Teredo. Al igual que el puerto externo, cuando el cliente Teredo envía su paquete inicial a un servidor Teredo, la dirección IP de origen del paquete se asigna mediante el NAT a una dirección externa (pública) distinta. El cliente Teredo mantiene esta asignación de direcciones para que permanezca en la tabla de traducción de NAT. Por lo tanto, todo el tráfico de Teredo para el host utiliza la misma dirección IPv4 pública, asignada y externa. La dirección IPv4 externa viene determinada por el servidor Teredo de la dirección IPv4 de origen del paquete inicial entrante enviado por el cliente Teredo y que se devuelve al cliente Teredo.

    La dirección externa está oscurecida por XORing la dirección externa con 0xFFFFFFFF. Por ejemplo, la versión oculta de la dirección IPv4 pública 131.107.0.1 en formato hexadecimal con dos puntos es 7C94: FFFE (131.107.0.1 = 0x836B0001, 0x836B0001 XOR 0xFFFFFFFF = 0x7C94FFFE). La ocultación de la dirección externa impide que los NAT contengan la dirección externa dentro de la carga de los paquetes que se reenvían.

 

 




