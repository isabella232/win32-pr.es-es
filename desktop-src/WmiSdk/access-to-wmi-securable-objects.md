---
description: WMI se basa en los descriptores de seguridad de Windows estándar para controlar y proteger el acceso a objetos protegibles como espacios de nombres WMI, impresoras, servicios y aplicaciones DCOM.
ms.assetid: 5893457d-3fc2-4d64-a6c2-0f410052ce52
ms.tgt_platform: multiple
title: Acceso a objetos protegibles de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad4ea78cd45d57856b0909283e7c2624fb26bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278778"
---
# <a name="access-to-wmi-securable-objects"></a><span data-ttu-id="2b3ae-103">Acceso a objetos protegibles de WMI</span><span class="sxs-lookup"><span data-stu-id="2b3ae-103">Access to WMI Securable Objects</span></span>

<span data-ttu-id="2b3ae-104">WMI se basa en los [*descriptores de seguridad*](/windows/desktop/SecGloss/s-gly) de Windows estándar para controlar y proteger el acceso a objetos protegibles como espacios de nombres WMI, impresoras, servicios y aplicaciones DCOM.</span><span class="sxs-lookup"><span data-stu-id="2b3ae-104">WMI relies on standard Windows [*security descriptors*](/windows/desktop/SecGloss/s-gly) to control and protect access to securable objects like WMI namespaces, printers, services, and DCOM applications.</span></span> <span data-ttu-id="2b3ae-105">Para obtener más información, vea [acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="2b3ae-105">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="2b3ae-106">En esta sección se explican los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="2b3ae-106">The following topics are discussed in this section:</span></span>

-   [<span data-ttu-id="2b3ae-107">Descriptores de seguridad y SID</span><span class="sxs-lookup"><span data-stu-id="2b3ae-107">Security Descriptors and SIDs</span></span>](#security-descriptors-and-sids)
-   [<span data-ttu-id="2b3ae-108">Control de acceso</span><span class="sxs-lookup"><span data-stu-id="2b3ae-108">Access Control</span></span>](#access-control)
-   [<span data-ttu-id="2b3ae-109">Cambiar la seguridad de acceso</span><span class="sxs-lookup"><span data-stu-id="2b3ae-109">Changing Access Security</span></span>](#changing-access-security)
-   [<span data-ttu-id="2b3ae-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2b3ae-110">Related topics</span></span>](#related-topics)

## <a name="security-descriptors-and-sids"></a><span data-ttu-id="2b3ae-111">Descriptores de seguridad y SID</span><span class="sxs-lookup"><span data-stu-id="2b3ae-111">Security Descriptors and SIDs</span></span>

<span data-ttu-id="2b3ae-112">WMI mantiene la seguridad de acceso al comparar el [*token de acceso*](/windows/desktop/SecGloss/a-gly) del usuario que intenta tener acceso a un objeto protegible con el descriptor de seguridad del objeto.</span><span class="sxs-lookup"><span data-stu-id="2b3ae-112">WMI maintains access security by comparing the [*access token*](/windows/desktop/SecGloss/a-gly) of the user that attempts to access a securable object with the security descriptor of the object.</span></span>

<span data-ttu-id="2b3ae-113">Cuando se crea un usuario o grupo en un sistema, a la cuenta se le asigna un [*identificador de seguridad (SID)*](/windows/desktop/SecGloss/s-gly) . el SID garantiza que una cuenta creada con el mismo nombre que una cuenta previamente eliminada no hereda la configuración de seguridad anterior.</span><span class="sxs-lookup"><span data-stu-id="2b3ae-113">When a user or group is created on a system, the account is given a [*security identifier (SID)*](/windows/desktop/SecGloss/s-gly) The SID ensures that an account created with the same name as a previously deleted account does not inherit the previous security settings.</span></span> <span data-ttu-id="2b3ae-114">Un token de acceso se crea mediante la combinación del SID, la lista de grupos a los que pertenece el usuario y la lista de privilegios habilitados o deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="2b3ae-114">An access token is created by combining the SID, the list of groups of which the user is a member, and the list of enabled or disabled privileges.</span></span> <span data-ttu-id="2b3ae-115">Estos tokens se asignan a todos los procesos y subprocesos que pertenecen al usuario.</span><span class="sxs-lookup"><span data-stu-id="2b3ae-115">These tokens are assigned to all processes and threads owned by the user.</span></span>

## <a name="access-control"></a><span data-ttu-id="2b3ae-116">Control de acceso</span><span class="sxs-lookup"><span data-stu-id="2b3ae-116">Access Control</span></span>

<span data-ttu-id="2b3ae-117">Cuando el usuario desea usar un objeto protegido, el token de acceso se compara con la [*lista de control de acceso discrecional (DACL)*](/windows/desktop/SecGloss/d-gly) del descriptor de seguridad del objeto.</span><span class="sxs-lookup"><span data-stu-id="2b3ae-117">When the user wants to use a secured object, the access token is compared with the [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) in the security descriptor on the object.</span></span> <span data-ttu-id="2b3ae-118">DACL contiene permisos denominados [*entradas de control de acceso (ACE)*](/windows/desktop/SecGloss/a-gly).</span><span class="sxs-lookup"><span data-stu-id="2b3ae-118">The DACL contains permissions called [*access control entries (ACE)*](/windows/desktop/SecGloss/a-gly).</span></span> <span data-ttu-id="2b3ae-119">Las [*listas de control de acceso del sistema (SACL)*](/windows/desktop/SecGloss/s-gly) hacen lo mismo que las DACL, pero pueden generar eventos de auditoría de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2b3ae-119">[*System access control lists (SACL)*](/windows/desktop/SecGloss/s-gly) do the same thing as DACLs, but can generate security audit events.</span></span> <span data-ttu-id="2b3ae-120">A partir de Windows Vista, WMI puede realizar entradas de auditoría en el registro de seguridad de Windows.</span><span class="sxs-lookup"><span data-stu-id="2b3ae-120">Starting with Windows Vista, WMI can make auditing entries in the Windows Security Log.</span></span> <span data-ttu-id="2b3ae-121">Para obtener más información acerca de la auditoría en WMI, consulte [acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="2b3ae-121">For more information about auditing in WMI, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="2b3ae-122">La DACL y la SACL constan de una lista de ACE que describen qué usuarios tienen derechos de acceso específicos, incluida la escritura en el repositorio WMI, el acceso remoto y la ejecución, y los permisos de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="2b3ae-122">Both the DACL and the SACL consist of a list of ACEs that describe which users have specific access rights, including writing to the WMI repository, remote access and execution, and logon permissions.</span></span> <span data-ttu-id="2b3ae-123">WMI almacena estas ACL en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="2b3ae-123">WMI stores these ACLs in the WMI repository.</span></span>

<span data-ttu-id="2b3ae-124">Las ACE contienen tres tipos de niveles de acceso o derechos de concesión o denegación: permitir, denegar para DACL y auditoría del sistema (para SACL).</span><span class="sxs-lookup"><span data-stu-id="2b3ae-124">ACEs hold three types of access levels or grant/deny rights: allow, deny for DACL, and system audit (for SACLs).</span></span> <span data-ttu-id="2b3ae-125">Las ACE de denegación preceden a las ACE de permiso en la DACL o SACL.</span><span class="sxs-lookup"><span data-stu-id="2b3ae-125">Deny ACEs precede allow ACEs in the DACL or SACL.</span></span> <span data-ttu-id="2b3ae-126">Al comprobar los derechos de acceso de usuario, WMI se ejecuta consecutivamente a través de la lista de control de acceso hasta que encuentra una ACE de permiso que se aplica al token de acceso que realiza la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2b3ae-126">When checking the user access rights, WMI runs consecutively through the access control list until it finds an allow ACE that applies to the requesting access token.</span></span> <span data-ttu-id="2b3ae-127">Las ACE restantes no se comprueban después de este punto.</span><span class="sxs-lookup"><span data-stu-id="2b3ae-127">The remaining ACEs are not checked after this point.</span></span> <span data-ttu-id="2b3ae-128">Si no se encuentra ningún ACE de permiso adecuado, se denegará el acceso.</span><span class="sxs-lookup"><span data-stu-id="2b3ae-128">If no appropriate allow ACE is found, then access is denied.</span></span> <span data-ttu-id="2b3ae-129">Para obtener más información, vea [orden de las ACE en una DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) y [crear una DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="2b3ae-129">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl) and [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

## <a name="changing-access-security"></a><span data-ttu-id="2b3ae-130">Cambiar la seguridad de acceso</span><span class="sxs-lookup"><span data-stu-id="2b3ae-130">Changing Access Security</span></span>

<span data-ttu-id="2b3ae-131">Con los permisos adecuados, puede cambiar la seguridad de un objeto protegible con un script o una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2b3ae-131">With appropriate permissions, you can change the security on a securable object with a script or application.</span></span> <span data-ttu-id="2b3ae-132">También puede cambiar la configuración de seguridad en los espacios de nombres WMI mediante el [*control WMI*](gloss-w.md) o agregando una cadena de [lenguaje de definición de descriptores de seguridad (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) en el archivo [*Managed Object Format (MOF)*](gloss-m.md) que define las clases para el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="2b3ae-132">You can also change the security settings on WMI namespaces using the [*WMI Control*](gloss-w.md) or by adding a [Security Descriptor Definition Language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) string in the [*Managed Object Format (MOF)*](gloss-m.md) file that defines classes for the namespace.</span></span> <span data-ttu-id="2b3ae-133">Para obtener más información, vea [acceso a espacios de nombres WMI](access-to-wmi-namespaces.md), [protección de espacios de nombres WMI](securing-wmi-namespaces.md)y [cambio de la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2b3ae-133">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md), [Securing WMI Namespaces](securing-wmi-namespaces.md), and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b3ae-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2b3ae-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b3ae-135">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="2b3ae-135">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="2b3ae-136">Constantes de seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="2b3ae-136">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="2b3ae-137">Control de cuentas de usuario y WMI</span><span class="sxs-lookup"><span data-stu-id="2b3ae-137">User Account Control and WMI</span></span>](user-account-control-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="2b3ae-138">Objetos de descriptor de seguridad WMI</span><span class="sxs-lookup"><span data-stu-id="2b3ae-138">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="2b3ae-139">Acceso a los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="2b3ae-139">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
