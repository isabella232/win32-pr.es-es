---
title: Clase MDM_Policy_Result01_Update02
description: La \_ clase Result01 de Update02 de directivas MDM \_ \_ representa las directivas de actualización disponibles.
ms.assetid: 06604da6-5298-4273-a030-529491c2823c
keywords:
- Clase MDM_Policy_Result01_Update02
- MDM_Policy_Result01_Update02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Update02
- MDM_Policy_Result01_Update02.InstanceID
- MDM_Policy_Result01_Update02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0be844bb4ef8fc20e7ab5bbc8b7709cdfde4034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995968"
---
# <a name="mdm_policy_result01_update02-class"></a><span data-ttu-id="65792-105">\_ \_ Clase Update02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="65792-105">MDM\_Policy\_Result01\_Update02 class</span></span>

<span data-ttu-id="65792-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="65792-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="65792-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="65792-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="65792-108">La **clase \_ \_ Result01 de \_ Update02 de directivas MDM** representa las directivas de actualización disponibles.</span><span class="sxs-lookup"><span data-stu-id="65792-108">The **MDM\_Policy\_Result01\_Update02** class represents the update policies available.</span></span>

<span data-ttu-id="65792-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="65792-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="65792-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65792-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Update02
{
  string InstanceID;
  string ParentID;
  sint32 RequireUpdateApproval;
  sint32 AllowAutoUpdate;
  sint32 AllowAutoWindowsUpdateDownloadOverMeteredNetwork;
  sint32 AllowMUUpdateService;
  sint32 ScheduledInstallDay;
  sint32 ScheduledInstallThirdWeek;
  sint32 ScheduledInstallSecondWeek;
  sint32 ScheduledInstallFourthWeek;
  sint32 ScheduledInstallFirstWeek;
  sint32 ScheduledInstallEveryWeek;
  sint32 ScheduledInstallTime;
  sint32 AllowUpdateService;
  sint32 DeferQualityUpdatesPeriodInDays;
  sint32 DeferFeatureUpdatesPeriodInDays;
  sint32 BranchReadinessLevel;
  string UpdateServiceUrl;
  sint32 SetEDURestart;
  sint32 AutoRestartDeadlinePeriodInDays;
  string UpdateServiceUrlAlternate;
  sint32 FillEmptyContentUrls;
  sint32 AllowNonMicrosoftSignedUpdate;
  sint32 RequireDeferUpgrade;
  sint32 PauseDeferrals;
  sint32 PauseQualityUpdates;
  sint32 PhoneUpdateRestrictions;
  string PauseQualityUpdatesStartTime;
  sint32 PauseFeatureUpdates;
  string PauseFeatureUpdatesStartTime;
  sint32 DeferUpgradePeriod;
  sint32 ExcludeWUDriversInQualityUpdate;
  sint32 IgnoreMOUpdateDownloadLimit;
  sint32 ManagePreviewBuilds;
  sint32 IgnoreMOAppDownloadLimit;
  sint32 DeferUpdatePeriod;
  sint32 ActiveHoursEnd;
  sint32 ActiveHoursStart;
  sint32 DetectionFrequency;
  sint32 DisableDualScan;
  sint32 EngagedRestartDeadline;
  sint32 EngagedRestartSnoozeSchedule;
  sint32 EngagedRestartTransitionSchedule;
  sint32 ScheduleImminentRestartWarning;
  sint32 ScheduleRestartWarning;
  sint32 SetAutoRestartNotificationDisable;
  sint32 AutoRestartNotificationSchedule;
  sint32 AutoRestartRequiredNotificationDismissal;
  sint32 ActiveHoursMaxRange;
};
```

## <a name="members"></a><span data-ttu-id="65792-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="65792-111">Members</span></span>

<span data-ttu-id="65792-112">La clase Result01 de la **\_ Directiva MDM \_ \_ Update02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="65792-112">The **MDM\_Policy\_Result01\_Update02** class has these types of members:</span></span>

-   [<span data-ttu-id="65792-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="65792-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65792-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="65792-114">Properties</span></span>

<span data-ttu-id="65792-115">La **clase \_ \_ Result01 de \_ Update02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="65792-115">The **MDM\_Policy\_Result01\_Update02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="65792-116">ActiveHoursEnd</span><span class="sxs-lookup"><span data-stu-id="65792-116">ActiveHoursEnd</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursend)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-119">ActiveHoursMaxRange</span><span class="sxs-lookup"><span data-stu-id="65792-119">ActiveHoursMaxRange</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursmaxrange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-122">ActiveHoursStart</span><span class="sxs-lookup"><span data-stu-id="65792-122">ActiveHoursStart</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursstart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-125">AllowAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="65792-125">AllowAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span><span class="sxs-lookup"><span data-stu-id="65792-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautowindowsupdatedownloadovermeterednetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-131">AllowMUUpdateService</span><span class="sxs-lookup"><span data-stu-id="65792-131">AllowMUUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowmuupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-134">AllowNonMicrosoftSignedUpdate</span><span class="sxs-lookup"><span data-stu-id="65792-134">AllowNonMicrosoftSignedUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allownonmicrosoftsignedupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-137">AllowUpdateService</span><span class="sxs-lookup"><span data-stu-id="65792-137">AllowUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-140">AutoRestartDeadlinePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="65792-140">AutoRestartDeadlinePeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartdeadlineperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-143">AutoRestartNotificationSchedule</span><span class="sxs-lookup"><span data-stu-id="65792-143">AutoRestartNotificationSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartnotificationschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-146">AutoRestartRequiredNotificationDismissal</span><span class="sxs-lookup"><span data-stu-id="65792-146">AutoRestartRequiredNotificationDismissal</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartrequirednotificationdismissal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-149">BranchReadinessLevel</span><span class="sxs-lookup"><span data-stu-id="65792-149">BranchReadinessLevel</span></span>](/windows/client-management/mdm/policy-csp-update#update-branchreadinesslevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-150">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-152">DeferFeatureUpdatesPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="65792-152">DeferFeatureUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferfeatureupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-153">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-155">DeferQualityUpdatesPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="65792-155">DeferQualityUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferqualityupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-156">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-158">DeferUpdatePeriod</span><span class="sxs-lookup"><span data-stu-id="65792-158">DeferUpdatePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupdateperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-159">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-161">DeferUpgradePeriod</span><span class="sxs-lookup"><span data-stu-id="65792-161">DeferUpgradePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupgradeperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-162">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-164">DetectionFrequency</span><span class="sxs-lookup"><span data-stu-id="65792-164">DetectionFrequency</span></span>](/windows/client-management/mdm/policy-csp-update#update-detectionfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-165">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-167">DisableDualScan</span><span class="sxs-lookup"><span data-stu-id="65792-167">DisableDualScan</span></span>](/windows/client-management/mdm/policy-csp-update#update-disabledualscan)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-168">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-170">EngagedRestartDeadline</span><span class="sxs-lookup"><span data-stu-id="65792-170">EngagedRestartDeadline</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartdeadline)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-171">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-173">EngagedRestartSnoozeSchedule</span><span class="sxs-lookup"><span data-stu-id="65792-173">EngagedRestartSnoozeSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartsnoozeschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-174">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-176">EngagedRestartTransitionSchedule</span><span class="sxs-lookup"><span data-stu-id="65792-176">EngagedRestartTransitionSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestarttransitionschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-177">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-179">ExcludeWUDriversInQualityUpdate</span><span class="sxs-lookup"><span data-stu-id="65792-179">ExcludeWUDriversInQualityUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-excludewudriversinqualityupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-180">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-182">FillEmptyContentUrls</span><span class="sxs-lookup"><span data-stu-id="65792-182">FillEmptyContentUrls</span></span>](/windows/client-management/mdm/policy-csp-update#update-fillemptycontenturls)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-183">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-184">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-185">IgnoreMOAppDownloadLimit</span><span class="sxs-lookup"><span data-stu-id="65792-185">IgnoreMOAppDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoappdownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-186">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-187">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-188">IgnoreMOUpdateDownloadLimit</span><span class="sxs-lookup"><span data-stu-id="65792-188">IgnoreMOUpdateDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoupdatedownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-189">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="65792-191">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="65792-191">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="65792-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65792-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65792-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65792-194">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="65792-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="65792-195">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="65792-195">Identifies the name of the parent node.</span></span> <span data-ttu-id="65792-196">Para esta clase, la cadena es "Update"</span><span class="sxs-lookup"><span data-stu-id="65792-196">For this class, the string is "Update"</span></span>

</dd> <dt>

[<span data-ttu-id="65792-197">ManagePreviewBuilds</span><span class="sxs-lookup"><span data-stu-id="65792-197">ManagePreviewBuilds</span></span>](/windows/client-management/mdm/policy-csp-update#update-managepreviewbuilds)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-198">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-199">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="65792-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="65792-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="65792-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65792-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65792-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65792-203">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="65792-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="65792-204">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="65792-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="65792-205">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="65792-205">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="65792-206">PauseDeferrals</span><span class="sxs-lookup"><span data-stu-id="65792-206">PauseDeferrals</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausedeferrals)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-207">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-208">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-209">PauseFeatureUpdates</span><span class="sxs-lookup"><span data-stu-id="65792-209">PauseFeatureUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-210">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-211">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-212">PauseFeatureUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="65792-212">PauseFeatureUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="65792-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65792-214">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-215">PauseQualityUpdates</span><span class="sxs-lookup"><span data-stu-id="65792-215">PauseQualityUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-216">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-217">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-218">PauseQualityUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="65792-218">PauseQualityUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="65792-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65792-220">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-221">PhoneUpdateRestrictions</span><span class="sxs-lookup"><span data-stu-id="65792-221">PhoneUpdateRestrictions</span></span>](/windows/client-management/mdm/policy-csp-update#update-phoneupdaterestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-222">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-223">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-224">RequireDeferUpgrade</span><span class="sxs-lookup"><span data-stu-id="65792-224">RequireDeferUpgrade</span></span>](/windows/client-management/mdm/policy-csp-update#update-requiredeferupgrade)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-225">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-226">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-227">RequireUpdateApproval</span><span class="sxs-lookup"><span data-stu-id="65792-227">RequireUpdateApproval</span></span>](/windows/client-management/mdm/policy-csp-update#update-requireupdateapproval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-228">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-229">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-230">ScheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="65792-230">ScheduledInstallDay</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-231">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-232">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-233">ScheduledInstallEveryWeek</span><span class="sxs-lookup"><span data-stu-id="65792-233">ScheduledInstallEveryWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalleveryweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-234">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-234">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-235">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-236">ScheduledInstallFirstWeek</span><span class="sxs-lookup"><span data-stu-id="65792-236">ScheduledInstallFirstWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfirstweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-237">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-237">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-238">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-239">ScheduledInstallFourthWeek</span><span class="sxs-lookup"><span data-stu-id="65792-239">ScheduledInstallFourthWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfourthweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-240">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-240">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-241">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-242">ScheduledInstallSecondWeek</span><span class="sxs-lookup"><span data-stu-id="65792-242">ScheduledInstallSecondWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallsecondweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-243">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-244">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-245">ScheduledInstallThirdWeek</span><span class="sxs-lookup"><span data-stu-id="65792-245">ScheduledInstallThirdWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallthirdweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-246">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-246">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-247">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-248">ScheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="65792-248">ScheduledInstallTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalltime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-249">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-249">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-250">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-251">ScheduleImminentRestartWarning</span><span class="sxs-lookup"><span data-stu-id="65792-251">ScheduleImminentRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduleimminentrestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-252">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-252">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-253">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-254">ScheduleRestartWarning</span><span class="sxs-lookup"><span data-stu-id="65792-254">ScheduleRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-schedulerestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-255">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-256">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-257">SetAutoRestartNotificationDisable</span><span class="sxs-lookup"><span data-stu-id="65792-257">SetAutoRestartNotificationDisable</span></span>](/windows/client-management/mdm/policy-csp-update#update-setautorestartnotificationdisable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-258">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-258">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-259">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-260">SetEDURestart</span><span class="sxs-lookup"><span data-stu-id="65792-260">SetEDURestart</span></span>](/windows/client-management/mdm/policy-csp-update#update-setedurestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-261">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="65792-261">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="65792-262">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-263">UpdateServiceUrl</span><span class="sxs-lookup"><span data-stu-id="65792-263">UpdateServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="65792-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65792-265">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="65792-266">UpdateServiceUrlAlternate</span><span class="sxs-lookup"><span data-stu-id="65792-266">UpdateServiceUrlAlternate</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurlalternate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="65792-267">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="65792-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65792-268">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="65792-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65792-269">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65792-269">Requirements</span></span>



| <span data-ttu-id="65792-270">Requisito</span><span class="sxs-lookup"><span data-stu-id="65792-270">Requirement</span></span> | <span data-ttu-id="65792-271">Value</span><span class="sxs-lookup"><span data-stu-id="65792-271">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65792-272">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65792-272">Minimum supported client</span></span><br/> | <span data-ttu-id="65792-273">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="65792-273">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="65792-274">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65792-274">Minimum supported server</span></span><br/> | <span data-ttu-id="65792-275">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="65792-275">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="65792-276">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="65792-276">Namespace</span></span><br/>                | <span data-ttu-id="65792-277">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="65792-277">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="65792-278">MOF</span><span class="sxs-lookup"><span data-stu-id="65792-278">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65792-279"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65792-279"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="65792-280">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65792-280">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65792-281"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65792-281"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65792-282">Vea también</span><span class="sxs-lookup"><span data-stu-id="65792-282">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65792-283">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="65792-283">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

