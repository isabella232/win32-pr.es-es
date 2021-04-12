---
title: MDM_Policy_Config01_Defender02 (clase)
description: La \_ Directiva MDM \_ Config01 \_ Defender02class representa las directivas relacionadas con Windows Defender.
ms.assetid: 6d9d4edd-fcb6-45ea-bc5d-1bffb9cf8740
keywords:
- MDM_Policy_Config01_Defender02 (clase)
- MDM_Policy_Config01_Defender02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Defender02
- MDM_Policy_Config01_Defender02.InstanceID
- MDM_Policy_Config01_Defender02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b184008fc0ce7fc44dcb7106ceec3abc0e91450d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489910"
---
# <a name="mdm_policy_config01_defender02-class"></a><span data-ttu-id="dddce-105">\_ \_ Clase Defender02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="dddce-105">MDM\_Policy\_Config01\_Defender02 class</span></span>

<span data-ttu-id="dddce-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="dddce-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dddce-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="dddce-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dddce-108">La **clase \_ \_ Config01 de \_ Defender02 de directivas MDM** representa las directivas relacionadas con Windows Defender</span><span class="sxs-lookup"><span data-stu-id="dddce-108">The **MDM\_Policy\_Config01\_Defender02** class represents policies related to Windows Defender</span></span>

