---
description: 'La API de agrupación utiliza las siguientes funciones:'
ms.assetid: 56ea2880-b468-4816-b6c9-5780c807b3f1
title: Agrupar funciones de la API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d2970ca68d69b16a32cf7a6d546a5852b07dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667432"
---
# <a name="grouping-api-functions"></a>Agrupar funciones de la API

La API de agrupación utiliza las siguientes funciones:

## <a name="group-initialization-and-cleanup-functions"></a>Funciones de inicialización y limpieza de grupos



| Función                                       | Descripción                                                                                                            |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupShutdown**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown) | Cierra un grupo del mismo nivel creado con [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) y desecha los recursos asignados. |
| [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup)   | Inicia un grupo del mismo nivel usando una versión solicitada de la infraestructura del mismo nivel.                                        |



 

## <a name="group-creation-and-access-functions"></a>Creación de grupos y funciones de acceso



| Función                                                                       | Descripción                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose)                                       | Invalida el identificador de grupo del mismo nivel obtenido por una llamada anterior a la función [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)o [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) . |
| [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)                                   | Inicia una búsqueda de PNRP para un grupo del mismo nivel e intenta conectarse a él. Una vez que se llama a esta función correctamente, un elemento del mismo nivel puede comunicarse con otros miembros del grupo del mismo nivel.                             |
| [**PeerGroupConnectByAddress**](/windows/desktop/api/P2P/nf-p2p-peergroupconnectbyaddress)                 | Intenta conectarse al grupo del mismo nivel en el que participan otros elementos del mismo nivel con direcciones IPv6 conocidas.                                                                                                       |
| [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)                                     | Crea un nuevo grupo del mismo nivel.                                                                                                                                                                                    |
| [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)                 | Devuelve una cadena XML que puede ser utilizada por el elemento del mismo nivel especificado para unirse a un grupo.                                                                                                                                |
| [**PeerGroupCreatePasswordInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreatepasswordinvitation) | Devuelve una cadena XML que el elemento del mismo nivel especificado puede usar para unir un grupo con una contraseña coincidente.                                                                                                       |
| [**PeerGroupDelete**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)                                     | Elimina los datos locales y el certificado asociado a un grupo del mismo nivel.                                                                                                                                         |
| [**PeerGroupGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus)                               | Recupera el estado actual de un grupo.                                                                                                                                                                     |
| [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)                 | Emite credenciales, incluido un GMC, a una identidad específica y, opcionalmente, devuelve una cadena XML de invitación que el elemento de mismo nivel invitado puede usar para unirse a un grupo del mismo nivel.                                                  |
| [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)                                         | Permite a un elemento del mismo nivel con una invitación para unirse a un grupo del mismo nivel existente.                                                                                                                                             |
| [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)                                         | Abre un grupo del mismo nivel que un elemento del mismo nivel ha creado o combinado.                                                                                                                                                        |
| [**PeerGroupParseInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)                   | Devuelve una estructura de [**\_ \_ información de invitación del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) con los detalles de una invitación concreta.                                                                                        |
| [**PeerGroupPasswordJoin**](/windows/desktop/api/P2P/nf-p2p-peergrouppasswordjoin)                         | Permite que un elemento del mismo nivel con una invitación y la contraseña correcta se unan a un grupo del mismo nivel protegido con contraseña.                                                                                                           |



 

## <a name="group-and-member-information-functions"></a>Funciones de información de grupo y miembro



| Función                                                 | Descripción                                                                                                                        |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)     | Crea una enumeración de los miembros del grupo del mismo nivel disponibles y la información de pertenencia asociada.                                  |
| [**PeerGroupGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergroupgetproperties) | Recupera información sobre las propiedades de un grupo especificado.                                                                      |
| [**PeerGroupSetProperties**](/windows/desktop/api/P2P/nf-p2p-peergroupsetproperties) | Establece las propiedades del grupo del mismo nivel actual. En la versión 1,0 de esta API, solo el creador del grupo del mismo nivel puede realizar esta operación. |



 

## <a name="records-and-record-management-functions"></a>Funciones de administración de registros y registros



| Función                                                 | Descripción                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)         | Agrega un nuevo registro al grupo del mismo nivel, que se propaga a todos los elementos del mismo nivel participantes. |
| [**PeerGroupDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)   | Elimina un registro de un grupo del mismo nivel. Solo el creador de un registro puede eliminarlo.      |
| [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)     | Crea una enumeración de registros de grupo del mismo nivel.                                        |
| [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord)         | Recupera un registro de grupo específico.                                                   |
| [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) | Busca en la base de datos de grupo del mismo nivel local los registros que coinciden con los criterios proporcionados. |
| [**PeerGroupUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)   | Actualiza un registro dentro de un grupo del mismo nivel específico.                                       |



 

## <a name="group-database-importexport-functions"></a>Funciones de importación y exportación de bases de datos de grupo



| Función                                                   | Descripción                                                                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase) | Exporta una base de datos de grupo del mismo nivel a un archivo específico, que se puede transportar a otro equipo e importarse con la función [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) . |
| [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) | Importa una base de datos de grupo del mismo nivel desde un archivo local.                                                                                                                                          |



 

## <a name="direct-connection-functions"></a>Funciones de conexión directas



| Función                                                                 | Descripción                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) | Cierra una conexión directa específica entre dos elementos del mismo nivel.              |
| [**PeerGroupEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections)             | Crea una enumeración de conexiones actualmente activas en el elemento del mismo nivel. |
| [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)   | Establece una conexión directa con otro elemento del mismo nivel en un grupo del mismo nivel.  |
| [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)                           | Envía datos a un miembro a través de una conexión vecino o directa.        |



 

## <a name="group-events-infrastructure"></a>Infraestructura de eventos de grupo



| Función                                                     | Descripción                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)       | Permite que una aplicación recupere los datos devueltos por un evento de agrupación.                       |
| [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)     | Registra un elemento del mismo nivel para eventos de grupo del mismo nivel concretos.                                               |
| [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) | Anula el registro de un elemento del mismo nivel de la notificación de eventos del mismo nivel asociados al identificador de eventos proporcionado. |



 

## <a name="group-time-conversion-functions"></a>Funciones de conversión de tiempo de grupo



| Función                                                                     | Descripción                                                                                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupPeerTimeToUniversalTime**](/windows/desktop/api/P2P/nf-p2p-peergrouppeertimetouniversaltime) | Convierte el valor de tiempo de referencia mantenido por el grupo del mismo nivel en un valor de hora adaptado adecuado para su presentación en un equipo del mismo nivel. |
| [**PeerGroupUniversalTimeToPeerTime**](/windows/desktop/api/P2P/nf-p2p-peergroupuniversaltimetopeertime) | Convierte un valor de hora local del equipo del mismo nivel a un valor común de tiempo de grupo del mismo nivel.                                         |



 

## <a name="group-configuration-functions"></a>Funciones de configuración de grupo



| Función                                               | Descripción                                                                                                                       |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig) | Exporta la configuración de grupo para un elemento del mismo nivel como una cadena XML que contiene la identidad, el nombre de grupo y el GMC para la identidad. |
| [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) | Importa una configuración de grupo del mismo nivel para una identidad basada en la configuración específica de una cadena de configuración XML proporcionada.         |



 

 

 



