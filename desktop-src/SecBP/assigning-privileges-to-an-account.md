---
description: Puede asignar privilegios a las cuentas mediante el complemento Directiva de seguridad local de Microsoft Management Console (MMC) (SECPOL. msc) o mediante una llamada a la función LsaAddAccountRights.
ms.assetid: F2DAB2E3-8B24-49A3-A2DD-E83B5181E9A2
title: Asignación de privilegios a una cuenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0865a59b8bad75e687fd12f6bfc42c2cd39f664d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668046"
---
# <a name="assigning-privileges-to-an-account"></a><span data-ttu-id="b192e-103">Asignación de privilegios a una cuenta</span><span class="sxs-lookup"><span data-stu-id="b192e-103">Assigning Privileges to an Account</span></span>

<span data-ttu-id="b192e-104">Puede asignar privilegios a las cuentas mediante el complemento Directiva de seguridad local de Microsoft Management Console (MMC) (SECPOL. msc) o mediante una llamada a la función [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) .</span><span class="sxs-lookup"><span data-stu-id="b192e-104">You can assign privileges to accounts either by using the Local Security Policy Microsoft Management Console (MMC) snap-in (Secpol.msc) or by calling the [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) function.</span></span>

<span data-ttu-id="b192e-105">La asignación de un privilegio a una cuenta no afecta a los tokens de usuario existentes.</span><span class="sxs-lookup"><span data-stu-id="b192e-105">Assigning a privilege to an account does not affect existing user tokens.</span></span> <span data-ttu-id="b192e-106">Un usuario debe cerrar sesión y volver a iniciarla para obtener un token de acceso con el privilegio recién asignado.</span><span class="sxs-lookup"><span data-stu-id="b192e-106">A user must log off and then log back on to get an access token with the newly assigned privilege.</span></span>

<span data-ttu-id="b192e-107">Para asignar privilegios mediante el complemento MMC de directiva de seguridad local, edite la lista de usuarios para cada privilegio que aparece en **configuración de seguridad/Directivas locales/asignación de derechos de usuario**.</span><span class="sxs-lookup"><span data-stu-id="b192e-107">To assign privileges by using the Local Security Policy MMC snap-in, edit the list of users for each privilege listed under **Security Settings/Local Policies/User Rights Assignment**.</span></span>

 

 
