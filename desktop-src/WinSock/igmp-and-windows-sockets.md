---
description: Windows Sockets habilita la detección de escucha de multidifusión (MLD) en IPv6 y el protocolo de administración de grupos de Internet (IGMP) en IPv4 para las aplicaciones de multidifusión mediante el uso de opciones de socket y ioctl.
ms.assetid: a5de4273-e86e-4f13-b068-256cb38706d4
title: MLD y IGMP con Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6cb9f9c345463e283adea0136037d7ccd03cebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275399"
---
# <a name="mld-and-igmp-using-windows-sockets"></a>MLD y IGMP con Windows Sockets

Windows Sockets habilita la detección de escucha de multidifusión (MLD) en IPv6 y el protocolo de administración de grupos de Internet (IGMP) en IPv4 para las aplicaciones de multidifusión mediante el uso de opciones de socket y ioctl. En esta página se describen las opciones de socket que habilitan la programación multidifusión y se describe cómo se usan. Para ver las definiciones de cada opción de socket, consulte la página [Opciones de socket](socket-options.md) .

Para obtener información sobre cómo usar ioctl para la programación de multidifusión, vea [programación de multidifusión basada en el estado final](final-state-based-multicast-programming.md) más adelante en esta sección.

En Windows Vista y versiones posteriores, hay disponible un conjunto de opciones de socket para la programación de multidifusión que admiten direcciones IPv6 e IPv4. Estas opciones de socket son independientes de IP y se pueden usar en IPv6 e IPv4. En IPv6, estas opciones de socket usan MLDv2. En IPv4, estas opciones de socket usan IGMPv3. Estas opciones independientes de IP son las opciones de socket preferidas para la programación multidifusión en Windows Vista y versiones posteriores. Windows Sockets usa las siguientes opciones de socket: 

| Opción de socket               | Tipo de argumento                                            |
|-----------------------------|----------------------------------------------------------|
| \_origen de bloque MCAST \_        | [**Grupo \_ de SOURCE \_ req**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) (estructura) |
| \_grupo de combinación MCAST \_          | [**Grupo \_ de REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req) (estructura)                |
| MCAST \_ unirse \_ al \_ grupo de origen  | [**Grupo \_ de SOURCE \_ req**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) (estructura) |
| Grupo de MCAST \_ leave \_         | [**Grupo \_ de REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req) (estructura)                |
| MCAST \_ abandonar \_ grupo de origen \_ | [**Grupo \_ de SOURCE \_ req**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) (estructura) |
| \_origen de DESbloqueo de MCAST \_      | [**Grupo \_ de SOURCE \_ req**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) (estructura) |



 

Hay disponible un conjunto de opciones de socket para la programación multidifusión que admiten direcciones solo IPv6. Estas opciones de socket usan MLDv1 o MLDv2. La versión de MLD utilizada depende de la versión de Windows. MLDv2 es compatible con Windows Vista y versiones posteriores. Windows Sockets usa las siguientes opciones de socket: 

| Opción de socket          | Tipo de argumento                             |
|------------------------|-------------------------------------------|
| IPV6 \_ agregar \_ pertenencia  | [**estructura \_ mreq de IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) |
| \_Eliminación de \_ PERtenencia IPv6 | [**estructura \_ mreq de IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) |



 

Hay disponible un conjunto de opciones de socket para la programación multidifusión que admiten direcciones solo IPv4. Estas opciones de socket usan IGMPv3 o IGMPv2. La versión de IGMP usada depende de la versión de Windows. IGMPv3 es compatible con Windows Vista y versiones posteriores. Windows Sockets usa las siguientes opciones de socket:

| Opción de socket                | Tipo de argumento                                        |
|------------------------------|------------------------------------------------------|
| \_agregar \_ pertenencia de IP          | estructura de [**\_ mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq)                |
| \_pertenencia \_ al origen de adición de IP \_  | estructura de [**\_ \_ origen de mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| \_origen de bloque de IP \_            | estructura de [**\_ \_ origen de mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| pertenencia de drop de IP \_ \_         | estructura de [**\_ mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq)                |
| \_pertenencia \_ al origen de eliminación de IP \_ | estructura de [**\_ \_ origen de mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| \_origen de DESbloqueo de IP \_          | estructura de [**\_ \_ origen de mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |



 

Cuando IGMPv3 está disponible, las \_ opciones IP Add \_ source \_ Membership, \_ \_ Source Block Source, IP \_ Drop \_ source \_ Membership y IP \_ unblock source \_ se controlan de forma más eficaz, ya que el enrutador puede controlar el filtrado. Cuando solo está disponible IGMPv2, el host debe controlar el filtrado.

Hay dos categorías en las que es probable que la mayoría de las aplicaciones queden: cualquier origen y código fuente controlado.

-   Las aplicaciones **de origen** aceptan todos los orígenes de forma predeterminada, lo que permite desactivar los orígenes individuales según sea necesario. Un ejemplo de una aplicación de origen cualquiera es una llamada de conferencia de vídeo que permite a todos los destinatarios participar.
-   Las aplicaciones **de origen controlado** limitan los orígenes a una lista determinada, como una estación de radio de Internet, o la difusión de un evento notable. El proceso de usar las opciones de socket es ligeramente diferente para cada uno.

En Windows Vista y versiones posteriores, los siguientes pasos se aplican a las aplicaciones de origen:

- Use **el \_ \_ Grupo MCAST join** para unirse a un grupo.  
- Use **el \_ \_ origen de bloque MCAST** para desactivar un origen determinado, si es necesario.  
- Use **el \_ \_ origen de desbloqueo de MCAST** para volver a permitir un origen bloqueado, si es necesario.  
- Use **MCAST \_ leave \_ Group** para abandonar el grupo.  

En Windows Vista y versiones posteriores, los siguientes pasos se aplican a las aplicaciones de origen controlado:

- Use **el \_ \_ \_ grupo de origen MCAST join** para unir cada par grupo/origen.  
- Use **MCAST \_ dejar \_ el \_ grupo de origen** para dejar cada grupo/origen, o use **MCAST \_ dejar \_ Grupo** para dejar todos los orígenes, si todos los orígenes usan la misma dirección de grupo.  

Los pasos siguientes se aplican a las aplicaciones de cualquier origen:

- Use **la \_ \_ pertenencia a agregar de IP** para unirse a un grupo (**IPv6 \_ agregar \_ pertenencia** para IPv6).  
- Use **el \_ \_ origen de bloque de IP** para desactivar un origen determinado, si es necesario.  
- Use **el \_ \_ origen de desbloqueo de IP** para volver a permitir un origen bloqueado, si es necesario.  
- Use **la \_ \_ pertenencia** a un drop de IP para abandonar el grupo (**IPv6 \_ Drop \_ Membership** para IPv6).  

Los pasos siguientes se aplican a las aplicaciones de origen controlado:

- Use **la \_ \_ \_ pertenencia** a un origen de adición de IP para combinar cada par de grupo/origen.  
- Use **la \_ \_ \_ pertenencia** a un origen de eliminación de IP para dejar cada grupo/origen, o use la **\_ \_ pertenencia de drop de IP** para dejar todos los orígenes, si todos los orígenes usan la misma dirección de grupo.  

El orden en el que se establecen estas opciones de socket tiene reglas asociadas. Para obtener información y solucionar problemas relacionados con las opciones de socket de multidifusión, vea comportamiento de la [opción de socket de multidifusión](multicast-socket-option-behavior.md).
