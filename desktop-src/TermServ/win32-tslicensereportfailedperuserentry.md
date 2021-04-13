---
title: Win32_TSLicenseReportFailedPerUserEntry (clase)
description: Proporciona detalles acerca de la licencia de acceso de cliente por usuario Servicios de Escritorio remoto con errores (RDS \ 160; CAL por usuario).
ms.assetid: 27d155a4-938e-4bca-8d15-03c44740e506
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportFailedPerUserEntry clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSLicenseReportFailedPerUserEntry de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserEntry
- Win32_TSLicenseReportFailedPerUserEntry.User
- Win32_TSLicenseReportFailedPerUserEntry.TriedIssuanceOn
- Win32_TSLicenseReportFailedPerUserEntry.CALType
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersion
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18098ce0510a39f6083edcf688a18c10a3e20278
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421959"
---
# <a name="win32_tslicensereportfailedperuserentry-class"></a><span data-ttu-id="da786-105">\_Clase Win32 TSLicenseReportFailedPerUserEntry</span><span class="sxs-lookup"><span data-stu-id="da786-105">Win32\_TSLicenseReportFailedPerUserEntry class</span></span>

<span data-ttu-id="da786-106">Proporciona detalles acerca de la licencia de acceso de cliente por usuario de Servicios de Escritorio remoto con errores (CAL por usuario de RDS).</span><span class="sxs-lookup"><span data-stu-id="da786-106">Provides details about the failed Remote Desktop Services Per User client access license (RDS Per User CAL).</span></span>

<span data-ttu-id="da786-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="da786-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="da786-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da786-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserEntry
{
  string   User;
  DATETIME TriedIssuanceOn;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="da786-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="da786-109">Members</span></span>

<span data-ttu-id="da786-110">La **clase \_ TSLicenseReportFailedPerUserEntry de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="da786-110">The **Win32\_TSLicenseReportFailedPerUserEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="da786-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="da786-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="da786-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="da786-112">Properties</span></span>

<span data-ttu-id="da786-113">La **clase \_ TSLicenseReportFailedPerUserEntry de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="da786-113">The **Win32\_TSLicenseReportFailedPerUserEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da786-114">**CALType**</span><span class="sxs-lookup"><span data-stu-id="da786-114">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da786-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="da786-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da786-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="da786-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da786-117">Especifica el tipo de CAL emitida.</span><span class="sxs-lookup"><span data-stu-id="da786-117">Specifies the type of CAL issued.</span></span> <span data-ttu-id="da786-118">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="da786-118">This will be one of the following values.</span></span>

<span data-ttu-id="da786-119">"CAL por dispositivo de TS integrada"</span><span class="sxs-lookup"><span data-stu-id="da786-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="da786-120">"CAL por dispositivo de TS"</span><span class="sxs-lookup"><span data-stu-id="da786-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="da786-121">"CAL de conector de Internet de TS"</span><span class="sxs-lookup"><span data-stu-id="da786-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="da786-122">"CAL por usuario de TS"</span><span class="sxs-lookup"><span data-stu-id="da786-122">"TS Per User CAL"</span></span>

<span data-ttu-id="da786-123">"CAL por dispositivo de TS o RDS"</span><span class="sxs-lookup"><span data-stu-id="da786-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="da786-124">"CAL por usuario de TS o RDS"</span><span class="sxs-lookup"><span data-stu-id="da786-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="da786-125">"Licencia de suscripción por dispositivo de VDI Standard Suite"</span><span class="sxs-lookup"><span data-stu-id="da786-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="da786-126">"Licencia de suscripción por dispositivo de VDI Premium Suite"</span><span class="sxs-lookup"><span data-stu-id="da786-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="da786-127">"CAL por dispositivo de RDS"</span><span class="sxs-lookup"><span data-stu-id="da786-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="da786-128">"CAL por usuario de RDS"</span><span class="sxs-lookup"><span data-stu-id="da786-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="da786-129">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="da786-129">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da786-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="da786-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da786-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="da786-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da786-132">Versión de Servicios de Escritorio remoto para la que se emitió la CAL por usuario de RDS.</span><span class="sxs-lookup"><span data-stu-id="da786-132">The version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span> <span data-ttu-id="da786-133">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="da786-133">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="da786-134">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="da786-134">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="da786-135">En esta licencia solo se admiten servidores que ejecuten Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="da786-135">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="da786-136">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="da786-136">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="da786-137">Con esta licencia solo se admiten servidores que ejecuten Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="da786-137">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="da786-138">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="da786-138">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="da786-139">Con esta licencia solo se admiten servidores que ejecuten Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="da786-139">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="da786-140">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="da786-140">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da786-141">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da786-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da786-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="da786-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da786-143">Identificador de la versión del producto para el paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="da786-143">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="da786-144">4</span><span class="sxs-lookup"><span data-stu-id="da786-144">4</span></span>
</dt> <dd>

<span data-ttu-id="da786-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="da786-145">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="da786-146">3</span><span class="sxs-lookup"><span data-stu-id="da786-146">3</span></span>
</dt> <dd>

<span data-ttu-id="da786-147">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="da786-147">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="da786-148">2</span><span class="sxs-lookup"><span data-stu-id="da786-148">2</span></span>
</dt> <dd>

<span data-ttu-id="da786-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da786-149">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="da786-150">1</span><span class="sxs-lookup"><span data-stu-id="da786-150">1</span></span>
</dt> <dd>

<span data-ttu-id="da786-151">No se admite.</span><span class="sxs-lookup"><span data-stu-id="da786-151">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="da786-152">0</span><span class="sxs-lookup"><span data-stu-id="da786-152">0</span></span>
</dt> <dd>

<span data-ttu-id="da786-153">No se admite.</span><span class="sxs-lookup"><span data-stu-id="da786-153">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="da786-154">**TriedIssuanceOn**</span><span class="sxs-lookup"><span data-stu-id="da786-154">**TriedIssuanceOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da786-155">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="da786-155">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="da786-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="da786-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da786-157">La fecha en la que se intentó la emisión de la licencia.</span><span class="sxs-lookup"><span data-stu-id="da786-157">The date on which license issuance was attempted.</span></span>

</dd> <dt>

<span data-ttu-id="da786-158">**User**</span><span class="sxs-lookup"><span data-stu-id="da786-158">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da786-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="da786-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da786-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="da786-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da786-161">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="da786-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="da786-162">Nombre del usuario al que se ha intentado emitir la licencia.</span><span class="sxs-lookup"><span data-stu-id="da786-162">The name of the user to whom the license issuance was attempted.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da786-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da786-163">Requirements</span></span>



| <span data-ttu-id="da786-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="da786-164">Requirement</span></span> | <span data-ttu-id="da786-165">Value</span><span class="sxs-lookup"><span data-stu-id="da786-165">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="da786-166">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da786-166">Minimum supported client</span></span><br/> | <span data-ttu-id="da786-167">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="da786-167">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="da786-168">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da786-168">Minimum supported server</span></span><br/> | <span data-ttu-id="da786-169">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="da786-169">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="da786-170">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="da786-170">Namespace</span></span><br/>                | <span data-ttu-id="da786-171">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="da786-171">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="da786-172">MOF</span><span class="sxs-lookup"><span data-stu-id="da786-172">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da786-173"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da786-173"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="da786-174">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="da786-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da786-175"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da786-175"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da786-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="da786-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da786-177">**FetchReportFailedPerUserEntries**</span><span class="sxs-lookup"><span data-stu-id="da786-177">**FetchReportFailedPerUserEntries**</span></span>](fetchreportfailedperuserentries-win32-tslicensereport.md)
</dt> </dl>

 

