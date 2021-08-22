---
description: Windows Sockets habilita la detección de agentes de escucha de multidifusión (MLD) en IPv6 y el Protocolo de administración de grupos de Internet (IGMP) en IPv4 para aplicaciones de multidifusión mediante el uso de opciones de socket e IOCTL.
ms.assetid: a5de4273-e86e-4f13-b068-256cb38706d4
title: MLD e IGMP mediante Windows sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2c550cf2c1463f5b646efc286c05010274d3cb44e13b9559302452bccb81c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051653"
---
# <a name="mld-and-igmp-using-windows-sockets"></a>MLD e IGMP mediante Windows sockets

Windows Sockets habilita la detección de agentes de escucha de multidifusión (MLD) en IPv6 y el Protocolo de administración de grupos de Internet (IGMP) en IPv4 para aplicaciones de multidifusión mediante el uso de opciones de socket e IOCTL. En esta página se describen las opciones de socket que habilitan la programación de multidifusión y se describe cómo se usan. Para obtener definiciones de cada opción de socket, consulte la [página Opciones de](socket-options.md) socket.

Para obtener información sobre el uso de IOCTL para la programación de multidifusión, vea [Programación de](final-state-based-multicast-programming.md) multidifusión basada en estado final más adelante en esta sección.

En Windows Vista y versiones posteriores, hay un conjunto de opciones de socket disponibles para la programación de multidifusión que admite direcciones IPv6 e IPv4. Estas opciones de socket son independientes de ip y se pueden usar en IPv6 e IPv4. En IPv6, estas opciones de socket usan MLDv2. En IPv4, estas opciones de socket usan IGMPv3. Estas opciones independientes de IP son las opciones de socket preferidas para la programación de multidifusión en Windows Vista y versiones posteriores. Windows Sockets usa las siguientes opciones de socket: 

