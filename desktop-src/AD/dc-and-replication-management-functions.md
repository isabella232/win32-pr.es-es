---
title: Funciones de administración de replicación y controlador de dominio
description: Este tema contiene una lista de funciones que se usan para la administración de la replicación y el controlador de dominio.
ms.assetid: a92783c2-ffb8-473e-8484-1c05ca5453ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00660658874bad4e34a8f6917e08289007cec4d7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077539"
---
# <a name="domain-controller-and-replication-management-functions"></a>Funciones de administración de replicación y controlador de dominio

Las funciones del controlador de dominio (DC) y de administración de replicación proporcionan herramientas para buscar datos acerca de un controlador de dominio, convertir los nombres de los objetos de red entre diferentes formatos, manipular nombres principales de servicio (SPN) y agentes de servicios de directorio (DSA), y administrar la replicación de servidores. Las funciones siguientes permiten a los desarrolladores trabajar con controladores de dominio, replicación y el servicio de directorio:

-   [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)
-   [**DsBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbinda)
-   [**DsBindingSetTimeout**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindingsettimeout)
-   [**DsBindToISTG**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindtoistga)
-   [**DsBindWithCred**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithcreda)
-   [**DsBindWithSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithspna)
-   [**DsBindWithSpnEx**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithspnexa)
-   [**DsClientMakeSpnForTargetServer**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsclientmakespnfortargetservera)
-   [**DsCrackNames**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dscracknamesa)
-   [**DsCrackSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dscrackspna)
-   [**DsCrackUnquotedMangledRdn**](/windows/desktop/api/Dsparse/nf-dsparse-dscrackunquotedmangledrdna)
-   [**DsFreeDomainControllerInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreedomaincontrollerinfoa)
-   [**DsFreeNameResult**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreenameresulta)
-   [**DsFreePasswordCredentials**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreepasswordcredentials)
-   [**DsFreeSchemaGuidMap**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreeschemaguidmapa)
-   [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya)
-   [**DsGetDomainControllerInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetdomaincontrollerinfoa)
-   [**DsGetRdnW**](/windows/desktop/api/Dsparse/nf-dsparse-dsgetrdnw)
-   [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna)
-   [**DsInheritSecurityIdentity**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsinheritsecurityidentitya)
-   [**DsIsMangledDn**](/windows/desktop/api/Dsparse/nf-dsparse-dsismangleddna)
-   [**DsIsMangledRdnValue**](/windows/desktop/api/Dsparse/nf-dsparse-dsismangledrdnvaluea)
-   [**DsListDomainsInSite**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistdomainsinsitea)
-   [**DsListInfoForServer**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistinfoforservera)
-   [**DsListRoles**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistrolesa)
-   [**DsListServersForDomainInSite**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistserversfordomaininsitea)
-   [**DsListServersInSite**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistserversinsitea)
-   [**DsListSites**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistsitesa)
-   [**DsMakePasswordCredentials**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa)
-   [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna)
-   [**DsMapSchemaGuids**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsmapschemaguidsa)
-   [**DsQuerySitesByCost**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsquerysitesbycosta)
-   [**DsQuerySitesFree**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsquerysitesfree)
-   [**DsQuoteRdnValue**](/windows/desktop/api/Dsparse/nf-dsparse-dsquoterdnvaluea)
-   [**DsRemoveDsDomain**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsremovedsdomaina)
-   [**DsRemoveDsServer**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsremovedsservera)
-   [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda)
-   [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck)
-   [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela)
-   [**DsReplicaFreeInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicafreeinfo)
-   [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow)
-   [**DsReplicaGetInfo2**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfo2w)
-   [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya)
-   [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca)
-   [**DsReplicaSyncAll**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasyncalla)
-   [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa)
-   [**DsReplicaVerifyObjects**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaverifyobjectsa)
-   [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna)
-   [**DsUnBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsunbinda)
-   [**DsUnquoteRdnValue**](/windows/desktop/api/Dsparse/nf-dsparse-dsunquoterdnvaluea)
-   [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)
-   [**SyncUpdateProc**](/previous-versions/windows/desktop/legacy/ms677968(v=vs.85))

La mayoría de estas funciones requieren un identificador enlazado al servicio de directorio. Las funciones [**DsBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbinda) y [**DsBindWithCred**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithcreda) inician una sesión RPC con un controlador de dominio determinado y, a continuación, enlazan un identificador al servicio de directorio y devuelven el identificador. Cuando ya no se necesite el identificador, utilice la función [**DsUnBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsunbinda) para finalizar la sesión RPC y desenlazar el controlador.

La replicación se produce entre un servidor de origen y un servidor de destino. Un servidor de origen mantiene una lista de los servidores de destino en los que se debe replicar y un servidor de destino mantiene una lista de los servidores de origen desde los que recibe la replicación. Use la función [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda) para agregar a la lista de servidores de origen en un servidor de destino y use la función [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela) para quitar las referencias de la lista de servidores de origen en un servidor de destino. La función [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya) se puede usar para cambiar una referencia de servidor de origen existente en un servidor de destino. Para cambiar la lista de servidores de destino en un servidor de origen, use la función [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa) .

La replicación real se realiza mediante las funciones [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) y [**DsReplicaSyncAll**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasyncalla) . La función **DsReplicaSync** sincroniza un servidor de destino específico con un solo servidor de origen. Utilice la función **DsReplicaSyncAll** para sincronizar un servidor de destino con todos los demás servidores del sitio.

 

 