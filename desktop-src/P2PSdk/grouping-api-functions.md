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
# <a name="grouping-api-functions"></a><span data-ttu-id="28fd4-103">Agrupar funciones de la API</span><span class="sxs-lookup"><span data-stu-id="28fd4-103">Grouping API Functions</span></span>

<span data-ttu-id="28fd4-104">La API de agrupación utiliza las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="28fd4-104">The Grouping API uses the following functions:</span></span>

## <a name="group-initialization-and-cleanup-functions"></a><span data-ttu-id="28fd4-105">Funciones de inicialización y limpieza de grupos</span><span class="sxs-lookup"><span data-stu-id="28fd4-105">Group Initialization and Cleanup Functions</span></span>



| <span data-ttu-id="28fd4-106">Función</span><span class="sxs-lookup"><span data-stu-id="28fd4-106">Function</span></span>                                       | <span data-ttu-id="28fd4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="28fd4-107">Description</span></span>                                                                                                            |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28fd4-108">**PeerGroupShutdown**</span><span class="sxs-lookup"><span data-stu-id="28fd4-108">**PeerGroupShutdown**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown) | <span data-ttu-id="28fd4-109">Cierra un grupo del mismo nivel creado con [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) y desecha los recursos asignados.</span><span class="sxs-lookup"><span data-stu-id="28fd4-109">Closes a peer group created with [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) and disposes of any allocated resources.</span></span> |
| [<span data-ttu-id="28fd4-110">**PeerGroupStartup**</span><span class="sxs-lookup"><span data-stu-id="28fd4-110">**PeerGroupStartup**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupstartup)   | <span data-ttu-id="28fd4-111">Inicia un grupo del mismo nivel usando una versión solicitada de la infraestructura del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="28fd4-111">Initiates a peer group by using a requested version of the Peer infrastructure.</span></span>                                        |



 

## <a name="group-creation-and-access-functions"></a><span data-ttu-id="28fd4-112">Creación de grupos y funciones de acceso</span><span class="sxs-lookup"><span data-stu-id="28fd4-112">Group Creation and Access Functions</span></span>



