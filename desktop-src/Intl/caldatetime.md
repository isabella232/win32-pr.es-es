---
description: Desusado. Representa un instante de tiempo, normalmente expresado como una fecha y hora del día y un calendario correspondiente.
ms.assetid: a714ff32-2b1f-4256-931e-324d64daf2ac
title: Estructura CALDATETIME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CALDATETIME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e3f0099a8e1dd7794b960af3d753085f2a32eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689565"
---
# <a name="caldatetime-structure"></a><span data-ttu-id="c3bd9-104">Estructura CALDATETIME</span><span class="sxs-lookup"><span data-stu-id="c3bd9-104">CALDATETIME structure</span></span>

<span data-ttu-id="c3bd9-105">En desuso.</span><span class="sxs-lookup"><span data-stu-id="c3bd9-105">Deprecated.</span></span> <span data-ttu-id="c3bd9-106">Representa un instante de tiempo, normalmente expresado como una fecha y hora del día y un calendario correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c3bd9-106">Represents an instant in time, typically expressed as a date and time of day and a corresponding calendar.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3bd9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3bd9-107">Syntax</span></span>


```C++
typedef struct _caldatetime {
  CALID CalId;
  UINT  Era;
  UINT  Year;
  UINT  Month;
  UINT  Day;
  UINT  DayOfWeek;
  UINT  Hour;
  UINT  Minute;
  UINT  Second;
  ULONG Tick;
} CALDATETIME, *LPCALDATETIME;
```



## <a name="members"></a><span data-ttu-id="c3bd9-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c3bd9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3bd9-109">**CalId**</span><span class="sxs-lookup"><span data-stu-id="c3bd9-109">**CalId**</span></span>
</dt> <dd>

<span data-ttu-id="c3bd9-110">[Identificador del calendario](calendar-identifiers.md) para el instante en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="c3bd9-110">The [calendar identifier](calendar-identifiers.md) for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="c3bd9-111">**Período**</span><span class="sxs-lookup"><span data-stu-id="c3bd9-111">**Era**</span></span>
</dt> <dd>

<span data-ttu-id="c3bd9-112">Información de la era para el instante en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="c3bd9-112">The era information for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="c3bd9-113">**Anual**</span><span class="sxs-lookup"><span data-stu-id="c3bd9-113">**Year**</span></span>
</dt> <dd>

<span data-ttu-id="c3bd9-114">Año para el instante en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="c3bd9-114">The year for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="c3bd9-115">**Mensuales**</span><span class="sxs-lookup"><span data-stu-id="c3bd9-115">**Month**</span></span>
</dt> <dd>

<span data-ttu-id="c3bd9-116">Mes para el instante en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="c3bd9-116">The month for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="c3bd9-117">**Day**</span><span class="sxs-lookup"><span data-stu-id="c3bd9-117">**Day**</span></span>
</dt> <dd>

<span data-ttu-id="c3bd9-118">Día del instante en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="c3bd9-118">The day for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="c3bd9-119">**DayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="c3bd9-119">**DayOfWeek**</span></span>
</dt> <dd>

<span data-ttu-id="c3bd9-120">El día de la semana para el instante en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="c3bd9-120">The day of the week for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="c3bd9-121">**Hora**</span><span class="sxs-lookup"><span data-stu-id="c3bd9-121">**Hour**</span></span>
</dt> <dd>

<span data-ttu-id="c3bd9-122">Hora del instante en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="c3bd9-122">The hour for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="c3bd9-123">**Minute**</span><span class="sxs-lookup"><span data-stu-id="c3bd9-123">**Minute**</span></span>
</dt> <dd>

<span data-ttu-id="c3bd9-124">Minuto para el instante en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="c3bd9-124">The minute for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="c3bd9-125">**Segundo**</span><span class="sxs-lookup"><span data-stu-id="c3bd9-125">**Second**</span></span>
</dt> <dd>

<span data-ttu-id="c3bd9-126">Segundo para el instante en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="c3bd9-126">The second for the instant in time.</span></span>

</dd> <dt>

<span data-ttu-id="c3bd9-127">**Ticker**</span><span class="sxs-lookup"><span data-stu-id="c3bd9-127">**Tick**</span></span>
</dt> <dd>

<span data-ttu-id="c3bd9-128">El paso del instante en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="c3bd9-128">The tick for the instant in time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3bd9-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3bd9-129">Requirements</span></span>



| <span data-ttu-id="c3bd9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3bd9-130">Requirement</span></span> | <span data-ttu-id="c3bd9-131">Value</span><span class="sxs-lookup"><span data-stu-id="c3bd9-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c3bd9-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3bd9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c3bd9-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c3bd9-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c3bd9-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3bd9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c3bd9-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c3bd9-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3bd9-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3bd9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3bd9-137">Estructuras de soporte de National Language</span><span class="sxs-lookup"><span data-stu-id="c3bd9-137">National Language Support Structures</span></span>](national-language-support-structures.md)
</dt> </dl>

 

 




