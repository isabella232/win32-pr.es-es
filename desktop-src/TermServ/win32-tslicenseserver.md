---
title: Win32_TSLicenseServer (clase)
description: Proporciona métodos y propiedades para ver y configurar licencias de Escritorio remoto (licencias de escritorio remoto) en un servidor de licencias de Escritorio remoto.
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseServer clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSLicenseServer de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer
- Win32_TSLicenseServer.FirstName
- Win32_TSLicenseServer.LastName
- Win32_TSLicenseServer.Company
- Win32_TSLicenseServer.CountryRegion
- Win32_TSLicenseServer.eMail
- Win32_TSLicenseServer.OrgUnit
- Win32_TSLicenseServer.Address
- Win32_TSLicenseServer.City
- Win32_TSLicenseServer.State
- Win32_TSLicenseServer.PostalCode
- Win32_TSLicenseServer.ServerRole
- Win32_TSLicenseServer.DatabasePath
- Win32_TSLicenseServer.ProductId
- Win32_TSLicenseServer.Version
- Win32_TSLicenseServer.VersionNumber
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31951b943723e620414b2f714327db8c786f9ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996670"
---
# <a name="win32_tslicenseserver-class"></a><span data-ttu-id="b76c0-105">\_Clase Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="b76c0-105">Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="b76c0-106">Proporciona métodos y propiedades para ver y configurar licencias de Escritorio remoto (licencias de escritorio remoto) en un servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-106">Provides methods and properties to view and configure Remote Desktop Licensing (RD Licensing) on a Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b76c0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b76c0-107">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseServer
{
  string FirstName;
  string LastName;
  string Company;
  string CountryRegion;
  string eMail;
  string OrgUnit;
  string Address;
  string City;
  string State;
  string PostalCode;
  uint32 ServerRole;
  string DatabasePath;
  string ProductId;
  string Version;
  string VersionNumber;
};
```

## <a name="members"></a><span data-ttu-id="b76c0-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b76c0-108">Members</span></span>

<span data-ttu-id="b76c0-109">La **clase \_ TSLicenseServer de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b76c0-109">The **Win32\_TSLicenseServer** class has these types of members:</span></span>

-   [<span data-ttu-id="b76c0-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b76c0-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b76c0-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b76c0-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b76c0-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b76c0-112">Methods</span></span>

<span data-ttu-id="b76c0-113">La clase **Win32 \_ TSLicenseServer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b76c0-113">The **Win32\_TSLicenseServer** class has these methods.</span></span>



| <span data-ttu-id="b76c0-114">Método</span><span class="sxs-lookup"><span data-stu-id="b76c0-114">Method</span></span>                                                                                   | <span data-ttu-id="b76c0-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b76c0-115">Description</span></span>                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b76c0-116">**ActivateServer**</span><span class="sxs-lookup"><span data-stu-id="b76c0-116">**ActivateServer**</span></span>](activateserver-win32-tslicenseserver.md)                           | <span data-ttu-id="b76c0-117">Activa el servidor de licencias de Escritorio remoto mediante un identificador de servidor de licencias Escritorio remoto que se obtiene a través del teléfono o Internet.</span><span class="sxs-lookup"><span data-stu-id="b76c0-117">Activates the Remote Desktop license server by using a Remote Desktop license server ID that is obtained over the phone or the Internet.</span></span><br/>                                                                                           |
| [<span data-ttu-id="b76c0-118">**ActivateServerAutomatic**</span><span class="sxs-lookup"><span data-stu-id="b76c0-118">**ActivateServerAutomatic**</span></span>](activateserverautomatic-win32-tslicenseserver.md)         | <span data-ttu-id="b76c0-119">Activa el servidor de licencias de Escritorio remoto automáticamente a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="b76c0-119">Activates the Remote Desktop license server automatically over the Internet.</span></span> <span data-ttu-id="b76c0-120">Las propiedades **FirstName**, **LastName**, **Company** y **CountryRegion** no deben estar vacías cuando se llama a este método o se producirá un error en el método.</span><span class="sxs-lookup"><span data-stu-id="b76c0-120">The **FirstName**, **LastName**, **Company**, and **CountryRegion** properties must not be empty when this method is called, or the method will fail.</span></span><br/> |
| [<span data-ttu-id="b76c0-121">**AddLStoTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="b76c0-121">**AddLStoTSLSGroup**</span></span>](addlstotslsgroup-win32-tslicenseserver.md)                       | <span data-ttu-id="b76c0-122">Agrega el servidor de licencias de Escritorio remoto al grupo servidores de licencias de Escritorio remoto en un controlador de dominio del mismo dominio que el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="b76c0-122">Adds the Remote Desktop license server to the Remote Desktop License Servers group on a domain controller in the same domain as the license server.</span></span><br/>                                                                                |
| [<span data-ttu-id="b76c0-123">**ChangeRole**</span><span class="sxs-lookup"><span data-stu-id="b76c0-123">**ChangeRole**</span></span>](changerole-win32-tslicenseserver.md)                                   | <span data-ttu-id="b76c0-124">Cambia el ámbito de detección del servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-124">Changes the discovery scope of the Remote Desktop license server.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="b76c0-125">**CreateTSCGroup**</span><span class="sxs-lookup"><span data-stu-id="b76c0-125">**CreateTSCGroup**</span></span>](createtscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="b76c0-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="b76c0-126">This method is not supported.</span></span><br/> <span data-ttu-id="b76c0-127">**Windows server 2008 R2 y Windows server 2008:** Crea el grupo local de Terminal Server equipos en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-127">**Windows Server 2008 R2 and Windows Server 2008:** Creates the Terminal Server Computers local group on the Remote Desktop license server.</span></span><br/>                                               |
| [<span data-ttu-id="b76c0-128">**DeactivateServer**</span><span class="sxs-lookup"><span data-stu-id="b76c0-128">**DeactivateServer**</span></span>](deactivateserver-win32-tslicenseserver.md)                       | <span data-ttu-id="b76c0-129">Desactiva el servidor de licencias de Escritorio remoto mediante un código de confirmación que se recibe a través del teléfono.</span><span class="sxs-lookup"><span data-stu-id="b76c0-129">Deactivates the Remote Desktop license server by using a confirmation code that is received over the phone.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="b76c0-130">**DeactivateServerAutomatic**</span><span class="sxs-lookup"><span data-stu-id="b76c0-130">**DeactivateServerAutomatic**</span></span>](deactivateserverautomatic-win32-tslicenseserver.md)     | <span data-ttu-id="b76c0-131">Desactiva el servidor de licencias de Escritorio remoto a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="b76c0-131">Deactivates the Remote Desktop license server over the Internet.</span></span> <span data-ttu-id="b76c0-132">Las propiedades **FirstName** y **LastName** no deben estar vacías cuando se llama a este método o se producirá un error en el método.</span><span class="sxs-lookup"><span data-stu-id="b76c0-132">The **FirstName** and **LastName** properties must not be empty when this method is called, or the method will fail.</span></span><br/>                                              |
| [<span data-ttu-id="b76c0-133">**GetActivationStatus**</span><span class="sxs-lookup"><span data-stu-id="b76c0-133">**GetActivationStatus**</span></span>](getactivationstatus-win32-tslicenseserver.md)                 | <span data-ttu-id="b76c0-134">Recupera el estado de activación actual.</span><span class="sxs-lookup"><span data-stu-id="b76c0-134">Retrieves the current activation status.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="b76c0-135">**GetLicenseServerId**</span><span class="sxs-lookup"><span data-stu-id="b76c0-135">**GetLicenseServerId**</span></span>](getlicenseserverid-win32-tslicenseserver.md)                   | <span data-ttu-id="b76c0-136">Recupera un identificador de servidor de licencias Escritorio remoto si el servidor está activado actualmente.</span><span class="sxs-lookup"><span data-stu-id="b76c0-136">Retrieves a Remote Desktop license server ID if the server is currently activated.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="b76c0-137">**IsLSinTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="b76c0-137">**IsLSinTSLSGroup**</span></span>](islsintslsgroup-win32-tslicenseserver.md)                         | <span data-ttu-id="b76c0-138">Recupera si el servidor de licencias Escritorio remoto es miembro del grupo servidores de licencias Escritorio remoto en un controlador de dominio de un dominio determinado.</span><span class="sxs-lookup"><span data-stu-id="b76c0-138">Retrieves whether the Remote Desktop license server is a member of the Remote Desktop License Servers group on a domain controller in a given domain.</span></span><br/>                                                                              |
| [<span data-ttu-id="b76c0-139">**IsLSonDC**</span><span class="sxs-lookup"><span data-stu-id="b76c0-139">**IsLSonDC**</span></span>](islsondc-win32-tslicenseserver.md)                                       | <span data-ttu-id="b76c0-140">Recupera si la concesión de licencias de escritorio remoto está instalada en un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="b76c0-140">Retrieves whether RD Licensing is installed on a domain controller.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="b76c0-141">**IsLSPreventUpgradeGPEnabled**</span><span class="sxs-lookup"><span data-stu-id="b76c0-141">**IsLSPreventUpgradeGPEnabled**</span></span>](islspreventupgradegpenabled-win32-tslicenseserver.md) | <span data-ttu-id="b76c0-142">Recupera si está habilitada la configuración de directiva de grupo "impedir actualización de licencia" en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-142">Retrieves whether the "prevent license upgrade" group policy setting is enabled on the Remote Desktop license server.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="b76c0-143">**IsLSPublished**</span><span class="sxs-lookup"><span data-stu-id="b76c0-143">**IsLSPublished**</span></span>](islspublished-win32-tslicenseserver.md)                             | <span data-ttu-id="b76c0-144">Recupera si el servidor de licencias de Escritorio remoto se publica en Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="b76c0-144">Retrieves whether the Remote Desktop license server is published in Active Directory Domain Services (AD DS).</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="b76c0-145">**IsLSRegisteredToSCP**</span><span class="sxs-lookup"><span data-stu-id="b76c0-145">**IsLSRegisteredToSCP**</span></span>](win32-tslicenseserver-islsregisteredtoscp.md)                 | <span data-ttu-id="b76c0-146">Recupera si el servidor de licencias de Escritorio remoto está registrado como punto de conexión de servicio en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="b76c0-146">Retrieves whether the Remote Desktop license server is registered as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                               |
| [<span data-ttu-id="b76c0-147">**IsLSSecGrpGPEnabled**</span><span class="sxs-lookup"><span data-stu-id="b76c0-147">**IsLSSecGrpGPEnabled**</span></span>](islssecgrpgpenabled-win32-tslicenseserver.md)                 | <span data-ttu-id="b76c0-148">Recupera si el valor de directiva de grupo "grupo de seguridad del servidor de licencias" está habilitado en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-148">Retrieves whether the "license server security group" group policy setting is enabled on the Remote Desktop license server.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="b76c0-149">**IsSecureAccessAllowed**</span><span class="sxs-lookup"><span data-stu-id="b76c0-149">**IsSecureAccessAllowed**</span></span>](issecureaccessallowed-win32-tslicenseserver.md)             | <span data-ttu-id="b76c0-150">Recupera si un servidor host de sesión de escritorio remoto tiene permiso para solicitar Servicios de Escritorio remoto licencias de acceso de cliente (cal de RDS) del servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-150">Retrieves whether an RD Session Host server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from the Remote Desktop license server.</span></span><br/>                                                                |
| [<span data-ttu-id="b76c0-151">**IsTSCGroupPresent**</span><span class="sxs-lookup"><span data-stu-id="b76c0-151">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)                     | <span data-ttu-id="b76c0-152">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="b76c0-152">This method is not supported.</span></span><br/> <span data-ttu-id="b76c0-153">**Windows server 2008 R2 y Windows server 2008:** Recupera si el grupo local de equipos Terminal Server existe en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-153">**Windows Server 2008 R2 and Windows Server 2008:** Retrieves whether the Terminal Server Computers local group exists on the Remote Desktop license server.</span></span><br/>                              |
| [<span data-ttu-id="b76c0-154">**IsTSinTSCGroup**</span><span class="sxs-lookup"><span data-stu-id="b76c0-154">**IsTSinTSCGroup**</span></span>](istsintscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="b76c0-155">Recupera si un servidor host de sesión de escritorio remoto es miembro del grupo local de Terminal Server equipos en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-155">Retrieves whether an RD Session Host server is a member of the Terminal Server Computers local group on the Remote Desktop license server.</span></span><br/>                                                                                         |
| [<span data-ttu-id="b76c0-156">**PublishLS**</span><span class="sxs-lookup"><span data-stu-id="b76c0-156">**PublishLS**</span></span>](publishls-win32-tslicenseserver.md)                                     | <span data-ttu-id="b76c0-157">Publica el servidor de licencias de Escritorio remoto en AD DS.</span><span class="sxs-lookup"><span data-stu-id="b76c0-157">Publishes the Remote Desktop license server in AD DS.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="b76c0-158">**ReactivateServer**</span><span class="sxs-lookup"><span data-stu-id="b76c0-158">**ReactivateServer**</span></span>](reactivateserver-win32-tslicenseserver.md)                       | <span data-ttu-id="b76c0-159">Reactiva el servidor de licencias de Escritorio remoto mediante un nuevo identificador de servidor de licencias Escritorio remoto que se obtiene a través del teléfono o Internet.</span><span class="sxs-lookup"><span data-stu-id="b76c0-159">Reactivates the Remote Desktop license server by using a new Remote Desktop license server ID that is obtained over the phone or the Internet.</span></span><br/>                                                                                     |
| [<span data-ttu-id="b76c0-160">**ReactivateServerAutomatic**</span><span class="sxs-lookup"><span data-stu-id="b76c0-160">**ReactivateServerAutomatic**</span></span>](reactivateserverautomatic-win32-tslicenseserver.md)     | <span data-ttu-id="b76c0-161">Reactiva el servidor de licencias de Escritorio remoto a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="b76c0-161">Reactivates the Remote Desktop license server over the Internet.</span></span> <span data-ttu-id="b76c0-162">Las propiedades **FirstName** y **LastName** no deben estar vacías cuando se llama a este método o se producirá un error en el método.</span><span class="sxs-lookup"><span data-stu-id="b76c0-162">The **FirstName** and **LastName** properties must not be empty when this method is called, or the method will fail.</span></span><br/>                                              |
| [<span data-ttu-id="b76c0-163">**RegisterLSToSCP**</span><span class="sxs-lookup"><span data-stu-id="b76c0-163">**RegisterLSToSCP**</span></span>](win32-tslicenseserver-registerlstoscp.md)                         | <span data-ttu-id="b76c0-164">Registra el servidor de licencias de Escritorio remoto como punto de conexión de servicio en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="b76c0-164">Registers the Remote Desktop license server as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="b76c0-165">**RemoveLSfromTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="b76c0-165">**RemoveLSfromTSLSGroup**</span></span>](removelsfromtslsgroup-win32-tslicenseserver.md)             | <span data-ttu-id="b76c0-166">Quita el servidor de licencias de Escritorio remoto del grupo servidores de licencias de Escritorio remoto en un controlador de dominio del mismo dominio que el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="b76c0-166">Removes the Remote Desktop license server from the Remote Desktop License Servers group on a domain controller in the same domain as the license server.</span></span><br/>                                                                           |
| [<span data-ttu-id="b76c0-167">**RemoveTSCGroup**</span><span class="sxs-lookup"><span data-stu-id="b76c0-167">**RemoveTSCGroup**</span></span>](removetscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="b76c0-168">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="b76c0-168">This method is not supported.</span></span><br/> <span data-ttu-id="b76c0-169">**Windows server 2008 R2 y Windows server 2008:** Quita el grupo local de Terminal Server equipos del servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-169">**Windows Server 2008 R2 and Windows Server 2008:** Removes the Terminal Server Computers local group from the Remote Desktop license server.</span></span><br/>                                             |
| [<span data-ttu-id="b76c0-170">**UnpublishLS**</span><span class="sxs-lookup"><span data-stu-id="b76c0-170">**UnpublishLS**</span></span>](unpublishls-win32-tslicenseserver.md)                                 | <span data-ttu-id="b76c0-171">Anula la publicación de un servidor de licencias de Escritorio remoto de AD DS.</span><span class="sxs-lookup"><span data-stu-id="b76c0-171">Unpublishes a Remote Desktop license server from AD DS.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="b76c0-172">**UnRegisterLSFromSCP**</span><span class="sxs-lookup"><span data-stu-id="b76c0-172">**UnRegisterLSFromSCP**</span></span>](win32-tslicenseserver-unregisterlsfromscp.md)                 | <span data-ttu-id="b76c0-173">Quita el servidor de licencias de Escritorio remoto como punto de conexión de servicio en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="b76c0-173">Removes the Remote Desktop license server as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="b76c0-174">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b76c0-174">Properties</span></span>

<span data-ttu-id="b76c0-175">La **clase \_ TSLicenseServer de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b76c0-175">The **Win32\_TSLicenseServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b76c0-176">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="b76c0-176">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b76c0-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b76c0-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b76c0-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b76c0-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b76c0-179">Dirección postal del contacto para la concesión de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-179">Street address of the contact for RD Licensing.</span></span> <span data-ttu-id="b76c0-180">Esta propiedad se usa cuando se llama al método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b76c0-180">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="b76c0-181">(Esta propiedad es opcional cuando se usa el método **ActivateServerAutomatic** ).</span><span class="sxs-lookup"><span data-stu-id="b76c0-181">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="b76c0-182">**Ciudad**</span><span class="sxs-lookup"><span data-stu-id="b76c0-182">**City**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b76c0-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b76c0-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b76c0-184">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b76c0-184">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b76c0-185">Ciudad del contacto para la concesión de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-185">City of the contact for RD Licensing.</span></span> <span data-ttu-id="b76c0-186">Esta propiedad se usa cuando se llama al método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b76c0-186">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="b76c0-187">(Esta propiedad es opcional cuando se usa el método **ActivateServerAutomatic** ).</span><span class="sxs-lookup"><span data-stu-id="b76c0-187">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="b76c0-188">**Company**</span><span class="sxs-lookup"><span data-stu-id="b76c0-188">**Company**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b76c0-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b76c0-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b76c0-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b76c0-190">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b76c0-191">Empresa del contacto para la concesión de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-191">Company of the contact for RD Licensing.</span></span> <span data-ttu-id="b76c0-192">Esta propiedad se usa (y se requiere) cuando se llama al método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b76c0-192">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span>

</dd> <dt>

<span data-ttu-id="b76c0-193">**CountryRegion**</span><span class="sxs-lookup"><span data-stu-id="b76c0-193">**CountryRegion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b76c0-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b76c0-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b76c0-195">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b76c0-195">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b76c0-196">País o región del contacto para la concesión de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-196">Country/region of the contact for RD Licensing.</span></span> <span data-ttu-id="b76c0-197">Esta propiedad se usa (y se requiere) cuando se llama al método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b76c0-197">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span>

</dd> <dt>

<span data-ttu-id="b76c0-198">**DatabasePath**</span><span class="sxs-lookup"><span data-stu-id="b76c0-198">**DatabasePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b76c0-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b76c0-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b76c0-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b76c0-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b76c0-201">Ruta de acceso de la base de datos de licencias RDS.</span><span class="sxs-lookup"><span data-stu-id="b76c0-201">Path of the RDS Licensing database.</span></span>

</dd> <dt>

<span data-ttu-id="b76c0-202">**Correo electrónico**</span><span class="sxs-lookup"><span data-stu-id="b76c0-202">**eMail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b76c0-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b76c0-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b76c0-204">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b76c0-204">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b76c0-205">Dirección de correo electrónico del contacto para la concesión de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-205">Email address of the contact for RD Licensing.</span></span> <span data-ttu-id="b76c0-206">Esta propiedad se usa cuando se llama a los métodos [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b76c0-206">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span> <span data-ttu-id="b76c0-207">(Esta propiedad es opcional para estas llamadas a métodos).</span><span class="sxs-lookup"><span data-stu-id="b76c0-207">(This property is optional for these method calls.)</span></span>

</dd> <dt>

<span data-ttu-id="b76c0-208">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b76c0-208">**FirstName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b76c0-209">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b76c0-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b76c0-210">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b76c0-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b76c0-211">Nombre del contacto para la concesión de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-211">First name of the contact for RD Licensing.</span></span> <span data-ttu-id="b76c0-212">Esta propiedad se usa (y se requiere) cuando se llama a los métodos [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b76c0-212">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="b76c0-213">**Apellidos**</span><span class="sxs-lookup"><span data-stu-id="b76c0-213">**LastName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b76c0-214">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b76c0-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b76c0-215">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b76c0-215">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b76c0-216">Apellido del contacto para la concesión de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-216">Last name of the contact for RD Licensing.</span></span> <span data-ttu-id="b76c0-217">Esta propiedad se usa (y se requiere) cuando se llama a los métodos [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md)o [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b76c0-217">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="b76c0-218">**OrgUnit**</span><span class="sxs-lookup"><span data-stu-id="b76c0-218">**OrgUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b76c0-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b76c0-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b76c0-220">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b76c0-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b76c0-221">Unidad organizativa del contacto para la concesión de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-221">Organizational unit of the contact for RD Licensing.</span></span> <span data-ttu-id="b76c0-222">Esta propiedad se usa cuando se llama a [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b76c0-222">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) is called.</span></span> <span data-ttu-id="b76c0-223">(Esta propiedad es opcional cuando se usa el método **ActivateServerAutomatic** ).</span><span class="sxs-lookup"><span data-stu-id="b76c0-223">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="b76c0-224">**PostalCode**</span><span class="sxs-lookup"><span data-stu-id="b76c0-224">**PostalCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b76c0-225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b76c0-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b76c0-226">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b76c0-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b76c0-227">Código postal del contacto para la concesión de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-227">Postal code of the contact for RD Licensing.</span></span> <span data-ttu-id="b76c0-228">Esta propiedad se usa cuando se llama al método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b76c0-228">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="b76c0-229">(Esta propiedad es opcional cuando se usa el método **ActivateServerAutomatic** ).</span><span class="sxs-lookup"><span data-stu-id="b76c0-229">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="b76c0-230">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="b76c0-230">**ProductId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b76c0-231">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b76c0-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b76c0-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b76c0-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b76c0-233">IDENTIFICADOR del producto del servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-233">Product ID of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="b76c0-234">**ServerRole**</span><span class="sxs-lookup"><span data-stu-id="b76c0-234">**ServerRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b76c0-235">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b76c0-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b76c0-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b76c0-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b76c0-237">Describe el ámbito de licencias para el servidor de licencias de Escritorio remoto dentro de la organización.</span><span class="sxs-lookup"><span data-stu-id="b76c0-237">Describes the licensing scope for the Remote Desktop license server within the organization.</span></span>

<dt>

<span data-ttu-id="b76c0-238">0</span><span class="sxs-lookup"><span data-stu-id="b76c0-238">0</span></span>
</dt> <dd>

<span data-ttu-id="b76c0-239">Los servidores host de sesión de escritorio remoto del mismo grupo de trabajo pueden detectar el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="b76c0-239">RD Session Host servers in the same workgroup can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="b76c0-240">1</span><span class="sxs-lookup"><span data-stu-id="b76c0-240">1</span></span>
</dt> <dd>

<span data-ttu-id="b76c0-241">Los servidores host de sesión de escritorio remoto del mismo dominio pueden detectar el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="b76c0-241">RD Session Host servers in the same domain can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="b76c0-242">2</span><span class="sxs-lookup"><span data-stu-id="b76c0-242">2</span></span>
</dt> <dd>

<span data-ttu-id="b76c0-243">Los servidores host de sesión de escritorio remoto de varios dominios del mismo bosque pueden detectar el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="b76c0-243">RD Session Host servers from multiple domains in the same forest can discover the license server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b76c0-244">**State**</span><span class="sxs-lookup"><span data-stu-id="b76c0-244">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b76c0-245">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b76c0-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b76c0-246">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b76c0-246">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b76c0-247">Estado del contacto para la concesión de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-247">State of the contact for RD Licensing.</span></span> <span data-ttu-id="b76c0-248">Esta propiedad se usa cuando se llama al método [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b76c0-248">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="b76c0-249">(Esta propiedad es opcional cuando se usa el método **ActivateServerAutomatic** ).</span><span class="sxs-lookup"><span data-stu-id="b76c0-249">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="b76c0-250">**Versión**</span><span class="sxs-lookup"><span data-stu-id="b76c0-250">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b76c0-251">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b76c0-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b76c0-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b76c0-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b76c0-253">Versión del servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-253">Version of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="b76c0-254">**NúmeroDeVersión**</span><span class="sxs-lookup"><span data-stu-id="b76c0-254">**VersionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b76c0-255">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b76c0-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b76c0-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b76c0-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b76c0-257">Número de versión del servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b76c0-257">Version number of the Remote Desktop license server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b76c0-258">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b76c0-258">Remarks</span></span>

<span data-ttu-id="b76c0-259">Esta clase es una clase [Singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) y solo puede tener una instancia.</span><span class="sxs-lookup"><span data-stu-id="b76c0-259">This class is a [singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) class and can have only one instance.</span></span> <span data-ttu-id="b76c0-260">Todos los métodos contenidos en esta clase son estáticos.</span><span class="sxs-lookup"><span data-stu-id="b76c0-260">All of the methods contained within this class are static.</span></span>

<span data-ttu-id="b76c0-261">Para usar esta clase, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="b76c0-261">You must be a member of the Administrators group to use this class.</span></span> <span data-ttu-id="b76c0-262">Si el autor de la llamada no es miembro del grupo administradores, las propiedades devueltas estarán vacías.</span><span class="sxs-lookup"><span data-stu-id="b76c0-262">If the caller is not a member of the Administrators group, the properties returned will be empty.</span></span>

<span data-ttu-id="b76c0-263">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b76c0-263">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b76c0-264">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b76c0-264">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b76c0-265">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="b76c0-265">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b76c0-266">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b76c0-266">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b76c0-267">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b76c0-267">Requirements</span></span>



| <span data-ttu-id="b76c0-268">Requisito</span><span class="sxs-lookup"><span data-stu-id="b76c0-268">Requirement</span></span> | <span data-ttu-id="b76c0-269">Value</span><span class="sxs-lookup"><span data-stu-id="b76c0-269">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b76c0-270">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b76c0-270">Minimum supported client</span></span><br/> | <span data-ttu-id="b76c0-271">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b76c0-271">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b76c0-272">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b76c0-272">Minimum supported server</span></span><br/> | <span data-ttu-id="b76c0-273">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b76c0-273">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="b76c0-274">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b76c0-274">Namespace</span></span><br/>                | <span data-ttu-id="b76c0-275">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b76c0-275">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b76c0-276">MOF</span><span class="sxs-lookup"><span data-stu-id="b76c0-276">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b76c0-277"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b76c0-277"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b76c0-278">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b76c0-278">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b76c0-279"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b76c0-279"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b76c0-280">Vea también</span><span class="sxs-lookup"><span data-stu-id="b76c0-280">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b76c0-281">**Win32 \_ TSIssuedLicense**</span><span class="sxs-lookup"><span data-stu-id="b76c0-281">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="b76c0-282">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="b76c0-282">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="b76c0-283">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="b76c0-283">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="b76c0-284">**Win32 \_ TSLicenseReportEntry**</span><span class="sxs-lookup"><span data-stu-id="b76c0-284">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> </dl>

 

