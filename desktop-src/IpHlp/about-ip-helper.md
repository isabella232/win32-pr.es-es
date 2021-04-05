---
description: La aplicación auxiliar de protocolo de Internet (aplicación auxiliar de IP) ayuda a la administración de red del equipo local, ya que permite a las aplicaciones recuperar información acerca de la configuración de red del equipo local y modificar dicha configuración.
ms.assetid: 9eb8af78-612f-406c-ab92-4623b10a510e
title: Acerca de la aplicación auxiliar de IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50587b4abdcbad0cddd6d6ce3281c908fdebef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082146"
---
# <a name="about-ip-helper"></a>Acerca de la aplicación auxiliar de IP

La aplicación auxiliar de protocolo de Internet (aplicación auxiliar de IP) ayuda a la administración de red del equipo local, ya que permite a las aplicaciones recuperar información acerca de la configuración de red del equipo local y modificar dicha configuración. La aplicación auxiliar de IP también proporciona mecanismos de notificación para asegurarse de que se notifique a una aplicación cuando se cambien determinados aspectos de la configuración de red del equipo local.

Muchas de las funciones auxiliares de IP pasan parámetros de estructura que representan los tipos de datos asociados a la tecnología de [base de información de administración](/previous-versions/windows/desktop/mib/about-management-information-base) . Las funciones auxiliares de IP usan estas estructuras para representar diversa información de red, como las entradas de caché ARP. Como la API MIB también utiliza estas estructuras, se describen en la referencia de la [base de datos de información de administración](/previous-versions/windows/desktop/mib/management-information-base-reference). Aunque la API auxiliar de IP utiliza estas estructuras, la aplicación auxiliar de IP es distinta de la base de datos de información de administración (MIB) y del Protocolo simple de administración de redes (SNMP).

La documentación de la aplicación auxiliar de IP utiliza los términos "adaptador" e "interfaz" en gran medida. Un "adaptador" es un término heredado que es una forma abreviada de adaptador de red que originalmente hacía referencia a algún tipo de hardware de red. Un adaptador es una abstracción de nivel de vínculo de los vínculos.

Una "interfaz" es un término más reciente que se usa en los documentos RFC de IETF. Las RFC definen una interfaz como un concepto abstracto que representa los datos adjuntos de un nodo a un vínculo. Una interfaz es una abstracción de nivel IP.

El adaptador y los términos de la interfaz se usan de forma ligeramente indistinta en la documentación de la aplicación auxiliar de IP. En la documentación de la aplicación auxiliar de IP, una lista de adaptadores podría incluir una interfaz de WAN de software, así como la interfaz de bucle invertido (ninguna de ellas hace referencia a un dispositivo de hardware). En las API auxiliares de IP, hay una asignación uno a uno de los adaptadores a las interfaces.

La aplicación auxiliar de IP proporciona capacidades en las siguientes áreas:

-   [Recuperación de información acerca de la configuración de red](retrieving-information-about-network-configuration.md)
-   [Administración de adaptadores de red](managing-network-adapters.md)
-   [Administrar interfaces](managing-interfaces.md)
-   [Administración de direcciones IP](managing-ip-addresses.md)
-   [Usar el protocolo de resolución de direcciones](using-the-address-resolution-protocol.md)
-   [Recuperación de información sobre el protocolo de Internet y el protocolo de mensajes de control de Internet](retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol.md)
-   [Administrar el enrutamiento](managing-routing.md)
-   [Recepción de notificaciones de eventos de red](receiving-notification-of-network-events.md)
-   [Recuperación de información sobre el protocolo de control de transmisión y el protocolo de datagramas de usuario](retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol.md)

 

 
