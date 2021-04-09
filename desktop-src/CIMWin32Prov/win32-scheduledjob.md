---
description: Representa un trabajo creado con el comando AT.
ms.assetid: 2fa69e3f-9a6c-4aa9-8a6c-ea28eb4342ca
ms.tgt_platform: multiple
title: Win32_ScheduledJob (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob
- Win32_ScheduledJob.Caption
- Win32_ScheduledJob.Description
- Win32_ScheduledJob.InstallDate
- Win32_ScheduledJob.Name
- Win32_ScheduledJob.Status
- Win32_ScheduledJob.ElapsedTime
- Win32_ScheduledJob.Notify
- Win32_ScheduledJob.Owner
- Win32_ScheduledJob.Priority
- Win32_ScheduledJob.TimeSubmitted
- Win32_ScheduledJob.UntilTime
- Win32_ScheduledJob.Command
- Win32_ScheduledJob.DaysOfMonth
- Win32_ScheduledJob.DaysOfWeek
- Win32_ScheduledJob.InteractWithDesktop
- Win32_ScheduledJob.JobId
- Win32_ScheduledJob.JobStatus
- Win32_ScheduledJob.RunRepeatedly
- Win32_ScheduledJob.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50162221e7ca18e07e3599deca2dba67b18ba708
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080125"
---
# <a name="win32_scheduledjob-class"></a><span data-ttu-id="5bc1f-103">\_Clase Win32 ScheduledJob</span><span class="sxs-lookup"><span data-stu-id="5bc1f-103">Win32\_ScheduledJob class</span></span>

<span data-ttu-id="5bc1f-104">La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ ScheduledJob de Win32**   representa un trabajo creado con el comando **at** .</span><span class="sxs-lookup"><span data-stu-id="5bc1f-104">The **Win32\_ScheduledJob** [WMI class](../wmisdk/retrieving-a-class.md) represents a job created with the **AT** command.</span></span>

> [!Note]  
> <span data-ttu-id="5bc1f-105">La **clase \_ ScheduledJob de Win32** no representa un trabajo creado con el Asistente para tareas programadas desde el panel de control.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-105">The **Win32\_ScheduledJob** class does not represent a job created with the Scheduled Task Wizard from the Control Panel.</span></span> <span data-ttu-id="5bc1f-106">No se puede cambiar una tarea creada por WMI en la interfaz de usuario de tareas programadas.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-106">You cannot change a task created by WMI in the Scheduled Tasks UI.</span></span> <span data-ttu-id="5bc1f-107">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-107">For more information, see the Remarks section.</span></span>

 

<span data-ttu-id="5bc1f-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5bc1f-109">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc1f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5bc1f-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E0-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("Delete"), AMENDMENT]
class Win32_ScheduledJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Command;
  uint32   DaysOfMonth;
  uint32   DaysOfWeek;
  boolean  InteractWithDesktop;
  uint32   JobId;
  string   JobStatus;
  boolean  RunRepeatedly;
  datetime StartTime;
};
```

## <a name="members"></a><span data-ttu-id="5bc1f-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="5bc1f-111">Members</span></span>

<span data-ttu-id="5bc1f-112">La **clase \_ ScheduledJob de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5bc1f-112">The **Win32\_ScheduledJob** class has these types of members:</span></span>

-   [<span data-ttu-id="5bc1f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="5bc1f-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="5bc1f-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5bc1f-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5bc1f-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="5bc1f-115">Methods</span></span>

<span data-ttu-id="5bc1f-116">La clase **Win32 \_ ScheduledJob** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-116">The **Win32\_ScheduledJob** class has these methods.</span></span>



| <span data-ttu-id="5bc1f-117">Método</span><span class="sxs-lookup"><span data-stu-id="5bc1f-117">Method</span></span>                                                      | <span data-ttu-id="5bc1f-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="5bc1f-118">Description</span></span>                                                                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5bc1f-119">**A**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-119">**Create**</span></span>](create-method-in-class-win32-scheduledjob.md) | <span data-ttu-id="5bc1f-120">Método de clase que envía un trabajo al sistema operativo para su ejecución en una fecha y hora futuras especificadas.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-120">Class method that submits a job to the operating system for execution at a specified future time and date.</span></span><br/> |
| [<span data-ttu-id="5bc1f-121">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-121">**Delete**</span></span>](delete-method-in-class-win32-scheduledjob.md) | <span data-ttu-id="5bc1f-122">Método de clase que elimina un trabajo programado.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-122">Class method that deletes a scheduled job.</span></span><br/>                                                                 |



 

### <a name="properties"></a><span data-ttu-id="5bc1f-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5bc1f-123">Properties</span></span>

<span data-ttu-id="5bc1f-124">La **clase \_ ScheduledJob de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-124">The **Win32\_ScheduledJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5bc1f-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-128">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-128">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-129">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-129">A short textual description of the object.</span></span>

<span data-ttu-id="5bc1f-130">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1f-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bc1f-131">**Comando**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-131">**Command**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-134">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| \| [**de administración de red en la \_ información**](/windows/win32/api/lmat/ns-lmat-at_info) \| ")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Command**")</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-135">Nombre del comando, programa por lotes o archivo binario (y argumentos de la línea de comandos) que el servicio de programación utiliza para invocar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-135">Name of the command, batch program, or binary file (and command-line arguments) that the schedule service uses to invoke the job.</span></span>

<span data-ttu-id="5bc1f-136">Ejemplo: "**Defrag** **/q/f**"</span><span class="sxs-lookup"><span data-stu-id="5bc1f-136">Example: "**defrag** **/q/f**"</span></span>

</dd> <dt>

<span data-ttu-id="5bc1f-137">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-137">**DaysOfMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-138">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-140">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfMonth**")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**DaysOfMonth**")</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-141">Días del mes en que el trabajo está programado para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-141">Days of the month when the job is scheduled to run.</span></span> <span data-ttu-id="5bc1f-142">Si un trabajo está programado para ejecutarse en varios días del mes, estos valores se pueden combinar en un operador lógico OR.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-142">If a job is scheduled to run on multiple days of the month, these values can be joined in a logical OR.</span></span> <span data-ttu-id="5bc1f-143">Por ejemplo, si un trabajo se va a ejecutar el 1 y el 16 de cada mes, el valor de la propiedad **DaysOfMonth** sería 1 o 32768.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-143">For example, if a job is to run on the 1st and 16th of each month, the value of the **DaysOfMonth** property would be 1 OR 32768.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="5bc1f-144"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-144"><span id="1"></span>**1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-145">1a</span><span class="sxs-lookup"><span data-stu-id="5bc1f-145">1st</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="5bc1f-146"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-146"><span id="2"></span>**2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-147">secundaria</span><span class="sxs-lookup"><span data-stu-id="5bc1f-147">2nd</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="5bc1f-148"><span id="3"></span>**3** (4)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-148"><span id="3"></span>**3** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-149">3rd (tercero)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-149">3rd</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="5bc1f-150"><span id="4"></span>**4** (8)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-150"><span id="4"></span>**4** (8)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-151">4.º</span><span class="sxs-lookup"><span data-stu-id="5bc1f-151">4th</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="5bc1f-152"><span id="5"></span>**5** (16)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-152"><span id="5"></span>**5** (16)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-153">5.º</span><span class="sxs-lookup"><span data-stu-id="5bc1f-153">5th</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="5bc1f-154"><span id="6"></span>**6** (32)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-154"><span id="6"></span>**6** (32)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-155">6.º</span><span class="sxs-lookup"><span data-stu-id="5bc1f-155">6th</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="5bc1f-156"><span id="7"></span>**7** (64)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-156"><span id="7"></span>**7** (64)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-157">7.º</span><span class="sxs-lookup"><span data-stu-id="5bc1f-157">7th</span></span>

</dd> <dt>

<span id="8"></span>

<span data-ttu-id="5bc1f-158"><span id="8"></span>**8** (128)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-158"><span id="8"></span>**8** (128)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-159">8.º</span><span class="sxs-lookup"><span data-stu-id="5bc1f-159">8th</span></span>

</dd> <dt>

<span id="9"></span>

<span data-ttu-id="5bc1f-160"><span id="9"></span>**9** (256)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-160"><span id="9"></span>**9** (256)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-161">9.º</span><span class="sxs-lookup"><span data-stu-id="5bc1f-161">9th</span></span>

</dd> <dt>

<span id="10"></span>

<span data-ttu-id="5bc1f-162"><span id="10"></span>**10** (512)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-162"><span id="10"></span>**10** (512)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-163">10</span><span class="sxs-lookup"><span data-stu-id="5bc1f-163">10th</span></span>

</dd> <dt>

<span id="11"></span>

<span data-ttu-id="5bc1f-164"><span id="11"></span>**11** (1024)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-164"><span id="11"></span>**11** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-165">11°</span><span class="sxs-lookup"><span data-stu-id="5bc1f-165">11th</span></span>

</dd> <dt>

<span id="12"></span>

<span data-ttu-id="5bc1f-166"><span id="12"></span>**12** (2048)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-166"><span id="12"></span>**12** (2048)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-167">12°</span><span class="sxs-lookup"><span data-stu-id="5bc1f-167">12th</span></span>

</dd> <dt>

<span id="13"></span>

<span data-ttu-id="5bc1f-168"><span id="13"></span>**13** (4096)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-168"><span id="13"></span>**13** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-169">13°</span><span class="sxs-lookup"><span data-stu-id="5bc1f-169">13th</span></span>

</dd> <dt>

<span id="14"></span>

<span data-ttu-id="5bc1f-170"><span id="14"></span>**14** (8192)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-170"><span id="14"></span>**14** (8192)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-171">14</span><span class="sxs-lookup"><span data-stu-id="5bc1f-171">14th</span></span>

</dd> <dt>

<span id="15"></span>

<span data-ttu-id="5bc1f-172"><span id="15"></span>**15** (16384)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-172"><span id="15"></span>**15** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-173">día</span><span class="sxs-lookup"><span data-stu-id="5bc1f-173">15th</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="5bc1f-174"><span id="16"></span>**16** (32768)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-174"><span id="16"></span>**16** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-175">16</span><span class="sxs-lookup"><span data-stu-id="5bc1f-175">16th</span></span>

</dd> <dt>

<span id="17"></span>

<span data-ttu-id="5bc1f-176"><span id="17"></span>**17** (65536)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-176"><span id="17"></span>**17** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-177">17</span><span class="sxs-lookup"><span data-stu-id="5bc1f-177">17th</span></span>

</dd> <dt>

<span id="18"></span>

<span data-ttu-id="5bc1f-178"><span id="18"></span>**18** (131072)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-178"><span id="18"></span>**18** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-179">18</span><span class="sxs-lookup"><span data-stu-id="5bc1f-179">18th</span></span>

</dd> <dt>

<span id="19"></span>

<span data-ttu-id="5bc1f-180"><span id="19"></span>**19** (262144)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-180"><span id="19"></span>**19** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-181">19</span><span class="sxs-lookup"><span data-stu-id="5bc1f-181">19th</span></span>

</dd> <dt>

<span id="20"></span>

<span data-ttu-id="5bc1f-182"><span id="20"></span>**20** (524288)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-182"><span id="20"></span>**20** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-183">20</span><span class="sxs-lookup"><span data-stu-id="5bc1f-183">20th</span></span>

</dd> <dt>

<span id="21"></span>

<span data-ttu-id="5bc1f-184"><span id="21"></span>**21** (1048576)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-184"><span id="21"></span>**21** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-185">21°</span><span class="sxs-lookup"><span data-stu-id="5bc1f-185">21st</span></span>

</dd> <dt>

<span id="22"></span>

<span data-ttu-id="5bc1f-186"><span id="22"></span>**22** (2097152)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-186"><span id="22"></span>**22** (2097152)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-187">22°</span><span class="sxs-lookup"><span data-stu-id="5bc1f-187">22nd</span></span>

</dd> <dt>

<span id="23"></span>

<span data-ttu-id="5bc1f-188"><span id="23"></span>**23** (4194304)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-188"><span id="23"></span>**23** (4194304)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-189">23°</span><span class="sxs-lookup"><span data-stu-id="5bc1f-189">23rd</span></span>

</dd> <dt>

<span id="24"></span>

<span data-ttu-id="5bc1f-190"><span id="24"></span>**24** (8388608)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-190"><span id="24"></span>**24** (8388608)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-191">24</span><span class="sxs-lookup"><span data-stu-id="5bc1f-191">24th</span></span>

</dd> <dt>

<span id="25"></span>

<span data-ttu-id="5bc1f-192"><span id="25"></span>**25** (16777216)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-192"><span id="25"></span>**25** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-193">25</span><span class="sxs-lookup"><span data-stu-id="5bc1f-193">25th</span></span>

</dd> <dt>

<span id="26"></span>

<span data-ttu-id="5bc1f-194"><span id="26"></span>**26** (33554432)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-194"><span id="26"></span>**26** (33554432)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-195">26</span><span class="sxs-lookup"><span data-stu-id="5bc1f-195">26th</span></span>

</dd> <dt>

<span id="27"></span>

<span data-ttu-id="5bc1f-196"><span id="27"></span>**27** (67108864)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-196"><span id="27"></span>**27** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-197">27</span><span class="sxs-lookup"><span data-stu-id="5bc1f-197">27th</span></span>

</dd> <dt>

<span id="28"></span>

<span data-ttu-id="5bc1f-198"><span id="28"></span>**28** (134217728)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-198"><span id="28"></span>**28** (134217728)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-199">28</span><span class="sxs-lookup"><span data-stu-id="5bc1f-199">28th</span></span>

</dd> <dt>

<span id="29"></span>

<span data-ttu-id="5bc1f-200"><span id="29"></span>**29** (268435456)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-200"><span id="29"></span>**29** (268435456)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-201">29</span><span class="sxs-lookup"><span data-stu-id="5bc1f-201">29th</span></span>

</dd> <dt>

<span id="30"></span>

<span data-ttu-id="5bc1f-202"><span id="30"></span>**30** (536870912)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-202"><span id="30"></span>**30** (536870912)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-203">semestre</span><span class="sxs-lookup"><span data-stu-id="5bc1f-203">30th</span></span>

</dd> <dt>

<span id="31"></span>

<span data-ttu-id="5bc1f-204"><span id="31"></span>**31** (1073741824)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-204"><span id="31"></span>**31** (1073741824)</span></span>


</dt> <dd>

<span data-ttu-id="5bc1f-205">día</span><span class="sxs-lookup"><span data-stu-id="5bc1f-205">31st</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5bc1f-206">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-206">**DaysOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-207">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-209">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfWeek**")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-209">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**DaysOfWeek**")</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-210">Días de la semana en los que está programada la ejecución de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-210">Days of the week when a job is scheduled to run.</span></span> <span data-ttu-id="5bc1f-211">Si un trabajo está programado para ejecutarse en varios días de la semana, los valores se pueden combinar en un operador lógico OR.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-211">If a job is scheduled to run on multiple days of the week, the values can be joined in a logical OR.</span></span> <span data-ttu-id="5bc1f-212">Por ejemplo, si un trabajo está programado para ejecutarse los lunes, miércoles y viernes, el valor de la propiedad **DaysOfWeek** sería 1 o 4 o 16.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-212">For example, if a job is scheduled to run on Mondays, Wednesdays, and Fridays the value of the **DaysOfWeek** property would be 1 OR 4 OR 16.</span></span>

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="5bc1f-213">**Lunes** (1)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-213">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="5bc1f-214">**Martes** (2)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-214">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="5bc1f-215">**Miércoles** (4)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-215">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="5bc1f-216">**Jueves** (8)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-216">**Thursday** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="5bc1f-217">**Viernes** (16)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-217">**Friday** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="5bc1f-218">**Sábado** (32)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-218">**Saturday** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="5bc1f-219">**Domingo** (64)</span><span class="sxs-lookup"><span data-stu-id="5bc1f-219">**Sunday** (64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5bc1f-220">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-220">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-221">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-223">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-223">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-224">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-224">A textual description of the object.</span></span>

<span data-ttu-id="5bc1f-225">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1f-225">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bc1f-226">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-226">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-227">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-227">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-229">Período de tiempo durante el que se ha estado ejecutando el trabajo.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-229">Length of time the job has been executing.</span></span>

<span data-ttu-id="5bc1f-230">Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1f-230">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bc1f-231">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-231">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-232">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-232">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-234">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-234">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-235">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-235">Indicates when the object was installed.</span></span> <span data-ttu-id="5bc1f-236">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-236">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5bc1f-237">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1f-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bc1f-238">**InteractWithDesktop**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-238">**InteractWithDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-239">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-241">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**at \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **Flags** no \| **\_ Interactive**")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-241">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Flags**\|**JOB\_NONINTERACTIVE**")</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-242">El trabajo especificado es interactivo, lo que significa que un usuario puede proporcionar la entrada a un trabajo programado mientras se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-242">Specified job is interactive, which means that a user can give input to a scheduled job while it is executing.</span></span>

</dd> <dt>

<span data-ttu-id="5bc1f-243">**JobId**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-243">**JobId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-244">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-244">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-246">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**at \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobID**")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-246">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**JobId**")</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-247">Número de identificación del trabajo.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-247">Identifying number of the job.</span></span> <span data-ttu-id="5bc1f-248">Los métodos los usan como identificador de un trabajo programado en este equipo.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-248">It is used by methods as a handle to one job being scheduled on this computer.</span></span>

</dd> <dt>

<span data-ttu-id="5bc1f-249">**Estado del trabajo**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-249">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-250">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-252">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| estructuras de administración \| [**de red en las marcas de \_ enumeración**](/windows/win32/api/lmat/ns-lmat-at_enum) \|  \| **\_ \_ error de trabajo exec**")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-252">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**Flags**\|**JOB\_EXEC\_ERROR**")</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-253">Estado de la ejecución la última vez que se programó la ejecución de este trabajo.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-253">Status of execution the last time this job was scheduled to run.</span></span>

<dt>

<span id="Success"></span><span id="success"></span><span id="SUCCESS"></span>

<span data-ttu-id="5bc1f-254">**Correcto** ("correcto")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-254">**Success** ("Success")</span></span>


</dt> <dd></dd> <dt>

<span id="Failure"></span><span id="failure"></span><span id="FAILURE"></span>

<span data-ttu-id="5bc1f-255">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-255">**Failure** ("Failure")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5bc1f-256">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-256">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-259">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-259">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-260">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-260">Label by which the object is known.</span></span> <span data-ttu-id="5bc1f-261">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-261">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5bc1f-262">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1f-262">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bc1f-263">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-263">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-266">Se notifica al usuario sobre la finalización o el error del trabajo.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-266">User is notified upon job completion or failure.</span></span>

<span data-ttu-id="5bc1f-267">Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1f-267">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bc1f-268">**Propietario**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-268">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-269">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-271">Usuario que envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-271">User who submitted the job.</span></span>

<span data-ttu-id="5bc1f-272">Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1f-272">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bc1f-273">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-273">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-274">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-276">Importancia de la ejecución de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-276">Importance of a job's execution.</span></span>

<span data-ttu-id="5bc1f-277">Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1f-277">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bc1f-278">**RunRepeatedly**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-278">**RunRepeatedly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-279">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-281">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| \| de estructuras de administración de red en el trabajo marcas [**de \_ información**](/windows/win32/api/lmat/ns-lmat-at_info)se \|  \| **\_ ejecutan \_ periódicamente**")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_INFO**](/windows/win32/api/lmat/ns-lmat-at_info)\|**Flags**\|**JOB\_RUN\_PERIODICALLY**")</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-282">El trabajo programado se ejecuta repetidamente en los días en los que está programado el trabajo.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-282">Scheduled job runs repeatedly on the days that the job is scheduled.</span></span> <span data-ttu-id="5bc1f-283">Si es **false**, el trabajo se ejecuta una vez.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-283">If **False**, then the job is run one time.</span></span>

</dd> <dt>

<span data-ttu-id="5bc1f-284">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-284">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-285">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-285">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-287">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("startTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Network Management Structures \| [**at \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobTime**")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-287">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("StartTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**AT\_ENUM**](/windows/win32/api/lmat/ns-lmat-at_enum)\|**JobTime**")</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-288">Hora UTC para ejecutar el trabajo, con el formato "AAAAMMDDHHMMSS. MMMMMM (+-) OOO ", donde" AAAAMMDD "debe reemplazarse por" \* \* \* \* \* \* \* \* ".</span><span class="sxs-lookup"><span data-stu-id="5bc1f-288">UTC time to run the job, in the form of "YYYYMMDDHHMMSS.MMMMMM(+-)OOO", where "YYYYMMDD" must be replaced by "\*\*\*\*\*\*\*\*".</span></span> <span data-ttu-id="5bc1f-289">El reemplazo es necesario porque el servicio de programación solo permite configurar los trabajos para que se ejecuten una vez, o se ejecuten en un día del mes o de la semana.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-289">The replacement is necessary because the scheduling service only allows jobs to be configured to run one time, or run on a day of the month or week.</span></span> <span data-ttu-id="5bc1f-290">No se puede ejecutar un trabajo en una fecha concreta.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-290">A job cannot be run on a specific date.</span></span>

<span data-ttu-id="5bc1f-291">La sección "(+-) OOO" del valor de la propiedad **startTime** es la diferencia actual de la conversión de hora local.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-291">The "(+-)OOO" section of the **StartTime** property value is the current bias for local time translation.</span></span> <span data-ttu-id="5bc1f-292">La diferencia es la diferencia entre la hora UTC y la hora local.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-292">The bias is the difference between the UTC time and local time.</span></span> <span data-ttu-id="5bc1f-293">Para calcular la diferencia de la zona horaria, multiplique el número de horas que la zona horaria está por encima o por detrás de la hora del meridiano de Greenwich (GMT) en 60 (use un número positivo para el número de horas si la zona horaria está por detrás de GMT y un número negativo si la zona horaria está tras la hora GMT).</span><span class="sxs-lookup"><span data-stu-id="5bc1f-293">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="5bc1f-294">Agregue un 60 adicional al cálculo si la zona horaria usa el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-294">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="5bc1f-295">Por ejemplo, la zona horaria estándar del Pacífico es de ocho horas tras la hora GMT, por lo que la diferencia es igual a-420 (-8 \* 60 + 60) cuando el horario de verano está en uso y-480 (-8 \* 60) cuando el horario de verano no está en uso.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-295">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="5bc1f-296">También puede determinar el valor de la diferencia consultando la propiedad bias de la clase [**\_ TimeZone de Win32**](win32-timezone.md) .</span><span class="sxs-lookup"><span data-stu-id="5bc1f-296">You can also determine the value of the bias by querying the bias property of the [**Win32\_TimeZone**](win32-timezone.md) class.</span></span>

<span data-ttu-id="5bc1f-297">Por ejemplo: " \* \* \* \* \* \* \* \* 123000.000000-420" especifica 14,30 (2:30 P.M.) PST con horario de verano en vigor.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-297">For example: "\*\*\*\*\*\*\*\*123000.000000-420" specifies 14.30 (2:30 P.M.) PST with daylight savings time in effect.</span></span>

</dd> <dt>

<span data-ttu-id="5bc1f-298">**Estado**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-298">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-299">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-301">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-301">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-302">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-302">String that indicates the current status of the object.</span></span> <span data-ttu-id="5bc1f-303">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-303">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="5bc1f-304">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="5bc1f-304">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5bc1f-305">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="5bc1f-305">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5bc1f-306">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="5bc1f-306">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5bc1f-307">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-307">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5bc1f-308">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-308">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5bc1f-309">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1f-309">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5bc1f-310">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5bc1f-310">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5bc1f-311">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-311">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5bc1f-312">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-312">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5bc1f-313">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-313">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5bc1f-314">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-314">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5bc1f-315">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-315">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5bc1f-316">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-316">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5bc1f-317">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-317">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5bc1f-318">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-318">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5bc1f-319">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-319">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5bc1f-320">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-320">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5bc1f-321">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-321">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5bc1f-322">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="5bc1f-322">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5bc1f-323">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-323">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-324">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-324">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-326">Hora a la que se envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-326">Time that the job was submitted.</span></span>

<span data-ttu-id="5bc1f-327">Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1f-327">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> <dt>

<span data-ttu-id="5bc1f-328">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-328">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bc1f-329">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5bc1f-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5bc1f-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5bc1f-331">Hora en la que el trabajo no es válido o debe detenerse.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-331">Time at which the job is invalid or should be stopped.</span></span>

<span data-ttu-id="5bc1f-332">Esta propiedad se hereda del [**\_ trabajo CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1f-332">This property is inherited from [**CIM\_Job**](cim-job.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5bc1f-333">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bc1f-333">Remarks</span></span>

<span data-ttu-id="5bc1f-334">Cada trabajo programado en el servicio de programación se almacena de forma persistente (el programador puede iniciar un trabajo después de un reinicio) y se ejecuta a la hora especificada y al día de la semana o mes.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-334">Each job scheduled against the schedule service is stored persistently (the scheduler can start a job after a reboot), and is executed at the specified time and day of the week or month.</span></span> <span data-ttu-id="5bc1f-335">Si el equipo no está activo o si el servicio programado no se está ejecutando en el tiempo de trabajo especificado, el servicio de programación ejecuta el trabajo especificado el día siguiente a la hora especificada.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-335">If the computer is not active, or if the scheduled service is not running at the specified job time, the schedule service runs the specified job on the next day at the specified time.</span></span>

<span data-ttu-id="5bc1f-336">Los trabajos se programan de acuerdo con la hora universal coordinada (UTC) con el desplazamiento de diferencia de la hora del meridiano de Greenwich (GMT), lo que significa que se puede especificar un trabajo mediante cualquier zona horaria.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-336">Jobs are scheduled according to Coordinated Universal Time (UTC) with bias offset from Greenwich Mean Time (GMT), which means that a job can be specified using any time zone.</span></span> <span data-ttu-id="5bc1f-337">La **clase \_ ScheduledJob de Win32** devuelve la hora local con el desplazamiento de UTC al enumerar un objeto y se convierte en la hora local al crear nuevos trabajos.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-337">The **Win32\_ScheduledJob** class returns the local time with UTC offset when enumerating an object, and converts to local time when creating new jobs.</span></span> <span data-ttu-id="5bc1f-338">Por ejemplo, un trabajo especificado para ejecutarse en un equipo de Boston a las 10:30 P.M.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-338">For example, a job specified to run on a computer in Boston at 10:30 P.M.</span></span> <span data-ttu-id="5bc1f-339">La hora del lunes PST se programará para ejecutarse localmente a las 1:30 A.M.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-339">Monday PST time will be scheduled to run locally at 1:30 A.M.</span></span> <span data-ttu-id="5bc1f-340">Martes EST.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-340">Tuesday EST.</span></span>

> [!Note]  
> <span data-ttu-id="5bc1f-341">Un cliente debe tener en cuenta si el horario de verano está en funcionamiento en el equipo local, y si es así, reste una diferencia de 60 minutos a partir del desplazamiento de UTC.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-341">A client must take into account whether or not daylight savings time is in operation on the local computer, and if it is, then subtract a bias of 60 minutes from the UTC offset.</span></span>

 

<span data-ttu-id="5bc1f-342">La **clase \_ ScheduledJob de Win32** se deriva [**del \_ trabajo CIM**](cim-job.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1f-342">The **Win32\_ScheduledJob** class is derived from [**CIM\_Job**](cim-job.md).</span></span> <span data-ttu-id="5bc1f-343">Debe ser miembro del grupo administradores para crear un trabajo programado mediante esta clase.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-343">You must be a member of the administrators group to create a scheduled job using this class.</span></span>

<span data-ttu-id="5bc1f-344">La **clase \_ ScheduledJob de Win32** usa internamente el protocolo at, que está enlazado a la degradación a partir de Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-344">The **Win32\_ScheduledJob** class is internally using the AT protocol, which is bound to deprecation starting with Windows 8 and Windows Server 2012.</span></span> <span data-ttu-id="5bc1f-345">Como primer paso, el protocolo AT está deshabilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-345">As a first step the AT protocol is disabled by default.</span></span> <span data-ttu-id="5bc1f-346">Si se deshabilita el protocolo, por ejemplo, al llamar al método [**Create**](create-method-in-class-win32-scheduledjob.md) en un objeto **\_ ScheduledJob de Win32** se producirá un error 0x8.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-346">If the protocol is disabled, for example calling the [**Create**](create-method-in-class-win32-scheduledjob.md) method on a **Win32\_ScheduledJob** object will fail with error 0x8.</span></span> <span data-ttu-id="5bc1f-347">Puede volver a activar el protocolo AT si agrega la siguiente entrada del registro:</span><span class="sxs-lookup"><span data-stu-id="5bc1f-347">You can turn the AT protocol back on by adding the following registry entry:</span></span>

``` syntax
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\Configuration 
Name: EnableAt 
Type: REG_DWORD
Value: 1
```

<span data-ttu-id="5bc1f-348">Es posible que tenga que reiniciar el equipo para que la configuración sea efectiva.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-348">You may need to restart the machine to make the setting effective.</span></span>

<span data-ttu-id="5bc1f-349">Dado que **Win32 \_ ScheduledJob** se basa en la API de Win32 [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) , no puede usar esta clase junto con el programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-349">Because **Win32\_ScheduledJob** is based on the [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) Win32 API, you cannot use this class in conjunction with the Task Scheduler.</span></span> <span data-ttu-id="5bc1f-350">Si desea usar Programador de tareas, use la API de Programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-350">If you wish to use Task Scheduler, use the Task Scheduler API.</span></span> <span data-ttu-id="5bc1f-351">Para obtener más información, consulte la [referencia de programador de tareas](../taskschd/task-scheduler-reference.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1f-351">For more information, see the [Task Scheduler Reference](../taskschd/task-scheduler-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5bc1f-352">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5bc1f-352">Examples</span></span>

<span data-ttu-id="5bc1f-353">El siguiente ejemplo de código de VBScript programa Notepad.exe para que se ejecute de forma interactiva en 1:25 por la hora del equipo local cada miércoles.</span><span class="sxs-lookup"><span data-stu-id="5bc1f-353">The following VBScript code example schedules Notepad.exe to run interactively at 1:25 by the local computer time every Wednesday.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set objNewJob = objWMIService.Get("Win32_ScheduledJob")
errJobCreated = objNewJob.Create("Notepad.exe", "********012500.000000-420", True , 4, , True, JobId) 
If errJobCreated <> 0 Then
Wscript.Echo "Error on task creation"
Else
Wscript.Echo "Task created"
End If
```



