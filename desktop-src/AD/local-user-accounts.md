---
title: Uso de una cuenta de usuario local como cuenta de inicio de sesión de servicio
description: Una cuenta de usuario local (formato de nombre \ 0034;. \\ Nombre de usuario \ 0034;) solo existe en la base de datos SAM del equipo host; no tiene un objeto de usuario en Active Directory Domain Services.
ms.assetid: a36d4d1c-3cfc-4ae1-8f1d-3f2e766f0c4b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84da502e99d2e5cd74e98e9f792e06f74f4852e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148749"
---
# <a name="using-a-local-user-account-as-a-service-logon-account"></a><span data-ttu-id="e7edb-103">Uso de una cuenta de usuario local como cuenta de inicio de sesión de servicio</span><span class="sxs-lookup"><span data-stu-id="e7edb-103">Using a Local User Account as a Service Logon Account</span></span>

<span data-ttu-id="e7edb-104">Una cuenta de usuario local (formato de nombre: ". \\ *Username*") solo existe en la base de datos SAM del equipo host; no tiene un objeto de usuario en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="e7edb-104">A local user account (name format: ".\\*UserName*") exists only in the SAM database of the host computer; it does not have a user object in Active Directory Domain Services.</span></span> <span data-ttu-id="e7edb-105">Esto significa que el dominio no puede autenticar una cuenta local.</span><span class="sxs-lookup"><span data-stu-id="e7edb-105">This means that a local account cannot be authenticated by the domain.</span></span> <span data-ttu-id="e7edb-106">Por consiguiente, un servicio que se ejecuta en el contexto de seguridad de una cuenta de usuario local no tiene acceso a los recursos de red (excepto como un usuario anónimo) y no admite la autenticación mutua de Kerberos en la que los clientes autentican el servicio.</span><span class="sxs-lookup"><span data-stu-id="e7edb-106">Consequently, a service that runs in the security context of a local user account does not have access to network resources (except as an anonymous user), and it cannot support Kerberos mutual authentication in which the service is authenticated by its clients.</span></span> <span data-ttu-id="e7edb-107">Por estos motivos, las cuentas de usuario locales no suelen ser adecuadas para los servicios habilitados para el uso de directorios.</span><span class="sxs-lookup"><span data-stu-id="e7edb-107">For these reasons, local user accounts are typically inappropriate for directory-enabled services.</span></span> <span data-ttu-id="e7edb-108">En el lado más, los errores del servicio no pueden dañar el sistema.</span><span class="sxs-lookup"><span data-stu-id="e7edb-108">On the plus side, bugs in the service cannot damage the system.</span></span> <span data-ttu-id="e7edb-109">Si el servicio se puede ejecutar bajo esas limitaciones, debería hacerlo.</span><span class="sxs-lookup"><span data-stu-id="e7edb-109">If your service can run under those limitations, it should.</span></span>

 

 




