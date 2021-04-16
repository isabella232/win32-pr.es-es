---
title: Win32_TSIssuedLicense (clase)
description: Describe las instancias de Servicios de Escritorio remoto licencias de acceso de cliente por dispositivo (RDS \ 160; Cal por dispositivo) que se emiten desde un servidor de licencias de Escritorio remoto.
ms.assetid: 15825dc5-9ada-4c11-ac77-beb681e9b33c
ms.tgt_platform: multiple
keywords:
- Win32_TSIssuedLicense clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSIssuedLicense de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense
- Win32_TSIssuedLicense.LicenseId
- Win32_TSIssuedLicense.KeyPackId
- Win32_TSIssuedLicense.sIssuedToUser
- Win32_TSIssuedLicense.sIssuedToComputer
- Win32_TSIssuedLicense.LicenseStatus
- Win32_TSIssuedLicense.IssueDate
- Win32_TSIssuedLicense.ExpirationDate
- Win32_TSIssuedLicense.sHardwareId
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c3d08a68ddcc15a912de4c674403928211a297e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685996"
---
# <a name="win32_tsissuedlicense-class"></a><span data-ttu-id="7f292-105">\_Clase Win32 TSIssuedLicense</span><span class="sxs-lookup"><span data-stu-id="7f292-105">Win32\_TSIssuedLicense class</span></span>