## <a name="requirements"></a><span data-ttu-id="5bc1f-354">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bc1f-354">Requirements</span></span>



| <span data-ttu-id="5bc1f-355">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bc1f-355">Requirement</span></span> | <span data-ttu-id="5bc1f-356">Value</span><span class="sxs-lookup"><span data-stu-id="5bc1f-356">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc1f-357">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bc1f-357">Minimum supported client</span></span><br/> | <span data-ttu-id="5bc1f-358">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5bc1f-358">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5bc1f-359">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bc1f-359">Minimum supported server</span></span><br/> | <span data-ttu-id="5bc1f-360">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5bc1f-360">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5bc1f-361">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5bc1f-361">Namespace</span></span><br/>                | <span data-ttu-id="5bc1f-362">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5bc1f-362">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5bc1f-363">MOF</span><span class="sxs-lookup"><span data-stu-id="5bc1f-363">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5bc1f-364"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5bc1f-364"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5bc1f-365">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5bc1f-365">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bc1f-366"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bc1f-366"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bc1f-367">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bc1f-367">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc1f-368">**Trabajo de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="5bc1f-368">**CIM\_Job**</span></span>](cim-job.md)
</dt> <dt>

[<span data-ttu-id="5bc1f-369">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="5bc1f-369">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="5bc1f-370">Tareas de WMI: tareas programadas</span><span class="sxs-lookup"><span data-stu-id="5bc1f-370">WMI Tasks: Scheduled Tasks</span></span>](../wmisdk/wmi-tasks--scheduled-tasks.md)
</dt> </dl>

 

 
