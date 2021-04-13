---
title: MDM_Policy_Result01_Defender02 (clase)
description: La \_ Directiva MDM \_ Result01 \_ Defender02class representa las directivas relacionadas con Windows Defender.
ms.assetid: 82c8a7a2-8369-46c4-aa87-b44b742a274d
keywords:
- MDM_Policy_Result01_Defender02 (clase)
- MDM_Policy_Result01_Defender02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Defender02
- MDM_Policy_Result01_Defender02.InstanceID
- MDM_Policy_Result01_Defender02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae898751a9f15af1c945efd3e6a473dfe07c7cd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489784"
---
# <a name="mdm_policy_result01_defender02-class"></a><span data-ttu-id="67e12-105">\_ \_ Clase Defender02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="67e12-105">MDM\_Policy\_Result01\_Defender02 class</span></span>

<span data-ttu-id="67e12-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="67e12-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="67e12-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="67e12-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="67e12-108">La **clase \_ \_ Result01 de \_ Defender02 de directivas MDM** representa las directivas relacionadas con Windows Defender</span><span class="sxs-lookup"><span data-stu-id="67e12-108">The **MDM\_Policy\_Result01\_Defender02** class represents policies related to Windows Defender</span></span>

<span data-ttu-id="67e12-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="67e12-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="67e12-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67e12-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Defender02
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
  sint32 ScheduleQuickScanTime;
  sint32 ScheduleScanDay;
  sint32 ScheduleScanTime;
  sint32 SignatureUpdateInterval;
  sint32 SubmitSamplesConsent;
  string ThreatSeverityDefaultAction;
  sint32 ScanParameter;
};
```

## <a name="members"></a><span data-ttu-id="67e12-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="67e12-111">Members</span></span>

<span data-ttu-id="67e12-112">La clase Result01 de la **\_ Directiva MDM \_ \_ Defender02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="67e12-112">The **MDM\_Policy\_Result01\_Defender02** class has these types of members:</span></span>

-   [<span data-ttu-id="67e12-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67e12-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67e12-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67e12-114">Properties</span></span>

<span data-ttu-id="67e12-115">La **clase \_ \_ Result01 de \_ Defender02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="67e12-115">The **MDM\_Policy\_Result01\_Defender02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="67e12-116">AllowArchiveScanning</span><span class="sxs-lookup"><span data-stu-id="67e12-116">AllowArchiveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowarchivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-119">AllowBehaviorMonitoring</span><span class="sxs-lookup"><span data-stu-id="67e12-119">AllowBehaviorMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowbehaviormonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-122">AllowCloudProtection</span><span class="sxs-lookup"><span data-stu-id="67e12-122">AllowCloudProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowcloudprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-125">AllowEmailScanning</span><span class="sxs-lookup"><span data-stu-id="67e12-125">AllowEmailScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowemailscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-128">AllowFullScanOnMappedNetworkDrives</span><span class="sxs-lookup"><span data-stu-id="67e12-128">AllowFullScanOnMappedNetworkDrives</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanonmappednetworkdrives)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-131">AllowFullScanRemovableDriveScanning</span><span class="sxs-lookup"><span data-stu-id="67e12-131">AllowFullScanRemovableDriveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanremovabledrivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-134">AllowIntrusionPreventionSystem</span><span class="sxs-lookup"><span data-stu-id="67e12-134">AllowIntrusionPreventionSystem</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowintrusionpreventionsystem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-137">AllowIOAVProtection</span><span class="sxs-lookup"><span data-stu-id="67e12-137">AllowIOAVProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowioavprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-140">AllowOnAccessProtection</span><span class="sxs-lookup"><span data-stu-id="67e12-140">AllowOnAccessProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowonaccessprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-143">AllowRealtimeMonitoring</span><span class="sxs-lookup"><span data-stu-id="67e12-143">AllowRealtimeMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowrealtimemonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-146">AllowScanningNetworkFiles</span><span class="sxs-lookup"><span data-stu-id="67e12-146">AllowScanningNetworkFiles</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscanningnetworkfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-149">AllowScriptScanning</span><span class="sxs-lookup"><span data-stu-id="67e12-149">AllowScriptScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscriptscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-150">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-152">AllowUserUIAccess</span><span class="sxs-lookup"><span data-stu-id="67e12-152">AllowUserUIAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowuseruiaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-153">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-155">AttackSurfaceReductionOnlyExclusions</span><span class="sxs-lookup"><span data-stu-id="67e12-155">AttackSurfaceReductionOnlyExclusions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67e12-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-158">AttackSurfaceReductionRules</span><span class="sxs-lookup"><span data-stu-id="67e12-158">AttackSurfaceReductionRules</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67e12-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-161">AVGCPULoadFactor</span><span class="sxs-lookup"><span data-stu-id="67e12-161">AVGCPULoadFactor</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-avgcpuloadfactor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-162">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-164">CloudBlockLevel</span><span class="sxs-lookup"><span data-stu-id="67e12-164">CloudBlockLevel</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudblocklevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-165">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-167">CloudExtendedTimeout</span><span class="sxs-lookup"><span data-stu-id="67e12-167">CloudExtendedTimeout</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudextendedtimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-168">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-170">ControlledFolderAccessAllowedApplications</span><span class="sxs-lookup"><span data-stu-id="67e12-170">ControlledFolderAccessAllowedApplications</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessallowedapplications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67e12-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-173">ControlledFolderAccessProtectedFolders</span><span class="sxs-lookup"><span data-stu-id="67e12-173">ControlledFolderAccessProtectedFolders</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67e12-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-176">DaysToRetainCleanedMalware</span><span class="sxs-lookup"><span data-stu-id="67e12-176">DaysToRetainCleanedMalware</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-daystoretaincleanedmalware)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-177">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-179">EnableControlledFolderAccess</span><span class="sxs-lookup"><span data-stu-id="67e12-179">EnableControlledFolderAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablecontrolledfolderaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-180">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-182">EnableNetworkProtection</span><span class="sxs-lookup"><span data-stu-id="67e12-182">EnableNetworkProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablenetworkprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-183">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-184">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-185">ExcludedExtensions</span><span class="sxs-lookup"><span data-stu-id="67e12-185">ExcludedExtensions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67e12-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-187">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-188">ExcludedPaths</span><span class="sxs-lookup"><span data-stu-id="67e12-188">ExcludedPaths</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67e12-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-191">ExcludedProcesses</span><span class="sxs-lookup"><span data-stu-id="67e12-191">ExcludedProcesses</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67e12-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-193">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="67e12-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="67e12-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67e12-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67e12-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67e12-197">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="67e12-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="67e12-198">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="67e12-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="67e12-199">Para esta clase, la cadena es "defender".</span><span class="sxs-lookup"><span data-stu-id="67e12-199">For this class, the string is "Defender".</span></span>

</dd> <dt>

<span data-ttu-id="67e12-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="67e12-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67e12-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67e12-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67e12-203">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="67e12-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="67e12-204">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="67e12-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="67e12-205">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="67e12-205">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="67e12-206">PUAProtection</span><span class="sxs-lookup"><span data-stu-id="67e12-206">PUAProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-puaprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-207">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-208">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-209">RealTimeScanDirection</span><span class="sxs-lookup"><span data-stu-id="67e12-209">RealTimeScanDirection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-realtimescandirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-210">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-211">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-212">ScanParameter</span><span class="sxs-lookup"><span data-stu-id="67e12-212">ScanParameter</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-scanparameter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-213">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-214">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-215">ScheduleQuickScanTime</span><span class="sxs-lookup"><span data-stu-id="67e12-215">ScheduleQuickScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulequickscantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-216">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-217">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-218">ScheduleScanDay</span><span class="sxs-lookup"><span data-stu-id="67e12-218">ScheduleScanDay</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescanday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-219">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-220">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-221">ScheduleScanTime</span><span class="sxs-lookup"><span data-stu-id="67e12-221">ScheduleScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-222">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-223">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-224">SignatureUpdateInterval</span><span class="sxs-lookup"><span data-stu-id="67e12-224">SignatureUpdateInterval</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-signatureupdateinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-225">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-226">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-227">SubmitSamplesConsent</span><span class="sxs-lookup"><span data-stu-id="67e12-227">SubmitSamplesConsent</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-228">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67e12-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-229">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="67e12-230">ThreatSeverityDefaultAction</span><span class="sxs-lookup"><span data-stu-id="67e12-230">ThreatSeverityDefaultAction</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-threatseveritydefaultaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="67e12-231">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67e12-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67e12-232">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="67e12-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="67e12-233">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67e12-233">Requirements</span></span>



| <span data-ttu-id="67e12-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="67e12-234">Requirement</span></span> | <span data-ttu-id="67e12-235">Value</span><span class="sxs-lookup"><span data-stu-id="67e12-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67e12-236">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67e12-236">Minimum supported client</span></span><br/> | <span data-ttu-id="67e12-237">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="67e12-237">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67e12-238">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67e12-238">Minimum supported server</span></span><br/> | <span data-ttu-id="67e12-239">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="67e12-239">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="67e12-240">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="67e12-240">Namespace</span></span><br/>                | <span data-ttu-id="67e12-241">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="67e12-241">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="67e12-242">MOF</span><span class="sxs-lookup"><span data-stu-id="67e12-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67e12-243"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67e12-243"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="67e12-244">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="67e12-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67e12-245"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67e12-245"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67e12-246">Vea también</span><span class="sxs-lookup"><span data-stu-id="67e12-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67e12-247">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="67e12-247">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

