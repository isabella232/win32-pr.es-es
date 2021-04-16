---
title: Propiedad TimeTrigger. RandomDelay
description: En el caso de scripting, obtiene o establece un tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador. | Propiedad TimeTrigger. RandomDelay
ms.assetid: ee55dd85-9696-4872-8670-f919fca7481d
keywords:
- Programador de tareas de la propiedad RandomDelay
- Programador de tareas de la propiedad RandomDelay, objeto TimeTrigger
- Programador de tareas de objeto TimeTrigger, propiedad RandomDelay
topic_type:
- apiref
api_name:
- TimeTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39c4acf4f38670332e723ac0824276695919cb1d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678706"
---
# <a name="timetriggerrandomdelay-property"></a><span data-ttu-id="29d04-107">Propiedad TimeTrigger. RandomDelay</span><span class="sxs-lookup"><span data-stu-id="29d04-107">TimeTrigger.RandomDelay property</span></span>

<span data-ttu-id="29d04-108">En el caso de scripting, obtiene o establece un tiempo de retraso que se agrega aleatoriamente a la hora de inicio del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="29d04-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="29d04-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29d04-109">Syntax</span></span>


```VB
TimeTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="29d04-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="29d04-110">Property value</span></span>

<span data-ttu-id="29d04-111">Tiempo de retardo que se agrega aleatoriamente a la hora de inicio del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="29d04-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="29d04-112">El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años. nM es el número de meses, nD es el número de días, ' t ' es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="29d04-112">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="29d04-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29d04-113">Requirements</span></span>



| <span data-ttu-id="29d04-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="29d04-114">Requirement</span></span> | <span data-ttu-id="29d04-115">Value</span><span class="sxs-lookup"><span data-stu-id="29d04-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29d04-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29d04-116">Minimum supported client</span></span><br/> | <span data-ttu-id="29d04-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="29d04-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="29d04-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29d04-118">Minimum supported server</span></span><br/> | <span data-ttu-id="29d04-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="29d04-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="29d04-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="29d04-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="29d04-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="29d04-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="29d04-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="29d04-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29d04-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29d04-123"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





