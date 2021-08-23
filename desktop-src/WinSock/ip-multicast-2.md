---
description: La multidifusión IP se incluye en la categoría de plano de datos no raíz y plano de control no raíz.
ms.assetid: 474a1c7f-0ece-4192-a2d9-6e2f3df2ac02
title: Multidifusión IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b80441826f490fedc3dac3dba405ddd0d9f09d57bfd0243a66cae320c76b0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051503"
---
# <a name="ip-multicast"></a>Multidifusión IP

La multidifusión IP se incluye en la categoría de plano de datos no raíz y plano de control no raíz. Todas las aplicaciones desempeñan un rol hoja. Actualmente, la mayoría de las implementaciones de multidifusión IP usan un conjunto de opciones de socket propuestas por Steve Deering al Grupo de tareas de ingeniería de Internet (IETF). Por lo tanto, hay cinco operaciones disponibles:

-   TTL de MULTIDIFUSIÓN IP: establece el ámbito de los controles de período de vida \_ de una sesión de \_ multidifusión.
-   IP \_ MULTICAST \_ IF: determina la interfaz que se usará para la multidifusión.
-   IP \_ ADD \_ MEMBERSHI : une una sesión de multidifusión especificada.
-   DROP \_ \_ MEMBERSHIP de IP: sale de una sesión de multidifusión.
-   BUCLE \_ DE \_ MULTIDIFUSIÓN IP: controla el bucle atrás del tráfico de multidifusión.

El establecimiento del período de vida de un socket de multidifusión IP se asigna directamente al uso del código de comando DE ÁMBITO DE MULTIDIFUSIÓN DE SIO \_ \_ para [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl).

El método para determinar la interfaz IP que se va a usar para la multidifusión es a través de una opción de socket específica de TCP/IP, como se describe en el anexo de Windows Sockets 2 Protocol-Specific. Las tres operaciones restantes se tratan bien con la semántica Windows Sockets 2 descrita aquí.

La aplicación abriría sockets con marcas \_ hoja/d de c \_ en [**WSASocket.**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) Usaría [**WSAJoinLeaf para**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) agregarse a un grupo de multidifusión en la interfaz predeterminada designada para las operaciones de multidifusión. Si la marca de **WSAJoinLeaf** indica que este socket es solo un remitente, la operación de combinación es básicamente una operación no operativa y no es necesario enviar ningún mensaje IGMP. De lo contrario, se envía un paquete IGMP al enrutador para indicar interés en recibir paquetes enviados a la dirección de multidifusión especificada. Puesto que la aplicación creó sockets hoja/d hoja especiales usados solo para realizar multidifusión, la función closesocket estándar se usaría para salir de la \_ \_ sesión de multidifusión. [](/windows/desktop/api/winsock/nf-winsock-closesocket) El código de comando \_ SIO MULTIPOINT LOOPBACK para \_ [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) proporciona un mecanismo de control genérico para determinar si los datos enviados en un socket hoja d en un esquema multipunto no raíz también se pueden recibir en el mismo \_ socket.

> [!Note]  
> La versión winsock de la opción BUCLE DE MULTIDIFUSIÓN IP es semánticamente diferente de la versión UNIX de \_ la opción BUCLE DE \_ \_ \_ MULTIDIFUSIÓN IP:

 

-   En Winsock, la opción BUCLE \_ DE \_ MULTIDIFUSIÓN DE IP solo se aplica a la ruta de acceso de recepción.
-   En la UNIX, la opción BUCLE \_ DE MULTIDIFUSIÓN IP se aplica a la ruta de acceso de \_ envío.

Por ejemplo, las aplicaciones ON y OFF (que son más fáciles de realizar que X e Y) se unen al mismo grupo en la misma interfaz; application ON establece la opción IP MULTICAST LOOP (BUCLE DE MULTIDIFUSIÓN DE IP) \_ en , application OFF establece la opción IP MULTICAST LOOP \_ \_ \_ (BUCLE DE MULTIDIFUSIÓN DE IP) desactivada. Si ON y OFF son aplicaciones Winsock, OFF puede enviarse a ON, pero ON no se puede enviar a OFF. Por el contrario, si ON y OFF UNIX aplicaciones, ON puede enviarse a OFF, pero OFF no puede enviarse a ON.

 

 



