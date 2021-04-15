---
description: El modelo de seguridad de Windows permite controlar el acceso al administrador de control de servicios (SCM) y a los objetos de servicio.
ms.assetid: 23d1c382-6ba4-49e2-8039-c2a91471076c
title: Derechos de acceso y seguridad del servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7677b8a9f7a5e1fadf8231999d266a9474fb731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668466"
---
# <a name="service-security-and-access-rights"></a><span data-ttu-id="c4ef3-103">Derechos de acceso y seguridad del servicio</span><span class="sxs-lookup"><span data-stu-id="c4ef3-103">Service Security and Access Rights</span></span>

<span data-ttu-id="c4ef3-104">El modelo de seguridad de Windows permite controlar el acceso al administrador de control de servicios (SCM) y a los objetos de servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-104">The Windows security model enables you to control access to the service control manager (SCM) and service objects.</span></span> <span data-ttu-id="c4ef3-105">En las secciones siguientes se proporciona información detallada:</span><span class="sxs-lookup"><span data-stu-id="c4ef3-105">The following sections provide detailed information:</span></span>

-   [<span data-ttu-id="c4ef3-106">Derechos de acceso para el administrador de control de servicios</span><span class="sxs-lookup"><span data-stu-id="c4ef3-106">Access Rights for the Service Control Manager</span></span>](#access-rights-for-the-service-control-manager)
-   [<span data-ttu-id="c4ef3-107">Derechos de acceso para un servicio</span><span class="sxs-lookup"><span data-stu-id="c4ef3-107">Access Rights for a Service</span></span>](#access-rights-for-a-service)

## <a name="access-rights-for-the-service-control-manager"></a><span data-ttu-id="c4ef3-108">Derechos de acceso para el administrador de control de servicios</span><span class="sxs-lookup"><span data-stu-id="c4ef3-108">Access Rights for the Service Control Manager</span></span>

<span data-ttu-id="c4ef3-109">A continuación se muestran los derechos de acceso específicos para el SCM.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-109">The following are the specific access rights for the SCM.</span></span>



| <span data-ttu-id="c4ef3-110">Derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="c4ef3-110">Access right</span></span>                                   | <span data-ttu-id="c4ef3-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4ef3-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ef3-112">**SC \_ ADMINISTRADOR \_ todo \_ acceso** (0xF003F)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-112">**SC\_MANAGER\_ALL\_ACCESS** (0xF003F)</span></span>         | <span data-ttu-id="c4ef3-113">Incluye **los \_ derechos estándar \_ necesarios**, además de todos los derechos de acceso de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-113">Includes **STANDARD\_RIGHTS\_REQUIRED**, in addition to all access rights in this table.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c4ef3-114">**SC \_ \_Crear \_ servicio de administración** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-114">**SC\_MANAGER\_CREATE\_SERVICE** (0x0002)</span></span>      | <span data-ttu-id="c4ef3-115">Necesario para llamar a la función [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para crear un objeto de servicio y agregarlo a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-115">Required to call the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to create a service object and add it to the database.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="c4ef3-116">**SC \_ \_Conexión de administrador** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-116">**SC\_MANAGER\_CONNECT** (0x0001)</span></span>              | <span data-ttu-id="c4ef3-117">Necesario para conectarse al administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-117">Required to connect to the service control manager.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="c4ef3-118">**SC \_ \_Enumerar \_ servicio** (0x0004)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-118">**SC\_MANAGER\_ENUMERATE\_SERVICE** (0x0004)</span></span>   | <span data-ttu-id="c4ef3-119">Necesario para llamar a la función [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) o [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) para enumerar los servicios que están en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-119">Required to call the [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) or [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) function to list the services that are in the database.</span></span><br/> <span data-ttu-id="c4ef3-120">Necesario para llamar a la función [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) para recibir una notificación cuando se crea o se elimina un servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-120">Required to call the [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) function to receive notification when any service is created or deleted.</span></span><br/> |
| <span data-ttu-id="c4ef3-121">**SC \_ \_Bloqueo de administrador** (0x0008)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-121">**SC\_MANAGER\_LOCK** (0x0008)</span></span>                 | <span data-ttu-id="c4ef3-122">Necesario para llamar a la función [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) para adquirir un bloqueo en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-122">Required to call the [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) function to acquire a lock on the database.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="c4ef3-123">**SC \_ ADMINISTRADOR \_ modificar \_ \_ configuración de arranque** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-123">**SC\_MANAGER\_MODIFY\_BOOT\_CONFIG** (0x0020)</span></span> | <span data-ttu-id="c4ef3-124">Necesario para llamar a la función [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .</span><span class="sxs-lookup"><span data-stu-id="c4ef3-124">Required to call the [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) function.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c4ef3-125">**SC \_ \_Estado de \_ bloqueo \_ de consulta de administrador** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-125">**SC\_MANAGER\_QUERY\_LOCK\_STATUS** (0x0010)</span></span>  | <span data-ttu-id="c4ef3-126">Necesario para llamar a la función [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) para recuperar la información de estado de bloqueo de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-126">Required to call the [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) function to retrieve the lock status information for the database.</span></span>                                                                                                                                                                                                                         |



 

<span data-ttu-id="c4ef3-127">A continuación se muestran los [derechos de acceso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para el SCM.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-127">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for the SCM.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c4ef3-128">Derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="c4ef3-128">Access right</span></span></th>
<th><span data-ttu-id="c4ef3-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4ef3-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4ef3-130"><strong>GENERIC_READ</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-130"><strong>GENERIC_READ</strong></span></span></td>
<td><dl> <span data-ttu-id="c4ef3-131"><strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-131"><strong>STANDARD_RIGHTS_READ</strong></span></span><br /><span data-ttu-id="c4ef3-132">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-132">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="c4ef3-133">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-133">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4ef3-134"><strong>GENERIC_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-134"><strong>GENERIC_WRITE</strong></span></span></td>
<td><dl> <span data-ttu-id="c4ef3-135"><strong>STANDARD_RIGHTS_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-135"><strong>STANDARD_RIGHTS_WRITE</strong></span></span><br /><span data-ttu-id="c4ef3-136">
<strong>SC_MANAGER_CREATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-136">
<strong>SC_MANAGER_CREATE_SERVICE</strong></span></span><br /><span data-ttu-id="c4ef3-137">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-137">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4ef3-138"><strong>GENERIC_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-138"><strong>GENERIC_EXECUTE</strong></span></span></td>
<td><dl> <span data-ttu-id="c4ef3-139"><strong>STANDARD_RIGHTS_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-139"><strong>STANDARD_RIGHTS_EXECUTE</strong></span></span><br /><span data-ttu-id="c4ef3-140">
<strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-140">
<strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="c4ef3-141">
<strong>SC_MANAGER_LOCK</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-141">
<strong>SC_MANAGER_LOCK</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4ef3-142"><strong>GENERIC_ALL</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-142"><strong>GENERIC_ALL</strong></span></span></td>
<td><dl> <span data-ttu-id="c4ef3-143"><strong>SC_MANAGER_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-143"><strong>SC_MANAGER_ALL_ACCESS</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c4ef3-144">Un proceso con los derechos de acceso correctos puede abrir un identificador del SCM que se puede usar en las funciones [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)y [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) .</span><span class="sxs-lookup"><span data-stu-id="c4ef3-144">A process with the correct access rights can open a handle to the SCM that can be used in the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa), and [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) functions.</span></span> <span data-ttu-id="c4ef3-145">Solo los procesos con privilegios de administrador pueden abrir identificadores en el SCM que las funciones [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) y [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) pueden usar.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-145">Only processes with Administrator privileges are able to open handles to the SCM that can be used by the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) functions.</span></span>

<span data-ttu-id="c4ef3-146">El sistema crea el descriptor de seguridad para el SCM.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-146">The system creates the security descriptor for the SCM.</span></span> <span data-ttu-id="c4ef3-147">Para obtener o establecer el descriptor de seguridad para el SCM, utilice las funciones [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) y [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) con un identificador para el objeto SCManager.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-147">To get or set the security descriptor for the SCM, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) and [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) functions with a handle to the SCManager object.</span></span>

<span data-ttu-id="c4ef3-148">**Windows Server 2003 y Windows XP:** A diferencia de la mayoría de los demás objetos protegibles, no se puede modificar el descriptor de seguridad para el SCM.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-148">**Windows Server 2003 and Windows XP:** Unlike most other securable objects, the security descriptor for the SCM cannot be modified.</span></span> <span data-ttu-id="c4ef3-149">Este comportamiento ha cambiado a partir de Windows Server 2003 con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c4ef3-149">This behavior has changed as of Windows Server 2003 with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="c4ef3-150">Se conceden los siguientes derechos de acceso.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-150">The following access rights are granted.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c4ef3-151">Cuenta</span><span class="sxs-lookup"><span data-stu-id="c4ef3-151">Account</span></span></th>
<th><span data-ttu-id="c4ef3-152">Derechos de acceso</span><span class="sxs-lookup"><span data-stu-id="c4ef3-152">Access rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4ef3-153">Usuarios autenticados remotos</span><span class="sxs-lookup"><span data-stu-id="c4ef3-153">Remote authenticated users</span></span></td>
<td><dl> <span data-ttu-id="c4ef3-154"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-154"><strong>SC_MANAGER_CONNECT</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4ef3-155">Usuarios autenticados localmente (incluido LocalService y NetworkService)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-155">Local authenticated users (including LocalService and NetworkService)</span></span></td>
<td><dl> <span data-ttu-id="c4ef3-156"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-156"><strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="c4ef3-157">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-157">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="c4ef3-158">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-158">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br /><span data-ttu-id="c4ef3-159">
<strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-159">
<strong>STANDARD_RIGHTS_READ</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4ef3-160">LocalSystem (Sistema local)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-160">LocalSystem</span></span></td>
<td><dl> <span data-ttu-id="c4ef3-161"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-161"><strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="c4ef3-162">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-162">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="c4ef3-163">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-163">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span></span><br /><span data-ttu-id="c4ef3-164">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-164">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br /><span data-ttu-id="c4ef3-165">
<strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-165">
<strong>STANDARD_RIGHTS_READ</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4ef3-166">Administradores</span><span class="sxs-lookup"><span data-stu-id="c4ef3-166">Administrators</span></span></td>
<td><dl> <span data-ttu-id="c4ef3-167"><strong>SC_MANAGER_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-167"><strong>SC_MANAGER_ALL_ACCESS</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c4ef3-168">Tenga en cuenta que los usuarios remotos autenticados a través de la red, pero que no han iniciado sesión de forma interactiva, pueden conectarse al SCM pero no realizar operaciones que requieran otros derechos de acceso.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-168">Notice that remote users authenticated over the network but not interactively logged on can connect to the SCM but not perform operations that require other access rights.</span></span> <span data-ttu-id="c4ef3-169">Para realizar estas operaciones, el usuario debe haber iniciado sesión de forma interactiva o el servicio debe usar una de las cuentas de servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-169">To perform these operations, the user must be logged on interactively or the service must use one of the service accounts.</span></span>

<span data-ttu-id="c4ef3-170">**Windows Server 2003 y Windows XP:** A los usuarios autenticados remotos se les conceden los derechos de acceso de **\_ \_ lectura** de **SC \_ Manager \_**, SC Manager y el **\_ \_ \_ servicio de enumeración** de SC Manager. **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c4ef3-170">**Windows Server 2003 and Windows XP:** Remote authenticated users are granted the **SC\_MANAGER\_CONNECT**, **SC\_MANAGER\_ENUMERATE\_SERVICE**, **SC\_MANAGER\_QUERY\_LOCK\_STATUS**, and **STANDARD\_RIGHTS\_READ** access rights.</span></span> <span data-ttu-id="c4ef3-171">Estos derechos de acceso están restringidos como se describe en la tabla anterior a partir de Windows Server 2003 con SP1.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-171">These access rights are restricted as described in the previous table as of Windows Server 2003 with SP1</span></span>

<span data-ttu-id="c4ef3-172">Cuando un proceso utiliza la función [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) para abrir un identificador de una base de datos de servicios instalados, puede solicitar derechos de acceso.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-172">When a process uses the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to open a handle to a database of installed services, it can request access rights.</span></span> <span data-ttu-id="c4ef3-173">El sistema realiza una comprobación de seguridad en el descriptor de seguridad del SCM antes de conceder los derechos de acceso solicitados.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-173">The system performs a security check against the security descriptor for the SCM before granting the requested access rights.</span></span>

## <a name="access-rights-for-a-service"></a><span data-ttu-id="c4ef3-174">Derechos de acceso para un servicio</span><span class="sxs-lookup"><span data-stu-id="c4ef3-174">Access Rights for a Service</span></span>

<span data-ttu-id="c4ef3-175">A continuación se muestran los derechos de acceso específicos para un servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-175">The following are the specific access rights for a service.</span></span>



| <span data-ttu-id="c4ef3-176">Derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="c4ef3-176">Access right</span></span>                                | <span data-ttu-id="c4ef3-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4ef3-177">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ef3-178">**Servicio \_ de TODO el \_ acceso** (0xF01FF)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-178">**SERVICE\_ALL\_ACCESS** (0xF01FF)</span></span>          | <span data-ttu-id="c4ef3-179">Incluye **los \_ derechos estándar \_ necesarios** además de todos los derechos de acceso de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-179">Includes **STANDARD\_RIGHTS\_REQUIRED** in addition to all access rights in this table.</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="c4ef3-180">**Servicio \_ de CAMBIAR \_ configuración** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-180">**SERVICE\_CHANGE\_CONFIG** (0x0002)</span></span>        | <span data-ttu-id="c4ef3-181">Necesario para llamar a la función [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) o [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) para cambiar la configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-181">Required to call the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) or [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function to change the service configuration.</span></span> <span data-ttu-id="c4ef3-182">Dado que esto concede al llamador el derecho de cambiar el archivo ejecutable que ejecuta el sistema, solo se debe conceder a los administradores.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-182">Because this grants the caller the right to change the executable file that the system runs, it should be granted only to administrators.</span></span>                                                              |
| <span data-ttu-id="c4ef3-183">**Servicio \_ de ENUMERAr \_ dependientes** (0x0008)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-183">**SERVICE\_ENUMERATE\_DEPENDENTS** (0x0008)</span></span> | <span data-ttu-id="c4ef3-184">Necesario para llamar a la función [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) para enumerar todos los servicios que dependen del servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-184">Required to call the [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) function to enumerate all the services dependent on the service.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="c4ef3-185">**Servicio \_ de INTERROGAte** (0x0080)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-185">**SERVICE\_INTERROGATE** (0x0080)</span></span>           | <span data-ttu-id="c4ef3-186">Necesario para llamar a la función [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para pedir al servicio que informe de su estado inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-186">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to ask the service to report its status immediately.</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c4ef3-187">**Servicio \_ de Pausar \_ continuar** (0x0040)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-187">**SERVICE\_PAUSE\_CONTINUE** (0x0040)</span></span>       | <span data-ttu-id="c4ef3-188">Necesario para llamar a la función [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para pausar o continuar el servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-188">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to pause or continue the service.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="c4ef3-189">**Servicio \_ de \_Configuración de consulta** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-189">**SERVICE\_QUERY\_CONFIG** (0x0001)</span></span>         | <span data-ttu-id="c4ef3-190">Necesario para llamar a las funciones [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) y [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) para consultar la configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-190">Required to call the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) functions to query the service configuration.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="c4ef3-191">**Servicio \_ de \_Estado** de la consulta (0x0004)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-191">**SERVICE\_QUERY\_STATUS** (0x0004)</span></span>         | <span data-ttu-id="c4ef3-192">Necesario para llamar a la función [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) o [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) para solicitar al administrador de control de servicios el estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-192">Required to call the [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) or [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function to ask the service control manager about the status of the service.</span></span><br/> <span data-ttu-id="c4ef3-193">Necesario para llamar a la función [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) para recibir una notificación cuando un servicio cambia de estado.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-193">Required to call the [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) function to receive notification when a service changes status.</span></span><br/> |
| <span data-ttu-id="c4ef3-194">**Servicio \_ de INICIAR** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-194">**SERVICE\_START** (0x0010)</span></span>                 | <span data-ttu-id="c4ef3-195">Necesario para llamar a la función [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) para iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-195">Required to call the [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) function to start the service.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="c4ef3-196">**Servicio \_ de DETENER** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-196">**SERVICE\_STOP** (0x0020)</span></span>                  | <span data-ttu-id="c4ef3-197">Necesario para llamar a la función [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para detener el servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-197">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to stop the service.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c4ef3-198">**Servicio \_ de \_ \_ Control definido por el usuario**(0x0100)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-198">**SERVICE\_USER\_DEFINED\_CONTROL**(0x0100)</span></span> | <span data-ttu-id="c4ef3-199">Necesario para llamar a la función [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para especificar un código de control definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-199">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to specify a user-defined control code.</span></span>                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="c4ef3-200">A continuación se muestran los [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights) para un servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-200">The following are the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) for a service.</span></span>



| <span data-ttu-id="c4ef3-201">Derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="c4ef3-201">Access right</span></span>                 | <span data-ttu-id="c4ef3-202">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4ef3-202">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ef3-203">**ACCESO a la \_ seguridad del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="c4ef3-203">**ACCESS\_SYSTEM\_SECURITY**</span></span> | <span data-ttu-id="c4ef3-204">Necesario para llamar a la función [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) o [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) para tener acceso a la SACL.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-204">Required to call the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) or [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to access the SACL.</span></span> <span data-ttu-id="c4ef3-205">La manera adecuada de obtener este acceso es habilitar el [**privilegio**](/windows/desktop/SecAuthZ/privileges) de **\_ \_ nombre de seguridad de se** en el token de acceso actual del autor de la llamada, abrir el identificador para tener acceso al acceso de **\_ \_ seguridad del sistema** y, a continuación, deshabilitar el privilegio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-205">The proper way to obtain this access is to enable the **SE\_SECURITY\_NAME**[**privilege**](/windows/desktop/SecAuthZ/privileges) in the caller's current access token, open the handle for **ACCESS\_SYSTEM\_SECURITY** access, and then disable the privilege.</span></span> |
| <span data-ttu-id="c4ef3-206">**Eliminar**   (0x10000)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-206">**DELETE**   (0x10000)</span></span>       | <span data-ttu-id="c4ef3-207">Necesario para llamar a la función [**actividades**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) para eliminar el servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-207">Required to call the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to delete the service.</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c4ef3-208">**Leer \_ CONTROL**  (0x20000)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-208">**READ\_CONTROL**  (0x20000)</span></span>    | <span data-ttu-id="c4ef3-209">Necesario para llamar a la función [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) para consultar el descriptor de seguridad del objeto de servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-209">Required to call the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function to query the security descriptor of the service object.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c4ef3-210">**Escribir \_ DAC**  (0x40000)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-210">**WRITE\_DAC**  (0x40000)</span></span>    | <span data-ttu-id="c4ef3-211">Necesario para llamar a la función [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) para modificar el miembro **DACL** del descriptor de seguridad del objeto de servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-211">Required to call the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to modify the **Dacl** member of the service object's security descriptor.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c4ef3-212">**Escribir \_ PROPIETARIO** (0x80000)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-212">**WRITE\_OWNER** (0x80000)</span></span>   | <span data-ttu-id="c4ef3-213">Necesario para llamar a la función [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) para modificar el **propietario** y los miembros del **Grupo** del descriptor de seguridad del objeto de servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-213">Required to call the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to modify the **Owner** and **Group** members of the service object's security descriptor.</span></span>                                                                                                                                                                                                                                                   |



 

<span data-ttu-id="c4ef3-214">A continuación se muestran los [derechos de acceso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para un servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-214">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a service.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c4ef3-215">Derecho de acceso</span><span class="sxs-lookup"><span data-stu-id="c4ef3-215">Access right</span></span></th>
<th><span data-ttu-id="c4ef3-216">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4ef3-216">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4ef3-217"><strong>GENERIC_READ</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-217"><strong>GENERIC_READ</strong></span></span></td>
<td><dl> <span data-ttu-id="c4ef3-218"><strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-218"><strong>STANDARD_RIGHTS_READ</strong></span></span><br /><span data-ttu-id="c4ef3-219">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-219">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="c4ef3-220">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-220">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="c4ef3-221">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-221">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="c4ef3-222">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-222">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4ef3-223"><strong>GENERIC_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-223"><strong>GENERIC_WRITE</strong></span></span></td>
<td><dl> <span data-ttu-id="c4ef3-224"><strong>STANDARD_RIGHTS_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-224"><strong>STANDARD_RIGHTS_WRITE</strong></span></span><br /><span data-ttu-id="c4ef3-225">
<strong>SERVICE_CHANGE_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-225">
<strong>SERVICE_CHANGE_CONFIG</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4ef3-226"><strong>GENERIC_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-226"><strong>GENERIC_EXECUTE</strong></span></span></td>
<td><dl> <span data-ttu-id="c4ef3-227"><strong>STANDARD_RIGHTS_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-227"><strong>STANDARD_RIGHTS_EXECUTE</strong></span></span><br /><span data-ttu-id="c4ef3-228">
<strong>SERVICE_START</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-228">
<strong>SERVICE_START</strong></span></span><br /><span data-ttu-id="c4ef3-229">
<strong>SERVICE_STOP</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-229">
<strong>SERVICE_STOP</strong></span></span><br /><span data-ttu-id="c4ef3-230">
<strong>SERVICE_PAUSE_CONTINUE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-230">
<strong>SERVICE_PAUSE_CONTINUE</strong></span></span><br /><span data-ttu-id="c4ef3-231">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-231">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c4ef3-232">El SCM crea el descriptor de seguridad de un objeto de servicio cuando la función [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) instala el servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-232">The SCM creates a service object's security descriptor when the service is installed by the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function.</span></span> <span data-ttu-id="c4ef3-233">El descriptor de seguridad predeterminado de un objeto de servicio concede el siguiente acceso.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-233">The default security descriptor of a service object grants the following access.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c4ef3-234">Cuenta</span><span class="sxs-lookup"><span data-stu-id="c4ef3-234">Account</span></span></th>
<th><span data-ttu-id="c4ef3-235">Derechos de acceso</span><span class="sxs-lookup"><span data-stu-id="c4ef3-235">Access rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4ef3-236">Usuarios autenticados remotos</span><span class="sxs-lookup"><span data-stu-id="c4ef3-236">Remote authenticated users</span></span></td>
<td><span data-ttu-id="c4ef3-237">No se concede de forma predeterminada. <strong>Windows Server 2003 con SP1: SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-237">Not granted by default.<strong>Windows Server 2003 with SP1:  SERVICE_USER_DEFINED_CONTROL</strong></span></span><br/> <span data-ttu-id="c4ef3-238"><strong>Windows Server 2003 y Windows XP:</strong> Los derechos de acceso para los usuarios autenticados remotos son los mismos que para los usuarios autenticados localmente.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-238"><strong>Windows Server 2003 and Windows XP:</strong> The access rights for remote authenticated users are the same as for local authenticated users.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4ef3-239">Usuarios autenticados localmente (incluido LocalService y NetworkService)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-239">Local authenticated users (including LocalService and NetworkService)</span></span></td>
<td><dl> <span data-ttu-id="c4ef3-240"><strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-240"><strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="c4ef3-241">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-241">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br /><span data-ttu-id="c4ef3-242">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-242">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="c4ef3-243">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-243">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="c4ef3-244">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-244">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="c4ef3-245">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-245">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4ef3-246">LocalSystem (Sistema local)</span><span class="sxs-lookup"><span data-stu-id="c4ef3-246">LocalSystem</span></span></td>
<td><dl> <span data-ttu-id="c4ef3-247"><strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-247"><strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="c4ef3-248">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-248">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br /><span data-ttu-id="c4ef3-249">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-249">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="c4ef3-250">
<strong>SERVICE_PAUSE_CONTINUE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-250">
<strong>SERVICE_PAUSE_CONTINUE</strong></span></span><br /><span data-ttu-id="c4ef3-251">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-251">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="c4ef3-252">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-252">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="c4ef3-253">
<strong>SERVICE_START</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-253">
<strong>SERVICE_START</strong></span></span><br /><span data-ttu-id="c4ef3-254">
<strong>SERVICE_STOP</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-254">
<strong>SERVICE_STOP</strong></span></span><br /><span data-ttu-id="c4ef3-255">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-255">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4ef3-256">Administradores</span><span class="sxs-lookup"><span data-stu-id="c4ef3-256">Administrators</span></span></td>
<td><dl> <span data-ttu-id="c4ef3-257"><strong>DELETE</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-257"><strong>DELETE</strong></span></span><br /><span data-ttu-id="c4ef3-258">
<strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-258">
<strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="c4ef3-259">
<strong>SERVICE_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-259">
<strong>SERVICE_ALL_ACCESS</strong></span></span><br /><span data-ttu-id="c4ef3-260">
<strong>WRITE_DAC</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-260">
<strong>WRITE_DAC</strong></span></span><br /><span data-ttu-id="c4ef3-261">
<strong>WRITE_OWNER</strong></span><span class="sxs-lookup"><span data-stu-id="c4ef3-261">
<strong>WRITE_OWNER</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c4ef3-262">Para realizar cualquier operación, el usuario debe haber iniciado sesión de forma interactiva o el servicio debe usar una de las cuentas de servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-262">To perform any operations, the user must be logged on interactively or the service must use one of the service accounts.</span></span>

<span data-ttu-id="c4ef3-263">Para obtener o establecer el descriptor de seguridad de un objeto de servicio, utilice las funciones [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) y [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="c4ef3-263">To get or set the security descriptor for a service object, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) and [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) functions.</span></span> <span data-ttu-id="c4ef3-264">Para obtener más información, consulte [modificar la DACL para un servicio](modifying-the-dacl-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="c4ef3-264">For more information, see [Modifying the DACL for a Service](modifying-the-dacl-for-a-service.md).</span></span>

<span data-ttu-id="c4ef3-265">Cuando un proceso utiliza la función [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) , el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad del objeto de servicio.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-265">When a process uses the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) function, the system checks the requested access rights against the security descriptor for the service object.</span></span>

<span data-ttu-id="c4ef3-266">Conceder determinados derechos de acceso a los usuarios que no son de confianza (como la **\_ \_ configuración de cambio de servicio** o la **\_ detención del servicio**) pueden permitirles interferir en la ejecución del servicio y, posiblemente, permitirles ejecutar aplicaciones con la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-266">Granting certain access rights to untrusted users (such as **SERVICE\_CHANGE\_CONFIG** or **SERVICE\_STOP**) can allow them to interfere with the execution of your service, and possibly allow them to run applications under the LocalSystem account.</span></span>

<span data-ttu-id="c4ef3-267">Cuando se llama a la [**función EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) , si el autor de la llamada no tiene el derecho de acceso de **\_ \_ Estado de consulta de servicio** a un servicio, el servicio se omite de forma silenciosa en la lista de servicios devueltos al cliente.</span><span class="sxs-lookup"><span data-stu-id="c4ef3-267">When [**EnumServicesStatusEx function**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) is called, if the caller does not have the **SERVICE\_QUERY\_STATUS** access right to a service, the service is silently omitted from the list of services returned to the client.</span></span>

 

