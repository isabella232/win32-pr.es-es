---
title: Win32_TSLicenseReportPerDeviceEntry (clase)
description: Proporciona detalles acerca de la licencia de acceso de cliente por dispositivo de Servicios de Escritorio remoto con errores (RDS \ 160; CAL por dispositivo).
ms.assetid: b26f2518-439c-4562-9492-a0cfa60c457a
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportPerDeviceEntry clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSLicenseReportPerDeviceEntry de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportPerDeviceEntry
- Win32_TSLicenseReportPerDeviceEntry.sIssuedToComputer
- Win32_TSLicenseReportPerDeviceEntry.sHardwareId
- Win32_TSLicenseReportPerDeviceEntry.ExpirationDate
- Win32_TSLicenseReportPerDeviceEntry.CALType
- Win32_TSLicenseReportPerDeviceEntry.ProductVersion
- Win32_TSLicenseReportPerDeviceEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a120d477ff03675f160d94f1506f59cdf1462fa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489353"
---
# <a name="win32_tslicensereportperdeviceentry-class"></a><span data-ttu-id="70a27-105">\_Clase Win32 TSLicenseReportPerDeviceEntry</span><span class="sxs-lookup"><span data-stu-id="70a27-105">Win32\_TSLicenseReportPerDeviceEntry class</span></span>

<span data-ttu-id="70a27-106">Proporciona detalles acerca de la licencia de acceso de cliente por dispositivo de Servicios de Escritorio remoto con errores (CAL por dispositivo de RDS).</span><span class="sxs-lookup"><span data-stu-id="70a27-106">Provides details about the failed Remote Desktop Services Per Device client access license (RDS Per Device CAL).</span></span>