| <span data-ttu-id="28fd4-113">Función</span><span class="sxs-lookup"><span data-stu-id="28fd4-113">Function</span></span>                                                                       | <span data-ttu-id="28fd4-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="28fd4-114">Description</span></span>                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28fd4-115">**PeerGroupClose**</span><span class="sxs-lookup"><span data-stu-id="28fd4-115">**PeerGroupClose**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupclose)                                       | <span data-ttu-id="28fd4-116">Invalida el identificador de grupo del mismo nivel obtenido por una llamada anterior a la función [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)o [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) .</span><span class="sxs-lookup"><span data-stu-id="28fd4-116">Invalidates the peer group handle obtained by a previous call to the [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), or [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) function.</span></span> |
| [<span data-ttu-id="28fd4-117">**PeerGroupConnect**</span><span class="sxs-lookup"><span data-stu-id="28fd4-117">**PeerGroupConnect**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)                                   | <span data-ttu-id="28fd4-118">Inicia una búsqueda de PNRP para un grupo del mismo nivel e intenta conectarse a él.</span><span class="sxs-lookup"><span data-stu-id="28fd4-118">Initiates a PNRP search for a peer group and attempts to connect to it.</span></span> <span data-ttu-id="28fd4-119">Una vez que se llama a esta función correctamente, un elemento del mismo nivel puede comunicarse con otros miembros del grupo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="28fd4-119">After this function is called successfully, a peer can communicate with other members of the peer group.</span></span>                             |
| [<span data-ttu-id="28fd4-120">**PeerGroupConnectByAddress**</span><span class="sxs-lookup"><span data-stu-id="28fd4-120">**PeerGroupConnectByAddress**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupconnectbyaddress)                 | <span data-ttu-id="28fd4-121">Intenta conectarse al grupo del mismo nivel en el que participan otros elementos del mismo nivel con direcciones IPv6 conocidas.</span><span class="sxs-lookup"><span data-stu-id="28fd4-121">Attempts to connect to the peer group that other peers with known IPv6 addresses are participating in.</span></span>                                                                                                       |
| [<span data-ttu-id="28fd4-122">**PeerGroupCreate**</span><span class="sxs-lookup"><span data-stu-id="28fd4-122">**PeerGroupCreate**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)                                     | <span data-ttu-id="28fd4-123">Crea un nuevo grupo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="28fd4-123">Creates a new peer group.</span></span>                                                                                                                                                                                    |
| [<span data-ttu-id="28fd4-124">**PeerGroupCreateInvitation**</span><span class="sxs-lookup"><span data-stu-id="28fd4-124">**PeerGroupCreateInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)                 | <span data-ttu-id="28fd4-125">Devuelve una cadena XML que puede ser utilizada por el elemento del mismo nivel especificado para unirse a un grupo.</span><span class="sxs-lookup"><span data-stu-id="28fd4-125">Returns an XML string that can be used by the specified peer to join a group.</span></span>                                                                                                                                |
| [<span data-ttu-id="28fd4-126">**PeerGroupCreatePasswordInvitation**</span><span class="sxs-lookup"><span data-stu-id="28fd4-126">**PeerGroupCreatePasswordInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreatepasswordinvitation) | <span data-ttu-id="28fd4-127">Devuelve una cadena XML que el elemento del mismo nivel especificado puede usar para unir un grupo con una contraseña coincidente.</span><span class="sxs-lookup"><span data-stu-id="28fd4-127">Returns an XML string that can be used by the specified peer to join a group with a matching password.</span></span>                                                                                                       |
| [<span data-ttu-id="28fd4-128">**PeerGroupDelete**</span><span class="sxs-lookup"><span data-stu-id="28fd4-128">**PeerGroupDelete**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)                                     | <span data-ttu-id="28fd4-129">Elimina los datos locales y el certificado asociado a un grupo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="28fd4-129">Deletes the local data and certificate associated with a peer group.</span></span>                                                                                                                                         |
| [<span data-ttu-id="28fd4-130">**PeerGroupGetStatus**</span><span class="sxs-lookup"><span data-stu-id="28fd4-130">**PeerGroupGetStatus**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus)                               | <span data-ttu-id="28fd4-131">Recupera el estado actual de un grupo.</span><span class="sxs-lookup"><span data-stu-id="28fd4-131">Retrieves the current status of a group.</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="28fd4-132">**PeerGroupIssueCredentials**</span><span class="sxs-lookup"><span data-stu-id="28fd4-132">**PeerGroupIssueCredentials**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)                 | <span data-ttu-id="28fd4-133">Emite credenciales, incluido un GMC, a una identidad específica y, opcionalmente, devuelve una cadena XML de invitación que el elemento de mismo nivel invitado puede usar para unirse a un grupo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="28fd4-133">Issues credentials, including a GMC, to a specific identity, and optionally returns an invitation XML string the invited peer can use to join a peer group.</span></span>                                                  |
| [<span data-ttu-id="28fd4-134">**PeerGroupJoin**</span><span class="sxs-lookup"><span data-stu-id="28fd4-134">**PeerGroupJoin**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)                                         | <span data-ttu-id="28fd4-135">Permite a un elemento del mismo nivel con una invitación para unirse a un grupo del mismo nivel existente.</span><span class="sxs-lookup"><span data-stu-id="28fd4-135">Allows a peer with an invitation to join an existing peer group.</span></span>                                                                                                                                             |
| [<span data-ttu-id="28fd4-136">**PeerGroupOpen**</span><span class="sxs-lookup"><span data-stu-id="28fd4-136">**PeerGroupOpen**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupopen)                                         | <span data-ttu-id="28fd4-137">Abre un grupo del mismo nivel que un elemento del mismo nivel ha creado o combinado.</span><span class="sxs-lookup"><span data-stu-id="28fd4-137">Opens a peer group that a peer has created or joined.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="28fd4-138">**PeerGroupParseInvitation**</span><span class="sxs-lookup"><span data-stu-id="28fd4-138">**PeerGroupParseInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)                   | <span data-ttu-id="28fd4-139">Devuelve una estructura de [**\_ \_ información de invitación del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) con los detalles de una invitación concreta.</span><span class="sxs-lookup"><span data-stu-id="28fd4-139">Returns a [**PEER\_INVITATION\_INFO**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) structure with the details of a specific invitation.</span></span>                                                                                        |
| [<span data-ttu-id="28fd4-140">**PeerGroupPasswordJoin**</span><span class="sxs-lookup"><span data-stu-id="28fd4-140">**PeerGroupPasswordJoin**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergrouppasswordjoin)                         | <span data-ttu-id="28fd4-141">Permite que un elemento del mismo nivel con una invitación y la contraseña correcta se unan a un grupo del mismo nivel protegido con contraseña.</span><span class="sxs-lookup"><span data-stu-id="28fd4-141">Allows a peer with an invitation and the correct password to join a password-protected peer group.</span></span>                                                                                                           |



 

