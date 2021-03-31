---
title: MSAD_DomainController (clase)
description: Representa el controlador de dominio (DC) en el que se está ejecutando el proveedor WMI.
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- MSAD_DomainController clase Active Directory
- Active Directory de MSAD_DomainController de clase, se describe
topic_type:
- apiref
api_name:
- MSAD_DomainController
- MSAD_DomainController.DistinguishedName
- MSAD_DomainController.CommonName
- MSAD_DomainController.SiteName
- MSAD_DomainController.NTDsaGUID
- MSAD_DomainController.IsGC
- MSAD_DomainController.TimeOfOldestReplSync
- MSAD_DomainController.TimeOfOldestReplAdd
- MSAD_DomainController.TimeOfOldestReplDel
- MSAD_DomainController.TimeOfOldestReplMod
- MSAD_DomainController.TimeOfOldestReplUpdRefs
- MSAD_DomainController.IsNextRIDPoolAvailable
- MSAD_DomainController.PercentOfRIDsLeft
- MSAD_DomainController.IsRegisteredInDNS
- MSAD_DomainController.IsAdvertisingToLocator
- MSAD_DomainController.IsSysVolReady
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303071d3d268953687bc387709c74531f8b40584
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490739"
---
# <a name="msad_domaincontroller-class"></a><span data-ttu-id="a05f8-105">MSAD \_ DomainController (clase)</span><span class="sxs-lookup"><span data-stu-id="a05f8-105">MSAD\_DomainController class</span></span>

