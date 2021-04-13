---
description: Envía un trabajo a un sistema operativo para su ejecución en una fecha y hora especificadas en el futuro.
ms.assetid: 9d582fbb-24cb-401d-8b77-af7671a24e6d
ms.tgt_platform: multiple
title: Método Create de la clase Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9f1acae94ea29d2d57b2952c0b0adc267ad3066c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360069"
---
# <a name="create-method-of-the-win32_scheduledjob-class"></a><span data-ttu-id="9cadf-103">Método Create de la \_ clase Win32 ScheduledJob</span><span class="sxs-lookup"><span data-stu-id="9cadf-103">Create method of the Win32\_ScheduledJob class</span></span>

<span data-ttu-id="9cadf-104">El método **crear** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) envía un trabajo a un sistema operativo para su ejecución en una fecha y hora especificadas en el futuro.</span><span class="sxs-lookup"><span data-stu-id="9cadf-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method submits a job to an operating system for execution at a specified time and date in the future.</span></span> <span data-ttu-id="9cadf-105">Este método requiere que el servicio de programación se inicie en el equipo al que se envía el trabajo.</span><span class="sxs-lookup"><span data-stu-id="9cadf-105">This method requires that the schedule service be started on the computer to which the job is submitted.</span></span>

<span data-ttu-id="9cadf-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="9cadf-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9cadf-107">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9cadf-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9cadf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9cadf-108">Syntax</span></span>


```mof
uint32 Create(
  [in]           string   Command,
  [in]           datetime StartTime,
  [in, optional] boolean  RunRepeatedly,
  [in, optional] uint32   DaysOfWeek,
  [in, optional] uint32   DaysOfMonth,
  [in, optional] boolean  InteractWithDesktop,
  [out]          uint32   JobId
);
```



## <a name="parameters"></a><span data-ttu-id="9cadf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9cadf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cadf-110">*Comando* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9cadf-110">*Command* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cadf-111">Nombre del comando, programa por lotes, archivo binario y parámetros de la línea de comandos que el servicio de programación utiliza para invocar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="9cadf-111">Name of the command, batch program, or binary file and command-line parameters that the schedule service uses to invoke the job.</span></span>

<span data-ttu-id="9cadf-112">Ejemplo: "Defrag/q/f".</span><span class="sxs-lookup"><span data-stu-id="9cadf-112">Example: "defrag /q /f".</span></span>

</dd> <dt>

<span data-ttu-id="9cadf-113">*StartTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9cadf-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cadf-114">Hora universal coordinada (hora UTC) para ejecutar un trabajo.</span><span class="sxs-lookup"><span data-stu-id="9cadf-114">Coordinated Universal Time (UTC) time to run a job.</span></span> <span data-ttu-id="9cadf-115">El formato debe ser: "AAAAMMDDHHMMSS. MMMMMM (+-) OOO ", donde" AAAAMMDD "debe reemplazarse por" \* \* \* \* \* \* \* \* ".</span><span class="sxs-lookup"><span data-stu-id="9cadf-115">The form must be: "YYYYMMDDHHMMSS.MMMMMM(+-)OOO", where "YYYYMMDD" must be replaced by "\*\*\*\*\*\*\*\*".</span></span> <span data-ttu-id="9cadf-116">Por ejemplo: " \* \* \* \* \* \* \* \* 143000.000000-420" especifica 14,30 (2:30 P.M.) PST con horario de verano en vigor.</span><span class="sxs-lookup"><span data-stu-id="9cadf-116">For example: "\*\*\*\*\*\*\*\*143000.000000-420" specifies 14.30 (2:30 P.M.) PST with daylight savings time in effect.</span></span>