## <a name="group-and-member-information-functions"></a><span data-ttu-id="28fd4-142">Funciones de información de grupo y miembro</span><span class="sxs-lookup"><span data-stu-id="28fd4-142">Group and Member Information Functions</span></span>



| <span data-ttu-id="28fd4-143">Función</span><span class="sxs-lookup"><span data-stu-id="28fd4-143">Function</span></span>                                                 | <span data-ttu-id="28fd4-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="28fd4-144">Description</span></span>                                                                                                                        |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28fd4-145">**PeerGroupEnumMembers**</span><span class="sxs-lookup"><span data-stu-id="28fd4-145">**PeerGroupEnumMembers**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)     | <span data-ttu-id="28fd4-146">Crea una enumeración de los miembros del grupo del mismo nivel disponibles y la información de pertenencia asociada.</span><span class="sxs-lookup"><span data-stu-id="28fd4-146">Creates an enumeration of available peer group members and the associated membership information.</span></span>                                  |
| [<span data-ttu-id="28fd4-147">**PeerGroupGetProperties**</span><span class="sxs-lookup"><span data-stu-id="28fd4-147">**PeerGroupGetProperties**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetproperties) | <span data-ttu-id="28fd4-148">Recupera información sobre las propiedades de un grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="28fd4-148">Retrieves information on the properties of a specified group.</span></span>                                                                      |
| [<span data-ttu-id="28fd4-149">**PeerGroupSetProperties**</span><span class="sxs-lookup"><span data-stu-id="28fd4-149">**PeerGroupSetProperties**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsetproperties) | <span data-ttu-id="28fd4-150">Establece las propiedades del grupo del mismo nivel actual.</span><span class="sxs-lookup"><span data-stu-id="28fd4-150">Sets the current peer group properties.</span></span> <span data-ttu-id="28fd4-151">En la versión 1,0 de esta API, solo el creador del grupo del mismo nivel puede realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="28fd4-151">In version 1.0 of this API, only the creator of the peer group can perform this operation.</span></span> |



 

## <a name="records-and-record-management-functions"></a><span data-ttu-id="28fd4-152">Funciones de administración de registros y registros</span><span class="sxs-lookup"><span data-stu-id="28fd4-152">Records and Record Management Functions</span></span>



| <span data-ttu-id="28fd4-153">Función</span><span class="sxs-lookup"><span data-stu-id="28fd4-153">Function</span></span>                                                 | <span data-ttu-id="28fd4-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="28fd4-154">Description</span></span>                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="28fd4-155">**PeerGroupAddRecord**</span><span class="sxs-lookup"><span data-stu-id="28fd4-155">**PeerGroupAddRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)         | <span data-ttu-id="28fd4-156">Agrega un nuevo registro al grupo del mismo nivel, que se propaga a todos los elementos del mismo nivel participantes.</span><span class="sxs-lookup"><span data-stu-id="28fd4-156">Adds a new record to the peer group, which is propagated to all participating peers.</span></span> |
| [<span data-ttu-id="28fd4-157">**PeerGroupDeleteRecord**</span><span class="sxs-lookup"><span data-stu-id="28fd4-157">**PeerGroupDeleteRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)   | <span data-ttu-id="28fd4-158">Elimina un registro de un grupo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="28fd4-158">Deletes a record from a peer group.</span></span> <span data-ttu-id="28fd4-159">Solo el creador de un registro puede eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="28fd4-159">Only the creator of a record can delete it.</span></span>      |
| [<span data-ttu-id="28fd4-160">**PeerGroupEnumRecords**</span><span class="sxs-lookup"><span data-stu-id="28fd4-160">**PeerGroupEnumRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)     | <span data-ttu-id="28fd4-161">Crea una enumeración de registros de grupo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="28fd4-161">Creates an enumeration of peer group records.</span></span>                                        |
| [<span data-ttu-id="28fd4-162">**PeerGroupGetRecord**</span><span class="sxs-lookup"><span data-stu-id="28fd4-162">**PeerGroupGetRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord)         | <span data-ttu-id="28fd4-163">Recupera un registro de grupo específico.</span><span class="sxs-lookup"><span data-stu-id="28fd4-163">Retrieves a specific group record.</span></span>                                                   |
| [<span data-ttu-id="28fd4-164">**PeerGroupSearchRecords**</span><span class="sxs-lookup"><span data-stu-id="28fd4-164">**PeerGroupSearchRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) | <span data-ttu-id="28fd4-165">Busca en la base de datos de grupo del mismo nivel local los registros que coinciden con los criterios proporcionados.</span><span class="sxs-lookup"><span data-stu-id="28fd4-165">Searches the local peer group database for records that match the supplied criteria.</span></span> |
| [<span data-ttu-id="28fd4-166">**PeerGroupUpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="28fd4-166">**PeerGroupUpdateRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)   | <span data-ttu-id="28fd4-167">Actualiza un registro dentro de un grupo del mismo nivel específico.</span><span class="sxs-lookup"><span data-stu-id="28fd4-167">Updates a record within a specific peer group.</span></span>                                       |



 

