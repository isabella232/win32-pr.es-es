---
description: La multidifusión IP se encuentra en la categoría de plano de datos no raíz y plano de control no raíz.
ms.assetid: 474a1c7f-0ece-4192-a2d9-6e2f3df2ac02
title: Multidifusión IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf9469822ae974b7c616b7904f9dc7120682acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705607"
---
# <a name="ip-multicast"></a>Multidifusión IP

La multidifusión IP se encuentra en la categoría de plano de datos no raíz y plano de control no raíz. Todas las aplicaciones desempeñan un rol hoja. Actualmente, la mayoría de las implementaciones de multidifusión IP usan un conjunto de opciones de socket propuesto por Steve Deering a Internet Engineering Task Force (IETF). Por lo tanto, hay cinco operaciones disponibles:

-   \_TTL de multidifusión IP \_ : establece el período de vida y controla el ámbito de una sesión de multidifusión.
-   IP \_ Multicast \_ If: determina la interfaz que se va a utilizar para la multidifusión.
-   IP \_ Add \_ MEMBERSHI: combina una sesión de multidifusión especificada.
-   \_Pertenencia \_ al grupo de direcciones IP: quita una sesión de multidifusión.
-   \_Bucle de multidifusión IP \_ : controla el bucle invertido de tráfico de multidifusión.

Establecer el período de vida de un socket de multidifusión IP se asigna directamente a mediante el \_ \_ código de comando de ámbito de multidifusión de SiO para [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl).

El método para determinar la interfaz IP que se va a utilizar para la multidifusión es a través de una opción de socket específica de TCP/IP, tal y como se describe en el anexo de Windows Sockets 2 Protocol-Specific. Las tres operaciones restantes se describen bien con la semántica de Windows Sockets 2 que se describe aquí.

La aplicación abriría sockets con \_ marcas hoja c/d \_ en [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa). Usaría [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para agregarse a un grupo de multidifusión en la interfaz predeterminada designada para las operaciones de multidifusión. Si la marca de **WSAJoinLeaf** indica que este socket solo es un remitente, la operación de Unión es esencialmente una no operativa y no es necesario enviar mensajes IGMP. De lo contrario, se envía un paquete IGMP al enrutador para indicar intereses en la recepción de paquetes enviados a la dirección de multidifusión especificada. Dado que la aplicación creó \_ sockets de hoja de c hoja/d especiales \_ que solo se usan para realizar la multidifusión, se utilizaría la función [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) estándar para quitar de la sesión de multidifusión. El \_ \_ código de comando de intercalación de Multipoint de SiO para [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) proporciona un mecanismo de control genérico para determinar si los datos enviados en un \_ socket de hoja d de un esquema Multipoint no raíz también se pueden recibir en el mismo Socket.

> [!Note]  
> La versión de Winsock de la \_ opción de bucle de multidifusión IP \_ es semánticamente diferente de la versión de UNIX de la \_ opción de bucle de multidifusión IP \_ :

 

-   En Winsock, la \_ opción de bucle de multidifusión IP \_ solo se aplica a la ruta de acceso de recepción.
-   En la versión de UNIX, la \_ opción de bucle de multidifusión IP \_ se aplica a la ruta de acceso de envío.

Por ejemplo, las aplicaciones que se activan y desactivan (que son más fáciles de supervisar que X e y) se unen al mismo grupo en la misma interfaz; la aplicación en establece la \_ \_ opción de bucle de multidifusión IP en, la aplicación desactivada establece la \_ opción de bucle de multidifusión IP \_ desactivada. Si ON y OFF son aplicaciones Winsock, OFF puede enviar a ON, pero ON no se puede enviar a OFF. Por el contrario, si ON y OFF son aplicaciones UNIX, ON puede enviar a OFF, pero OFF no puede enviar a ON.

 

 



