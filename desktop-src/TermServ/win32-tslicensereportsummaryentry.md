---
title: Win32_TSLicenseReportSummaryEntry (clase)
description: Proporciona un resumen de las licencias de acceso de cliente de los Servicios de Escritorio remoto instalados y emitidos por usuario (RDS \ 160; Cal por usuario).
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportSummaryEntry clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSLicenseReportSummaryEntry de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportSummaryEntry
- Win32_TSLicenseReportSummaryEntry.ProductVersion
- Win32_TSLicenseReportSummaryEntry.ProductVersionID
- Win32_TSLicenseReportSummaryEntry.TSCALType
- Win32_TSLicenseReportSummaryEntry.InstalledLicenses
- Win32_TSLicenseReportSummaryEntry.IssuedLicenses
- Win32_TSLicenseReportSummaryEntry.TSCALAvailability
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34482e9c6199ef6586024d43d586421a54071ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676579"
---
# <a name="win32_tslicensereportsummaryentry-class"></a><span data-ttu-id="cec3b-105">\_Clase Win32 TSLicenseReportSummaryEntry</span><span class="sxs-lookup"><span data-stu-id="cec3b-105">Win32\_TSLicenseReportSummaryEntry class</span></span>

<span data-ttu-id="cec3b-106">Proporciona un resumen de las licencias de acceso de cliente de los Servicios de Escritorio remoto instalados y emitidos por usuario (cal por usuario de RDS).</span><span class="sxs-lookup"><span data-stu-id="cec3b-106">Provides a summary of the installed and issued Remote Desktop Services Per User client access licenses (RDS Per User CALs).</span></span>

