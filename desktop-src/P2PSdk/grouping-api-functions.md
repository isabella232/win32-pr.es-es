---
description: 'La API de agrupación usa las siguientes funciones:'
ms.assetid: 56ea2880-b468-4816-b6c9-5780c807b3f1
title: Agrupación de funciones de API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 888a64096f66a9adf048d91c2d577d71203a03da6d1b698f2ea305396c4be0db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776175"
---
# <a name="grouping-api-functions"></a>Agrupación de funciones de API

La API de agrupación usa las siguientes funciones:

## <a name="group-initialization-and-cleanup-functions"></a>Funciones de inicialización y limpieza de grupos



| Función                                       | Descripción                                                                                                            |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupShutdown**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown) | Cierra un grupo del mismo nivel creado con [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) y elimina los recursos asignados. |
| [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup)   | Inicia un grupo del mismo nivel mediante una versión solicitada de la infraestructura del mismo nivel.                                        |



 

## <a name="group-creation-and-access-functions"></a>Funciones de acceso y creación de grupos



| Función                                                                       | Descripción                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose)                                       | Invalida el identificador de grupo del mismo nivel obtenido por una llamada anterior a la función [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)o [**PeerGroupOpen.**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) |
| [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)                                   | Inicia una búsqueda PNRP para un grupo del mismo nivel e intenta conectarse a él. Una vez que se llama correctamente a esta función, un usuario del mismo nivel puede comunicarse con otros miembros del grupo del mismo nivel.                             |
| [**PeerGroupConnectByAddress**](/windows/desktop/api/P2P/nf-p2p-peergroupconnectbyaddress)                 | Intenta conectarse al grupo del mismo nivel en el que participan otros elementos del mismo nivel con direcciones IPv6 conocidas.                                                                                                       |
| [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)                                     | Crea un nuevo grupo del mismo nivel.                                                                                                                                                                                    |
| [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)                 | Devuelve una cadena XML que puede usar el elemento del mismo nivel especificado para unirse a un grupo.                                                                                                                                |
| [**PeerGroupCreatePasswordInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreatepasswordinvitation) | Devuelve una cadena XML que puede usar el elemento del mismo nivel especificado para unir un grupo con una contraseña correspondiente.                                                                                                       |
| [**PeerGroupDelete**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)                                     | Elimina los datos locales y el certificado asociados a un grupo del mismo nivel.                                                                                                                                         |
| [**PeerGroupGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus)                               | Recupera el estado actual de un grupo.                                                                                                                                                                     |
| [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)                 | Emite credenciales, incluido un GMC, a una identidad específica y, opcionalmente, devuelve una cadena XML de invitación que el elemento del mismo nivel invitado puede usar para unirse a un grupo del mismo nivel.                                                  |
| [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)                                         | Permite que un elemento del mismo nivel con una invitación se una a un grupo del mismo nivel existente.                                                                                                                                             |
| [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)                                         | Abre un grupo del mismo nivel que un mismo nivel ha creado o unido.                                                                                                                                                        |
| [**PeerGroupParseInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)                   | Devuelve una [**estructura DE INFORMACIÓN DE INVITACIÓN \_ \_ DEL**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) MISMO NIVEL con los detalles de una invitación específica.                                                                                        |
| [**PeerGroupPasswordJoin**](/windows/desktop/api/P2P/nf-p2p-peergrouppasswordjoin)                         | Permite a un elemento del mismo nivel con una invitación y la contraseña correcta unirse a un grupo del mismo nivel protegido con contraseña.                                                                                                           |



 

## <a name="group-and-member-information-functions"></a>Funciones de información de grupos y miembros



| Función                                                 | Descripción                                                                                                                        |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)     | Crea una enumeración de los miembros disponibles del grupo del mismo nivel y la información de pertenencia asociada.                                  |
| [**PeerGroupGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergroupgetproperties) | Recupera información sobre las propiedades de un grupo especificado.                                                                      |
| [**PeerGroupSetProperties**](/windows/desktop/api/P2P/nf-p2p-peergroupsetproperties) | Establece las propiedades actuales del grupo del mismo nivel. En la versión 1.0 de esta API, solo el creador del grupo del mismo nivel puede realizar esta operación. |



 

## <a name="records-and-record-management-functions"></a>Funciones de administración de registros y registros



| Función                                                 | Descripción                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)         | Agrega un nuevo registro al grupo del mismo nivel, que se propaga a todos los pares participantes. |
| [**PeerGroupDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)   | Elimina un registro de un grupo del mismo nivel. Solo el creador de un registro puede eliminarlo.      |
| [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)     | Crea una enumeración de registros de grupo del mismo nivel.                                        |
| [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord)         | Recupera un registro de grupo específico.                                                   |
| [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) | Busca registros que coincidan con los criterios proporcionados en la base de datos del grupo del mismo nivel local. |
| [**PeerGroupUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)   | Actualiza un registro dentro de un grupo del mismo nivel específico.                                       |



 

## <a name="group-database-importexport-functions"></a>Funciones de grupo de Import/Export base de datos



| Función                                                   | Descripción                                                                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase) | Exporta una base de datos de grupo del mismo nivel a un archivo específico, que se puede transportar a otro equipo e importar con la [**función PeerGroupImportDatabase.**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) |
| [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) | Importa una base de datos de grupo del mismo nivel desde un archivo local.                                                                                                                                          |



 

## <a name="direct-connection-functions"></a>Funciones de conexión directa



| Función                                                                 | Descripción                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) | Cierra una conexión directa específica entre dos pares.              |
| [**PeerGroupEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections)             | Crea una enumeración de las conexiones activas actualmente en el mismo nivel. |
| [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)   | Establece una conexión directa con otro del mismo nivel en un grupo del mismo nivel.  |
| [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)                           | Envía datos a un miembro a través de una conexión directa o vecino.        |



 

## <a name="group-events-infrastructure"></a>Infraestructura de eventos de grupo



| Función                                                     | Descripción                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)       | Permite a una aplicación recuperar los datos devueltos por un evento de agrupación.                       |
| [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)     | Registra un par para eventos de grupo del mismo nivel específicos.                                               |
| [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) | Anula el registro de un objeto del mismo nivel de la notificación de eventos del mismo nivel asociados al identificador de eventos proporcionado. |



 

## <a name="group-time-conversion-functions"></a>Funciones de conversión de tiempo de grupo



| Función                                                                     | Descripción                                                                                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupPeerTimeToUniversalTime**](/windows/desktop/api/P2P/nf-p2p-peergrouppeertimetouniversaltime) | Convierte el valor de tiempo de referencia mantenido por el grupo del mismo nivel en un valor de tiempo localizado adecuado para mostrarlo en un equipo del mismo nivel. |
| [**PeerGroupUniversalTimeToPeerTime**](/windows/desktop/api/P2P/nf-p2p-peergroupuniversaltimetopeertime) | Convierte un valor de hora local del equipo de un mismo nivel en un valor de tiempo de grupo del mismo nivel común.                                         |



 

## <a name="group-configuration-functions"></a>Funciones de configuración de grupo



| Función                                               | Descripción                                                                                                                       |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig) | Exporta la configuración de grupo para un elemento del mismo nivel como una cadena XML que contiene la identidad, el nombre del grupo y el GMC de la identidad. |
| [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) | Importa una configuración de grupo del mismo nivel para una identidad en función de la configuración específica de una cadena de configuración XML proporcionada.         |



 

 

 