## <a name="group-database-importexport-functions"></a><span data-ttu-id="28fd4-168">Funciones de importación y exportación de bases de datos de grupo</span><span class="sxs-lookup"><span data-stu-id="28fd4-168">Group Database Import/Export Functions</span></span>



| <span data-ttu-id="28fd4-169">Función</span><span class="sxs-lookup"><span data-stu-id="28fd4-169">Function</span></span>                                                   | <span data-ttu-id="28fd4-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="28fd4-170">Description</span></span>                                                                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28fd4-171">**PeerGroupExportDatabase**</span><span class="sxs-lookup"><span data-stu-id="28fd4-171">**PeerGroupExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase) | <span data-ttu-id="28fd4-172">Exporta una base de datos de grupo del mismo nivel a un archivo específico, que se puede transportar a otro equipo e importarse con la función [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) .</span><span class="sxs-lookup"><span data-stu-id="28fd4-172">Exports a peer group database to a specific file, which can be transported to another computer and imported with the [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) function.</span></span> |
| [<span data-ttu-id="28fd4-173">**PeerGroupImportDatabase**</span><span class="sxs-lookup"><span data-stu-id="28fd4-173">**PeerGroupImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) | <span data-ttu-id="28fd4-174">Importa una base de datos de grupo del mismo nivel desde un archivo local.</span><span class="sxs-lookup"><span data-stu-id="28fd4-174">Imports a peer group database from a local file.</span></span>                                                                                                                                          |



 

## <a name="direct-connection-functions"></a><span data-ttu-id="28fd4-175">Funciones de conexión directas</span><span class="sxs-lookup"><span data-stu-id="28fd4-175">Direct Connection Functions</span></span>



| <span data-ttu-id="28fd4-176">Función</span><span class="sxs-lookup"><span data-stu-id="28fd4-176">Function</span></span>                                                                 | <span data-ttu-id="28fd4-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="28fd4-177">Description</span></span>                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="28fd4-178">**PeerGroupCloseDirectConnection**</span><span class="sxs-lookup"><span data-stu-id="28fd4-178">**PeerGroupCloseDirectConnection**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) | <span data-ttu-id="28fd4-179">Cierra una conexión directa específica entre dos elementos del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="28fd4-179">Closes a specific direct connection between two peers.</span></span>              |
| [<span data-ttu-id="28fd4-180">**PeerGroupEnumConnections**</span><span class="sxs-lookup"><span data-stu-id="28fd4-180">**PeerGroupEnumConnections**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections)             | <span data-ttu-id="28fd4-181">Crea una enumeración de conexiones actualmente activas en el elemento del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="28fd4-181">Creates an enumeration of connections currently active on the peer.</span></span> |
| [<span data-ttu-id="28fd4-182">**PeerGroupOpenDirectConnection**</span><span class="sxs-lookup"><span data-stu-id="28fd4-182">**PeerGroupOpenDirectConnection**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)   | <span data-ttu-id="28fd4-183">Establece una conexión directa con otro elemento del mismo nivel en un grupo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="28fd4-183">Establishes a direct connection with another peer in a peer group.</span></span>  |
| [<span data-ttu-id="28fd4-184">**PeerGroupSendData**</span><span class="sxs-lookup"><span data-stu-id="28fd4-184">**PeerGroupSendData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)                           | <span data-ttu-id="28fd4-185">Envía datos a un miembro a través de una conexión vecino o directa.</span><span class="sxs-lookup"><span data-stu-id="28fd4-185">Sends data to a member over a neighbor or direct connection.</span></span>        |



 

## <a name="group-events-infrastructure"></a><span data-ttu-id="28fd4-186">Infraestructura de eventos de grupo</span><span class="sxs-lookup"><span data-stu-id="28fd4-186">Group Events Infrastructure</span></span>



