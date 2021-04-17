---
description: Indica un impacto alto, medio o bajo de un dispositivo que ejecuta un sistema operativo obsoleto.
ms.assetid: C7F30B63-66B0-4F37-A05B-7D366A12B640
title: Enumeración UpdateImpactLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateImpactLevel
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: c18cc7916abbc1dce595df9a21d2fdef3976af11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666633"
---
# <a name="updateimpactlevel-enumeration"></a><span data-ttu-id="8fa91-103">Enumeración UpdateImpactLevel</span><span class="sxs-lookup"><span data-stu-id="8fa91-103">UpdateImpactLevel enumeration</span></span>

<span data-ttu-id="8fa91-104">Indica un impacto alto, medio o bajo de un dispositivo que ejecuta un sistema operativo obsoleto.</span><span class="sxs-lookup"><span data-stu-id="8fa91-104">Indicates a high, medium, or low impact of a device running an out-of-date OS.</span></span> <span data-ttu-id="8fa91-105">Esta enumeración se usa generalmente en las estructuras [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) , que a su vez se anidan dentro del [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) devuelto desde [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).</span><span class="sxs-lookup"><span data-stu-id="8fa91-105">This enumeration is generally used by [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) structures, which is in turn nested inside the returned [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) from [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).</span></span>

## <a name="syntax"></a><span data-ttu-id="8fa91-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fa91-106">Syntax</span></span>


```C++
typedef enum TagUpdateImpactLevel { 
      UpdateImpactLevel_None    = 0,
  UpdateImpactLevel_Low         = 1,
      UpdateImpactLevel_Medium  = 2,
  UpdateImpactLevel_High        = 3
} UpdateImpactLevel;
```



## <a name="constants"></a><span data-ttu-id="8fa91-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="8fa91-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8fa91-108"><span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span>**UpdateImpactLevel \_ Ninguno**</span><span class="sxs-lookup"><span data-stu-id="8fa91-108"><span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span> **UpdateImpactLevel\_None**</span></span>
</dt> <dd>

<span data-ttu-id="8fa91-109">No hay ningún impacto previsible en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8fa91-109">There is no foreseeable impact to your device.</span></span> <span data-ttu-id="8fa91-110">Esto puede deberse a que el dispositivo está actualizado o no está actualizado, ya que el dispositivo está respetando su Windows Update para los períodos de aplazamiento de la empresa, o no está actualizada, pero aún no ha alcanzado el umbral de **daysOutOfDate** para alcanzar un nivel de impacto superior.</span><span class="sxs-lookup"><span data-stu-id="8fa91-110">This can be because the device is up-to-date, or is not up-to-date because the device is honoring its Windows Update for Business deferral periods, or is out-of-date but has not yet reached the **daysOutOfDate** threshold to reach a higher impact level.</span></span>

</dd> <dt>

<span data-ttu-id="8fa91-111"><span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel \_ bajo**</span><span class="sxs-lookup"><span data-stu-id="8fa91-111"><span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel\_Low**</span></span>
</dt> <dd>

<span data-ttu-id="8fa91-112">El dispositivo no está ejecutando el sistema operativo más reciente, pero tiene una actualización reciente.</span><span class="sxs-lookup"><span data-stu-id="8fa91-112">The device is not running the latest OS, but has a recent update.</span></span>

</dd> <dt>

<span data-ttu-id="8fa91-113"><span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span>**UpdateImpactLevel \_ Medio**</span><span class="sxs-lookup"><span data-stu-id="8fa91-113"><span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span> **UpdateImpactLevel\_Medium**</span></span>
</dt> <dd>

<span data-ttu-id="8fa91-114">El dispositivo está ejecutando el sistema operativo más reciente, pero tiene una actualización moderada.</span><span class="sxs-lookup"><span data-stu-id="8fa91-114">The device is running the latest OS, but has a moderately recent update.</span></span>

</dd> <dt>

<span data-ttu-id="8fa91-115"><span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel \_ alto**</span><span class="sxs-lookup"><span data-stu-id="8fa91-115"><span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel\_High**</span></span>
</dt> <dd>

<span data-ttu-id="8fa91-116">El dispositivo no está actualizado durante mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="8fa91-116">The device has been out-of-date for a long time.</span></span> <span data-ttu-id="8fa91-117">Es posible que este dispositivo tenga vulnerabilidades de seguridad y que falten correcciones importantes que hagan que Windows funcione mejor.</span><span class="sxs-lookup"><span data-stu-id="8fa91-117">This device may have security vulnerabilities and may be missing important fixes that make Windows run better.</span></span> <span data-ttu-id="8fa91-118">Cuando un dispositivo está ejecutando una versión de Windows que ya no se admite, siempre se devuelve **UpdateImpactLevel \_ High** .</span><span class="sxs-lookup"><span data-stu-id="8fa91-118">When a device is running a version of Windows that is no longer supported, **UpdateImpactLevel\_High** is always returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8fa91-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8fa91-119">Remarks</span></span>

<span data-ttu-id="8fa91-120">Cuando se llama a [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) , se devuelve una estructura [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) .</span><span class="sxs-lookup"><span data-stu-id="8fa91-120">When [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) is called, an [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structure is returned.</span></span> <span data-ttu-id="8fa91-121">Dentro de la estructura hay un **assessmentForCurrent** y un **assessmentForUpToDate**.</span><span class="sxs-lookup"><span data-stu-id="8fa91-121">Within the structure there is an **assessmentForCurrent** and **assessmentForUpToDate**.</span></span> <span data-ttu-id="8fa91-122">Ambas son estructuras [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) .</span><span class="sxs-lookup"><span data-stu-id="8fa91-122">Both of these are [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) structures.</span></span> <span data-ttu-id="8fa91-123">Ambos miembros tienen una enumeración **UpdateImpactLevel** , que indica un impacto alto, medio, bajo o no en un dispositivo que ejecuta un sistema operativo obsoleto.</span><span class="sxs-lookup"><span data-stu-id="8fa91-123">Both members have an **UpdateImpactLevel** enumeration, which indicates a high, medium, low or no impact for a device running an out-of-date OS.</span></span> <span data-ttu-id="8fa91-124">Estos niveles vienen determinados por el valor de **daysOutOfDate**.</span><span class="sxs-lookup"><span data-stu-id="8fa91-124">The These levels are determined by the value of **daysOutOfDate**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fa91-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fa91-125">Requirements</span></span>



| <span data-ttu-id="8fa91-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fa91-126">Requirement</span></span> | <span data-ttu-id="8fa91-127">Value</span><span class="sxs-lookup"><span data-stu-id="8fa91-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fa91-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8fa91-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8fa91-129">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="8fa91-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8fa91-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8fa91-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8fa91-131">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="8fa91-131">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8fa91-132">IDL</span><span class="sxs-lookup"><span data-stu-id="8fa91-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8fa91-133"><dt>WaaSAPI. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8fa91-133"><dt>WaaSAPI.idl</dt></span></span> </dl> |



 

 