## <a name="syntax"></a><span data-ttu-id="cec3b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cec3b-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportSummaryEntry
{
  string ProductVersion;
  uint32 ProductVersionID;
  string TSCALType;
  uint32 InstalledLicenses;
  uint32 IssuedLicenses;
  string TSCALAvailability;
};
```

## <a name="members"></a><span data-ttu-id="cec3b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="cec3b-108">Members</span></span>

<span data-ttu-id="cec3b-109">La **clase \_ TSLicenseReportSummaryEntry de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cec3b-109">The **Win32\_TSLicenseReportSummaryEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="cec3b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cec3b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cec3b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cec3b-111">Properties</span></span>

<span data-ttu-id="cec3b-112">La **clase \_ TSLicenseReportSummaryEntry de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cec3b-112">The **Win32\_TSLicenseReportSummaryEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cec3b-113">**InstalledLicenses**</span><span class="sxs-lookup"><span data-stu-id="cec3b-113">**InstalledLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec3b-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cec3b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cec3b-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cec3b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cec3b-116">Número de cal por usuario de RDS instaladas.</span><span class="sxs-lookup"><span data-stu-id="cec3b-116">Number of RDS Per User CALs that are installed.</span></span>

</dd> <dt>

<span data-ttu-id="cec3b-117">**IssuedLicenses**</span><span class="sxs-lookup"><span data-stu-id="cec3b-117">**IssuedLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec3b-118">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cec3b-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cec3b-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cec3b-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cec3b-120">Número de cal por usuario de RDS que se emiten.</span><span class="sxs-lookup"><span data-stu-id="cec3b-120">Number of RDS Per User CALs that are issued.</span></span>

</dd> <dt>

<span data-ttu-id="cec3b-121">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="cec3b-121">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec3b-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cec3b-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cec3b-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cec3b-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cec3b-124">Versión de Servicios de Escritorio remoto para la que se emitió la CAL por usuario de RDS.</span><span class="sxs-lookup"><span data-stu-id="cec3b-124">Version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span>

<dt>

<span data-ttu-id="cec3b-125">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="cec3b-125">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="cec3b-126">En esta licencia solo se admiten servidores que ejecuten Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cec3b-126">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="cec3b-127">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="cec3b-127">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="cec3b-128">Con esta licencia solo se admiten servidores que ejecuten Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cec3b-128">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="cec3b-129">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="cec3b-129">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="cec3b-130">Con esta licencia solo se admiten servidores que ejecuten Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cec3b-130">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cec3b-131">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="cec3b-131">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec3b-132">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cec3b-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cec3b-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cec3b-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cec3b-134">Identificador de la versión del producto para el paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="cec3b-134">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="cec3b-135">4</span><span class="sxs-lookup"><span data-stu-id="cec3b-135">4</span></span>
</dt> <dd>

<span data-ttu-id="cec3b-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cec3b-136">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="cec3b-137">3</span><span class="sxs-lookup"><span data-stu-id="cec3b-137">3</span></span>
</dt> <dd>

<span data-ttu-id="cec3b-138">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cec3b-138">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="cec3b-139">2</span><span class="sxs-lookup"><span data-stu-id="cec3b-139">2</span></span>
</dt> <dd>

<span data-ttu-id="cec3b-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cec3b-140">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="cec3b-141">1</span><span class="sxs-lookup"><span data-stu-id="cec3b-141">1</span></span>
</dt> <dd>

<span data-ttu-id="cec3b-142">No se admite.</span><span class="sxs-lookup"><span data-stu-id="cec3b-142">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cec3b-143">0</span><span class="sxs-lookup"><span data-stu-id="cec3b-143">0</span></span>
</dt> <dd>

<span data-ttu-id="cec3b-144">No se admite.</span><span class="sxs-lookup"><span data-stu-id="cec3b-144">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cec3b-145">**TSCALAvailability**</span><span class="sxs-lookup"><span data-stu-id="cec3b-145">**TSCALAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec3b-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cec3b-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cec3b-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cec3b-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cec3b-148">La disponibilidad de las cal por usuario de RDS.</span><span class="sxs-lookup"><span data-stu-id="cec3b-148">The availability of the RDS Per User CALs.</span></span> <span data-ttu-id="cec3b-149">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cec3b-149">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="cec3b-150">Disponible</span><span class="sxs-lookup"><span data-stu-id="cec3b-150">"Available"</span></span>
</dt> <dd>

<span data-ttu-id="cec3b-151">Las cal por usuario de RDS están disponibles.</span><span class="sxs-lookup"><span data-stu-id="cec3b-151">The RDS Per User CALs are available.</span></span>

</dd> <dt>

<span data-ttu-id="cec3b-152">Separados</span><span class="sxs-lookup"><span data-stu-id="cec3b-152">"Limited"</span></span>
</dt> <dd>

<span data-ttu-id="cec3b-153">La disponibilidad de las cal por usuario de RDS es limitada.</span><span class="sxs-lookup"><span data-stu-id="cec3b-153">The availability of the RDS Per User CALs is limited.</span></span>

</dd> <dt>

<span data-ttu-id="cec3b-154">"None"</span><span class="sxs-lookup"><span data-stu-id="cec3b-154">"None"</span></span>
</dt> <dd>

<span data-ttu-id="cec3b-155">Las cal por usuario de RDS no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="cec3b-155">The RDS Per User CALs are not available.</span></span>

</dd> <dt>

<span data-ttu-id="cec3b-156">"No tracking"</span><span class="sxs-lookup"><span data-stu-id="cec3b-156">"Not Tracking"</span></span>
</dt> <dd>

<span data-ttu-id="cec3b-157">No se está realizando el seguimiento de la disponibilidad de las cal por usuario de RDS.</span><span class="sxs-lookup"><span data-stu-id="cec3b-157">The availability of the RDS Per User CALs is not being tracked.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cec3b-158">**TSCALType**</span><span class="sxs-lookup"><span data-stu-id="cec3b-158">**TSCALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cec3b-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cec3b-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cec3b-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cec3b-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cec3b-161">Tipo de cal por usuario de RDS.</span><span class="sxs-lookup"><span data-stu-id="cec3b-161">The type of RDS Per User CALs.</span></span> <span data-ttu-id="cec3b-162">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cec3b-162">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="cec3b-163">"Por dispositivo"</span><span class="sxs-lookup"><span data-stu-id="cec3b-163">"Per Device"</span></span>
</dt> <dd>

<span data-ttu-id="cec3b-164">Las cal por usuario de RDS se emiten por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cec3b-164">The RDS Per User CALs are issued per device.</span></span>

</dd> <dt>

<span data-ttu-id="cec3b-165">"Por usuario"</span><span class="sxs-lookup"><span data-stu-id="cec3b-165">"Per User"</span></span>
</dt> <dd>

<span data-ttu-id="cec3b-166">Las cal por usuario de RDS se emiten por usuario.</span><span class="sxs-lookup"><span data-stu-id="cec3b-166">The RDS Per User CALs are issued per user.</span></span>

</dd> <dt>

<span data-ttu-id="cec3b-167">Unknown</span><span class="sxs-lookup"><span data-stu-id="cec3b-167">"Unknown"</span></span>
</dt> <dd>

<span data-ttu-id="cec3b-168">Se desconoce el tipo de cal por usuario de RDS.</span><span class="sxs-lookup"><span data-stu-id="cec3b-168">The type of RDS Per User CALs is unknown.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cec3b-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cec3b-169">Requirements</span></span>



| <span data-ttu-id="cec3b-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="cec3b-170">Requirement</span></span> | <span data-ttu-id="cec3b-171">Value</span><span class="sxs-lookup"><span data-stu-id="cec3b-171">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cec3b-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cec3b-172">Minimum supported client</span></span><br/> | <span data-ttu-id="cec3b-173">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cec3b-173">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="cec3b-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cec3b-174">Minimum supported server</span></span><br/> | <span data-ttu-id="cec3b-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cec3b-175">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="cec3b-176">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cec3b-176">Namespace</span></span><br/>                | <span data-ttu-id="cec3b-177">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="cec3b-177">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="cec3b-178">MOF</span><span class="sxs-lookup"><span data-stu-id="cec3b-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cec3b-179"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cec3b-179"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cec3b-180">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cec3b-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cec3b-181"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cec3b-181"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



 

 





