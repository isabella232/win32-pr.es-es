---
title: Entidades de seguridad
description: En Windows 2000, una entidad de seguridad es un usuario, un grupo o un equipo \ 8212; entidad que el sistema de seguridad reconoce.
ms.assetid: 213ee563-35cd-43d2-abb2-f66652df5be1
ms.tgt_platform: multiple
keywords:
- AD de entidades de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877ed77b365fa4a61444e4936dbe859379ee397
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656215"
---
# <a name="security-principals"></a><span data-ttu-id="2981b-104">Entidades de seguridad</span><span class="sxs-lookup"><span data-stu-id="2981b-104">Security Principals</span></span>

<span data-ttu-id="2981b-105">En Windows 2000, una entidad de seguridad es un usuario, un grupo o un equipo, una entidad que el sistema de seguridad reconoce.</span><span class="sxs-lookup"><span data-stu-id="2981b-105">In Windows 2000, a security principal is a user, group, or computer — an entity that the security system recognizes.</span></span> <span data-ttu-id="2981b-106">Esto incluye a los usuarios humanos, así como a los procesos autónomos.</span><span class="sxs-lookup"><span data-stu-id="2981b-106">This includes human users as well as autonomous processes.</span></span> <span data-ttu-id="2981b-107">En realidad, el sistema de seguridad no puede indicar la diferencia entre los usuarios que han iniciado sesión y los procesos que se ejecutan en el equipo.</span><span class="sxs-lookup"><span data-stu-id="2981b-107">Strictly speaking, the security system cannot tell the difference between users who are logged in and processes running on the computer.</span></span> <span data-ttu-id="2981b-108">Ve ambos como entidades de seguridad con nombres de entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2981b-108">It sees both as security principals with security principal names.</span></span>

<span data-ttu-id="2981b-109">Los usuarios, los grupos y los equipos se crean y almacenan como objetos en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="2981b-109">Users, groups, and computers are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="2981b-110">También hay entidades de seguridad conocidas que representan identidades especiales definidas por el sistema de seguridad de Windows 2000, como todos, sistema local, propio usuario principal, usuario autenticado, propietario del creador, etc.</span><span class="sxs-lookup"><span data-stu-id="2981b-110">There are also well-known security principals that represent special identities defined by the Windows 2000 security system, such as Everyone, Local System, Principal Self, Authenticated User, Creator Owner, and so on.</span></span> <span data-ttu-id="2981b-111">Los objetos que representan las entidades de seguridad conocidas, como el inicio de sesión anónimo, se almacenan en el contenedor de entidades de seguridad WellKnown bajo el contenedor de configuración.</span><span class="sxs-lookup"><span data-stu-id="2981b-111">Objects representing the well-known security principals, such as Anonymous Logon, are stored in the WellKnown Security Principals container beneath the Configuration container.</span></span>

 

 




