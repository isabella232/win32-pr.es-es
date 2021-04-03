---
title: Directrices para seleccionar una cuenta de inicio de sesión de servicio
description: Un servicio basado en Win32 puede ejecutarse en el contexto de seguridad de una cuenta de usuario local, una cuenta de usuario de dominio o la cuenta LocalSystem.
ms.assetid: aa2b93c7-335f-4e03-9198-fe2b396e296e
ms.tgt_platform: multiple
keywords:
- Directrices para seleccionar una cuenta de inicio de sesión de servicio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bb8f5b4fe6a57863c09c9563454fc3ec09e75c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075118"
---
# <a name="guidelines-for-selecting-a-service-logon-account"></a><span data-ttu-id="97a23-104">Directrices para seleccionar una cuenta de inicio de sesión de servicio</span><span class="sxs-lookup"><span data-stu-id="97a23-104">Guidelines for Selecting a Service Logon Account</span></span>

<span data-ttu-id="97a23-105">Un servicio basado en Win32 puede ejecutarse en el contexto de seguridad de una cuenta de usuario local, una cuenta de usuario de dominio o la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="97a23-105">A Win32-based service can run in the security context of a local user account, a domain user account, or the LocalSystem account.</span></span> <span data-ttu-id="97a23-106">Para decidir qué cuenta usar, un administrador debe instalar el servicio con el conjunto mínimo de permisos necesario para realizar las operaciones de servicio.</span><span class="sxs-lookup"><span data-stu-id="97a23-106">To decide which account to use, an administrator should install the service with the minimum set of permissions required to perform the service operations.</span></span> <span data-ttu-id="97a23-107">En un servicio típico habilitado para directorios, esto significa que el instalador del servicio debe crear una cuenta de usuario de dominio para el servicio y conceder a esa cuenta los derechos de acceso y privilegios específicos que requiere el servicio en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="97a23-107">In a typical directory-enabled service, this means the service installer should create a domain user account for the service and grant that account the specific access rights and privileges required by the service at run time.</span></span> <span data-ttu-id="97a23-108">Un servicio solo debe ejecutarse con la cuenta LocalSystem si el servicio requiere privilegios administrativos o debe actuar como parte del sistema operativo en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="97a23-108">A service should only run under the LocalSystem account if the service requires administrative privileges or must act as part of the operating system on the local computer.</span></span>

<span data-ttu-id="97a23-109">Tenga en cuenta que, de forma predeterminada, el instalador del servicio debe configurar el servicio para que se ejecute en una cuenta de usuario de dominio.</span><span class="sxs-lookup"><span data-stu-id="97a23-109">Be aware that the service installer should, by default, set up the service to run under a domain user account.</span></span> <span data-ttu-id="97a23-110">Para ejecutar el servicio con la cuenta LocalSystem, el instalador del servicio debe consultar al administrador para obtener permiso para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="97a23-110">To run the service under the LocalSystem account, the service installer should query the administrator for permission to do so.</span></span>

<span data-ttu-id="97a23-111">Para obtener más información acerca de las descripciones, las ventajas y las desventajas de cada tipo de cuenta, consulte:</span><span class="sxs-lookup"><span data-stu-id="97a23-111">For more information about descriptions, advantages, and disadvantages of each account type, see:</span></span>

-   <span data-ttu-id="97a23-112">[Cuentas de usuario locales](local-user-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="97a23-112">[Local User Accounts](local-user-accounts.md).</span></span>
-   <span data-ttu-id="97a23-113">[Cuentas de usuario de dominio](domain-user-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="97a23-113">[Domain User Accounts](domain-user-accounts.md).</span></span>
-   <span data-ttu-id="97a23-114">[La cuenta LocalSystem](the-localsystem-account.md).</span><span class="sxs-lookup"><span data-stu-id="97a23-114">[The LocalSystem Account](the-localsystem-account.md).</span></span>

 

 




