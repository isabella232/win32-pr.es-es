---
title: Elemento RandomDelay (calendarTriggerType)
description: Contiene el tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. | Elemento RandomDelay (calendarTriggerType)
ms.assetid: 497fab4e-ad63-43e6-a086-2d77b43662d9
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
ms.openlocfilehash: d71149bfeceeb6c17cafa27f56bb15bb184ead06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362275"
---
# <a name="randomdelay-calendartriggertype-element"></a><span data-ttu-id="49676-105">Elemento RandomDelay (calendarTriggerType)</span><span class="sxs-lookup"><span data-stu-id="49676-105">RandomDelay (calendarTriggerType) Element</span></span>

<span data-ttu-id="49676-106">Contiene el tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="49676-106">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="49676-107">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="49676-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="49676-108">Para obtener más información acerca del tipo Duration, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="49676-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

<span data-ttu-id="49676-109">El elemento **RandomDelay** se define mediante el tipo complejo de [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="49676-109">The **RandomDelay** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="49676-110">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="49676-110">Parent element</span></span>



| <span data-ttu-id="49676-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="49676-111">Element</span></span>                                                                                            | <span data-ttu-id="49676-112">Derivado de</span><span class="sxs-lookup"><span data-stu-id="49676-112">Derived from</span></span>                                                                       | <span data-ttu-id="49676-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="49676-113">Description</span></span>                                                                                 |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49676-114">**CalendarTrigger (triggerGroup)**</span><span class="sxs-lookup"><span data-stu-id="49676-114">**CalendarTrigger (triggerGroup)**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="49676-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="49676-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="49676-116">Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.</span><span class="sxs-lookup"><span data-stu-id="49676-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="49676-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49676-117">Requirements</span></span>



| <span data-ttu-id="49676-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="49676-118">Requirement</span></span> | <span data-ttu-id="49676-119">Value</span><span class="sxs-lookup"><span data-stu-id="49676-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49676-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49676-120">Minimum supported client</span></span><br/> | <span data-ttu-id="49676-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="49676-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="49676-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49676-122">Minimum supported server</span></span><br/> | <span data-ttu-id="49676-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="49676-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





