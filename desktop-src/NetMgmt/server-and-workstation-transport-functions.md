---
title: Funciones de transporte de servidor y estación de trabajo
description: Las funciones de transporte de estación de trabajo y el servidor de administración de red controlan el enlace y el desenlace de los protocolos de transporte hacia y desde el servidor y el redirector.
ms.assetid: 64342e21-98f1-42d3-b541-46b826391fad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1ab4a4ce5dcc3b887eb9eb9d5759db89dfed55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665647"
---
# <a name="server-and-workstation-transport-functions"></a>Funciones de transporte de servidor y estación de trabajo

Las funciones de transporte de estación de trabajo y el servidor de administración de red controlan el enlace y el desenlace de los protocolos de transporte hacia y desde el servidor y el redirector. Las funciones de transporte del servidor se ocupan de los protocolos de transporte administrados por el servidor. las funciones de transporte de estación de trabajo se ocupan de los protocolos de transporte administrados por el redirector.

El uso compartido de archivos entre un dispositivo de transporte y un servidor de tiene dos componentes:

-   El equipo servidor donde residen los archivos
-   Un cliente de bloque de mensajes del servidor (SMB) que tiene acceso a los archivos

El equipo cliente se comunica con el equipo servidor a través de una red de área local mediante un protocolo de transporte. por ejemplo, TCP o XNS. El cliente envía las solicitudes al servidor para recuperar los datos. El software del equipo cliente que genera las solicitudes de archivo se denomina *redirector* porque redirige las solicitudes de archivos locales al equipo servidor. El software del equipo que recibe y actúa sobre las solicitudes de archivo se denomina *servidor* porque sirve a los clientes. El formato específico de estas solicitudes se denomina protocolo SMB.

A continuación se enumeran las funciones de transporte de servidor.



| Función                                                     | Descripción                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetServerComputerNameAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernameadd) | Enlaza un nombre de servidor emulado a cada uno de los protocolos de transporte en los que un servidor está activo. (Combina la funcionalidad de la función [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum) y la función [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex) ).                                            |
| [**NetServerComputerNameDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernamedel) | Desconecta cada protocolo de transporte de red de un nombre de servidor emulado establecido por una llamada anterior a la función **NetServerComputerNameAdd** .                                                                                                                                                                               |
| [**NetServerTransportAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportadd)       | Enlaza el servidor especificado al Protocolo de transporte. (Esta función solo admite el nivel de información de la información de [**transporte del servidor \_ \_ \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0) ).                                                                                                                                                |
| [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)   | Enlaza el servidor especificado al Protocolo de transporte. (Esta función extendida es compatible con los niveles de información de transporte de servidor [**\_ \_ información \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1), información de [**transporte de servidor \_ \_ \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)e información de [**transporte de servidor \_ \_ \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3) ). |
| [**NetServerTransportDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportdel)       | Desconecta el protocolo de transporte del servidor.                                                                                                                                                                                                                                                                         |
| [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum)     | Enumera los protocolos de transporte administrados por el servidor.                                                                                                                                                                                                                                                                   |



 

Las funciones de transporte de servidor están disponibles en los siguientes niveles de información:

-   [**Información de transporte de servidor \_ \_ \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0)
-   [**Información de transporte de servidor \_ \_ \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1)
-   [**Información de transporte de servidor \_ \_ \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)
-   [**Información de transporte de servidor \_ \_ \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3)

Las funciones de transporte de estación de trabajo realizan operaciones equivalentes para la estación de trabajo.

**Windows Server 2003 y Windows XP/2000:** El redirector no admite la función [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd) o la función [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel) . Puede cambiar la configuración predeterminada de los protocolos de transporte manualmente a través del cuadro de diálogo **propiedades de conexión de área local** en la carpeta **redes y conexiones de acceso telefónico** .

A continuación se enumeran las funciones de transporte de estación de trabajo.



| Función                                               | Descripción                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------|
| [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd)   | Conecta el redirector al Protocolo de transporte.                |
| [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel)   | Desconecta el protocolo de transporte del redirector.           |
| [**NetWkstaTransportEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstatransportenum) | Enumera los protocolos de transporte administrados por el redirector. |



 

Las funciones de transporte de estación de trabajo están disponibles en un nivel de información:

-   [**Información de transporte de WKSTA \_ \_ \_ 0**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_transport_info_0)

 

 




