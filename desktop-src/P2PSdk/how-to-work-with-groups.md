---
description: La agrupación punto a punto es una tecnología que permite a los desarrolladores crear una red del mismo nivel segura de forma rápida y eficaz.
ms.assetid: ee72f60b-1e5b-4b69-bda0-2ae80734c144
title: Cómo trabajar con grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7bebf958d0c3fdee6ad0dc400d495c54ec2e6fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069240"
---
# <a name="how-to-work-with-groups"></a>Cómo trabajar con grupos

La agrupación punto a punto es una tecnología que permite a los desarrolladores crear una red del mismo nivel segura de forma rápida y eficaz. En la lista siguiente se identifican las consideraciones principales a la hora de crear una aplicación de agrupación del mismo nivel.

-   [Obtención de una identidad del mismo nivel](#obtaining-a-peer-identity)
-   [Iniciar un grupo del mismo nivel](#starting-up-the-peer-grouping-infrastructure)
-   [Registro de eventos de agrupación](#registering-for-peer-grouping-events)
-   [Conexión a un grupo](#obtaining-a-group-handle)
-   [Creación de roles de administrador y miembro](#creating-administrator-and-member-roles)
-   [Búsqueda de un mismo nivel](#finding-a-peer)
-   [Conectarse directamente a un mismo nivel](#connecting-directly-to-a-peer)
-   [Cerrar y apagar un grupo](#closing-and-shutting-down-a-peer-group)

## <a name="obtaining-a-peer-identity"></a>Obtención de una identidad del mismo nivel

Antes de crear o conectarse a un grupo, un mismo nivel debe obtener una identidad del mismo nivel, que es un nombre que se usa para identificar de forma única un punto a un grupo. Para obtener una lista enumerada de todas las identidades del mismo nivel definidas en el elemento del mismo nivel, llame a [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities), que devuelve un identificador a la enumeración . Para obtener las identidades del mismo nivel, llame a [**PeerGetNextItem con**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) el identificador de enumeración y el número de miembros que se recuperarán. Siga llamando **a PeerGetNextItem hasta** que el *parámetro pCount* devuelva un valor menor que el número de identidades del mismo nivel solicitadas.

Si no existe una identidad del mismo nivel para el mismo nivel, se puede crear llamando a [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate). Después de crear una identidad del mismo nivel, el elemento del mismo nivel genera un blob XML de identidad que contiene la clave pública asignada.

La información de identidad del mismo nivel se obtiene mediante una llamada [**a PeerIdentityGetXML.**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) El creador del grupo o un administrador usan esta información de identidad del mismo nivel para emitir las credenciales necesarias para unirse al grupo, como un blob XML de invitación.

Para más información sobre las identidades del mismo nivel, consulte la documentación de [la API de Identity Manager.](identity-manager-api.md)

## <a name="starting-up-the-peer-grouping-infrastructure"></a>Iniciar la infraestructura de agrupación del mismo nivel

Antes de que una aplicación llame a cualquier función de peer grouping API, se debe llamar a [**PeerGroupStartup.**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) Esta función inicializa la infraestructura de agrupación del mismo nivel para la aplicación y establece la versión admitida.

## <a name="obtaining-a-group-handle"></a>Obtener un identificador de grupo

Para conectarse a un grupo y empezar a participar, se debe obtener un identificador a un grupo del mismo nivel. En la lista siguiente se identifican las tres maneras de conectarse a un grupo del mismo nivel:

-   Crear un grupo del mismo nivel mediante una llamada a [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), que inicializa un nuevo grupo del mismo nivel y devuelve un identificador válido con el mismo nivel como propietario y administrador único.
-   Unirse a un grupo del mismo nivel mediante una [**llamada a PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin). Para unirse a un grupo del mismo nivel, un elemento del mismo nivel debe recibir una invitación de un administrador del grupo del mismo nivel. Para obtener una invitación, envíe el blob XML de información de identidad al administrador que crea una invitación y la envía mediante un mecanismo externo, como correo electrónico o FTP. La invitación y la identidad del mismo nivel se pasan a **PeerGroupJoin**, que devuelve un identificador válido al grupo.
-   Para abrir un grupo del mismo nivel al que se ha unido anteriormente un mismo nivel, llame a [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen). En esta situación, no es necesario obtener una invitación.

Después de obtener un identificador de grupo del mismo nivel válido de una de las funciones anteriores, puede conectarse a un grupo del mismo nivel llamando a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) con el nuevo identificador.

> [!Note]  
> Si se produce un error en la conexión a un grupo del mismo nivel, se produce el evento PEER \_ GROUP \_ EVENT CONNECTION \_ \_ FAILED. El controlador puede intentar restablecer la conexión al grupo del mismo nivel.

 

## <a name="registering-for-peer-grouping-events"></a>Registro de eventos de agrupación del mismo nivel

Antes de que un mismo nivel participe en un grupo del mismo nivel, el mismo nivel debe registrarse para los eventos de grupo del mismo nivel. Para registrarse para eventos del mismo nivel específicos, llame a [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)y pase uno o varios de los tipos de eventos del mismo nivel definidos en PEER \_ GROUP EVENT \_ \_ TYPE. Debe registrarse para cada evento del mismo nivel que se aplique a la aplicación; Por ejemplo, para recibir datos a través de una conexión directa, regístrese para los eventos PEER GROUP EVENT DIRECT CONNECTION y \_ \_ PEER GROUP EVENT \_ \_ \_ \_ \_ INCOMING \_ DATA. Cada llamada toma un identificador de evento y devuelve un **identificador HPEEREVENT** para ese evento del mismo nivel.

Los controladores de eventos pueden obtener los datos asociados a un evento del mismo nivel pasando el identificador a los eventos del mismo nivel registrados a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata). Estos datos de eventos del mismo nivel se devuelven como una unión DE \_ DATOS DE EVENTOS DE GRUPO DEL MISMO \_ \_ NIVEL. Si la cola de eventos del mismo nivel está vacía, esta función devuelve PEER \_ S \_ NO EVENT \_ \_ DATA.

Puede anular el registro de eventos del mismo nivel llamando a [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) y proporcionando el identificador del evento del mismo nivel que desea anular el registro. Después de llamar a la función, los eventos del mismo nivel asociados al identificador ya no se registran.

## <a name="creating-administrator-and-member-roles"></a>Creación de roles de administrador y miembro

El usuario del mismo nivel que crea el grupo del mismo nivel se conoce como creador del grupo del mismo nivel y tiene el rol de administrador de forma predeterminada. Solo el creador del grupo del mismo nivel puede establecer las propiedades del grupo.

Los usuarios del mismo nivel invitados al grupo del mismo nivel pueden ser administradores o miembros. Si el administrador que emite la invitación les asigna un rol de administrador, puede invitar a nuevos miembros al grupo del mismo nivel y, del mismo modo, asignar el rol de administrador a otros miembros.

Los roles de los miembros del grupo del mismo nivel se establecen en las invitaciones que el administrador proporciona a un miembro. Para agregar más administradores, establezca el valor del parámetro *pRoles* de [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) en PEER GROUP ROLE ADMIN al \_ crear una \_ \_ invitación.

Los miembros pueden participar en un grupo del mismo nivel, pero no pueden invitar ni autorizar a nuevos miembros, establecer propiedades de grupo o actualizar o eliminar registros de grupo que no creen específicamente. Para asignar el estado de miembro a un elemento del mismo nivel participante, establezca el valor del parámetro **pRoles** de [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) en PEER GROUP ROLE MEMBER al crear una invitación para ese elemento del \_ mismo \_ \_ nivel.

Para cambiar el rol de un miembro, se deben emitir nuevas credenciales que contengan el nuevo rol a ese miembro. Para ello, obtenga la estructura [**PEER \_ CREDENTIAL \_ INFO**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) para este miembro de la estructura PEER MEMBER devuelta por \_ [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers). Cambie el **campo pRoles** de **PEER \_ CREDENTIAL \_ INFO** al nuevo rol y pase la estructura a [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials).

Las nuevas credenciales no entrarán en vigor para el mismo nivel hasta que se conecten al grupo del mismo nivel. Si están conectados actualmente, deben cerrar el grupo y volver a conectarse para obtener las credenciales actualizadas.

## <a name="finding-a-peer"></a>Búsqueda de un mismo nivel

Para obtener una lista enumerada de todos los elementos del mismo nivel que participan en el grupo del mismo nivel, llame a [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) con el identificador de grupo, que devuelve un identificador a la enumeración . Para obtener los miembros, llame a [**PeerGetNextItem con**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) el identificador de enumeración y el número de miembros que se recuperarán. Siga llamando **a PeerGetNextItem** hasta que el *parámetro pCount* devuelva un valor menor que el número de miembros solicitados. Tenga en cuenta que es posible que no se devuelva la lista completa de miembros disponibles.

Cada miembro se representa como una estructura [**PEER \_ MEMBER,**](/windows/desktop/api/P2P/ns-p2p-peer_member) que contiene la identidad del elemento del mismo nivel, los id. de nodo y las direcciones IP de los elementos del mismo nivel activos.

Cuando termine, cierre la enumeración y libere la memoria asociada mediante una llamada [**a PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration).

## <a name="connecting-directly-to-a-peer"></a>Conectarse directamente a un mismo nivel

Cuando un mismo nivel está conectado a un grupo del mismo nivel, los intercambios directos uno a uno con otros miembros conectados se inician llamando a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) y suministrando la identidad del otro mismo nivel. Esta llamada es asincrónica y devuelve un identificador de conexión de 64 bits. Si la llamada se realiza correctamente, recibirá el evento del mismo nivel EVENTO DE CONEXIÓN DIRECTA DEL MISMO GRUPO DE EVENTOS para indicar \_ que la conexión se ha realizado \_ \_ \_ \_ correctamente. Si la conexión es correcta, el identificador de conexión es válido y se puede usar para enviar y recibir datos a través de la conexión directa.

Para poder recibir conexiones directas, el otro mismo nivel también debe haber registrado previamente para el evento del mismo nivel PEER \_ GROUP \_ EVENT DIRECT \_ \_ CONNECTION.

Para enviar datos a un elemento del mismo nivel, llame a [**PeerGroupSendData con**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) un identificador de conexión válido. Para recibir datos, el otro del mismo nivel debe estar registrado para el evento del mismo nivel PEER \_ GROUP \_ EVENT \_ INCOMING \_ DATA. Del mismo modo, si el mismo nivel de envío quiere recibir datos a su vez, también se debe registrar para el evento del mismo nivel DE DATOS ENTRANTES EVENTO DE GRUPO DEL \_ \_ MISMO \_ \_ NIVEL.

Para recibir el conjunto total de conexiones directas activas actualmente con otros elementos del mismo nivel de un grupo, llame a [**PeerGroupEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections) para abrir la enumeración e iterar por la lista de conexiones mediante [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem).

Para cerrar una conexión directa, llame a [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) y pase el identificador de conexión.

## <a name="closing-and-shutting-down-a-peer-group"></a>Cerrar y apagar un grupo del mismo nivel

Para cerrar una conexión a un grupo del mismo nivel, llame a [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose), lo que invalida el identificador de grupo, pero no cierra la infraestructura de agrupación del mismo nivel. Los datos del grupo punto a punto se eliminan mediante una llamada [**a PeerGroupDelete**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete).

Cuando la aplicación termine de usar la infraestructura de agrupación del mismo nivel, debe llamar a [**PeerGroupShutdown**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown).

 

 