<span data-ttu-id="9cadf-117">La sección "(+-) OOO" del valor de la propiedad StartTime es la diferencia actual de la conversión de hora local.</span><span class="sxs-lookup"><span data-stu-id="9cadf-117">The "(+-)OOO" section of the StartTime property value is the current bias for local time translation.</span></span> <span data-ttu-id="9cadf-118">La diferencia es la diferencia entre la hora UTC y la hora local.</span><span class="sxs-lookup"><span data-stu-id="9cadf-118">The bias is the difference between the UTC time and the local time.</span></span> <span data-ttu-id="9cadf-119">Para calcular la diferencia de la zona horaria, multiplique el número de horas que la zona horaria está por encima o por detrás de la hora del meridiano de Greenwich (GMT) en 60 (use un número positivo para el número de horas si la zona horaria está por detrás de GMT y un número negativo si la zona horaria está tras la hora GMT).</span><span class="sxs-lookup"><span data-stu-id="9cadf-119">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="9cadf-120">Agregue un 60 adicional al cálculo si la zona horaria usa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="9cadf-120">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="9cadf-121">Por ejemplo, la zona horaria estándar del Pacífico es de ocho horas tras la hora GMT, por lo que la diferencia es igual a-420 (-8 \* 60 + 60) cuando el horario de verano está en uso y-480 (-8 \* 60) cuando el horario de verano no está en uso.</span><span class="sxs-lookup"><span data-stu-id="9cadf-121">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="9cadf-122">También puede determinar el valor de la diferencia consultando la propiedad bias de la clase [**\_ TimeZone de Win32**](win32-timezone.md) .</span><span class="sxs-lookup"><span data-stu-id="9cadf-122">You can also determine the value of the bias by querying the bias property of the [**Win32\_TimeZone**](win32-timezone.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="9cadf-123">*RunRepeatedly* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9cadf-123">*RunRepeatedly* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cadf-124">Si **es true**, un trabajo programado se ejecuta repetidamente en días específicos.</span><span class="sxs-lookup"><span data-stu-id="9cadf-124">If **True**, a scheduled job runs repeatedly on specific days.</span></span> <span data-ttu-id="9cadf-125">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="9cadf-125">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="9cadf-126">*DaysOfWeek* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9cadf-126">*DaysOfWeek* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cadf-127">Días de la semana en los que está programada la ejecución de un trabajo; solo se usa cuando el parámetro *RunRepeatedly* es **true**.</span><span class="sxs-lookup"><span data-stu-id="9cadf-127">Days of the week when a job is scheduled to run; used only when the *RunRepeatedly* parameter is **True**.</span></span> <span data-ttu-id="9cadf-128">Para programar un trabajo durante más de un día de la semana, combine los valores adecuados en un operador lógico OR.</span><span class="sxs-lookup"><span data-stu-id="9cadf-128">To schedule a job for more than one day of the week, join the appropriate values in a logical OR.</span></span> <span data-ttu-id="9cadf-129">Por ejemplo, para programar un trabajo para los martes y viernes, el valor de *DaysOfWeek* es 2 o 16.</span><span class="sxs-lookup"><span data-stu-id="9cadf-129">For example, to schedule a job for Tuesdays and Fridays, the value of *DaysOfWeek* are 2 OR 16.</span></span>

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="9cadf-130">**Lunes** (1)</span><span class="sxs-lookup"><span data-stu-id="9cadf-130">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="9cadf-131">**Martes** (2)</span><span class="sxs-lookup"><span data-stu-id="9cadf-131">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="9cadf-132">**Miércoles** (4)</span><span class="sxs-lookup"><span data-stu-id="9cadf-132">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="9cadf-133">**Jueves** (8)</span><span class="sxs-lookup"><span data-stu-id="9cadf-133">**Thursday** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="9cadf-134">**Viernes** (16)</span><span class="sxs-lookup"><span data-stu-id="9cadf-134">**Friday** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="9cadf-135">**Sábado** (32)</span><span class="sxs-lookup"><span data-stu-id="9cadf-135">**Saturday** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="9cadf-136">**Domingo** (64)</span><span class="sxs-lookup"><span data-stu-id="9cadf-136">**Sunday** (64)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="9cadf-137">*DaysOfMonth* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9cadf-137">*DaysOfMonth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cadf-138">Días del mes en que se programa la ejecución de un trabajo; solo se usa cuando el parámetro *RunRepeatedly* es **true**.</span><span class="sxs-lookup"><span data-stu-id="9cadf-138">Days of the month when a job is scheduled to run; used only when the *RunRepeatedly* parameter is **True**.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="9cadf-139"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="9cadf-139"><span id="1"></span>**1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-140">Día 1 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-140">Day 1 of a month</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="9cadf-141"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="9cadf-141"><span id="2"></span>**2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-142">Día 2 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-142">Day 2 of a month</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="9cadf-143"><span id="3"></span>**3** (4)</span><span class="sxs-lookup"><span data-stu-id="9cadf-143"><span id="3"></span>**3** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-144">Día 3 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-144">Day 3 of a month</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="9cadf-145"><span id="4"></span>**4** (8)</span><span class="sxs-lookup"><span data-stu-id="9cadf-145"><span id="4"></span>**4** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-146">Día 4 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-146">Day 4 of a month</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="9cadf-147"><span id="5"></span>**5** (16)</span><span class="sxs-lookup"><span data-stu-id="9cadf-147"><span id="5"></span>**5** (16)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-148">Día 5 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-148">Day 5 of a month</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="9cadf-149"><span id="6"></span>**6** (32)</span><span class="sxs-lookup"><span data-stu-id="9cadf-149"><span id="6"></span>**6** (32)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-150">Día 6 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-150">Day 6 of a month</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="9cadf-151"><span id="7"></span>**7** (64)</span><span class="sxs-lookup"><span data-stu-id="9cadf-151"><span id="7"></span>**7** (64)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-152">Día 7 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-152">Day 7 of a month</span></span>

</dd> <dt>

<span id="8"></span>

<span data-ttu-id="9cadf-153"><span id="8"></span>**8** (128)</span><span class="sxs-lookup"><span data-stu-id="9cadf-153"><span id="8"></span>**8** (128)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-154">Día 8 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-154">Day 8 of a month</span></span>

</dd> <dt>

<span id="9"></span>

<span data-ttu-id="9cadf-155"><span id="9"></span>**9** (256)</span><span class="sxs-lookup"><span data-stu-id="9cadf-155"><span id="9"></span>**9** (256)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-156">Día 9 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-156">Day 9 of a month</span></span>

</dd> <dt>

<span id="10"></span>

<span data-ttu-id="9cadf-157"><span id="10"></span>**10** (512)</span><span class="sxs-lookup"><span data-stu-id="9cadf-157"><span id="10"></span>**10** (512)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-158">Día 10 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-158">Day 10 of a month</span></span>

</dd> <dt>

<span id="11"></span>

<span data-ttu-id="9cadf-159"><span id="11"></span>**11** (1024)</span><span class="sxs-lookup"><span data-stu-id="9cadf-159"><span id="11"></span>**11** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-160">Día 11 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-160">Day 11 of a month</span></span>

</dd> <dt>

<span id="12"></span>

<span data-ttu-id="9cadf-161"><span id="12"></span>**12** (2048)</span><span class="sxs-lookup"><span data-stu-id="9cadf-161"><span id="12"></span>**12** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-162">Día 12 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-162">Day 12 of a month</span></span>

</dd> <dt>

<span id="13"></span>

<span data-ttu-id="9cadf-163"><span id="13"></span>**13** (4096)</span><span class="sxs-lookup"><span data-stu-id="9cadf-163"><span id="13"></span>**13** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-164">Día 13 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-164">Day 13 of a month</span></span>

</dd> <dt>

<span id="14"></span>

<span data-ttu-id="9cadf-165"><span id="14"></span>**14** (8192)</span><span class="sxs-lookup"><span data-stu-id="9cadf-165"><span id="14"></span>**14** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-166">Día 14 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-166">Day 14 of a month</span></span>

</dd> <dt>

<span id="15"></span>

<span data-ttu-id="9cadf-167"><span id="15"></span>**15** (16384)</span><span class="sxs-lookup"><span data-stu-id="9cadf-167"><span id="15"></span>**15** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-168">Día 15 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-168">Day 15 of a month</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="9cadf-169"><span id="16"></span>**16** (32768)</span><span class="sxs-lookup"><span data-stu-id="9cadf-169"><span id="16"></span>**16** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-170">Día 16 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-170">Day 16 of a month</span></span>

</dd> <dt>

<span id="17"></span>

<span data-ttu-id="9cadf-171"><span id="17"></span>**17** (65536)</span><span class="sxs-lookup"><span data-stu-id="9cadf-171"><span id="17"></span>**17** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-172">Día 17 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-172">Day 17 of a month</span></span>

</dd> <dt>

<span id="18"></span>

<span data-ttu-id="9cadf-173"><span id="18"></span>**18** (131072)</span><span class="sxs-lookup"><span data-stu-id="9cadf-173"><span id="18"></span>**18** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-174">Día 18 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-174">Day 18 of a month</span></span>

</dd> <dt>

<span id="19"></span>

<span data-ttu-id="9cadf-175"><span id="19"></span>**19** (262144)</span><span class="sxs-lookup"><span data-stu-id="9cadf-175"><span id="19"></span>**19** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-176">Día 19 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-176">Day 19 of a month</span></span>

</dd> <dt>

<span id="20"></span>

<span data-ttu-id="9cadf-177"><span id="20"></span>**20** (524288)</span><span class="sxs-lookup"><span data-stu-id="9cadf-177"><span id="20"></span>**20** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-178">Día 20 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-178">Day 20 of a month</span></span>

</dd> <dt>

<span id="21"></span>

<span data-ttu-id="9cadf-179"><span id="21"></span>**21** (1048576)</span><span class="sxs-lookup"><span data-stu-id="9cadf-179"><span id="21"></span>**21** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-180">Día 21 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-180">Day 21 of a month</span></span>

</dd> <dt>

<span id="22"></span>

<span data-ttu-id="9cadf-181"><span id="22"></span>**22** (2097152)</span><span class="sxs-lookup"><span data-stu-id="9cadf-181"><span id="22"></span>**22** (2097152)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-182">Día 22 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-182">Day 22 of a month</span></span>

</dd> <dt>

<span id="23"></span>

<span data-ttu-id="9cadf-183"><span id="23"></span>**23** (4194304)</span><span class="sxs-lookup"><span data-stu-id="9cadf-183"><span id="23"></span>**23** (4194304)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-184">Día 23 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-184">Day 23 of a month</span></span>

</dd> <dt>

<span id="24"></span>

<span data-ttu-id="9cadf-185"><span id="24"></span>**24** (8388608)</span><span class="sxs-lookup"><span data-stu-id="9cadf-185"><span id="24"></span>**24** (8388608)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-186">Día 24 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-186">Day 24 of a month</span></span>

</dd> <dt>

<span id="25"></span>

<span data-ttu-id="9cadf-187"><span id="25"></span>**25** (16777216)</span><span class="sxs-lookup"><span data-stu-id="9cadf-187"><span id="25"></span>**25** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-188">Día 25 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-188">Day 25 of a month</span></span>

</dd> <dt>

<span id="26"></span>

<span data-ttu-id="9cadf-189"><span id="26"></span>**26** (33554432)</span><span class="sxs-lookup"><span data-stu-id="9cadf-189"><span id="26"></span>**26** (33554432)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-190">Día 26 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-190">Day 26 of a month</span></span>

</dd> <dt>

<span id="27"></span>

<span data-ttu-id="9cadf-191"><span id="27"></span>**27** (67108864)</span><span class="sxs-lookup"><span data-stu-id="9cadf-191"><span id="27"></span>**27** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-192">Día 27 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-192">Day 27 of a month</span></span>

</dd> <dt>

<span id="28"></span>

<span data-ttu-id="9cadf-193"><span id="28"></span>**28** (134217728)</span><span class="sxs-lookup"><span data-stu-id="9cadf-193"><span id="28"></span>**28** (134217728)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-194">Día 28 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-194">Day 28 of a month</span></span>

</dd> <dt>

<span id="29"></span>

<span data-ttu-id="9cadf-195"><span id="29"></span>**29** (268435456)</span><span class="sxs-lookup"><span data-stu-id="9cadf-195"><span id="29"></span>**29** (268435456)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-196">Día 29 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-196">Day 29 of a month</span></span>

</dd> <dt>

<span id="30"></span>

<span data-ttu-id="9cadf-197"><span id="30"></span>**30** (536870912)</span><span class="sxs-lookup"><span data-stu-id="9cadf-197"><span id="30"></span>**30** (536870912)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-198">Día 30 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-198">Day 30 of a month</span></span>

</dd> <dt>

<span id="31"></span>

<span data-ttu-id="9cadf-199"><span id="31"></span>**31** (1073741824)</span><span class="sxs-lookup"><span data-stu-id="9cadf-199"><span id="31"></span>**31** (1073741824)</span></span>


</dt> <dd>

<span data-ttu-id="9cadf-200">Día 31 de un mes</span><span class="sxs-lookup"><span data-stu-id="9cadf-200">Day 31 of a month</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9cadf-201">*InteractWithDesktop* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9cadf-201">*InteractWithDesktop* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9cadf-202">Si es **true**, el trabajo especificado debe ser interactivo, lo que significa que un usuario puede proporcionar la entrada a un trabajo programado mientras se está ejecutando el trabajo.</span><span class="sxs-lookup"><span data-stu-id="9cadf-202">If **True**, the specified job should be interactive, which means that a user can give input to a scheduled job while the job is executing.</span></span> <span data-ttu-id="9cadf-203">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="9cadf-203">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="9cadf-204">*JobID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9cadf-204">*JobId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cadf-205">Número de identificación de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="9cadf-205">Identifier number of a job.</span></span> <span data-ttu-id="9cadf-206">Este parámetro es un identificador de un trabajo programado en un equipo.</span><span class="sxs-lookup"><span data-stu-id="9cadf-206">This parameter is a handle to a job being scheduled on a computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cadf-207">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9cadf-207">Return value</span></span>

<span data-ttu-id="9cadf-208">Devuelve un valor de 0 (cero) cuando se realiza correctamente y un número diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="9cadf-208">Returns a value of 0 (zero) when successful, and a different number to indicate an error.</span></span> <span data-ttu-id="9cadf-209">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9cadf-209">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9cadf-210">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9cadf-210">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9cadf-211">**Completado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="9cadf-211">**Successful completion**</span></span>
</dt> <dd>

<span data-ttu-id="9cadf-212">0</span><span class="sxs-lookup"><span data-stu-id="9cadf-212">0</span></span>

<span data-ttu-id="9cadf-213">Se acepta la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9cadf-213">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="9cadf-214">**No admitido**</span><span class="sxs-lookup"><span data-stu-id="9cadf-214">**Not supported**</span></span>
</dt> <dd>

<span data-ttu-id="9cadf-215">1</span><span class="sxs-lookup"><span data-stu-id="9cadf-215">1</span></span>

<span data-ttu-id="9cadf-216">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9cadf-216">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9cadf-217">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="9cadf-217">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="9cadf-218">2</span><span class="sxs-lookup"><span data-stu-id="9cadf-218">2</span></span>

<span data-ttu-id="9cadf-219">El usuario no tiene el acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="9cadf-219">The user does not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="9cadf-220">**Error desconocido**</span><span class="sxs-lookup"><span data-stu-id="9cadf-220">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="9cadf-221">8</span><span class="sxs-lookup"><span data-stu-id="9cadf-221">8</span></span>

<span data-ttu-id="9cadf-222">Proceso interactivo.</span><span class="sxs-lookup"><span data-stu-id="9cadf-222">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="9cadf-223">**No se encuentra la ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="9cadf-223">**Path not found**</span></span>
</dt> <dd>

<span data-ttu-id="9cadf-224">9</span><span class="sxs-lookup"><span data-stu-id="9cadf-224">9</span></span>

<span data-ttu-id="9cadf-225">No se encuentra la ruta de acceso al directorio del archivo ejecutable del servicio.</span><span class="sxs-lookup"><span data-stu-id="9cadf-225">The directory path to the service executable file cannot be found.</span></span>

</dd> <dt>

<span data-ttu-id="9cadf-226">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="9cadf-226">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9cadf-227">21</span><span class="sxs-lookup"><span data-stu-id="9cadf-227">21</span></span>

<span data-ttu-id="9cadf-228">Se han pasado parámetros no válidos al servicio.</span><span class="sxs-lookup"><span data-stu-id="9cadf-228">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9cadf-229">**Servicio no iniciado**</span><span class="sxs-lookup"><span data-stu-id="9cadf-229">**Service not started**</span></span>
</dt> <dd>

<span data-ttu-id="9cadf-230">22</span><span class="sxs-lookup"><span data-stu-id="9cadf-230">22</span></span>

<span data-ttu-id="9cadf-231">La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.</span><span class="sxs-lookup"><span data-stu-id="9cadf-231">The account that this service runs under is invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="9cadf-232">**Otros**</span><span class="sxs-lookup"><span data-stu-id="9cadf-232">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="9cadf-233">23 4294967295</span><span class="sxs-lookup"><span data-stu-id="9cadf-233">23 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9cadf-234">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9cadf-234">Remarks</span></span>

<span data-ttu-id="9cadf-235">Si el trabajo programado inicia un programa interactivo como el Bloc de notas, la propiedad **InteractWithDeskto** debe establecerse en **true** o la pantalla del programa no está visible.</span><span class="sxs-lookup"><span data-stu-id="9cadf-235">If your scheduled job starts an interactive program such as Notepad, then the **InteractWithDeskto** property must be set to **True** or the program's screen is not visible.</span></span> <span data-ttu-id="9cadf-236">El proceso sigue apareciendo en el **Administrador de tareas** aunque no aparezca en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="9cadf-236">The process still appears in the **Task Manager** even if it does not appear on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cadf-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cadf-237">Requirements</span></span>



| <span data-ttu-id="9cadf-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cadf-238">Requirement</span></span> | <span data-ttu-id="9cadf-239">Value</span><span class="sxs-lookup"><span data-stu-id="9cadf-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cadf-240">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cadf-240">Minimum supported client</span></span><br/> | <span data-ttu-id="9cadf-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cadf-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9cadf-242">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cadf-242">Minimum supported server</span></span><br/> | <span data-ttu-id="9cadf-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cadf-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9cadf-244">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9cadf-244">Namespace</span></span><br/>                | <span data-ttu-id="9cadf-245">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9cadf-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9cadf-246">MOF</span><span class="sxs-lookup"><span data-stu-id="9cadf-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9cadf-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9cadf-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9cadf-248">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9cadf-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cadf-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cadf-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cadf-250">Vea también</span><span class="sxs-lookup"><span data-stu-id="9cadf-250">See also</span></span>

<dl> <dt>

<span data-ttu-id="9cadf-251">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9cadf-251">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9cadf-252">**Win32 \_ ScheduledJob**</span><span class="sxs-lookup"><span data-stu-id="9cadf-252">**Win32\_ScheduledJob**</span></span>](win32-scheduledjob.md)
</dt> </dl>

 

