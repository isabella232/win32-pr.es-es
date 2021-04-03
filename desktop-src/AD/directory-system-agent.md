---
title: Agente de sistema de directorio
description: El agente de sistema de directorio (DSA) es una colección de servicios y procesos que se ejecutan en cada controlador de dominio y proporciona acceso al almacén de datos.
ms.assetid: a921a822-6b2e-4a84-8112-0ae516443667
ms.tgt_platform: multiple
keywords:
- Active Directory del agente de sistema de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df39d1670f6668f933c20bcd2b9a8771ce83ec56
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904505"
---
# <a name="directory-system-agent"></a><span data-ttu-id="f51ed-104">Agente de sistema de directorio</span><span class="sxs-lookup"><span data-stu-id="f51ed-104">Directory System Agent</span></span>

<span data-ttu-id="f51ed-105">El [*agente de sistema de directorio*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) es una colección de servicios y procesos que se ejecutan en cada controlador de dominio y proporciona acceso al almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="f51ed-105">The [*directory system agent*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) is a collection of services and processes that run on each domain controller and provides access to the data store.</span></span> <span data-ttu-id="f51ed-106">El almacén de datos es el almacenamiento físico de los datos de directorio ubicados en un disco duro.</span><span class="sxs-lookup"><span data-stu-id="f51ed-106">The data store is the physical store of directory data located on a hard disk.</span></span> <span data-ttu-id="f51ed-107">En Active Directory Domain Services, el DSA es parte del subsistema de la entidad de sistema local (LSA).</span><span class="sxs-lookup"><span data-stu-id="f51ed-107">In Active Directory Domain Services, the DSA is part of the local system authority (LSA) subsystem.</span></span> <span data-ttu-id="f51ed-108">Los clientes acceden al directorio mediante uno de los siguientes mecanismos admitidos por el DSA:</span><span class="sxs-lookup"><span data-stu-id="f51ed-108">Clients access the directory using one of the following mechanisms supported by the DSA:</span></span>

-   <span data-ttu-id="f51ed-109">Los clientes LDAP se conectan al DSA mediante el Protocolo ligero de acceso a directorios (LDAP).</span><span class="sxs-lookup"><span data-stu-id="f51ed-109">LDAP clients connect to the DSA using the Lightweight Directory Access Protocol (LDAP).</span></span> <span data-ttu-id="f51ed-110">Active Directory Domain Services admite LDAP 3,0, definido por RFC 3377 y LDAP 2,0, definido por RFC 1777.</span><span class="sxs-lookup"><span data-stu-id="f51ed-110">Active Directory Domain Services support LDAP 3.0, defined by RFC 3377, and LDAP 2.0, defined by RFC 1777.</span></span> <span data-ttu-id="f51ed-111">Los clientes de Windows usan LDAP 3,0 para conectarse al DSA.</span><span class="sxs-lookup"><span data-stu-id="f51ed-111">Windows clients use LDAP 3.0 to connect to the DSA.</span></span>
-   <span data-ttu-id="f51ed-112">Los clientes MAPI, como Microsoft Exchange Server, se conectan al DSA mediante la interfaz de llamada a procedimiento remoto de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f51ed-112">MAPI clients such as Microsoft Exchange Server connect to the DSA using the MAPI remote procedure call interface.</span></span>
-   <span data-ttu-id="f51ed-113">Los DSA en Active Directory Domain Services conectarse entre sí para realizar la replicación mediante una interfaz de llamada a procedimiento remoto propia.</span><span class="sxs-lookup"><span data-stu-id="f51ed-113">The DSAs in Active Directory Domain Services connect to each other to perform replication using a proprietary remote procedure call interface.</span></span>

 

 