<span data-ttu-id="70a27-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="70a27-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a27-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70a27-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportPerDeviceEntry
{
  string   sIssuedToComputer;
  string   sHardwareId;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="70a27-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="70a27-109">Members</span></span>

<span data-ttu-id="70a27-110">La **clase \_ TSLicenseReportPerDeviceEntry de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="70a27-110">The **Win32\_TSLicenseReportPerDeviceEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="70a27-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="70a27-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70a27-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="70a27-112">Properties</span></span>

<span data-ttu-id="70a27-113">La **clase \_ TSLicenseReportPerDeviceEntry de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="70a27-113">The **Win32\_TSLicenseReportPerDeviceEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="70a27-114">**CALType**</span><span class="sxs-lookup"><span data-stu-id="70a27-114">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a27-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="70a27-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a27-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70a27-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70a27-117">Especifica el tipo de CAL emitida.</span><span class="sxs-lookup"><span data-stu-id="70a27-117">Specifies the type of CAL issued.</span></span> <span data-ttu-id="70a27-118">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="70a27-118">This will be one of the following values.</span></span>

<span data-ttu-id="70a27-119">"CAL por dispositivo de TS integrada"</span><span class="sxs-lookup"><span data-stu-id="70a27-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="70a27-120">"CAL por dispositivo de TS"</span><span class="sxs-lookup"><span data-stu-id="70a27-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="70a27-121">"CAL de conector de Internet de TS"</span><span class="sxs-lookup"><span data-stu-id="70a27-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="70a27-122">"CAL por usuario de TS"</span><span class="sxs-lookup"><span data-stu-id="70a27-122">"TS Per User CAL"</span></span>

<span data-ttu-id="70a27-123">"CAL por dispositivo de TS o RDS"</span><span class="sxs-lookup"><span data-stu-id="70a27-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="70a27-124">"CAL por usuario de TS o RDS"</span><span class="sxs-lookup"><span data-stu-id="70a27-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="70a27-125">"Licencia de suscripción por dispositivo de VDI Standard Suite"</span><span class="sxs-lookup"><span data-stu-id="70a27-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="70a27-126">"Licencia de suscripción por dispositivo de VDI Premium Suite"</span><span class="sxs-lookup"><span data-stu-id="70a27-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="70a27-127">"CAL por dispositivo de RDS"</span><span class="sxs-lookup"><span data-stu-id="70a27-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="70a27-128">"CAL por usuario de RDS"</span><span class="sxs-lookup"><span data-stu-id="70a27-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="70a27-129">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="70a27-129">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a27-130">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="70a27-130">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="70a27-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70a27-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70a27-132">Fecha de expiración de la licencia.</span><span class="sxs-lookup"><span data-stu-id="70a27-132">The expiration date of the license.</span></span>

</dd> <dt>

<span data-ttu-id="70a27-133">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="70a27-133">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a27-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="70a27-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a27-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70a27-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70a27-136">Versión de Servicios de Escritorio remoto para la que se emitió la CAL por usuario de RDS.</span><span class="sxs-lookup"><span data-stu-id="70a27-136">The version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span> <span data-ttu-id="70a27-137">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="70a27-137">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="70a27-138">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="70a27-138">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="70a27-139">En esta licencia solo se admiten servidores que ejecuten Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="70a27-139">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="70a27-140">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="70a27-140">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="70a27-141">Con esta licencia solo se admiten servidores que ejecuten Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="70a27-141">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="70a27-142">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="70a27-142">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="70a27-143">Con esta licencia solo se admiten servidores que ejecuten Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="70a27-143">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="70a27-144">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="70a27-144">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a27-145">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="70a27-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="70a27-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70a27-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70a27-147">Identificador de la versión del producto para el paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="70a27-147">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="70a27-148">4</span><span class="sxs-lookup"><span data-stu-id="70a27-148">4</span></span>
</dt> <dd>

<span data-ttu-id="70a27-149">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="70a27-149">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="70a27-150">3</span><span class="sxs-lookup"><span data-stu-id="70a27-150">3</span></span>
</dt> <dd>

<span data-ttu-id="70a27-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="70a27-151">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="70a27-152">2</span><span class="sxs-lookup"><span data-stu-id="70a27-152">2</span></span>
</dt> <dd>

<span data-ttu-id="70a27-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70a27-153">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="70a27-154">1</span><span class="sxs-lookup"><span data-stu-id="70a27-154">1</span></span>
</dt> <dd>

<span data-ttu-id="70a27-155">No se admite.</span><span class="sxs-lookup"><span data-stu-id="70a27-155">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="70a27-156">0</span><span class="sxs-lookup"><span data-stu-id="70a27-156">0</span></span>
</dt> <dd>

<span data-ttu-id="70a27-157">No se admite.</span><span class="sxs-lookup"><span data-stu-id="70a27-157">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="70a27-158">**sHardwareId**</span><span class="sxs-lookup"><span data-stu-id="70a27-158">**sHardwareId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a27-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="70a27-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a27-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70a27-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70a27-161">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="70a27-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="70a27-162">El identificador de hardware del equipo.</span><span class="sxs-lookup"><span data-stu-id="70a27-162">The hardware identifier of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="70a27-163">**sIssuedToComputer**</span><span class="sxs-lookup"><span data-stu-id="70a27-163">**sIssuedToComputer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70a27-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="70a27-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70a27-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="70a27-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="70a27-166">Nombre del equipo para el que se intentó la emisión de licencias.</span><span class="sxs-lookup"><span data-stu-id="70a27-166">The name of the computer that the license issuance was attempted for.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70a27-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70a27-167">Requirements</span></span>



| <span data-ttu-id="70a27-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="70a27-168">Requirement</span></span> | <span data-ttu-id="70a27-169">Value</span><span class="sxs-lookup"><span data-stu-id="70a27-169">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="70a27-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70a27-170">Minimum supported client</span></span><br/> | <span data-ttu-id="70a27-171">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="70a27-171">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="70a27-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70a27-172">Minimum supported server</span></span><br/> | <span data-ttu-id="70a27-173">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="70a27-173">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="70a27-174">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="70a27-174">Namespace</span></span><br/>                | <span data-ttu-id="70a27-175">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="70a27-175">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="70a27-176">MOF</span><span class="sxs-lookup"><span data-stu-id="70a27-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70a27-177"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70a27-177"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="70a27-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="70a27-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70a27-179"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70a27-179"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70a27-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="70a27-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70a27-181">**FetchReportPerDeviceEntries**</span><span class="sxs-lookup"><span data-stu-id="70a27-181">**FetchReportPerDeviceEntries**</span></span>](fetchreportperdeviceentries-win32-tslicensereport.md)
</dt> </dl>

 

