---
title: Win32_TSLicenseReportEntry (clase)
description: Proporciona detalles de la licencia de acceso de cliente por usuario Servicios de Escritorio remoto emitida (RDS \ 160; CAL por usuario).
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportEntry clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSLicenseReportEntry de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportEntry
- Win32_TSLicenseReportEntry.User
- Win32_TSLicenseReportEntry.ExpirationDate
- Win32_TSLicenseReportEntry.CALType
- Win32_TSLicenseReportEntry.ProductVersion
- Win32_TSLicenseReportEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44fa97a91561a9d4cf3fd571c773288796754858
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421960"
---
# <a name="win32_tslicensereportentry-class"></a><span data-ttu-id="f33b4-105">\_Clase Win32 TSLicenseReportEntry</span><span class="sxs-lookup"><span data-stu-id="f33b4-105">Win32\_TSLicenseReportEntry class</span></span>

<span data-ttu-id="f33b4-106">Proporciona detalles de la licencia de acceso de cliente por usuario de Servicios de Escritorio remoto emitida (CAL por usuario de RDS).</span><span class="sxs-lookup"><span data-stu-id="f33b4-106">Provides details of the issued Remote Desktop Services Per User client access license (RDS Per User CAL).</span></span>

## <a name="syntax"></a><span data-ttu-id="f33b4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f33b4-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportEntry
{
  string   User;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="f33b4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f33b4-108">Members</span></span>

<span data-ttu-id="f33b4-109">La **clase \_ TSLicenseReportEntry de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f33b4-109">The **Win32\_TSLicenseReportEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="f33b4-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f33b4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f33b4-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f33b4-111">Properties</span></span>

<span data-ttu-id="f33b4-112">La **clase \_ TSLicenseReportEntry de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f33b4-112">The **Win32\_TSLicenseReportEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f33b4-113">**CALType**</span><span class="sxs-lookup"><span data-stu-id="f33b4-113">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f33b4-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f33b4-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f33b4-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f33b4-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f33b4-116">Especifica el tipo de CAL emitida.</span><span class="sxs-lookup"><span data-stu-id="f33b4-116">Specifies the type of CAL issued.</span></span> <span data-ttu-id="f33b4-117">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f33b4-117">This will be one of the following values.</span></span>

<span data-ttu-id="f33b4-118">**Windows server 2008 R2 y Windows server 2008:** Esta propiedad no se admite.</span><span class="sxs-lookup"><span data-stu-id="f33b4-118">**Windows Server 2008 R2 and Windows Server 2008:** This property is not supported.</span></span>

<span data-ttu-id="f33b4-119">"CAL por dispositivo de TS integrada"</span><span class="sxs-lookup"><span data-stu-id="f33b4-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="f33b4-120">"CAL por dispositivo de TS"</span><span class="sxs-lookup"><span data-stu-id="f33b4-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="f33b4-121">"CAL de conector de Internet de TS"</span><span class="sxs-lookup"><span data-stu-id="f33b4-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="f33b4-122">"CAL por usuario de TS"</span><span class="sxs-lookup"><span data-stu-id="f33b4-122">"TS Per User CAL"</span></span>

<span data-ttu-id="f33b4-123">"CAL por dispositivo de TS o RDS"</span><span class="sxs-lookup"><span data-stu-id="f33b4-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="f33b4-124">"CAL por usuario de TS o RDS"</span><span class="sxs-lookup"><span data-stu-id="f33b4-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="f33b4-125">"Licencia de suscripción por dispositivo de VDI Standard Suite"</span><span class="sxs-lookup"><span data-stu-id="f33b4-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="f33b4-126">"Licencia de suscripción por dispositivo de VDI Premium Suite"</span><span class="sxs-lookup"><span data-stu-id="f33b4-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="f33b4-127">"CAL por dispositivo de RDS"</span><span class="sxs-lookup"><span data-stu-id="f33b4-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="f33b4-128">"CAL por usuario de RDS"</span><span class="sxs-lookup"><span data-stu-id="f33b4-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="f33b4-129">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="f33b4-129">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f33b4-130">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f33b4-130">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="f33b4-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f33b4-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f33b4-132">Fecha de expiración de la licencia que se emitió para el usuario.</span><span class="sxs-lookup"><span data-stu-id="f33b4-132">Expiration date of the license that was issued to the user.</span></span>

</dd> <dt>

<span data-ttu-id="f33b4-133">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="f33b4-133">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f33b4-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f33b4-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f33b4-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f33b4-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f33b4-136">Versión de Servicios de Escritorio remoto para la que se emitió la CAL por usuario de RDS.</span><span class="sxs-lookup"><span data-stu-id="f33b4-136">Version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span>

<dt>

<span data-ttu-id="f33b4-137">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="f33b4-137">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="f33b4-138">En esta licencia solo se admiten servidores que ejecuten Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f33b4-138">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="f33b4-139">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="f33b4-139">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="f33b4-140">Con esta licencia solo se admiten servidores que ejecuten Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f33b4-140">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="f33b4-141">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="f33b4-141">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="f33b4-142">Con esta licencia solo se admiten servidores que ejecuten Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f33b4-142">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f33b4-143">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="f33b4-143">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f33b4-144">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f33b4-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f33b4-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f33b4-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f33b4-146">Identificador de la versión del producto para el paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f33b4-146">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="f33b4-147">4</span><span class="sxs-lookup"><span data-stu-id="f33b4-147">4</span></span>
</dt> <dd>

<span data-ttu-id="f33b4-148">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f33b4-148">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="f33b4-149">3</span><span class="sxs-lookup"><span data-stu-id="f33b4-149">3</span></span>
</dt> <dd>

<span data-ttu-id="f33b4-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f33b4-150">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="f33b4-151">2</span><span class="sxs-lookup"><span data-stu-id="f33b4-151">2</span></span>
</dt> <dd>

<span data-ttu-id="f33b4-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f33b4-152">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="f33b4-153">1</span><span class="sxs-lookup"><span data-stu-id="f33b4-153">1</span></span>
</dt> <dd>

<span data-ttu-id="f33b4-154">No se admite.</span><span class="sxs-lookup"><span data-stu-id="f33b4-154">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f33b4-155">0</span><span class="sxs-lookup"><span data-stu-id="f33b4-155">0</span></span>
</dt> <dd>

<span data-ttu-id="f33b4-156">No se admite.</span><span class="sxs-lookup"><span data-stu-id="f33b4-156">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f33b4-157">**User**</span><span class="sxs-lookup"><span data-stu-id="f33b4-157">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f33b4-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f33b4-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f33b4-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f33b4-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f33b4-160">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f33b4-160">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f33b4-161">Nombre del usuario al que se emitió la licencia.</span><span class="sxs-lookup"><span data-stu-id="f33b4-161">Name of the user to whom the license was issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f33b4-162">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f33b4-162">Remarks</span></span>

<span data-ttu-id="f33b4-163">Para usar esta clase, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="f33b4-163">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="f33b4-164">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f33b4-164">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f33b4-165">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f33b4-165">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f33b4-166">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="f33b4-166">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f33b4-167">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f33b4-167">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f33b4-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f33b4-168">Requirements</span></span>



| <span data-ttu-id="f33b4-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="f33b4-169">Requirement</span></span> | <span data-ttu-id="f33b4-170">Value</span><span class="sxs-lookup"><span data-stu-id="f33b4-170">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f33b4-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f33b4-171">Minimum supported client</span></span><br/> | <span data-ttu-id="f33b4-172">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f33b4-172">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f33b4-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f33b4-173">Minimum supported server</span></span><br/> | <span data-ttu-id="f33b4-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f33b4-174">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f33b4-175">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f33b4-175">Namespace</span></span><br/>                | <span data-ttu-id="f33b4-176">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f33b4-176">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f33b4-177">MOF</span><span class="sxs-lookup"><span data-stu-id="f33b4-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f33b4-178"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f33b4-178"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f33b4-179">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f33b4-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f33b4-180"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f33b4-180"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f33b4-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="f33b4-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f33b4-182">**FetchReportEntries**</span><span class="sxs-lookup"><span data-stu-id="f33b4-182">**FetchReportEntries**</span></span>](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="f33b4-183">**Win32 \_ TSIssuedLicense**</span><span class="sxs-lookup"><span data-stu-id="f33b4-183">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="f33b4-184">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="f33b4-184">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="f33b4-185">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="f33b4-185">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="f33b4-186">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="f33b4-186">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

