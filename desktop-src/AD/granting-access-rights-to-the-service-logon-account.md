---
title: Conceder derechos de acceso a la cuenta de inicio de sesión del servicio
description: Una consideración principal de la instalación de una instancia de servicio es asegurarse de que el servicio instalado pueda acceder a los recursos necesarios.
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- Conceder derechos de acceso a la cuenta de inicio de sesión del servicio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f4ea5b85e6158109338b881eeb3f59d74a3910
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "105656338"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a><span data-ttu-id="49b87-104">Conceder derechos de acceso a la cuenta de inicio de sesión del servicio</span><span class="sxs-lookup"><span data-stu-id="49b87-104">Granting Access Rights to the Service Logon Account</span></span>

<span data-ttu-id="49b87-105">Una consideración principal de la instalación de una instancia de servicio es asegurarse de que el servicio instalado pueda acceder a los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="49b87-105">A primary consideration of installing a service instance is to ensure that the installed service can access the necessary resources.</span></span> <span data-ttu-id="49b87-106">Para ello, establezca las ACE en los descriptores de seguridad de los objetos a los que el servicio debe tener acceso.</span><span class="sxs-lookup"><span data-stu-id="49b87-106">To do this, set ACEs in the security descriptors of objects that the service must access.</span></span> <span data-ttu-id="49b87-107">Una ACE puede conceder o denegar derechos de acceso a una entidad de seguridad especificada, como la cuenta de usuario de servicio, o la cuenta de equipo para un servicio LocalSystem, o un grupo al que pertenece la cuenta del servicio.</span><span class="sxs-lookup"><span data-stu-id="49b87-107">An ACE can grant or deny access rights to a specified security principal, such as the service user account, or the computer account for a LocalSystem service, or a group to which the service's account belongs.</span></span> <span data-ttu-id="49b87-108">Para obtener más información sobre las ACE, los descriptores de seguridad y el control de acceso, vea [controlar el acceso a objetos en Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) y [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="49b87-108">For more information about ACEs, security descriptors, and access control, see [Controlling Access to objects in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) and [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="49b87-109">Para obtener más información y un ejemplo de código que se puede usar para establecer una ACE que permita al servicio modificar su punto de conexión de servicio, consulte [habilitación de la cuenta de servicio para acceder a las propiedades de SCP](enabling-service-account-to-access-scp-properties.md).</span><span class="sxs-lookup"><span data-stu-id="49b87-109">For more information and a code example that can be used to set an ACE that enables the service to modify its service connection point, see [Enabling Service Account to Access SCP Properties](enabling-service-account-to-access-scp-properties.md).</span></span>

<span data-ttu-id="49b87-110">En algunos casos, debe agregar la cuenta de usuario de servicio como miembro de uno o varios grupos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="49b87-110">In some cases, you must add your service user account as a member of one or more security groups.</span></span> <span data-ttu-id="49b87-111">Por ejemplo, si crea un grupo de administradores para su servicio, es posible que el servicio sea miembro del grupo.</span><span class="sxs-lookup"><span data-stu-id="49b87-111">For example, if you create an administrators group for your service, you might make the service a member of the group.</span></span> <span data-ttu-id="49b87-112">Después, puede conceder derechos de acceso al grupo en lugar de concederlos explícitamente a la cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="49b87-112">You can then grant access rights to the group rather than granting them explicitly to the service account.</span></span> <span data-ttu-id="49b87-113">Para obtener más información acerca de los grupos de seguridad, consulte [Administración de grupos](managing-groups.md).</span><span class="sxs-lookup"><span data-stu-id="49b87-113">For more information about security groups, see [Managing Groups](managing-groups.md).</span></span>

 

 