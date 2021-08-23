---
description: El asistente de protocolos de Internet (asistente de IP) ayuda a la administración de red del equipo local al permitir que las aplicaciones recuperen información sobre la configuración de red del equipo local y modifiquen esa configuración.
ms.assetid: 9eb8af78-612f-406c-ab92-4623b10a510e
title: Acerca del asistente de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77445eb999b08bda038fbffc4de5d440b7a3e79c3fa921d50f6da4ccc1f42237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014193"
---
# <a name="about-ip-helper"></a>Acerca del asistente de IP

El asistente de protocolos de Internet (asistente de IP) ayuda a la administración de red del equipo local al permitir que las aplicaciones recuperen información sobre la configuración de red del equipo local y modifiquen esa configuración. El asistente de IP también proporciona mecanismos de notificación para asegurarse de que se notifica a una aplicación cuando cambian determinados aspectos de la configuración de red del equipo local.

Muchas de las funciones auxiliares de IP pasan parámetros de estructura que representan tipos de datos asociados a la [tecnología de base de información de](/previous-versions/windows/desktop/mib/about-management-information-base) administración. Las funciones auxiliares de IP usan estas estructuras para representar diversas información de red, como entradas de caché ARP. Dado que la API de MIB también usa estas estructuras, se describen en management information base reference (Referencia [base de información de administración).](/previous-versions/windows/desktop/mib/management-information-base-reference) Aunque la API del asistente de IP usa estas estructuras, el asistente de IP es distinto de la Base de información de administración (MIB) y el Protocolo simple de administración de redes (SNMP).

La documentación del asistente de IP usa ampliamente los términos "adaptador" e "interfaz". Un "adaptador" es un término heredado que es una forma abreviada de adaptador de red que originalmente hacía referencia a algún tipo de hardware de red. Un adaptador es una abstracción de nivel de vínculo de datos.

Una "interfaz" es un término más reciente que se usa en los documentos RFC de IETF. Las RFC definen una interfaz como un concepto abstracto que representa los datos adjuntos de un nodo a un vínculo. Una interfaz es una abstracción de nivel de IP.

Los términos del adaptador y de la interfaz se usan indistintamente en la documentación del asistente de IP. En la documentación del asistente de IP, una lista de adaptadores podría incluir una interfaz WAN de software, así como la interfaz de bucle atrás (ninguno de ellos hace referencia a un dispositivo de hardware). En las API del asistente de IP, hay una asignación uno a uno de adaptadores a interfaces.

El asistente de IP proporciona funcionalidades en las siguientes áreas:

-   [Recuperar información sobre la configuración de red](retrieving-information-about-network-configuration.md)
-   [Administración de adaptadores de red](managing-network-adapters.md)
-   [Administración de interfaces](managing-interfaces.md)
-   [Administración de direcciones IP](managing-ip-addresses.md)
-   [Uso del protocolo de resolución de direcciones](using-the-address-resolution-protocol.md)
-   [Recuperar información sobre el protocolo de Internet y el protocolo de mensajes de control de Internet](retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol.md)
-   [Administrar el enrutamiento](managing-routing.md)
-   [Recepción de notificaciones de eventos de red](receiving-notification-of-network-events.md)
-   [Recuperar información sobre el protocolo de control de transmisión y el protocolo de datagramas de usuario](retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol.md)

 

 
