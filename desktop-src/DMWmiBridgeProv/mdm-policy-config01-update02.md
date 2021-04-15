---
title: Clase MDM_Policy_Config01_Update02
description: La \_ clase Config01 de Update02 de directivas MDM \_ \_ representa las directivas de actualización disponibles.
ms.assetid: 7324912c-7ac5-42fd-baee-f7e2d81de023
keywords:
- Clase MDM_Policy_Config01_Update02
- MDM_Policy_Config01_Update02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Update02
- MDM_Policy_Config01_Update02.InstanceID
- MDM_Policy_Config01_Update02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3044fc527fd23d49fac383dc25778d3a978b2788
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490810"
---
# <a name="mdm_policy_config01_update02-class"></a><span data-ttu-id="c879a-105">\_ \_ Clase Update02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="c879a-105">MDM\_Policy\_Config01\_Update02 class</span></span>

<span data-ttu-id="c879a-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="c879a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c879a-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="c879a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c879a-108">La **clase \_ \_ Config01 de \_ Update02 de directivas MDM** representa las directivas de actualización disponibles.</span><span class="sxs-lookup"><span data-stu-id="c879a-108">The **MDM\_Policy\_Config01\_Update02** class represents the update policies available.</span></span>

<span data-ttu-id="c879a-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c879a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c879a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c879a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Update02
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

## <a name="members"></a><span data-ttu-id="c879a-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="c879a-111">Members</span></span>

<span data-ttu-id="c879a-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Update02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c879a-112">The **MDM\_Policy\_Config01\_Update02** class has these types of members:</span></span>

