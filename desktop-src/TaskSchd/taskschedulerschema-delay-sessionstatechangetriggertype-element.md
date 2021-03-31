---
title: Elemento Delay (sessionStateChangeTriggerType)
description: Contiene un valor que indica la duración del retraso para una hora de inicio de la tarea, cuando se detecta un cambio de estado de sesión Terminal Server.
ms.assetid: 7fb87c4c-0b69-4c5b-b038-d61fb7c4ab9a
keywords:
- Programador de tareas del elemento Delay
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03f230465f2e2b49ce83f1af358dfa1f84f21433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151185"
---
# <a name="delay-sessionstatechangetriggertype-element"></a><span data-ttu-id="382af-104">Elemento Delay (sessionStateChangeTriggerType)</span><span class="sxs-lookup"><span data-stu-id="382af-104">Delay (sessionStateChangeTriggerType) Element</span></span>

<span data-ttu-id="382af-105">Contiene un valor que indica la duración del retraso para una hora de inicio de la tarea, cuando se detecta un cambio de estado de sesión Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="382af-105">Contains a value that indicates the delay length for a task start time, when a Terminal Server session state change is detected.</span></span> <span data-ttu-id="382af-106">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="382af-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="382af-107">Para obtener más información acerca del tipo Duration, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="382af-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="382af-108">El elemento **Delay** se define mediante el tipo complejo [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="382af-108">The **Delay** element is defined by the [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="382af-109">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="382af-109">Parent element</span></span>



| <span data-ttu-id="382af-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="382af-110">Element</span></span>                       | <span data-ttu-id="382af-111">Derivado de</span><span class="sxs-lookup"><span data-stu-id="382af-111">Derived from</span></span>                                                                                           | <span data-ttu-id="382af-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="382af-112">Description</span></span>                                                                                      |
|-------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="382af-113">**SessionStateChangeTrigger**</span><span class="sxs-lookup"><span data-stu-id="382af-113">**SessionStateChangeTrigger**</span></span> | [<span data-ttu-id="382af-114">**sessionStateChangeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="382af-114">**sessionStateChangeTriggerType**</span></span>](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | <span data-ttu-id="382af-115">Especifica un desencadenador que inicia una tarea cuando se cambia el estado de una sesión de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="382af-115">Specifies a trigger that starts a task when a Terminal Server session changes state.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="382af-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="382af-116">Remarks</span></span>

<span data-ttu-id="382af-117">Para el desarrollo de scripting, el retraso del desencadenador de cambio de estado de sesión se especifica mediante la propiedad [**SessionStateChangeTrigger. Delay**](sessionstatechangetrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="382af-117">For scripting development, the session state change trigger delay is specified using the [**SessionStateChangeTrigger.Delay**](sessionstatechangetrigger-delay.md) property.</span></span>

<span data-ttu-id="382af-118">En el desarrollo de C++, el retraso del desencadenador de cambio de estado de sesión se especifica mediante la [**propiedad Delay de ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).</span><span class="sxs-lookup"><span data-stu-id="382af-118">For C++ development, the session state change trigger delay is specified using the [**Delay property of ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="382af-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="382af-119">Requirements</span></span>



| <span data-ttu-id="382af-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="382af-120">Requirement</span></span> | <span data-ttu-id="382af-121">Value</span><span class="sxs-lookup"><span data-stu-id="382af-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="382af-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="382af-122">Minimum supported client</span></span><br/> | <span data-ttu-id="382af-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="382af-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="382af-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="382af-124">Minimum supported server</span></span><br/> | <span data-ttu-id="382af-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="382af-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





