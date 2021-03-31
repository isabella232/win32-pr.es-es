---
title: SessionStateChangeTrigger. Delay (propiedad)
description: En el caso de scripting, obtiene o establece un valor que indica cuánto tiempo se produce un retraso antes de que se inicie una tarea después de que se detecte un cambio de estado de sesión Terminal Server.
ms.assetid: 3a17884f-fd74-491a-99dc-dce300a2cc77
keywords:
- Propiedad Delay Programador de tareas
- Propiedad Delay Programador de tareas, objeto SessionStateChangeTrigger
- Programador de tareas de objeto SessionStateChangeTrigger, propiedad Delay
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd5afde8ebd2884aee19fbdafb785355b9fedb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150048"
---
# <a name="sessionstatechangetriggerdelay-property"></a><span data-ttu-id="753a4-106">SessionStateChangeTrigger. Delay (propiedad)</span><span class="sxs-lookup"><span data-stu-id="753a4-106">SessionStateChangeTrigger.Delay property</span></span>

<span data-ttu-id="753a4-107">En el caso de scripting, obtiene o establece un valor que indica cuánto tiempo se produce un retraso antes de que se inicie una tarea después de que se detecte un cambio de estado de sesión Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="753a4-107">For scripting, gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected.</span></span> <span data-ttu-id="753a4-108">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="753a4-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="753a4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="753a4-109">Syntax</span></span>


```VB
SessionStateChangeTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="753a4-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="753a4-110">Property value</span></span>

<span data-ttu-id="753a4-111">Retraso que tiene lugar antes de que se inicie una tarea después de que se detecte un cambio de estado de sesión Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="753a4-111">The delay that takes place before a task is started after a Terminal Server session state change is detected.</span></span>

## <a name="requirements"></a><span data-ttu-id="753a4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="753a4-112">Requirements</span></span>



| <span data-ttu-id="753a4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="753a4-113">Requirement</span></span> | <span data-ttu-id="753a4-114">Value</span><span class="sxs-lookup"><span data-stu-id="753a4-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="753a4-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="753a4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="753a4-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="753a4-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="753a4-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="753a4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="753a4-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="753a4-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="753a4-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="753a4-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="753a4-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="753a4-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="753a4-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="753a4-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="753a4-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="753a4-122"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





