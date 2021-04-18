---
description: La agrupación punto a punto es una tecnología que permite a los desarrolladores crear una red del mismo nivel segura de forma rápida y eficaz.
ms.assetid: ee72f60b-1e5b-4b69-bda0-2ae80734c144
title: Cómo trabajar con grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7bebf958d0c3fdee6ad0dc400d495c54ec2e6fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545526"
---
# <a name="how-to-work-with-groups"></a>Cómo trabajar con grupos

La agrupación punto a punto es una tecnología que permite a los desarrolladores crear una red del mismo nivel segura de forma rápida y eficaz. En la lista siguiente se identifican las consideraciones principales para crear una aplicación de agrupación del mismo nivel.

-   [Obtener una identidad del mismo nivel](#obtaining-a-peer-identity)
-   [Inicio de un grupo del mismo nivel](#starting-up-the-peer-grouping-infrastructure)
-   [Registro para agrupar eventos](#registering-for-peer-grouping-events)
-   [Conexión a un grupo](#obtaining-a-group-handle)
-   [Crear roles de administrador y de miembro](#creating-administrator-and-member-roles)
-   [Buscar un elemento del mismo nivel](#finding-a-peer)
-   [Conectarse directamente a un elemento del mismo nivel](#connecting-directly-to-a-peer)
-   [Cerrar y cerrar un grupo](#closing-and-shutting-down-a-peer-group)

## <a name="obtaining-a-peer-identity"></a>Obtener una identidad del mismo nivel

Antes de crear o conectarse a un grupo, un elemento del mismo nivel debe obtener una identidad del mismo nivel, que es un nombre que se usa para identificar de forma única un elemento del mismo nivel con un grupo. Para obtener una lista enumerada de todas las identidades del mismo nivel definidas en el elemento del mismo nivel, llame a [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities), que devuelve un identificador a la enumeración. Para obtener las identidades del mismo nivel, llame a [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) con el identificador de la enumeración y el número de miembros que se van a recuperar. Continúe llamando a **PeerGetNextItem** hasta que el parámetro *pCount* devuelva un valor menor que el número de identidades del mismo nivel solicitadas.

Si no existe una identidad del mismo nivel para el mismo nivel, puede crearse mediante una llamada a [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate). Después de crear una identidad del mismo nivel, el elemento del mismo nivel genera un BLOB XML de identidad que contiene la clave pública asignada a él.

La información de identidad del mismo nivel se obtiene llamando a [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml). El creador de grupo o un administrador usan esta información de identidad del mismo nivel para emitir las credenciales necesarias para unirse al grupo, como un BLOB XML de invitación.

Para obtener más información sobre las identidades del mismo nivel, consulte la documentación de la [API de Identity Manager](identity-manager-api.md) .

## <a name="starting-up-the-peer-grouping-infrastructure"></a>Inicio de la infraestructura de agrupación del mismo nivel

Antes de que una aplicación llame a cualquier función de la API de agrupación del mismo nivel, se debe llamar a [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) . Esta función inicializa la infraestructura de agrupación del mismo nivel para la aplicación y establece la versión admitida.

## <a name="obtaining-a-group-handle"></a>Obtener un identificador de grupo

Para conectarse a un grupo y comenzar a participar, se debe obtener un identificador de un grupo del mismo nivel. En la lista siguiente se identifican las tres formas de conectarse a un grupo del mismo nivel:

-   Crear un grupo del mismo nivel llamando a [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), que inicializa un nuevo grupo del mismo nivel y devuelve un identificador válido con el elemento del mismo nivel como propietario y administrador único.
-   Unirse a un grupo del mismo nivel mediante una llamada a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin). Para unirse a un grupo del mismo nivel, un elemento del mismo nivel debe recibir una invitación de un administrador de grupo del mismo nivel. Para obtener una invitación, envíe el BLOB XML de información de identidad al administrador que crea una invitación y la envía a usted mediante un mecanismo externo, como correo electrónico o FTP. La invitación y la identidad del mismo nivel se pasan a **PeerGroupJoin**, que devuelve un identificador válido para el grupo.
-   Abrir un grupo del mismo nivel que un elemento del mismo nivel ha unido previamente llamando a [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen). En esta situación, no es necesario obtener una invitación.

Después de obtener un identificador de grupo del mismo nivel válido de una de las funciones anteriores, puede conectarse a un grupo del mismo nivel llamando a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) con el nuevo identificador.

> [!Note]  
> Si se produce un error en la conexión a un grupo del mismo nivel, \_ \_ \_ se produce el evento error de conexión de eventos de grupo del mismo nivel \_ . El controlador puede intentar restablecer la conexión con el grupo del mismo nivel.

 

## <a name="registering-for-peer-grouping-events"></a>Registrando eventos de agrupación del mismo nivel

Antes de que un elemento del mismo nivel participe en un grupo del mismo nivel, el mismo nivel debe registrarse para los eventos de grupo del mismo nivel. Para registrarse para eventos del mismo nivel específicos, llame a [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)y pase uno o varios de los tipos de evento del mismo nivel definidos en el tipo de evento de grupo del mismo nivel \_ \_ \_ . Debe registrarse para cada evento del mismo nivel que se aplique a la aplicación; por ejemplo, para recibir datos a través de una conexión directa, Regístrese para los eventos de datos entrantes de eventos de grupo del mismo nivel y de eventos \_ \_ \_ \_ de grupo del mismo nivel \_ \_ \_ \_ . Cada llamada toma un identificador de evento y devuelve un identificador de **HPEEREVENT** para ese evento del mismo nivel.

Los controladores de eventos pueden obtener los datos asociados a un evento del mismo nivel pasando el identificador a los eventos del mismo nivel registrados a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata). Estos datos de eventos del mismo nivel se devuelven como una Unión de datos de eventos de grupo del mismo nivel \_ \_ \_ . Si la cola de eventos del mismo nivel está vacía, esta función devuelve elementos del mismo nivel que \_ \_ no son datos de \_ evento \_ .

Puede anular el registro para los eventos del mismo nivel llamando a [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) y proporcionando el identificador del evento del mismo nivel que desea eliminar del registro. Una vez que se llama a la función, los eventos del mismo nivel asociados al identificador ya no se registran.

## <a name="creating-administrator-and-member-roles"></a>Crear roles de administrador y de miembro

El elemento del mismo nivel que crea el grupo del mismo nivel se conoce como creador de grupo del mismo nivel y tiene el rol de administrador de forma predeterminada. Solo el creador del grupo del mismo nivel puede establecer las propiedades del grupo.

Los pares invitados al grupo del mismo nivel pueden ser un administrador o un miembro. Si el administrador que emite la invitación le asigna un rol de administrador, puede invitar a nuevos miembros al grupo del mismo nivel y asignar igualmente el rol de administrador a otros miembros.

Los roles de los miembros del grupo del mismo nivel se establecen en las invitaciones que el administrador proporciona a un miembro. Para agregar más administradores, establezca el valor del parámetro *pRoles* de [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) en Administrador de \_ rol de \_ grupo \_ cuando cree una invitación.

Los miembros pueden participar en un grupo del mismo nivel, pero no pueden invitar y autorizar nuevos miembros, establecer propiedades de grupo o actualizar o eliminar registros de grupo que no crean específicamente. Para asignar el estado de un miembro a un elemento del mismo nivel participante, establezca el valor del parámetro **pRoles** de [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) en miembro del rol de grupo del mismo nivel \_ \_ \_ cuando cree una invitación para ese mismo nivel.

Para cambiar el rol de un miembro, se deben emitir nuevas credenciales que contengan el nuevo rol para ese miembro. Para ello, obtenga la estructura [**de \_ \_ información de la credencial del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) para este miembro de la estructura de miembro del mismo nivel \_ devuelta por [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers). Cambie el campo **pRoles** de la información de la **\_ credencial \_ del mismo nivel** al nuevo rol y pase la estructura a [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials).

Las nuevas credenciales no entrarán en vigor para el elemento del mismo nivel hasta que se conecten al grupo del mismo nivel. Si están conectados actualmente, deben cerrar el grupo y volver a conectarse para obtener las credenciales actualizadas.

## <a name="finding-a-peer"></a>Buscar un elemento del mismo nivel

Para obtener una lista enumerada de todos los elementos del mismo nivel que participan en el grupo del mismo nivel, llame a [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) con el identificador de grupo, que devuelve un identificador a la enumeración. Para obtener los miembros, llame a [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) con el identificador de enumeración y el número de miembros que se van a recuperar. Continúe llamando a **PeerGetNextItem** hasta que el parámetro *pCount* devuelva un valor menor que el número de miembros solicitados. Tenga en cuenta que es posible que no se devuelva la lista completa de miembros disponibles.

Cada miembro se representa como una estructura de [**\_ miembro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_member) , que contiene la identidad del elemento del mismo nivel, los identificadores de nodo y las direcciones IP para los pares activos.

Cuando termine, cierre la enumeración y libere la memoria asociada llamando a [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration).

## <a name="connecting-directly-to-a-peer"></a>Conectarse directamente a un elemento del mismo nivel

Cuando un elemento del mismo nivel se conecta a un grupo del mismo nivel, los intercambios uno a uno directo con otros miembros conectados se inician llamando a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) y proporcionando la identidad del otro nodo del mismo nivel. Esta llamada es asincrónica y devuelve un identificador de conexión de 64 bits. Si la llamada se realiza correctamente, recibirá el \_ evento del mismo nivel evento de conexión directa de evento de grupo del mismo nivel \_ \_ \_ \_ para indicar que la conexión se ha realizado correctamente. Si la conexión es correcta, el identificador de conexión es válido y se puede usar para enviar y recibir datos a través de la conexión directa.

Para poder recibir conexiones directas, el otro elemento del mismo nivel también debe haberse registrado previamente para el \_ \_ evento del \_ mismo nivel de conexión directa de eventos de grupo del mismo nivel \_ .

Para enviar datos a un elemento del mismo nivel, llame a [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) con un identificador de conexión válido. Para recibir datos, el otro nodo del mismo nivel debe estar registrado para el \_ \_ evento del \_ mismo nivel de datos entrantes del evento de grupo del mismo nivel \_ . Del mismo modo, si el elemento de envío del mismo nivel desea recibir datos a su vez, también debe registrarse para el \_ \_ evento del \_ mismo nivel de datos entrantes del evento de grupo del mismo nivel \_ .

Para recibir el conjunto total de conexiones directas activas actualmente con otros elementos del mismo nivel en un grupo, llame a [**PeerGroupEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections) para abrir la enumeración y recorra en iteración la lista de conexiones con [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem).

Para cerrar una conexión directa, llame a [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) y pase el identificador de conexión.

## <a name="closing-and-shutting-down-a-peer-group"></a>Cerrar y apagar un grupo del mismo nivel

Para cerrar una conexión a un grupo del mismo nivel, llame a [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose), que invalida el identificador de grupo, pero no cierra la infraestructura de agrupación del mismo nivel. Los datos del grupo punto a punto se eliminan llamando a [**PeerGroupDelete**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete).

Cuando la aplicación termine de usar la infraestructura de agrupación del mismo nivel, debe llamar a [**PeerGroupShutdown**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown).

 

 