| Opción socket               | Tipo de argumento                                            |
|-----------------------------|----------------------------------------------------------|
| ORIGEN DEL \_ BLOQUE MCAST \_        | [**GROUP \_ Source \_ REQ (estructura)**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| MCAST \_ JOIN \_ GROUP          | [**GROUP \_ Estructura REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req)                |
| MCAST \_ JOIN \_ SOURCE \_ GROUP  | [**GROUP \_ Source \_ REQ (estructura)**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| MCAST \_ LEAVE \_ GROUP         | [**GROUP \_ Estructura REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req)                |
| MCAST \_ LEAVE \_ SOURCE \_ GROUP | [**GROUP \_ Source \_ REQ (estructura)**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| ORIGEN DE DESBLOQUEO DE MCAST \_ \_      | [**GROUP \_ Source \_ REQ (estructura)**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |



 

Hay un conjunto de opciones de socket disponibles para la programación de multidifusión que admite solo direcciones IPv6. Estas opciones de socket usan MLDv1 o MLDv2. La versión de MLD usada depende de la versión de Windows. MLDv2 se admite en Windows Vista y versiones posteriores. Windows Sockets usa las siguientes opciones de socket: 

| Opción socket          | Tipo de argumento                             |
|------------------------|-------------------------------------------|
| AGREGAR PERTENENCIA A IPV6 \_ \_  | [**Estructura \_ mreq de ipv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) |
| DROP MEMBERSHIP de IPV6 \_ \_ | [**Estructura \_ mreq de ipv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) |



 

Hay un conjunto de opciones de socket disponibles para la programación de multidifusión que admite solo direcciones IPv4. Estas opciones de socket usan IGMPv3 o IGMPv2. La versión de IGMP usada depende de la versión de Windows. IGMPv3 se admite en Windows Vista y versiones posteriores. Windows Sockets usa las siguientes opciones de socket:

| Opción socket                | Tipo de argumento                                        |
|------------------------------|------------------------------------------------------|
| AGREGAR PERTENENCIA A IP \_ \_          | [**ip \_ mreq (estructura)**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq)                |
| IP \_ ADD \_ SOURCE \_ MEMBERSHIP  | [**Ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) structure |
| ORIGEN \_ DE BLOQUE DE \_ IP            | [**Ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) structure |
| DROP \_ MEMBERSHIP de IP \_         | [**ip \_ mreq (estructura)**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq)                |
| PERTENENCIA AL \_ ORIGEN \_ DE DROP DE IP \_ | [**Ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) structure |
| ORIGEN \_ DE DESBLOQUEO DE \_ IP          | [**Ip \_ mreq \_ source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) structure |



 

Cuando IGMPv3 está disponible, las opciones IP \_ ADD \_ SOURCE \_ MEMBERSHIP, IP BLOCK SOURCE, IP DROP SOURCE MEMBERSHIP y \_ IP UNBLOCK \_ \_ \_ \_ \_ \_ SOURCE se controlan de forma más eficaz, ya que el enrutador puede controlar el filtrado. Cuando solo está disponible IGMPv2, el host debe controlar el filtrado.

Hay dos categorías en las que es probable que la mayoría de las aplicaciones se resalte: cualquier origen y origen controlado.

-   **Las aplicaciones de cualquier** origen aceptan todos los orígenes de forma predeterminada, lo que permite desactivar los orígenes individuales según sea necesario. Un ejemplo de una aplicación de cualquier origen es una llamada de videoconferencia que permite a todos los destinatarios participar.
-   **Las aplicaciones de origen** controlado limitan los orígenes a una lista determinada, como una estación de radio de Internet o la difusión de un evento importante. El proceso de uso de las opciones de socket es ligeramente diferente para cada una.

En Windows Vista y versiones posteriores, los pasos siguientes se aplican a las aplicaciones de cualquier origen:

- Use **MCAST \_ JOIN GROUP \_ para** unirse a un grupo.  
- Use **MCAST \_ BLOCK SOURCE \_ para** desactivar un origen determinado, si es necesario.  
- Use **MCAST \_ UNBLOCK \_ SOURCE para** volver a permitir un origen bloqueado, si es necesario.  
- Use **MCAST \_ LEAVE GROUP \_ para** salir del grupo.  

En Windows Vista y versiones posteriores, los pasos siguientes se aplican a las aplicaciones de origen controlado:

- Use **MCAST \_ JOIN SOURCE \_ GROUP \_ para** unirse a cada par de grupo/origen.  
- Use **MCAST \_ LEAVE SOURCE \_ GROUP \_ para** salir de cada grupo o origen, o use **MCAST LEAVE \_ \_ GROUP** para dejar todos los orígenes, si todos los orígenes usan la misma dirección de grupo.  

Los pasos siguientes se aplican a las aplicaciones de cualquier origen:

- Use **IP ADD MEMBERSHIP \_ \_ para** unirse a un grupo **(IPV6 \_ ADD \_ MEMBERSHIP** for IPv6).  
- Use **IP BLOCK SOURCE \_ \_ para** desactivar un origen determinado, si es necesario.  
- Use **IP \_ UNBLOCK SOURCE \_ para** volver a permitir un origen bloqueado, si es necesario.  
- Use **DROP \_ MEMBERSHIP \_ de IP** para salir del grupo **(IPV6 \_ DROP \_ MEMBERSHIP** para IPv6).  

Los pasos siguientes se aplican a las aplicaciones de origen controlado:

- Use **IP ADD SOURCE MEMBERSHIP \_ \_ \_ para** unirse a cada par de grupo/origen.  
- Use **IP DROP SOURCE MEMBERSHIP \_ \_ \_ para** salir de cada grupo o origen, o use **IP DROP \_ \_ MEMBERSHIP** para dejar todos los orígenes, si todos los orígenes usan la misma dirección de grupo.  

El orden en que se establecen estas opciones de socket tiene reglas asociadas. Para obtener información e información de solución de problemas sobre las opciones de socket de multidifusión, vea Comportamiento de [las opciones de socket de multidifusión.](multicast-socket-option-behavior.md)