-   [<span data-ttu-id="c879a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c879a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c879a-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c879a-114">Properties</span></span>

<span data-ttu-id="c879a-115">La **clase \_ \_ Config01 de \_ Update02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c879a-115">The **MDM\_Policy\_Config01\_Update02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c879a-116">ActiveHoursEnd</span><span class="sxs-lookup"><span data-stu-id="c879a-116">ActiveHoursEnd</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursend)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-119">ActiveHoursMaxRange</span><span class="sxs-lookup"><span data-stu-id="c879a-119">ActiveHoursMaxRange</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursmaxrange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-122">ActiveHoursStart</span><span class="sxs-lookup"><span data-stu-id="c879a-122">ActiveHoursStart</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursstart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-125">AllowAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="c879a-125">AllowAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span><span class="sxs-lookup"><span data-stu-id="c879a-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautowindowsupdatedownloadovermeterednetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-131">AllowMUUpdateService</span><span class="sxs-lookup"><span data-stu-id="c879a-131">AllowMUUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowmuupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-134">AllowNonMicrosoftSignedUpdate</span><span class="sxs-lookup"><span data-stu-id="c879a-134">AllowNonMicrosoftSignedUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allownonmicrosoftsignedupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-137">AllowUpdateService</span><span class="sxs-lookup"><span data-stu-id="c879a-137">AllowUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-140">AutoRestartDeadlinePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="c879a-140">AutoRestartDeadlinePeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartdeadlineperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-143">AutoRestartNotificationSchedule</span><span class="sxs-lookup"><span data-stu-id="c879a-143">AutoRestartNotificationSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartnotificationschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-146">AutoRestartRequiredNotificationDismissal</span><span class="sxs-lookup"><span data-stu-id="c879a-146">AutoRestartRequiredNotificationDismissal</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartrequirednotificationdismissal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-149">BranchReadinessLevel</span><span class="sxs-lookup"><span data-stu-id="c879a-149">BranchReadinessLevel</span></span>](/windows/client-management/mdm/policy-csp-update#update-branchreadinesslevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-150">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-152">DeferFeatureUpdatesPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="c879a-152">DeferFeatureUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferfeatureupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-153">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-155">DeferQualityUpdatesPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="c879a-155">DeferQualityUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferqualityupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-156">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-158">DeferUpdatePeriod</span><span class="sxs-lookup"><span data-stu-id="c879a-158">DeferUpdatePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupdateperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-159">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-161">DeferUpgradePeriod</span><span class="sxs-lookup"><span data-stu-id="c879a-161">DeferUpgradePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupgradeperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-162">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-164">DetectionFrequency</span><span class="sxs-lookup"><span data-stu-id="c879a-164">DetectionFrequency</span></span>](/windows/client-management/mdm/policy-csp-update#update-detectionfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-165">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-167">DisableDualScan</span><span class="sxs-lookup"><span data-stu-id="c879a-167">DisableDualScan</span></span>](/windows/client-management/mdm/policy-csp-update#update-disabledualscan)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-168">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-170">EngagedRestartDeadline</span><span class="sxs-lookup"><span data-stu-id="c879a-170">EngagedRestartDeadline</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartdeadline)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-171">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-173">EngagedRestartSnoozeSchedule</span><span class="sxs-lookup"><span data-stu-id="c879a-173">EngagedRestartSnoozeSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartsnoozeschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-174">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-176">EngagedRestartTransitionSchedule</span><span class="sxs-lookup"><span data-stu-id="c879a-176">EngagedRestartTransitionSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestarttransitionschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-177">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-179">ExcludeWUDriversInQualityUpdate</span><span class="sxs-lookup"><span data-stu-id="c879a-179">ExcludeWUDriversInQualityUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-excludewudriversinqualityupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-180">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-182">FillEmptyContentUrls</span><span class="sxs-lookup"><span data-stu-id="c879a-182">FillEmptyContentUrls</span></span>](/windows/client-management/mdm/policy-csp-update#update-fillemptycontenturls)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-183">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-184">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-185">IgnoreMOAppDownloadLimit</span><span class="sxs-lookup"><span data-stu-id="c879a-185">IgnoreMOAppDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoappdownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-186">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-187">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-188">IgnoreMOUpdateDownloadLimit</span><span class="sxs-lookup"><span data-stu-id="c879a-188">IgnoreMOUpdateDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoupdatedownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-189">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c879a-191">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c879a-191">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c879a-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c879a-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c879a-194">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c879a-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c879a-195">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="c879a-195">Identifies the name of the parent node.</span></span> <span data-ttu-id="c879a-196">Para esta clase, la cadena es "Update"</span><span class="sxs-lookup"><span data-stu-id="c879a-196">For this class, the string is "Update"</span></span>

</dd> <dt>