<span data-ttu-id="7f292-106">Describe las instancias de Servicios de Escritorio remoto licencias de acceso de cliente por dispositivo (cal por dispositivo de RDS) que se emiten desde un servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="7f292-106">Describes instances of Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) that are issued from a Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f292-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f292-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSIssuedLicense
{
  uint32   LicenseId;
  uint32   KeyPackId;
  string   sIssuedToUser;
  string   sIssuedToComputer;
  uint32   LicenseStatus;
  DATETIME IssueDate;
  DATETIME ExpirationDate;
  string   sHardwareId;
};
```

## <a name="members"></a><span data-ttu-id="7f292-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7f292-108">Members</span></span>

<span data-ttu-id="7f292-109">La **clase \_ TSIssuedLicense de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7f292-109">The **Win32\_TSIssuedLicense** class has these types of members:</span></span>

-   [<span data-ttu-id="7f292-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="7f292-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="7f292-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7f292-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7f292-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="7f292-112">Methods</span></span>

<span data-ttu-id="7f292-113">La clase **Win32 \_ TSIssuedLicense** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7f292-113">The **Win32\_TSIssuedLicense** class has these methods.</span></span>



| <span data-ttu-id="7f292-114">Método</span><span class="sxs-lookup"><span data-stu-id="7f292-114">Method</span></span>                                         | <span data-ttu-id="7f292-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7f292-115">Description</span></span>                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f292-116">**Revocar**</span><span class="sxs-lookup"><span data-stu-id="7f292-116">**Revoke**</span></span>](revoke-win32-tsissuedlicense.md) | <span data-ttu-id="7f292-117">Revoca las cal por dispositivo de RDS representadas por el **objeto \_ TSIssuedLicense de Win32** .</span><span class="sxs-lookup"><span data-stu-id="7f292-117">Revokes the RDS Per Device CALs that are represented by the **Win32\_TSIssuedLicense** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7f292-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7f292-118">Properties</span></span>

<span data-ttu-id="7f292-119">La **clase \_ TSIssuedLicense de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7f292-119">The **Win32\_TSIssuedLicense** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7f292-120">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="7f292-120">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f292-121">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7f292-121">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="7f292-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7f292-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f292-123">Identifica la fecha en la que expirará la licencia.</span><span class="sxs-lookup"><span data-stu-id="7f292-123">Identifies the date that the license will expire.</span></span>

</dd> <dt>

<span data-ttu-id="7f292-124">**IssueDate**</span><span class="sxs-lookup"><span data-stu-id="7f292-124">**IssueDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f292-125">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7f292-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="7f292-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7f292-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f292-127">Identifica la fecha en la que se emitió la licencia.</span><span class="sxs-lookup"><span data-stu-id="7f292-127">Identifies the date that the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="7f292-128">**KeyPackId**</span><span class="sxs-lookup"><span data-stu-id="7f292-128">**KeyPackId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f292-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f292-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f292-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7f292-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f292-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7f292-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7f292-132">Identifica el paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="7f292-132">Identifies the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="7f292-133">**LicenseId**</span><span class="sxs-lookup"><span data-stu-id="7f292-133">**LicenseId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f292-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f292-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f292-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7f292-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f292-136">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7f292-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7f292-137">Identificador único para esta licencia.</span><span class="sxs-lookup"><span data-stu-id="7f292-137">Unique identifier for this license.</span></span>

</dd> <dt>

<span data-ttu-id="7f292-138">**Estado de la licencia**</span><span class="sxs-lookup"><span data-stu-id="7f292-138">**LicenseStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f292-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f292-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f292-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7f292-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f292-141">Estado de la licencia.</span><span class="sxs-lookup"><span data-stu-id="7f292-141">Status of the license.</span></span>

<dt>

<span data-ttu-id="7f292-142">0</span><span class="sxs-lookup"><span data-stu-id="7f292-142">0</span></span>
</dt> <dd>

<span data-ttu-id="7f292-143">Se desconoce el estado de la licencia.</span><span class="sxs-lookup"><span data-stu-id="7f292-143">The license status is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="7f292-144">1</span><span class="sxs-lookup"><span data-stu-id="7f292-144">1</span></span>
</dt> <dd>

<span data-ttu-id="7f292-145">La licencia es una licencia temporal.</span><span class="sxs-lookup"><span data-stu-id="7f292-145">The license is a temporary license.</span></span>

</dd> <dt>

<span data-ttu-id="7f292-146">2</span><span class="sxs-lookup"><span data-stu-id="7f292-146">2</span></span>
</dt> <dd>

<span data-ttu-id="7f292-147">La licencia está activa.</span><span class="sxs-lookup"><span data-stu-id="7f292-147">The license is active.</span></span>

</dd> <dt>

<span data-ttu-id="7f292-148">3</span><span class="sxs-lookup"><span data-stu-id="7f292-148">3</span></span>
</dt> <dd>

<span data-ttu-id="7f292-149">La licencia es una licencia de actualización.</span><span class="sxs-lookup"><span data-stu-id="7f292-149">The license is an upgrade license.</span></span>

</dd> <dt>

<span data-ttu-id="7f292-150">4</span><span class="sxs-lookup"><span data-stu-id="7f292-150">4</span></span>
</dt> <dd>

<span data-ttu-id="7f292-151">La licencia se ha revocado.</span><span class="sxs-lookup"><span data-stu-id="7f292-151">The license has been revoked.</span></span>

</dd> <dt>

<span data-ttu-id="7f292-152">5</span><span class="sxs-lookup"><span data-stu-id="7f292-152">5</span></span>
</dt> <dd>

<span data-ttu-id="7f292-153">El estado de la licencia es pendiente.</span><span class="sxs-lookup"><span data-stu-id="7f292-153">The license status is pending.</span></span>

</dd> <dt>

<span data-ttu-id="7f292-154">6</span><span class="sxs-lookup"><span data-stu-id="7f292-154">6</span></span>
</dt> <dd>

<span data-ttu-id="7f292-155">La licencia es una licencia simultánea.</span><span class="sxs-lookup"><span data-stu-id="7f292-155">The license is a concurrent license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f292-156">**sHardwareId**</span><span class="sxs-lookup"><span data-stu-id="7f292-156">**sHardwareId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f292-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7f292-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f292-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7f292-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f292-159">Identificador de hardware para el que se emitió la licencia.</span><span class="sxs-lookup"><span data-stu-id="7f292-159">Hardware identifier for which the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="7f292-160">**sIssuedToComputer**</span><span class="sxs-lookup"><span data-stu-id="7f292-160">**sIssuedToComputer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f292-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7f292-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f292-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7f292-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f292-163">Nombre del equipo para el que se emitió la licencia.</span><span class="sxs-lookup"><span data-stu-id="7f292-163">Computer name for which the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="7f292-164">**sIssuedToUser**</span><span class="sxs-lookup"><span data-stu-id="7f292-164">**sIssuedToUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f292-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7f292-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f292-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7f292-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f292-167">Nombre de usuario para el que se emitió la licencia.</span><span class="sxs-lookup"><span data-stu-id="7f292-167">User name for which the license was issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f292-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f292-168">Remarks</span></span>

<span data-ttu-id="7f292-169">Para usar esta clase, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="7f292-169">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="7f292-170">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7f292-170">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7f292-171">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7f292-171">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7f292-172">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="7f292-172">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7f292-173">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7f292-173">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f292-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f292-174">Requirements</span></span>



| <span data-ttu-id="7f292-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f292-175">Requirement</span></span> | <span data-ttu-id="7f292-176">Value</span><span class="sxs-lookup"><span data-stu-id="7f292-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f292-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f292-177">Minimum supported client</span></span><br/> | <span data-ttu-id="7f292-178">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7f292-178">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="7f292-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f292-179">Minimum supported server</span></span><br/> | <span data-ttu-id="7f292-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f292-180">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="7f292-181">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7f292-181">Namespace</span></span><br/>                | <span data-ttu-id="7f292-182">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="7f292-182">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="7f292-183">MOF</span><span class="sxs-lookup"><span data-stu-id="7f292-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f292-184"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f292-184"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f292-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7f292-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f292-186"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f292-186"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f292-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f292-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f292-188">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="7f292-188">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="7f292-189">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="7f292-189">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="7f292-190">**Win32 \_ TSLicenseReportEntry**</span><span class="sxs-lookup"><span data-stu-id="7f292-190">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="7f292-191">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="7f292-191">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

