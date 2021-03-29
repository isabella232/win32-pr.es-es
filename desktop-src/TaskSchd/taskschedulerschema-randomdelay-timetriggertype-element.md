---
title: Elemento RandomDelay (timeTriggerType)
description: Contiene el tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. | Elemento RandomDelay (timeTriggerType)
ms.assetid: 84dffd18-651d-4e81-8c02-6cee9759a9b9
keywords:
- Programador de tareas del elemento RandomDelay
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a28613cb236b6dc8a3ae77dce9452423a992a866
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678731"
---
# <a name="randomdelay-timetriggertype-element"></a><span data-ttu-id="d23de-105">Elemento RandomDelay (timeTriggerType)</span><span class="sxs-lookup"><span data-stu-id="d23de-105">RandomDelay (timeTriggerType) Element</span></span>

<span data-ttu-id="d23de-106">Contiene el tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="d23de-106">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="d23de-107">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="d23de-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="d23de-108">Para obtener más información acerca del tipo Duration, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="d23de-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

<span data-ttu-id="d23de-109">El elemento se define mediante el tipo complejo de [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d23de-109">The element is defined by the [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d23de-110">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="d23de-110">Parent element</span></span>



| <span data-ttu-id="d23de-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="d23de-111">Element</span></span>                                                                                    | <span data-ttu-id="d23de-112">Derivado de</span><span class="sxs-lookup"><span data-stu-id="d23de-112">Derived from</span></span>                                                               | <span data-ttu-id="d23de-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="d23de-113">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="d23de-114">**TimeTrigger (triggerGroup)**</span><span class="sxs-lookup"><span data-stu-id="d23de-114">**TimeTrigger (triggerGroup)**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md) | [<span data-ttu-id="d23de-115">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="d23de-115">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md) | <span data-ttu-id="d23de-116">Especifica un desencadenador que inicia una tarea cuando se activa el desencadenador.</span><span class="sxs-lookup"><span data-stu-id="d23de-116">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d23de-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d23de-117">Remarks</span></span>

<span data-ttu-id="d23de-118">Para el desarrollo de C++, consulte la [**propiedad RandomDelay de ITimeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay).</span><span class="sxs-lookup"><span data-stu-id="d23de-118">For C++ development, see [**RandomDelay Property of ITimeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay).</span></span>

<span data-ttu-id="d23de-119">Para el desarrollo de scripts, vea [**TimeTrigger. RandomDelay**](timetrigger-randomdelay.md).</span><span class="sxs-lookup"><span data-stu-id="d23de-119">For script development, see [**TimeTrigger.RandomDelay**](timetrigger-randomdelay.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d23de-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d23de-120">Requirements</span></span>



| <span data-ttu-id="d23de-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d23de-121">Requirement</span></span> | <span data-ttu-id="d23de-122">Value</span><span class="sxs-lookup"><span data-stu-id="d23de-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d23de-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d23de-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d23de-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d23de-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d23de-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d23de-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d23de-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d23de-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