<span data-ttu-id="dddce-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="dddce-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dddce-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dddce-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Defender02
{
  string InstanceID;
  string ParentID;
  sint32 AllowArchiveScanning;
  sint32 AllowBehaviorMonitoring;
  sint32 AllowCloudProtection;
  sint32 AllowEmailScanning;
  sint32 AllowFullScanOnMappedNetworkDrives;
  sint32 AllowFullScanRemovableDriveScanning;
  sint32 AllowIntrusionPreventionSystem;
  sint32 AllowIOAVProtection;
  sint32 AllowOnAccessProtection;
  sint32 AllowRealtimeMonitoring;
  sint32 AllowScanningNetworkFiles;
  sint32 AllowScriptScanning;
  sint32 AllowUserUIAccess;
  string AttackSurfaceReductionRules;
  string AttackSurfaceReductionOnlyExclusions;
  sint32 AVGCPULoadFactor;
  sint32 CloudExtendedTimeout;
  string ControlledFolderAccessProtectedFolders;
  string ControlledFolderAccessAllowedApplications;
  sint32 CloudBlockLevel;
  sint32 DaysToRetainCleanedMalware;
  sint32 EnableControlledFolderAccess;
  sint32 EnableNetworkProtection;
  sint32 PUAProtection;
  string ExcludedProcesses;
  string ExcludedPaths;
  string ExcludedExtensions;
  sint32 RealTimeScanDirection;
  sint32 ScanParameter;
  sint32 ScheduleQuickScanTime;
  sint32 ScheduleScanDay;
  sint32 ScheduleScanTime;
  sint32 SignatureUpdateInterval;
  sint32 SubmitSamplesConsent;
  string ThreatSeverityDefaultAction;
};
```

## <a name="members"></a><span data-ttu-id="dddce-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="dddce-111">Members</span></span>

<span data-ttu-id="dddce-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Defender02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dddce-112">The **MDM\_Policy\_Config01\_Defender02** class has these types of members:</span></span>

-   [<span data-ttu-id="dddce-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dddce-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dddce-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dddce-114">Properties</span></span>

<span data-ttu-id="dddce-115">La **clase \_ \_ Config01 de \_ Defender02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dddce-115">The **MDM\_Policy\_Config01\_Defender02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="dddce-116">AllowArchiveScanning</span><span class="sxs-lookup"><span data-stu-id="dddce-116">AllowArchiveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowarchivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-119">AllowBehaviorMonitoring</span><span class="sxs-lookup"><span data-stu-id="dddce-119">AllowBehaviorMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowbehaviormonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-122">AllowCloudProtection</span><span class="sxs-lookup"><span data-stu-id="dddce-122">AllowCloudProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowcloudprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-125">AllowEmailScanning</span><span class="sxs-lookup"><span data-stu-id="dddce-125">AllowEmailScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowemailscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-128">AllowFullScanOnMappedNetworkDrives</span><span class="sxs-lookup"><span data-stu-id="dddce-128">AllowFullScanOnMappedNetworkDrives</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanonmappednetworkdrives)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-131">AllowFullScanRemovableDriveScanning</span><span class="sxs-lookup"><span data-stu-id="dddce-131">AllowFullScanRemovableDriveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanremovabledrivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-134">AllowIntrusionPreventionSystem</span><span class="sxs-lookup"><span data-stu-id="dddce-134">AllowIntrusionPreventionSystem</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowintrusionpreventionsystem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-137">AllowIOAVProtection</span><span class="sxs-lookup"><span data-stu-id="dddce-137">AllowIOAVProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowioavprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-140">AllowOnAccessProtection</span><span class="sxs-lookup"><span data-stu-id="dddce-140">AllowOnAccessProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowonaccessprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-143">AllowRealtimeMonitoring</span><span class="sxs-lookup"><span data-stu-id="dddce-143">AllowRealtimeMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowrealtimemonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-146">AllowScanningNetworkFiles</span><span class="sxs-lookup"><span data-stu-id="dddce-146">AllowScanningNetworkFiles</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscanningnetworkfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-149">AllowScriptScanning</span><span class="sxs-lookup"><span data-stu-id="dddce-149">AllowScriptScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscriptscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-150">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-152">AllowUserUIAccess</span><span class="sxs-lookup"><span data-stu-id="dddce-152">AllowUserUIAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowuseruiaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-153">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-155">AttackSurfaceReductionOnlyExclusions</span><span class="sxs-lookup"><span data-stu-id="dddce-155">AttackSurfaceReductionOnlyExclusions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dddce-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-158">AttackSurfaceReductionRules</span><span class="sxs-lookup"><span data-stu-id="dddce-158">AttackSurfaceReductionRules</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dddce-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-161">AVGCPULoadFactor</span><span class="sxs-lookup"><span data-stu-id="dddce-161">AVGCPULoadFactor</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-avgcpuloadfactor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-162">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-164">CloudBlockLevel</span><span class="sxs-lookup"><span data-stu-id="dddce-164">CloudBlockLevel</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudblocklevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-165">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-167">CloudExtendedTimeout</span><span class="sxs-lookup"><span data-stu-id="dddce-167">CloudExtendedTimeout</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudextendedtimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-168">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-170">ControlledFolderAccessAllowedApplications</span><span class="sxs-lookup"><span data-stu-id="dddce-170">ControlledFolderAccessAllowedApplications</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessallowedapplications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dddce-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-173">ControlledFolderAccessProtectedFolders</span><span class="sxs-lookup"><span data-stu-id="dddce-173">ControlledFolderAccessProtectedFolders</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dddce-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-176">DaysToRetainCleanedMalware</span><span class="sxs-lookup"><span data-stu-id="dddce-176">DaysToRetainCleanedMalware</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-daystoretaincleanedmalware)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-177">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-179">EnableControlledFolderAccess</span><span class="sxs-lookup"><span data-stu-id="dddce-179">EnableControlledFolderAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablecontrolledfolderaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-180">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-182">EnableNetworkProtection</span><span class="sxs-lookup"><span data-stu-id="dddce-182">EnableNetworkProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablenetworkprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-183">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-184">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-185">ExcludedExtensions</span><span class="sxs-lookup"><span data-stu-id="dddce-185">ExcludedExtensions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dddce-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-187">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-188">ExcludedPaths</span><span class="sxs-lookup"><span data-stu-id="dddce-188">ExcludedPaths</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dddce-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-191">ExcludedProcesses</span><span class="sxs-lookup"><span data-stu-id="dddce-191">ExcludedProcesses</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dddce-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-193">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dddce-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dddce-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dddce-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dddce-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dddce-197">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dddce-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dddce-198">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="dddce-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="dddce-199">Para esta clase, la cadena es "defender".</span><span class="sxs-lookup"><span data-stu-id="dddce-199">For this class, the string is "Defender".</span></span>

</dd> <dt>

<span data-ttu-id="dddce-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dddce-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dddce-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dddce-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dddce-203">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dddce-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dddce-204">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="dddce-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="dddce-205">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="dddce-205">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="dddce-206">PUAProtection</span><span class="sxs-lookup"><span data-stu-id="dddce-206">PUAProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-puaprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-207">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-208">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-209">RealTimeScanDirection</span><span class="sxs-lookup"><span data-stu-id="dddce-209">RealTimeScanDirection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-realtimescandirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-210">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-211">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-212">ScanParameter</span><span class="sxs-lookup"><span data-stu-id="dddce-212">ScanParameter</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-scanparameter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-213">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-214">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-215">ScheduleQuickScanTime</span><span class="sxs-lookup"><span data-stu-id="dddce-215">ScheduleQuickScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulequickscantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-216">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-217">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-218">ScheduleScanDay</span><span class="sxs-lookup"><span data-stu-id="dddce-218">ScheduleScanDay</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescanday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-219">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-220">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-221">ScheduleScanTime</span><span class="sxs-lookup"><span data-stu-id="dddce-221">ScheduleScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-222">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-223">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-224">SignatureUpdateInterval</span><span class="sxs-lookup"><span data-stu-id="dddce-224">SignatureUpdateInterval</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-signatureupdateinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-225">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-226">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-227">SubmitSamplesConsent</span><span class="sxs-lookup"><span data-stu-id="dddce-227">SubmitSamplesConsent</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-228">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dddce-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-229">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dddce-230">ThreatSeverityDefaultAction</span><span class="sxs-lookup"><span data-stu-id="dddce-230">ThreatSeverityDefaultAction</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-threatseveritydefaultaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dddce-231">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dddce-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dddce-232">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dddce-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dddce-233">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dddce-233">Requirements</span></span>



| <span data-ttu-id="dddce-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="dddce-234">Requirement</span></span> | <span data-ttu-id="dddce-235">Value</span><span class="sxs-lookup"><span data-stu-id="dddce-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dddce-236">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dddce-236">Minimum supported client</span></span><br/> | <span data-ttu-id="dddce-237">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="dddce-237">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dddce-238">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dddce-238">Minimum supported server</span></span><br/> | <span data-ttu-id="dddce-239">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dddce-239">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="dddce-240">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dddce-240">Namespace</span></span><br/>                | <span data-ttu-id="dddce-241">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="dddce-241">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="dddce-242">MOF</span><span class="sxs-lookup"><span data-stu-id="dddce-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dddce-243"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dddce-243"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dddce-244">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dddce-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dddce-245"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dddce-245"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dddce-246">Vea también</span><span class="sxs-lookup"><span data-stu-id="dddce-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dddce-247">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="dddce-247">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