[<span data-ttu-id="c879a-197">ManagePreviewBuilds</span><span class="sxs-lookup"><span data-stu-id="c879a-197">ManagePreviewBuilds</span></span>](/windows/client-management/mdm/policy-csp-update#update-managepreviewbuilds)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-198">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-199">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c879a-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c879a-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c879a-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c879a-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c879a-203">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c879a-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c879a-204">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="c879a-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="c879a-205">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="c879a-205">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="c879a-206">PauseDeferrals</span><span class="sxs-lookup"><span data-stu-id="c879a-206">PauseDeferrals</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausedeferrals)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-207">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-208">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-209">PauseFeatureUpdates</span><span class="sxs-lookup"><span data-stu-id="c879a-209">PauseFeatureUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-210">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-211">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-212">PauseFeatureUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="c879a-212">PauseFeatureUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c879a-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-214">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-215">PauseQualityUpdates</span><span class="sxs-lookup"><span data-stu-id="c879a-215">PauseQualityUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-216">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-217">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-218">PauseQualityUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="c879a-218">PauseQualityUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c879a-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-220">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-221">PhoneUpdateRestrictions</span><span class="sxs-lookup"><span data-stu-id="c879a-221">PhoneUpdateRestrictions</span></span>](/windows/client-management/mdm/policy-csp-update#update-phoneupdaterestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-222">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-223">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-224">RequireDeferUpgrade</span><span class="sxs-lookup"><span data-stu-id="c879a-224">RequireDeferUpgrade</span></span>](/windows/client-management/mdm/policy-csp-update#update-requiredeferupgrade)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-225">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-226">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-227">RequireUpdateApproval</span><span class="sxs-lookup"><span data-stu-id="c879a-227">RequireUpdateApproval</span></span>](/windows/client-management/mdm/policy-csp-update#update-requireupdateapproval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-228">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-229">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-230">ScheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="c879a-230">ScheduledInstallDay</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-231">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-232">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-233">ScheduledInstallEveryWeek</span><span class="sxs-lookup"><span data-stu-id="c879a-233">ScheduledInstallEveryWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalleveryweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-234">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-234">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-235">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-236">ScheduledInstallFirstWeek</span><span class="sxs-lookup"><span data-stu-id="c879a-236">ScheduledInstallFirstWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfirstweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-237">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-237">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-238">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-239">ScheduledInstallFourthWeek</span><span class="sxs-lookup"><span data-stu-id="c879a-239">ScheduledInstallFourthWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfourthweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-240">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-240">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-241">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-242">ScheduledInstallSecondWeek</span><span class="sxs-lookup"><span data-stu-id="c879a-242">ScheduledInstallSecondWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallsecondweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-243">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-244">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-245">ScheduledInstallThirdWeek</span><span class="sxs-lookup"><span data-stu-id="c879a-245">ScheduledInstallThirdWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallthirdweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-246">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-246">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-247">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-248">ScheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="c879a-248">ScheduledInstallTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalltime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-249">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-249">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-250">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-251">ScheduleImminentRestartWarning</span><span class="sxs-lookup"><span data-stu-id="c879a-251">ScheduleImminentRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduleimminentrestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-252">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-252">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-253">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-254">ScheduleRestartWarning</span><span class="sxs-lookup"><span data-stu-id="c879a-254">ScheduleRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-schedulerestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-255">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-256">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-257">SetAutoRestartNotificationDisable</span><span class="sxs-lookup"><span data-stu-id="c879a-257">SetAutoRestartNotificationDisable</span></span>](/windows/client-management/mdm/policy-csp-update#update-setautorestartnotificationdisable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-258">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-258">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-259">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-260">SetEDURestart</span><span class="sxs-lookup"><span data-stu-id="c879a-260">SetEDURestart</span></span>](/windows/client-management/mdm/policy-csp-update#update-setedurestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-261">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c879a-261">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-262">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-263">UpdateServiceUrl</span><span class="sxs-lookup"><span data-stu-id="c879a-263">UpdateServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c879a-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-265">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c879a-266">UpdateServiceUrlAlternate</span><span class="sxs-lookup"><span data-stu-id="c879a-266">UpdateServiceUrlAlternate</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurlalternate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c879a-267">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c879a-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c879a-268">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c879a-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c879a-269">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c879a-269">Requirements</span></span>



| <span data-ttu-id="c879a-270">Requisito</span><span class="sxs-lookup"><span data-stu-id="c879a-270">Requirement</span></span> | <span data-ttu-id="c879a-271">Value</span><span class="sxs-lookup"><span data-stu-id="c879a-271">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c879a-272">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c879a-272">Minimum supported client</span></span><br/> | <span data-ttu-id="c879a-273">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="c879a-273">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c879a-274">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c879a-274">Minimum supported server</span></span><br/> | <span data-ttu-id="c879a-275">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c879a-275">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c879a-276">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c879a-276">Namespace</span></span><br/>                | <span data-ttu-id="c879a-277">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="c879a-277">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="c879a-278">MOF</span><span class="sxs-lookup"><span data-stu-id="c879a-278">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c879a-279"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c879a-279"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c879a-280">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c879a-280">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c879a-281"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c879a-281"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c879a-282">Vea también</span><span class="sxs-lookup"><span data-stu-id="c879a-282">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c879a-283">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="c879a-283">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