<span data-ttu-id="a05f8-106">Representa el controlador de dominio (DC) en el que se está ejecutando el proveedor WMI.</span><span class="sxs-lookup"><span data-stu-id="a05f8-106">Represents the domain controller (DC) on which the WMI provider is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="a05f8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a05f8-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class  MSAD_DomainController
{
  String   DistinguishedName;
  String   CommonName;
  String   SiteName;
  String   NTDsaGUID;
  boolean  IsGC = FALSE;
  datetime TimeOfOldestReplSync;
  datetime TimeOfOldestReplAdd;
  datetime TimeOfOldestReplDel;
  datetime TimeOfOldestReplMod;
  datetime TimeOfOldestReplUpdRefs;
  boolean  IsNextRIDPoolAvailable = FALSE;
  uint32   PercentOfRIDsLeft;
  boolean  IsRegisteredInDNS;
  boolean  IsAdvertisingToLocator = FALSE;
  boolean  IsSysVolReady = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="a05f8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a05f8-108">Members</span></span>

<span data-ttu-id="a05f8-109">La clase **MSAD \_ DomainController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a05f8-109">The **MSAD\_DomainController** class has these types of members:</span></span>

-   [<span data-ttu-id="a05f8-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a05f8-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="a05f8-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a05f8-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a05f8-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a05f8-112">Methods</span></span>

<span data-ttu-id="a05f8-113">La clase **MSAD \_ DomainController** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a05f8-113">The **MSAD\_DomainController** class has these methods.</span></span>



| <span data-ttu-id="a05f8-114">Método</span><span class="sxs-lookup"><span data-stu-id="a05f8-114">Method</span></span>                                                 | <span data-ttu-id="a05f8-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="a05f8-115">Description</span></span>                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="a05f8-116">**ExecuteKCC**</span><span class="sxs-lookup"><span data-stu-id="a05f8-116">**ExecuteKCC**</span></span>](executekcc-msad-domaincontroller.md) | <span data-ttu-id="a05f8-117">Invoca el comprobador de coherencia de la información para comprobar la topología de replicación.</span><span class="sxs-lookup"><span data-stu-id="a05f8-117">Invokes the Knowledge Consistency Checker to verify the replication topology.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a05f8-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a05f8-118">Properties</span></span>

<span data-ttu-id="a05f8-119">La clase **MSAD \_ DomainController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a05f8-119">The **MSAD\_DomainController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a05f8-120">**CommonName**</span><span class="sxs-lookup"><span data-stu-id="a05f8-120">**CommonName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a05f8-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a05f8-121">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="a05f8-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a05f8-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a05f8-123">Obtiene el nombre común del objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="a05f8-123">Gets the common name of the server object.</span></span>

</dd> <dt>

<span data-ttu-id="a05f8-124">**DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="a05f8-124">**DistinguishedName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a05f8-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a05f8-125">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="a05f8-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a05f8-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a05f8-127">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a05f8-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a05f8-128">Obtiene la ruta de acceso X. 500 del objeto [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) .</span><span class="sxs-lookup"><span data-stu-id="a05f8-128">Gets the X.500 path of the [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) object.</span></span>

</dd> <dt>

<span data-ttu-id="a05f8-129">**IsAdvertisingToLocator**</span><span class="sxs-lookup"><span data-stu-id="a05f8-129">**IsAdvertisingToLocator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a05f8-130">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a05f8-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a05f8-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a05f8-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a05f8-132">Obtiene el valor que indica si el servicio de localizador del controlador de dominio se está anunciando correctamente.</span><span class="sxs-lookup"><span data-stu-id="a05f8-132">Gets the value that indicates whether the locator service on the DC is advertising correctly.</span></span> <span data-ttu-id="a05f8-133">**True** si el servicio de ubicación en el controlador de dominio se está anunciando correctamente; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a05f8-133">**TRUE** if the locator service on the DC is advertising correctly; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a05f8-134">**IsGC**</span><span class="sxs-lookup"><span data-stu-id="a05f8-134">**IsGC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a05f8-135">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a05f8-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a05f8-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a05f8-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a05f8-137">Obtiene el valor que indica si el controlador de dominio es un servidor de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="a05f8-137">Gets the value that indicates whether the DC is a Global Catalog server.</span></span> <span data-ttu-id="a05f8-138">**True** si el controlador de dominio es un servidor de catálogo global; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a05f8-138">**TRUE** if the DC is a Global Catalog server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a05f8-139">**IsNextRIDPoolAvailable**</span><span class="sxs-lookup"><span data-stu-id="a05f8-139">**IsNextRIDPoolAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a05f8-140">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a05f8-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a05f8-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a05f8-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a05f8-142">Obtiene el valor que indica si el controlador de dominio ha obtenido otro grupo de RID.</span><span class="sxs-lookup"><span data-stu-id="a05f8-142">Gets the value that indicates whether the DC has obtained another RID pool.</span></span> <span data-ttu-id="a05f8-143">**True** si el controlador de dominio ha obtenido otro grupo de RID y la asignación de los RID en este controlador de dominio puede continuar incluso si se ha agotado el grupo actual de RID; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a05f8-143">**TRUE** if the DC has obtained another RID pool and allocation of RIDs on this DC can continue even if the current pool of RIDs is exhausted; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a05f8-144">**IsRegisteredInDNS**</span><span class="sxs-lookup"><span data-stu-id="a05f8-144">**IsRegisteredInDNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a05f8-145">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a05f8-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a05f8-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a05f8-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a05f8-147">Obtiene el valor que indica si el controlador de dominio está registrado correctamente en DNS.</span><span class="sxs-lookup"><span data-stu-id="a05f8-147">Gets the value that indicates whether the DC is registered correctly in DNS.</span></span> <span data-ttu-id="a05f8-148">**True** si el controlador de dominio está registrado correctamente en DNS; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a05f8-148">**TRUE** if the DC is registered correctly in DNS; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a05f8-149">**IsSysVolReady**</span><span class="sxs-lookup"><span data-stu-id="a05f8-149">**IsSysVolReady**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a05f8-150">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a05f8-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a05f8-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a05f8-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a05f8-152">Obtiene el valor que indica si SysVol se ha publicado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a05f8-152">Gets the value that indicates whether the SysVol has published correctly.</span></span> <span data-ttu-id="a05f8-153">**True** si SYSVOL se ha publicado correctamente; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a05f8-153">**TRUE** if the SysVol has published correctly; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a05f8-154">**NTDsaGUID**</span><span class="sxs-lookup"><span data-stu-id="a05f8-154">**NTDsaGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a05f8-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a05f8-155">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="a05f8-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a05f8-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a05f8-157">Obtiene el GUID asociado al objeto [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) en el contenedor de configuración.</span><span class="sxs-lookup"><span data-stu-id="a05f8-157">Gets the GUID that is associated with the [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) object in the configuration container.</span></span> <span data-ttu-id="a05f8-158">El objeto **NTDS-DSA** representa el proceso DSA de servicio dominio de Active Directory en el servidor.</span><span class="sxs-lookup"><span data-stu-id="a05f8-158">The **NTDS-DSA** object represents the Active Directory Domain Service DSA process on the server.</span></span>

</dd> <dt>

<span data-ttu-id="a05f8-159">**PercentOfRIDsLeft**</span><span class="sxs-lookup"><span data-stu-id="a05f8-159">**PercentOfRIDsLeft**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a05f8-160">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a05f8-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a05f8-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a05f8-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a05f8-162">Obtiene el porcentaje de los RID que se dejan en el grupo de RID actual de este controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="a05f8-162">Gets the percentage of RIDs that are left in the current RID pool on this DC.</span></span>

</dd> <dt>

<span data-ttu-id="a05f8-163">**Nombresitio**</span><span class="sxs-lookup"><span data-stu-id="a05f8-163">**SiteName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a05f8-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a05f8-164">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="a05f8-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a05f8-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a05f8-166">Obtiene el sitio en el que existe el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="a05f8-166">Gets the site in which the DC exists.</span></span>

</dd> <dt>

<span data-ttu-id="a05f8-167">**TimeOfOldestReplAdd**</span><span class="sxs-lookup"><span data-stu-id="a05f8-167">**TimeOfOldestReplAdd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a05f8-168">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a05f8-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a05f8-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a05f8-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a05f8-170">Obtiene la marca de tiempo de la operación de adición de replicación más antigua que aún está en la cola de este controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="a05f8-170">Gets the timestamp of the oldest replication add operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="a05f8-171">**TimeOfOldestReplDel**</span><span class="sxs-lookup"><span data-stu-id="a05f8-171">**TimeOfOldestReplDel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a05f8-172">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a05f8-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a05f8-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a05f8-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a05f8-174">Obtiene la marca de tiempo de la operación de eliminación de replicación más antigua que todavía está en la cola de este controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="a05f8-174">Gets the timestamp of the oldest replication delete operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="a05f8-175">**TimeOfOldestReplMod**</span><span class="sxs-lookup"><span data-stu-id="a05f8-175">**TimeOfOldestReplMod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a05f8-176">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a05f8-176">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a05f8-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a05f8-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a05f8-178">Obtiene la marca de tiempo de la operación de modificación de replicación más antigua que todavía está en la cola de este controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="a05f8-178">Gets the timestamp of the oldest replication modify operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="a05f8-179">**TimeOfOldestReplSync**</span><span class="sxs-lookup"><span data-stu-id="a05f8-179">**TimeOfOldestReplSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a05f8-180">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a05f8-180">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a05f8-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a05f8-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a05f8-182">Obtiene la marca de tiempo de la operación de sincronización de replicación más antigua que aún está en la cola de este controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="a05f8-182">Gets the timestamp of the oldest replication sync operation that is still in the queue on this domain controller.</span></span>

</dd> <dt>

<span data-ttu-id="a05f8-183">**TimeOfOldestReplUpdRefs**</span><span class="sxs-lookup"><span data-stu-id="a05f8-183">**TimeOfOldestReplUpdRefs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a05f8-184">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a05f8-184">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a05f8-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a05f8-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a05f8-186">Obtiene la marca de tiempo de la operación de actualización de replicación más antigua que aún está en la cola de este controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="a05f8-186">Gets the timestamp of the oldest replication update operation that is still in the queue on this domain controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a05f8-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a05f8-187">Requirements</span></span>



| <span data-ttu-id="a05f8-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="a05f8-188">Requirement</span></span> | <span data-ttu-id="a05f8-189">Value</span><span class="sxs-lookup"><span data-stu-id="a05f8-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a05f8-190">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a05f8-190">Minimum supported client</span></span><br/> | <span data-ttu-id="a05f8-191">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a05f8-191">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a05f8-192">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a05f8-192">Minimum supported server</span></span><br/> | <span data-ttu-id="a05f8-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a05f8-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a05f8-194">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a05f8-194">Namespace</span></span><br/>                | <span data-ttu-id="a05f8-195">\\MicrosoftActiveDirectory raíz</span><span class="sxs-lookup"><span data-stu-id="a05f8-195">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="a05f8-196">MOF</span><span class="sxs-lookup"><span data-stu-id="a05f8-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a05f8-197"><dt>ReplProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a05f8-197"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="a05f8-198">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a05f8-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a05f8-199"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a05f8-199"><dt>Replprov.dll</dt></span></span> </dl> |



 

