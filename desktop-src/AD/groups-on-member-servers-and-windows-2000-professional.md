---
title: Grupos en servidores miembro y Windows 2000 Professional
description: En los servidores miembro y equipos que ejecutan Windows 2000 Professional, hay una base de datos de seguridad local.
ms.assetid: 17a651e2-3650-4e12-b17e-badd3d479515
ms.tgt_platform: multiple
keywords:
- Grupos en servidores miembro y Windows 2000 Professional AD
- grupos AD, grupos en servidores miembro y Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530da03182d05764540a85f1c2529ced5877be5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356724"
---
# <a name="groups-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="229d4-105">Grupos en servidores miembro y Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="229d4-105">Groups on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="229d4-106">En los servidores miembro y equipos que ejecutan Windows 2000 Professional, hay una base de datos de seguridad local.</span><span class="sxs-lookup"><span data-stu-id="229d4-106">On member servers and computers running on Windows 2000 Professional, there is a local security database.</span></span> <span data-ttu-id="229d4-107">Esta base de datos de seguridad local puede contener su propio usuario local y grupos locales cuyo ámbito sea solo el equipo determinado en el que se crean.</span><span class="sxs-lookup"><span data-stu-id="229d4-107">This local security database can contain its own local user and local groups whose scope is only the particular computer where they are created.</span></span> <span data-ttu-id="229d4-108">Al administrar estos tipos de usuarios y grupos en servidores miembro y equipos que ejecutan Windows NT Workstation o Windows 2000 Professional, use el proveedor de Winnt.</span><span class="sxs-lookup"><span data-stu-id="229d4-108">When managing these types of users and groups on member servers and computers running on Windows NT Workstation or Windows 2000 Professional, use the WinNT provider.</span></span>

<span data-ttu-id="229d4-109">Cuando un servidor miembro o un equipo que se ejecuta en Windows 2000 Professional o Windows 2000 Professional es miembro de un dominio de Windows 2000, los grupos o usuarios del dominio se pueden usar en la base de datos de seguridad local para conceder derechos a ese grupo en ese equipo en particular.</span><span class="sxs-lookup"><span data-stu-id="229d4-109">When a member server or a computer running on Windows 2000 Professional or Windows 2000 Professional is a member of a Windows 2000 domain, the groups or users in the domain can be used in the local security database to grant rights to that group on that particular computer.</span></span>

<span data-ttu-id="229d4-110">Al administrar grupos en un dominio de Windows 2000 mediante ADSI, use el proveedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="229d4-110">When managing groups on a Windows 2000 domain using ADSI, use the LDAP provider.</span></span> <span data-ttu-id="229d4-111">Al administrar grupos en servidores miembro y equipos que ejecutan Windows NT Workstation o Windows 2000 Professional, use el proveedor de Winnt.</span><span class="sxs-lookup"><span data-stu-id="229d4-111">When managing groups on member servers and computers running on Windows NT Workstation or Windows 2000 Professional, use the WinNT provider.</span></span>

<span data-ttu-id="229d4-112">Debe enlazar, al menos una instancia, a cada proveedor: 1) enlazar con el proveedor LDAP para recuperar el ADsPath al grupo o usuario que desea agregar a un grupo en la base de datos local y 2) enlazar con el proveedor WinNT para agregar ese usuario o grupo a un grupo local.</span><span class="sxs-lookup"><span data-stu-id="229d4-112">You must bind, at least one instance, to each provider: 1) Bind to the LDAP provider to retrieve the ADsPath to the group or user you want to add to a group in the local database and 2) Bind to the WinNT provider to add that user or group to a local group.</span></span>

 

 




