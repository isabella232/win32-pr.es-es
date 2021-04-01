---
title: Win32_TSLicenseReport (clase)
description: Proporciona instancias de Servicios de Escritorio remoto licencia de acceso de cliente por usuario (RDS \ 160; Los informes de uso de CAL por usuario) que se generan en el servidor de licencias de Escritorio remoto, y métodos para las operaciones de generación, recuperación y eliminación de informes de licencias.
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReport clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSLicenseReport de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport
- Win32_TSLicenseReport.FileName
- Win32_TSLicenseReport.LicenseUsageCount
- Win32_TSLicenseReport.InstalledLicenses
- Win32_TSLicenseReport.GenerationDateTime
- Win32_TSLicenseReport.ScopeType
- Win32_TSLicenseReport.ScopeValue
- Win32_TSLicenseReport.Version
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de997056222c1b525253f320f6fe191f017614f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905046"
---
# <a name="win32_tslicensereport-class"></a><span data-ttu-id="fe31e-105">\_Clase Win32 TSLicenseReport</span><span class="sxs-lookup"><span data-stu-id="fe31e-105">Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="fe31e-106">Proporciona instancias de Servicios de Escritorio remoto informes de uso de licencias de acceso de cliente por usuario (CAL por usuario de RDS) que se generan en el servidor de licencias de Escritorio remoto y métodos para la generación de informes de licencias, la recuperación y las operaciones de eliminación.</span><span class="sxs-lookup"><span data-stu-id="fe31e-106">Provides instances of Remote Desktop Services Per User client access license (RDS Per User CAL) usage reports that are generated on the Remote Desktop license server, and methods for license report generation, fetch, and delete operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe31e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe31e-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseReport
{
  string   FileName;
  uint32   LicenseUsageCount;
  uint32   InstalledLicenses;
  DATETIME GenerationDateTime;
  uint32   ScopeType;
  string   ScopeValue;
  uint32   Version;
};
```

## <a name="members"></a><span data-ttu-id="fe31e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="fe31e-108">Members</span></span>

<span data-ttu-id="fe31e-109">La **clase \_ TSLicenseReport de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fe31e-109">The **Win32\_TSLicenseReport** class has these types of members:</span></span>

-   [<span data-ttu-id="fe31e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="fe31e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="fe31e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fe31e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fe31e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="fe31e-112">Methods</span></span>

<span data-ttu-id="fe31e-113">La clase **Win32 \_ TSLicenseReport** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fe31e-113">The **Win32\_TSLicenseReport** class has these methods.</span></span>



| <span data-ttu-id="fe31e-114">Método</span><span class="sxs-lookup"><span data-stu-id="fe31e-114">Method</span></span>                                                                                                         | <span data-ttu-id="fe31e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe31e-115">Description</span></span>                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe31e-116">**DeleteReport**</span><span class="sxs-lookup"><span data-stu-id="fe31e-116">**DeleteReport**</span></span>](deletereport-win32-tslicensereport.md)                                                     | <span data-ttu-id="fe31e-117">Elimina un objeto de informe en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fe31e-117">Deletes a report object on the Remote Desktop license server.</span></span> <span data-ttu-id="fe31e-118">No es un método estático.</span><span class="sxs-lookup"><span data-stu-id="fe31e-118">This is not a static method.</span></span><br/>                                                                                           |
| [<span data-ttu-id="fe31e-119">**FetchReportEntries**</span><span class="sxs-lookup"><span data-stu-id="fe31e-119">**FetchReportEntries**</span></span>](fetchreportentries-win32-tslicensereport.md)                                         | <span data-ttu-id="fe31e-120">Recupera entradas en el objeto de informe.</span><span class="sxs-lookup"><span data-stu-id="fe31e-120">Retrieves entries in the report object.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="fe31e-121">**FetchReportFailedPerUserEntries**</span><span class="sxs-lookup"><span data-stu-id="fe31e-121">**FetchReportFailedPerUserEntries**</span></span>](fetchreportfailedperuserentries-win32-tslicensereport.md)               | <span data-ttu-id="fe31e-122">Recupera los detalles de las licencias de acceso de cliente por usuario (cal por usuario de RDS) con Servicios de Escritorio remoto error en el informe.</span><span class="sxs-lookup"><span data-stu-id="fe31e-122">Retrieves details of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span><br/>                                                             |
| [<span data-ttu-id="fe31e-123">**FetchReportFailedPerUserSummaryEntries**</span><span class="sxs-lookup"><span data-stu-id="fe31e-123">**FetchReportFailedPerUserSummaryEntries**</span></span>](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | <span data-ttu-id="fe31e-124">Recupera información de Resumen de las licencias de acceso de cliente por usuario de Servicios de Escritorio remoto con errores (cal por usuario de RDS) del informe.</span><span class="sxs-lookup"><span data-stu-id="fe31e-124">Retrieves summary information of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span><br/>                                                 |
| [<span data-ttu-id="fe31e-125">**FetchReportPerDeviceEntries**</span><span class="sxs-lookup"><span data-stu-id="fe31e-125">**FetchReportPerDeviceEntries**</span></span>](fetchreportperdeviceentries-win32-tslicensereport.md)                       | <span data-ttu-id="fe31e-126">Recupera la información de las licencias de acceso de cliente por dispositivo de Servicios de Escritorio remoto emitidas (cal por dispositivo de RDS) del informe.</span><span class="sxs-lookup"><span data-stu-id="fe31e-126">Retrieves information of issued Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) from the report.</span></span><br/>                                                     |
| [<span data-ttu-id="fe31e-127">**FetchReportSummaryEntries**</span><span class="sxs-lookup"><span data-stu-id="fe31e-127">**FetchReportSummaryEntries**</span></span>](win32-tslicensereport-fetchreportsummaryentries.md)                           | <span data-ttu-id="fe31e-128">Recupera los resúmenes de licencia del objeto de informe.</span><span class="sxs-lookup"><span data-stu-id="fe31e-128">Retrieves license summaries from the report object.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="fe31e-129">**GenerateReport**</span><span class="sxs-lookup"><span data-stu-id="fe31e-129">**GenerateReport**</span></span>](generatereport-win32-tslicensereport.md)                                                 | <span data-ttu-id="fe31e-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="fe31e-130">This method is not supported.</span></span><br/> <span data-ttu-id="fe31e-131">**Windows server 2008 R2 y Windows server 2008:** Genera un informe de uso de licencias por usuario actual en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fe31e-131">**Windows Server 2008 R2 and Windows Server 2008:** Generates a current per user license usage report on the Remote Desktop license server.</span></span><br/> |
| [<span data-ttu-id="fe31e-132">**GenerateReportEx**</span><span class="sxs-lookup"><span data-stu-id="fe31e-132">**GenerateReportEx**</span></span>](generatereportex-win32-tslicensereport.md)                                             | <span data-ttu-id="fe31e-133">Genera un informe de uso de licencias por usuario actual en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fe31e-133">Generates a current per user license usage report on the Remote Desktop license server.</span></span><br/>                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="fe31e-134">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fe31e-134">Properties</span></span>

<span data-ttu-id="fe31e-135">La **clase \_ TSLicenseReport de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fe31e-135">The **Win32\_TSLicenseReport** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe31e-136">**FileName**</span><span class="sxs-lookup"><span data-stu-id="fe31e-136">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe31e-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fe31e-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe31e-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fe31e-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe31e-139">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fe31e-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fe31e-140">Nombre del informe.</span><span class="sxs-lookup"><span data-stu-id="fe31e-140">The report name.</span></span>

</dd> <dt>

<span data-ttu-id="fe31e-141">**GenerationDateTime**</span><span class="sxs-lookup"><span data-stu-id="fe31e-141">**GenerationDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe31e-142">Tipo de datos: **[DateTime](/windows/desktop/WmiSdk/datetime)**</span><span class="sxs-lookup"><span data-stu-id="fe31e-142">Data type: **[DATETIME](/windows/desktop/WmiSdk/datetime)**</span></span>
</dt> <dt>

<span data-ttu-id="fe31e-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fe31e-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe31e-144">Fecha y hora de generación de informes de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fe31e-144">RD Licensing report generation date and time.</span></span>

</dd> <dt>

<span data-ttu-id="fe31e-145">**InstalledLicenses**</span><span class="sxs-lookup"><span data-stu-id="fe31e-145">**InstalledLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe31e-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fe31e-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe31e-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fe31e-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe31e-148">Calificadores: [ **desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fe31e-148">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fe31e-149">Esta propiedad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="fe31e-149">This property is not supported.</span></span>

<span data-ttu-id="fe31e-150">**Windows server 2008 R2 y Windows server 2008:** Número de cal por usuario de RDS instaladas.</span><span class="sxs-lookup"><span data-stu-id="fe31e-150">**Windows Server 2008 R2 and Windows Server 2008:** Number of RDS Per User CALs that are installed.</span></span>

</dd> <dt>

<span data-ttu-id="fe31e-151">**LicenseUsageCount**</span><span class="sxs-lookup"><span data-stu-id="fe31e-151">**LicenseUsageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe31e-152">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fe31e-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe31e-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fe31e-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe31e-154">Calificadores: [ **desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fe31e-154">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fe31e-155">Esta propiedad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="fe31e-155">This property is not supported.</span></span>

<span data-ttu-id="fe31e-156">**Windows server 2008 R2 y Windows server 2008:** Número de cal por usuario de RDS que están actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="fe31e-156">**Windows Server 2008 R2 and Windows Server 2008:** Number of RDS Per User CALs that are currently in use.</span></span>

</dd> <dt>

<span data-ttu-id="fe31e-157">**ScopeType**</span><span class="sxs-lookup"><span data-stu-id="fe31e-157">**ScopeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe31e-158">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fe31e-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe31e-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fe31e-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe31e-160">Calificadores: [ **desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fe31e-160">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fe31e-161">Esta propiedad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="fe31e-161">This property is not supported.</span></span>

<span data-ttu-id="fe31e-162">**Windows server 2008 R2 y Windows server 2008:** Tipo de ámbito de informe de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fe31e-162">**Windows Server 2008 R2 and Windows Server 2008:** RD Licensing report scope type.</span></span>

</dd> <dt>

<span data-ttu-id="fe31e-163">**ScopeValue**</span><span class="sxs-lookup"><span data-stu-id="fe31e-163">**ScopeValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe31e-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fe31e-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe31e-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fe31e-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe31e-166">Calificadores: [ **desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fe31e-166">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fe31e-167">Esta propiedad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="fe31e-167">This property is not supported.</span></span>

<span data-ttu-id="fe31e-168">**Windows server 2008 R2 y Windows server 2008:** Valor de ámbito del informe de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fe31e-168">**Windows Server 2008 R2 and Windows Server 2008:** RD Licensing report scope value.</span></span>

</dd> <dt>

<span data-ttu-id="fe31e-169">**Versión**</span><span class="sxs-lookup"><span data-stu-id="fe31e-169">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe31e-170">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fe31e-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fe31e-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fe31e-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe31e-172">Versión del informe de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fe31e-172">RD Licensing report version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe31e-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe31e-173">Remarks</span></span>

<span data-ttu-id="fe31e-174">Los informes que se generan mediante WMI se muestran en el administrador de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fe31e-174">Reports that are generated by using WMI are displayed in RD Licensing Manager.</span></span> <span data-ttu-id="fe31e-175">Los informes que se eliminan mediante WMI también se eliminan del administrador de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fe31e-175">Reports that are deleted by using WMI are also deleted from RD Licensing Manager.</span></span>

<span data-ttu-id="fe31e-176">Para usar esta clase, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="fe31e-176">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="fe31e-177">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fe31e-177">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fe31e-178">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fe31e-178">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fe31e-179">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="fe31e-179">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fe31e-180">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fe31e-180">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe31e-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe31e-181">Requirements</span></span>



| <span data-ttu-id="fe31e-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe31e-182">Requirement</span></span> | <span data-ttu-id="fe31e-183">Value</span><span class="sxs-lookup"><span data-stu-id="fe31e-183">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe31e-184">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe31e-184">Minimum supported client</span></span><br/> | <span data-ttu-id="fe31e-185">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fe31e-185">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="fe31e-186">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe31e-186">Minimum supported server</span></span><br/> | <span data-ttu-id="fe31e-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe31e-187">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="fe31e-188">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fe31e-188">Namespace</span></span><br/>                | <span data-ttu-id="fe31e-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="fe31e-189">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="fe31e-190">MOF</span><span class="sxs-lookup"><span data-stu-id="fe31e-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe31e-191"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe31e-191"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe31e-192">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fe31e-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe31e-193"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe31e-193"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe31e-194">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe31e-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe31e-195">**Win32 \_ TSIssuedLicense**</span><span class="sxs-lookup"><span data-stu-id="fe31e-195">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="fe31e-196">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="fe31e-196">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="fe31e-197">**Win32 \_ TSLicenseReportEntry**</span><span class="sxs-lookup"><span data-stu-id="fe31e-197">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="fe31e-198">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="fe31e-198">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

