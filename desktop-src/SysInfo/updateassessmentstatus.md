---
description: Describe la actualización del sistema operativo en un dispositivo.
ms.assetid: 157E241E-E8D8-41F8-9565-5C9298DCD1BE
title: Enumeración UpdateAssessmentStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateAssessmentStatus
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: 790077118db7704bdd04801758f44cbb50cc54b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666634"
---
# <a name="updateassessmentstatus-enumeration"></a><span data-ttu-id="50311-103">Enumeración UpdateAssessmentStatus</span><span class="sxs-lookup"><span data-stu-id="50311-103">UpdateAssessmentStatus enumeration</span></span>

<span data-ttu-id="50311-104">Describe la actualización del sistema operativo en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="50311-104">Describes how up-to-date the OS on a device is.</span></span> <span data-ttu-id="50311-105">**UpdateAssessmentStatus** se usa en las estructuras [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) y [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , en los miembros **assessmentForCurrent**, **assessmentForUpToDate** y **securityStatus** .</span><span class="sxs-lookup"><span data-stu-id="50311-105">**UpdateAssessmentStatus** is used by the [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) and [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structures, in the **assessmentForCurrent**, **assessmentForUpToDate**, and **securityStatus** members.</span></span> <span data-ttu-id="50311-106">Se devuelve exactamente una constante.</span><span class="sxs-lookup"><span data-stu-id="50311-106">Exactly one constant is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="50311-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50311-107">Syntax</span></span>


```C++
typedef enum TagUpdateAssessmentStatus { 
      UpdateAssessmentStatus_Latest                    = 0,
      UpdateAssessmentStatus_NotLatestSoftRestriction  = 1,
      UpdateAssessmentStatus_NotLatestHardRestriction  = 2,
      UpdateAssessmentStatus_NotLatestEndOfSupport     = 3,
      UpdateAssessmentStatus_NotLatestServicingTrain   = 4,
      UpdateAssessmentStatus_NotLatestDeferredFeature  = 5,
      UpdateAssessmentStatus_NotLatestDeferredQuality  = 6,
      UpdateAssessmentStatus_NotLatestPausedFeature    = 7,
      UpdateAssessmentStatus_NotLatestPausedQuality    = 8,
      UpdateAssessmentStatus_NotLatestManaged          = 9,
      UpdateAssessmentStatus_NotLatestUnknown          = 10,
      UpdateAssessmentStatus_NotLatestTargetedVersion  = 11
} UpdateAssessmentStatus;
```



## <a name="constants"></a><span data-ttu-id="50311-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="50311-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="50311-109"><span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span>**UpdateAssessmentStatus \_ Más reciente**</span><span class="sxs-lookup"><span data-stu-id="50311-109"><span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span> **UpdateAssessmentStatus\_Latest**</span></span>
</dt> <dd>

<span data-ttu-id="50311-110">Este resultado en **assessmentForCurrent** implica que el dispositivo está en la actualización de características y la actualización de calidad más recientes disponibles para ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="50311-110">This result within **assessmentForCurrent** implies that the device is on the latest feature update and quality update available for that device.</span></span> <span data-ttu-id="50311-111">Dentro de **assessmentForUpToDate**, este resultado implica que el dispositivo está en la última actualización de calidad para la versión de Windows que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="50311-111">Within **assessmentForUpToDate**, this result implies that the device is on the latest quality update for the release of Windows it is running.</span></span>

</dd> <dt>

<span data-ttu-id="50311-112"><span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestSoftRestriction**</span><span class="sxs-lookup"><span data-stu-id="50311-112"><span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span> **UpdateAssessmentStatus\_NotLatestSoftRestriction**</span></span>
</dt> <dd>

<span data-ttu-id="50311-113">No se ha instalado la actualización de características más reciente debido a una restricción temporal.</span><span class="sxs-lookup"><span data-stu-id="50311-113">The latest feature update has not been installed due to a soft restriction.</span></span> <span data-ttu-id="50311-114">Cuando se ha colocado una restricción de software en una actualización, la actualización no se instalará automáticamente. un usuario debe iniciar automáticamente la descarga dentro de la experiencia de actualización.</span><span class="sxs-lookup"><span data-stu-id="50311-114">When a soft restriction has been placed on an update, the update will not be automatically installed; a user must self-initiate the download within the Update UX.</span></span> <span data-ttu-id="50311-115">Este estado solo se aplica a **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="50311-115">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="50311-116"><span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestHardRestriction**</span><span class="sxs-lookup"><span data-stu-id="50311-116"><span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span> **UpdateAssessmentStatus\_NotLatestHardRestriction**</span></span>
</dt> <dd>

<span data-ttu-id="50311-117">No se ha instalado la actualización de características más reciente debido a una restricción estricta.</span><span class="sxs-lookup"><span data-stu-id="50311-117">The latest feature update has not been installed due to a hard restriction.</span></span> <span data-ttu-id="50311-118">Cuando se ha colocado una restricción rígida en una actualización, la actualización no es aplicable al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="50311-118">When a hard restriction has been placed on an update, the update is not applicable to the device.</span></span> <span data-ttu-id="50311-119">Este estado solo se aplica a **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="50311-119">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="50311-120"><span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span>**UpdateAssessmentStatus \_ NotLatestEndOfSupport**</span><span class="sxs-lookup"><span data-stu-id="50311-120"><span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span> **UpdateAssessmentStatus\_NotLatestEndOfSupport**</span></span>
</dt> <dd>

<span data-ttu-id="50311-121">El dispositivo no está en la actualización más reciente porque Microsoft ya no admite la actualización de características del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="50311-121">The device is not on the latest update because the device's feature update is no longer supported by Microsoft.</span></span> <span data-ttu-id="50311-122">Cuando Microsoft deja de admitir una versión de característica, este estado se devolverá para **assessmentForCurrent** y **assessmentForUpToDate**.</span><span class="sxs-lookup"><span data-stu-id="50311-122">When Microsoft stops supporting a feature release, this status will be returned for both **assessmentForCurrent** and **assessmentForUpToDate**.</span></span>

> [!Note]  
> <span data-ttu-id="50311-123">Cuando se devuelve **UpdateAssessmentStatus \_ NotLatestEndOfSupport** , el **UpdateImpactLevel** de la evaluación siempre es **UpdateImpactLevel \_ alto**.</span><span class="sxs-lookup"><span data-stu-id="50311-123">When **UpdateAssessmentStatus\_NotLatestEndOfSupport** is returned, the assessment's **UpdateImpactLevel** is always **UpdateImpactLevel\_High**.</span></span>

 

</dd> <dt>

<span data-ttu-id="50311-124"><span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span>**UpdateAssessmentStatus \_ NotLatestServicingTrain**</span><span class="sxs-lookup"><span data-stu-id="50311-124"><span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span> **UpdateAssessmentStatus\_NotLatestServicingTrain**</span></span>
</dt> <dd>

<span data-ttu-id="50311-125">El dispositivo no está en la actualización de características más reciente porque el tren de mantenimiento del dispositivo limita el dispositivo a la actualización más reciente de las características.</span><span class="sxs-lookup"><span data-stu-id="50311-125">The device is not on the latest feature update because the device's servicing train limits the device from updating to the latest feature update.</span></span> <span data-ttu-id="50311-126">Por ejemplo: Si un dispositivo está en Rama actual para empresas (CBB) y se ha publicado una nueva actualización de características para Rama actual (CB), se devolverá.</span><span class="sxs-lookup"><span data-stu-id="50311-126">For example: if a device is on Current Branch for Business (CBB) and a new feature update has been released for Current Branch (CB), this will be returned.</span></span> <span data-ttu-id="50311-127">Este estado solo se aplica a **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="50311-127">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="50311-128"><span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestDeferredFeature**</span><span class="sxs-lookup"><span data-stu-id="50311-128"><span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span> **UpdateAssessmentStatus\_NotLatestDeferredFeature**</span></span>
</dt> <dd>

<span data-ttu-id="50311-129">No se ha instalado la actualización de características más reciente debido a que la Directiva de aplazamiento de actualizaciones de características empresariales Windows Update del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="50311-129">The latest feature update has not been installed due to the device's Windows Update for Business Feature Update Deferral policy.</span></span> <span data-ttu-id="50311-130">La determinación de **daysOutOfDate** tiene en cuenta las directivas de aplazamiento; **daysOutOfDate** no comenzará a incrementar hasta que expire el período de aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="50311-130">Determining **daysOutOfDate** takes into account deferral policies; **daysOutOfDate** will not begin incrementing until the deferral period has expired.</span></span> <span data-ttu-id="50311-131">Este estado solo se aplica a **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="50311-131">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="50311-132"><span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestDeferredQuality**</span><span class="sxs-lookup"><span data-stu-id="50311-132"><span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span> **UpdateAssessmentStatus\_NotLatestDeferredQuality**</span></span>
</dt> <dd>

<span data-ttu-id="50311-133">El dispositivo no está en la última actualización de la calidad debido a la Windows Update del dispositivo para la Directiva de aplazamiento de actualizaciones de calidad empresarial.</span><span class="sxs-lookup"><span data-stu-id="50311-133">The device is not on the latest quality update due to the device's Windows Update for Business Quality Update Deferral policy.</span></span> <span data-ttu-id="50311-134">La determinación de **daysOutOfDate** tiene en cuenta las directivas de aplazamiento; **daysOutOfDate** no comenzará a incrementar hasta que expire el período de aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="50311-134">Determining **daysOutOfDate** takes into account deferral policies; **daysOutOfDate** will not begin incrementing until the deferral period has expired.</span></span>

</dd> <dt>

<span data-ttu-id="50311-135"><span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestPausedFeature**</span><span class="sxs-lookup"><span data-stu-id="50311-135"><span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span> **UpdateAssessmentStatus\_NotLatestPausedFeature**</span></span>
</dt> <dd>

<span data-ttu-id="50311-136">El dispositivo no está en la actualización de características más reciente debido a que el dispositivo tiene actualizaciones de características en pausa.</span><span class="sxs-lookup"><span data-stu-id="50311-136">The device is not on the latest feature update due to the device having paused Feature Updates.</span></span> <span data-ttu-id="50311-137">El hecho de que un dispositivo esté en pausa no se factoriza en el cálculo de **daysOutOfDate**.</span><span class="sxs-lookup"><span data-stu-id="50311-137">Whether a device is paused is not factored into the calculation of **daysOutOfDate**.</span></span> <span data-ttu-id="50311-138">Este estado solo se aplica a **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="50311-138">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="50311-139"><span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestPausedQuality**</span><span class="sxs-lookup"><span data-stu-id="50311-139"><span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span> **UpdateAssessmentStatus\_NotLatestPausedQuality**</span></span>
</dt> <dd>

<span data-ttu-id="50311-140">El dispositivo no está en la última actualización de la calidad debido a que el dispositivo tiene actualizaciones de calidad en pausa.</span><span class="sxs-lookup"><span data-stu-id="50311-140">The device is not on the latest quality update due to the device having paused Quality Updates.</span></span> <span data-ttu-id="50311-141">El hecho de que un dispositivo esté en pausa no se factoriza en el cálculo de **daysOutOfDate**.</span><span class="sxs-lookup"><span data-stu-id="50311-141">Whether a device is paused is not factored into the calculation of **daysOutOfDate**.</span></span> <span data-ttu-id="50311-142">**daysOutOfDate** no Factoriza si un dispositivo está en pausa en su cálculo.</span><span class="sxs-lookup"><span data-stu-id="50311-142">**daysOutOfDate** does not factor whether a device is paused into its calculation.</span></span>

</dd> <dt>

<span data-ttu-id="50311-143"><span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span>**UpdateAssessmentStatus \_ NotLatestManaged**</span><span class="sxs-lookup"><span data-stu-id="50311-143"><span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span> **UpdateAssessmentStatus\_NotLatestManaged**</span></span>
</dt> <dd>

<span data-ttu-id="50311-144">El dispositivo no está en la actualización más reciente porque la aprobación de actualizaciones no se realiza a través de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="50311-144">The device is not on the latest update because the approval of updates is not done through Windows Update.</span></span>

</dd> <dt>

<span data-ttu-id="50311-145"><span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span>**UpdateAssessmentStatus \_ NotLatestUnknown**</span><span class="sxs-lookup"><span data-stu-id="50311-145"><span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span> **UpdateAssessmentStatus\_NotLatestUnknown**</span></span>
</dt> <dd>

<span data-ttu-id="50311-146">El dispositivo no está en la actualización más reciente debido a un motivo que no se puede determinar en la evaluación.</span><span class="sxs-lookup"><span data-stu-id="50311-146">The device is not on the latest update due to a reason that cannot be determined by the assessment.</span></span>

</dd> <dt>

<span data-ttu-id="50311-147"><span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span>**UpdateAssessmentStatus \_ NotLatestTargetedVersion**</span><span class="sxs-lookup"><span data-stu-id="50311-147"><span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span> **UpdateAssessmentStatus\_NotLatestTargetedVersion**</span></span>
</dt> <dd>

<span data-ttu-id="50311-148">El dispositivo no está en la última actualización de características debido a la Directiva de la versión de destino de la Windows Update del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="50311-148">The device is not on the latest feature update due to the device's Windows Update for Business Target Version policy.</span></span> <span data-ttu-id="50311-149">Esta Directiva mantiene el dispositivo en la versión de lanzamiento de la característica de destino.</span><span class="sxs-lookup"><span data-stu-id="50311-149">This policy is keeping the device on the targeted feature release version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50311-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50311-150">Remarks</span></span>

<span data-ttu-id="50311-151">Esta enumeración se usa con mayor frecuencia con las estructuras [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) y [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , que a su vez se usan con el método [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) para [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).</span><span class="sxs-lookup"><span data-stu-id="50311-151">This enumeration is used most often with the [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) and [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structures, which are in turn used with the [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) method for [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).</span></span>

## <a name="requirements"></a><span data-ttu-id="50311-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50311-152">Requirements</span></span>



| <span data-ttu-id="50311-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="50311-153">Requirement</span></span> | <span data-ttu-id="50311-154">Value</span><span class="sxs-lookup"><span data-stu-id="50311-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50311-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50311-155">Minimum supported client</span></span><br/> | <span data-ttu-id="50311-156">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="50311-156">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="50311-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50311-157">Minimum supported server</span></span><br/> | <span data-ttu-id="50311-158">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="50311-158">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="50311-159">IDL</span><span class="sxs-lookup"><span data-stu-id="50311-159">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50311-160"><dt>WaaSAPI. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50311-160"><dt>WaaSAPI.idl</dt></span></span> </dl> |



 

 




