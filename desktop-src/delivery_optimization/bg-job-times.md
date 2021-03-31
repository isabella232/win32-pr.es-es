---
title: BG_JOB_TIMES estructura (Deliveryoptimization. h)
description: La estructura BG_JOB_TIMES proporciona marcas de tiempo relacionadas con el trabajo.
ms.assetid: 0147478F-C850-4B66-AB15-042C1A81D6B5
keywords:
- Estructura de BG_JOB_TIMES
topic_type:
- apiref
api_name:
- BG_JOB_TIMES
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a2d4e56bb616254537e26fc1ba0fdf5b9e251a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801393"
---
# <a name="bg_job_times-structure"></a><span data-ttu-id="e3d7d-104">Estructura de BG_JOB_TIMES</span><span class="sxs-lookup"><span data-stu-id="e3d7d-104">BG_JOB_TIMES structure</span></span>

<span data-ttu-id="e3d7d-105">La estructura **BG_JOB_TIMES** proporciona marcas de tiempo relacionadas con el trabajo.</span><span class="sxs-lookup"><span data-stu-id="e3d7d-105">The **BG_JOB_TIMES** structure provides job-related time stamps.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3d7d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3d7d-106">Syntax</span></span>


```C++
typedef struct _BG_JOB_TIMES {
  FILETIME CreationTime;
  FILETIME ModificationTime;
  FILETIME TransferCompletionTime;
} BG_JOB_TIMES;
```



## <a name="members"></a><span data-ttu-id="e3d7d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e3d7d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e3d7d-108">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="e3d7d-108">**CreationTime**</span></span>
</dt> <dd>

<span data-ttu-id="e3d7d-109">Hora en que se creó el trabajo.</span><span class="sxs-lookup"><span data-stu-id="e3d7d-109">Time the job was created.</span></span> <span data-ttu-id="e3d7d-110">La hora se especifica como [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="e3d7d-110">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="e3d7d-111">**ModificationTime**</span><span class="sxs-lookup"><span data-stu-id="e3d7d-111">**ModificationTime**</span></span>
</dt> <dd>

<span data-ttu-id="e3d7d-112">Hora en que el trabajo se modificó por última vez o se transfirieron bytes.</span><span class="sxs-lookup"><span data-stu-id="e3d7d-112">Time the job was last modified or bytes were transferred.</span></span> <span data-ttu-id="e3d7d-113">La adición de archivos o la llamada a cualquiera de los métodos set de las interfaces [ \* *IBackgroundCopyJob \** _](/previous-versions//mt811348(v=vs.85)) cambia este valor.</span><span class="sxs-lookup"><span data-stu-id="e3d7d-113">Adding files or calling any of the set methods in the [\**IBackgroundCopyJob\** _](/previous-versions//mt811348(v=vs.85)) interfaces changes this value.</span></span> <span data-ttu-id="e3d7d-114">Además, los cambios en el estado del trabajo y la llamada a los métodos [_ *Suspend* \*](ibackgroundcopyjob-suspend.md), [**resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md)y [**Complete**](ibackgroundcopyjob-complete.md) cambian este valor.</span><span class="sxs-lookup"><span data-stu-id="e3d7d-114">In addition, changes to the state of the job and calling the [_ *Suspend*\*](ibackgroundcopyjob-suspend.md), [**Resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md), and [**Complete**](ibackgroundcopyjob-complete.md) methods change this value.</span></span> <span data-ttu-id="e3d7d-115">La hora se especifica como [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="e3d7d-115">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="e3d7d-116">**TransferCompletionTime**</span><span class="sxs-lookup"><span data-stu-id="e3d7d-116">**TransferCompletionTime**</span></span>
</dt> <dd>

<span data-ttu-id="e3d7d-117">Hora en que el trabajo entró en el estado BG_JOB_STATE_TRANSFERRED.</span><span class="sxs-lookup"><span data-stu-id="e3d7d-117">Time the job entered the BG_JOB_STATE_TRANSFERRED state.</span></span> <span data-ttu-id="e3d7d-118">La hora se especifica como [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="e3d7d-118">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3d7d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3d7d-119">Requirements</span></span>



| <span data-ttu-id="e3d7d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3d7d-120">Requirement</span></span> | <span data-ttu-id="e3d7d-121">Value</span><span class="sxs-lookup"><span data-stu-id="e3d7d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3d7d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3d7d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e3d7d-123">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="e3d7d-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e3d7d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3d7d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e3d7d-125">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="e3d7d-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e3d7d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3d7d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3d7d-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3d7d-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3d7d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3d7d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3d7d-129">**IBackgroundCopyJob::GetTimes**</span><span class="sxs-lookup"><span data-stu-id="e3d7d-129">**IBackgroundCopyJob::GetTimes**</span></span>](ibackgroundcopyjob-gettimes.md)
</dt> </dl>

 