| <span data-ttu-id="28fd4-187">Función</span><span class="sxs-lookup"><span data-stu-id="28fd4-187">Function</span></span>                                                     | <span data-ttu-id="28fd4-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="28fd4-188">Description</span></span>                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28fd4-189">**PeerGroupGetEventData**</span><span class="sxs-lookup"><span data-stu-id="28fd4-189">**PeerGroupGetEventData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)       | <span data-ttu-id="28fd4-190">Permite que una aplicación recupere los datos devueltos por un evento de agrupación.</span><span class="sxs-lookup"><span data-stu-id="28fd4-190">Allows an application to retrieve the data returned by a grouping event.</span></span>                       |
| [<span data-ttu-id="28fd4-191">**PeerGroupRegisterEvent**</span><span class="sxs-lookup"><span data-stu-id="28fd4-191">**PeerGroupRegisterEvent**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)     | <span data-ttu-id="28fd4-192">Registra un elemento del mismo nivel para eventos de grupo del mismo nivel concretos.</span><span class="sxs-lookup"><span data-stu-id="28fd4-192">Registers a peer for specific peer group events.</span></span>                                               |
| [<span data-ttu-id="28fd4-193">**PeerGroupUnregisterEvent**</span><span class="sxs-lookup"><span data-stu-id="28fd4-193">**PeerGroupUnregisterEvent**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) | <span data-ttu-id="28fd4-194">Anula el registro de un elemento del mismo nivel de la notificación de eventos del mismo nivel asociados al identificador de eventos proporcionado.</span><span class="sxs-lookup"><span data-stu-id="28fd4-194">Unregisters a peer from notification of peer events associated with the supplied event handle.</span></span> |



 

## <a name="group-time-conversion-functions"></a><span data-ttu-id="28fd4-195">Funciones de conversión de tiempo de grupo</span><span class="sxs-lookup"><span data-stu-id="28fd4-195">Group Time Conversion Functions</span></span>



| <span data-ttu-id="28fd4-196">Función</span><span class="sxs-lookup"><span data-stu-id="28fd4-196">Function</span></span>                                                                     | <span data-ttu-id="28fd4-197">Descripción</span><span class="sxs-lookup"><span data-stu-id="28fd4-197">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28fd4-198">**PeerGroupPeerTimeToUniversalTime**</span><span class="sxs-lookup"><span data-stu-id="28fd4-198">**PeerGroupPeerTimeToUniversalTime**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergrouppeertimetouniversaltime) | <span data-ttu-id="28fd4-199">Convierte el valor de tiempo de referencia mantenido por el grupo del mismo nivel en un valor de hora adaptado adecuado para su presentación en un equipo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="28fd4-199">Converts the peer group-maintained reference time value to a localized time value appropriate for display on a peer computer.</span></span> |
| [<span data-ttu-id="28fd4-200">**PeerGroupUniversalTimeToPeerTime**</span><span class="sxs-lookup"><span data-stu-id="28fd4-200">**PeerGroupUniversalTimeToPeerTime**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupuniversaltimetopeertime) | <span data-ttu-id="28fd4-201">Convierte un valor de hora local del equipo del mismo nivel a un valor común de tiempo de grupo del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="28fd4-201">Converts a local time value from a peer's computer to a common peer group time value.</span></span>                                         |



 

## <a name="group-configuration-functions"></a><span data-ttu-id="28fd4-202">Funciones de configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="28fd4-202">Group Configuration Functions</span></span>



| <span data-ttu-id="28fd4-203">Función</span><span class="sxs-lookup"><span data-stu-id="28fd4-203">Function</span></span>                                               | <span data-ttu-id="28fd4-204">Descripción</span><span class="sxs-lookup"><span data-stu-id="28fd4-204">Description</span></span>                                                                                                                       |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28fd4-205">**PeerGroupExportConfig**</span><span class="sxs-lookup"><span data-stu-id="28fd4-205">**PeerGroupExportConfig**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig) | <span data-ttu-id="28fd4-206">Exporta la configuración de grupo para un elemento del mismo nivel como una cadena XML que contiene la identidad, el nombre de grupo y el GMC para la identidad.</span><span class="sxs-lookup"><span data-stu-id="28fd4-206">Exports the group configuration for a peer as an XML string that contains the identity, group name, and the GMC for the identity.</span></span> |
| [<span data-ttu-id="28fd4-207">**PeerGroupImportConfig**</span><span class="sxs-lookup"><span data-stu-id="28fd4-207">**PeerGroupImportConfig**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) | <span data-ttu-id="28fd4-208">Importa una configuración de grupo del mismo nivel para una identidad basada en la configuración específica de una cadena de configuración XML proporcionada.</span><span class="sxs-lookup"><span data-stu-id="28fd4-208">Imports a peer group configuration for an identity based on the specific settings in a supplied XML configuration string.</span></span>         |



 

 

 



