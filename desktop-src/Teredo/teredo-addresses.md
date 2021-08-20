---
title: Direcciones de Teredo
ms.assetid: e2e185c2-e53d-471d-aedb-54d75f9db0bb
description: 'Más información sobre: Direcciones de Teredo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a8b283d2bab6c9ba091ecc3b37c6218fadb0face78e04b807be03d68b814d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354141"
---
# <a name="teredo-addresses"></a>Direcciones de Teredo

Una dirección de Teredo consta de lo siguiente:

-   **Prefijo de Teredo**

    Los primeros 32 bits son para el prefijo Teredo, que es el mismo para todas las direcciones de Teredo. Windows XP y Windows Server 2003 usaban inicialmente el prefijo Teredo 3FFE:831F::/32. El prefijo definido para Teredo en RFC 4380 es 2001::/32 y es el prefijo usado por Teredo en Windows Vista y Windows Server 2008. Los equipos que ejecutan Windows XP y Windows Server 2003 usarán el prefijo Teredo 2001::/32 cuando se actualice con el Boletín de seguridad de Microsoft MS06-064.

-   **Dirección IPv4 del servidor Teredo**

    Los 32 bits siguientes contienen la dirección pública IPv4 del servidor de Teredo que ayudó a configurar esta dirección de Teredo. Para obtener más información, vea "Configuración inicial para clientes de Teredo" en este artículo.

-   **Marcas**

    Los 16 bits siguientes para están reservados para las marcas de Teredo. Para Windows de Teredo basado en XP, la única marca definida es el bit de orden alto conocido como marca Cone. La marca Cone se establece cuando el cliente de Teredo está detrás de una NAT de cono. La determinación de si la NAT conectada a Internet es un NAT de cono se produce durante la configuración inicial del cliente de Teredo. Para obtener más información, vea "Configuración inicial para clientes de Teredo" en este artículo.

    Para los clientes de Teredo basados en Windows Vista y Windows Server 2008, los bits no usados del campo Marcas proporcionan un nivel de protección frente a los exámenes de direcciones por parte de usuarios malintencionados. Los 16 bits del campo Marcas para los clientes teredo basados en Windows Vista y Windows Server 2008 constan de lo siguiente: CRAAAAUG AAAAAAAA. El bit C es para la marca Cone. El bit de R está reservado para su uso futuro. El bit U es para la marca Universal/Local (establecida en 0). El bit G es la marca Individual/Group (se establece en 0). Los bits A se establecen en un número de 12 bits generado aleatoriamente. Mediante el uso de un número aleatorio para los bits A, un usuario malintencionado que haya determinado el resto de la dirección de Teredo mediante la captura del intercambio de configuración inicial de paquetes entre el cliente de Teredo y el servidor de Teredo tendrá que probar hasta 4096 (212) direcciones diferentes para determinar la dirección de un cliente de Teredo durante un examen de direcciones.

-   **Puerto externo oculto**

    Los 16 bits siguientes almacenan una versión oculta del puerto UDP externo correspondiente a todo el tráfico de Teredo para este cliente de Teredo. Cuando el cliente de Teredo envía su paquete inicial a un servidor de Teredo, nat asigna el puerto UDP de origen del paquete a otro puerto UDP externo. El cliente de Teredo mantiene esta asignación de puerto para que permanezca en la tabla de traducción de NAT. Por lo tanto, todo el tráfico de Teredo para el host usa el mismo puerto UDP externo y asignado. El puerto UDP externo viene determinado por el servidor de Teredo desde el puerto UDP de origen del paquete inicial entrante enviado por el cliente de Teredo y enviado de vuelta al cliente de Teredo.

    El puerto externo se oculta mediante XORing el puerto externo con 0xFFFF. Por ejemplo, la versión oculta del puerto externo 5000 en formato hexadecimal es EC77 (5000 = 0x1388, 0x1388 XOR 0xFFFF = 0xEC77). Ocultar el puerto externo impide que los NAT traduzcan el puerto externo dentro de la carga de los paquetes que están reenviando.

-   **Dirección externa oculta**

    Los últimos 32 bits almacenan una versión oculta de la dirección IPv4 externa correspondiente a todo el tráfico de Teredo para este cliente de Teredo. Al igual que el puerto externo, cuando el cliente de Teredo envía su paquete inicial a un servidor de Teredo, la dirección IP de origen del paquete se asigna mediante nat a una dirección externa (pública) diferente. El cliente de Teredo mantiene esta asignación de direcciones para que permanezca en la tabla de traducción de NAT. Por lo tanto, todo el tráfico de Teredo para el host usa la misma dirección IPv4 externa, asignada y pública. La dirección IPv4 externa viene determinada por el servidor de Teredo a partir de la dirección IPv4 de origen del paquete inicial entrante enviado por el cliente de Teredo y enviado de vuelta al cliente de Teredo.

    La dirección externa se oculta mediante XORing la dirección externa con 0xFFFFFFFF. Por ejemplo, la versión oculta de la dirección IPv4 pública 131.107.0.1 en formato hexadecimal de dos puntos es 7C94:FFFE (131.107.0.1 = 0x836B0001, 0x836B0001 XOR 0xFFFFFFFF = 0x7C94FFFE). Ocultar la dirección externa impide que los NAT traduzcan la dirección externa dentro de la carga de los paquetes que están reenviando.

 

 




