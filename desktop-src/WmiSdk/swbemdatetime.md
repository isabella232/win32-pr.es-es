---
description: El objeto SWbemDateTime es un objeto auxiliar para analizar y establecer valores de fecha y hora de Modelo de información común (CIM).
ms.assetid: 3dd34c73-3c2b-4d59-827b-169cf8020213
ms.tgt_platform: multiple
title: Objeto SWbemDateTime (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime
- ISWbemDateTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 65f3f9836b52693e3f74bac5cfd94553e02d7bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706457"
---
# <a name="swbemdatetime-object"></a><span data-ttu-id="6f4a0-103">Objeto SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="6f4a0-103">SWbemDateTime object</span></span>

<span data-ttu-id="6f4a0-104">El objeto **SWbemDateTime** es un objeto auxiliar para analizar y establecer valores de [fecha y hora](datetime.md) de modelo de información común (CIM).</span><span class="sxs-lookup"><span data-stu-id="6f4a0-104">The **SWbemDateTime** object is a helper object to parse and set Common Information Model (CIM) [datetime](datetime.md) values.</span></span> <span data-ttu-id="6f4a0-105">Desempeña un papel similar a [**SWbemObjectPath**](swbemobjectpath.md), que proporciona ayuda para dar formato e interpretar las rutas de acceso a los objetos.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-105">It plays a role similar to [**SWbemObjectPath**](swbemobjectpath.md), which provides assistance to format and interpret object paths.</span></span> <span data-ttu-id="6f4a0-106">Puede usar la llamada [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript para crear el objeto **SWbemDateTime** .</span><span class="sxs-lookup"><span data-stu-id="6f4a0-106">You can use the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call to create the **SWbemDateTime** object.</span></span>

<span data-ttu-id="6f4a0-107">Un objeto **SWbemDateTime** se puede inicializar a partir de y debe tener el formato de los valores **VT \_ Date** o **FILETIME** mediante métodos en el objeto.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-107">An **SWbemDateTime** object can be initialized from and formatted in either **VT\_DATE** or **FILETIME** values using methods on the object.</span></span> <span data-ttu-id="6f4a0-108">Con las propiedades del objeto, el valor se puede analizar en el año del componente, mes, día, hora, minutos, segundos o microsegundos.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-108">Using properties of the object, the value can be parsed into component year, month, day, hour, minutes, seconds, or microseconds.</span></span> <span data-ttu-id="6f4a0-109">Se puede dar formato al objeto **SWbemDateTime** en valores locales o de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="6f4a0-109">The **SWbemDateTime** object can be formatted into either local or Coordinated Universal Time (UTC) values.</span></span> <span data-ttu-id="6f4a0-110">Para obtener más información, vea [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="6f4a0-110">For more information, see [Date and Time Format](date-and-time-format.md).</span></span>

<span data-ttu-id="6f4a0-111">**SWbemDateTime** es el único objeto de scripting de instrumental de administración de Windows (WMI) que está marcado como seguro para la inicialización y los scripts que se ejecutan en páginas HTML en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-111">**SWbemDateTime** is the only Windows Management Instrumentation (WMI) scripting object that is marked safe for initialization and scripts running on HTML pages in Internet Explorer.</span></span>

## <a name="members"></a><span data-ttu-id="6f4a0-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="6f4a0-112">Members</span></span>

<span data-ttu-id="6f4a0-113">El objeto **SWbemDateTime** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6f4a0-113">The **SWbemDateTime** object has these types of members:</span></span>

-   [<span data-ttu-id="6f4a0-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="6f4a0-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="6f4a0-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6f4a0-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6f4a0-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="6f4a0-116">Methods</span></span>

<span data-ttu-id="6f4a0-117">El objeto **SWbemDateTime** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-117">The **SWbemDateTime** object has these methods.</span></span>



| <span data-ttu-id="6f4a0-118">Método</span><span class="sxs-lookup"><span data-stu-id="6f4a0-118">Method</span></span>                                           | <span data-ttu-id="6f4a0-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f4a0-119">Description</span></span>                                                                                                          |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f4a0-120">**GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-120">**GetFileTime**</span></span>](swbemdatetime-getfiletime.md) | <span data-ttu-id="6f4a0-121">Convierte una fecha y hora de **FILETIME** , expresadas como **BSTR**, en [un formato de fecha y](datetime.md) hora de WMI.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-121">Converts a **FILETIME** date and time, expressed as a **BSTR**, to a WMI [DATETIME](datetime.md) format.</span></span><br/> |
| [<span data-ttu-id="6f4a0-122">**Getvardate (**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-122">**GetVarDate**</span></span>](swbemdatetime-getvardate.md)   | <span data-ttu-id="6f4a0-123">Convierte un valor de fecha y hora con formato [DateTime](datetime.md) de WMI en una **\_ fecha de VT**.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-123">Converts a WMI [DATETIME](datetime.md) formatted date and time value to a **VT\_DATE**.</span></span><br/>                  |
| [<span data-ttu-id="6f4a0-124">**SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-124">**SetFileTime**</span></span>](swbemdatetime-setfiletime.md) | <span data-ttu-id="6f4a0-125">Convierte un formato [DateTime](datetime.md) de WMI en una fecha y hora de **FILETIME** , expresadas como **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-125">Converts a WMI [DATETIME](datetime.md) format to a **FILETIME** date and time, expressed as a **BSTR**.</span></span><br/>  |
| [<span data-ttu-id="6f4a0-126">**SetVarDate**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-126">**SetVarDate**</span></span>](swbemdatetime-setvardate.md)   | <span data-ttu-id="6f4a0-127">Convierte una fecha y hora con formato de **\_ fecha VT** en un [valor DateTime](datetime.md)de WMI.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-127">Converts a **VT\_DATE** formatted date and time to a WMI [DATETIME](datetime.md).</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="6f4a0-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6f4a0-128">Properties</span></span>

<span data-ttu-id="6f4a0-129">El objeto **SWbemDateTime** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-129">The **SWbemDateTime** object has these properties.</span></span>



| <span data-ttu-id="6f4a0-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6f4a0-130">Property</span></span>                                                                        | <span data-ttu-id="6f4a0-131">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="6f4a0-131">Access type</span></span>           | <span data-ttu-id="6f4a0-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f4a0-132">Description</span></span>                                                                                                                     |
|:--------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f4a0-133">**Diariamente**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-133">**Day**</span></span>](swbemdatetime-day.md)<br/>                                     | <span data-ttu-id="6f4a0-134">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-134">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-135">El componente de día de un valor [DateTime](datetime.md) de CIM.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-135">The day component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                           |
| [<span data-ttu-id="6f4a0-136">**DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-136">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)<br/>                   | <span data-ttu-id="6f4a0-137">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-137">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-138">Indica si el día se especifica o se deja como carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-138">Indicates whether the day is specified or left as a wildcard.</span></span><br/>                                                        |
| [<span data-ttu-id="6f4a0-139">**Hours**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-139">**Hours**</span></span>](swbemdatetime-hours.md)<br/>                                 | <span data-ttu-id="6f4a0-140">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-140">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-141">Horas del componente de día de un valor [DateTime](datetime.md) de CIM.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-141">The hours of the day component of a CIM [datetime](datetime.md) value.</span></span><br/>                                              |
| [<span data-ttu-id="6f4a0-142">**HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-142">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)<br/>               | <span data-ttu-id="6f4a0-143">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-143">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-144">Indica si la hora se especifica o se deja como un carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-144">Indicates whether the hour is specified or left as a wildcard.</span></span><br/>                                                       |
| [<span data-ttu-id="6f4a0-145">**IsInterval**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-145">**IsInterval**</span></span>](swbemdatetime-isinterval.md)<br/>                       | <span data-ttu-id="6f4a0-146">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-146">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-147">Indica que al menos un componente de la [fecha y hora](datetime.md) de CIM representa un intervalo en lugar de una fecha.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-147">Indicates that at least one component of the CIM [datetime](datetime.md) represents an interval rather than a date.</span></span><br/> |
| [<span data-ttu-id="6f4a0-148">**Microsegundos**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-148">**Microseconds**</span></span>](swbemdatetime-microseconds.md)<br/>                   | <span data-ttu-id="6f4a0-149">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-149">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-150">Componente de microsegundos de un valor [DateTime](datetime.md) de CIM.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-150">The microseconds component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                  |
| [<span data-ttu-id="6f4a0-151">**MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-151">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)<br/> | <span data-ttu-id="6f4a0-152">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-152">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-153">Indica si el componente de microsegundos se especifica o se deja como carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-153">Indicates whether the microseconds component is specified or left as a wildcard.</span></span><br/>                                     |
| [<span data-ttu-id="6f4a0-154">**Minutos**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-154">**Minutes**</span></span>](swbemdatetime-minutes.md)<br/>                             | <span data-ttu-id="6f4a0-155">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-155">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-156">El componente de minutos de un valor [DateTime](datetime.md) de CIM.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-156">The minutes component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                       |
| [<span data-ttu-id="6f4a0-157">**MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-157">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)<br/>           | <span data-ttu-id="6f4a0-158">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-158">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-159">Indica si el componente de minutos se especifica o se deja como carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-159">Indicates whether the minutes component is specified or left as a wildcard.</span></span><br/>                                          |
| [<span data-ttu-id="6f4a0-160">**Mensuales**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-160">**Month**</span></span>](swbemdatetime-month.md)<br/>                                 | <span data-ttu-id="6f4a0-161">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-161">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-162">El componente de mes de un valor [DateTime](datetime.md) de CIM.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-162">The month component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                         |
| [<span data-ttu-id="6f4a0-163">**MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-163">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)<br/>               | <span data-ttu-id="6f4a0-164">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-164">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-165">Indica si el mes se especifica o se deja como carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-165">Indicates whether the month is specified or left as a wildcard.</span></span><br/>                                                      |
| [<span data-ttu-id="6f4a0-166">**Segundos**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-166">**Seconds**</span></span>](swbemdatetime-seconds.md)<br/>                             | <span data-ttu-id="6f4a0-167">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-167">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-168">Componente de segundos de un valor [DateTime](datetime.md) de CIM.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-168">The seconds component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                       |
| [<span data-ttu-id="6f4a0-169">**SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-169">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)<br/>           | <span data-ttu-id="6f4a0-170">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-170">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-171">Indica si el componente de segundos se especifica o se deja como carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-171">Indicates whether the seconds component is specified or left as a wildcard.</span></span><br/>                                          |
| [<span data-ttu-id="6f4a0-172">**UTC**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-172">**UTC**</span></span>](swbemdatetime-utc.md)<br/>                                     | <span data-ttu-id="6f4a0-173">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-173">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-174">Componente UTC de un valor [DateTime](datetime.md) de CIM.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-174">The UTC component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                           |
| [<span data-ttu-id="6f4a0-175">**UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-175">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)<br/>                   | <span data-ttu-id="6f4a0-176">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-176">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-177">Indica si el componente UTC se especifica o se deja como carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-177">Indicates whether the UTC component is specified or left as a wildcard.</span></span><br/>                                              |
| [<span data-ttu-id="6f4a0-178">**Value**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-178">**Value**</span></span>](swbemdatetime-value.md)<br/>                                 | <span data-ttu-id="6f4a0-179">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-179">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-180">El valor de [fecha y hora](datetime.md) de CIM completo.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-180">The full CIM [datetime](datetime.md) value.</span></span><br/>                                                                         |
| [<span data-ttu-id="6f4a0-181">**Anual**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-181">**Year**</span></span>](swbemdatetime-year.md)<br/>                                   | <span data-ttu-id="6f4a0-182">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-182">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-183">Componente de año de un valor [DateTime](datetime.md) de CIM.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-183">The year component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                          |
| [<span data-ttu-id="6f4a0-184">**YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="6f4a0-184">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)<br/>                 | <span data-ttu-id="6f4a0-185">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6f4a0-185">Read/write</span></span><br/> | <span data-ttu-id="6f4a0-186">Indica si se ha especificado o no el año como carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-186">Indicates whether or not the year is specified or left as a wildcard.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="6f4a0-187">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f4a0-187">Remarks</span></span>

<span data-ttu-id="6f4a0-188">WMI registra las marcas de tiempo en el formato de coordenadas de hora universal (UTC).</span><span class="sxs-lookup"><span data-stu-id="6f4a0-188">WMI records timestamps in universal time coordinate (UTC) format.</span></span> <span data-ttu-id="6f4a0-189">UTC no es el formato que usan la mayoría de los desarrolladores y administradores de ti.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-189">UTC is not the format that most developers and IT administrators use.</span></span> <span data-ttu-id="6f4a0-190">Por lo tanto, un problema común es determinar cómo traducir la hora UTC a algo más legible.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-190">Therefore, a common issue is determining how to translate UTC into something more readable.</span></span> <span data-ttu-id="6f4a0-191">Para obtener más información sobre cómo trabajar con UTC, vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md) y [trabajar con fechas y horas mediante WMI](/previous-versions/tn-archive/ee198928(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="6f4a0-191">For more information on how to work with UTC, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md) and [Working with Dates and Times using WMI](/previous-versions/tn-archive/ee198928(v=technet.10)).</span></span> <span data-ttu-id="6f4a0-192">También puede leer la información [sobre la TI sobre el tiempo (Oh, y sobre las fechas)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) y [cómo se puede restar un número especificado de días a partir de un valor UTC](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) . entradas de blog para obtener información adicional.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-192">You can also read the [It s About Time (Oh, and About Dates, Too)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) and [How Can I Subtract a Specified Number of Days from a UTC Value?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) blog posts for additional information.</span></span>

<span data-ttu-id="6f4a0-193">Cualquier campo numérico puede tener un valor comodín si la propiedad [**IsInterval**](swbemdatetime-isinterval.md) está establecida en **false**.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-193">Any numeric field can have a wildcard value if the [**IsInterval**](swbemdatetime-isinterval.md) property is set to **FALSE**.</span></span> <span data-ttu-id="6f4a0-194">Los campos con valores comodín contienen asteriscos en todo el campo.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-194">Fields with wildcard values contain asterisks in the entire field.</span></span>

<span data-ttu-id="6f4a0-195">Cada propiedad, por ejemplo [**Day**](swbemdatetime-day.md), tiene un valor booleano especificado correspondiente, como [**DaySpecified**](swbemdatetime-dayspecified.md).</span><span class="sxs-lookup"><span data-stu-id="6f4a0-195">Each property, for example [**Day**](swbemdatetime-day.md), has a corresponding specified Boolean value, such as [**DaySpecified**](swbemdatetime-dayspecified.md).</span></span> <span data-ttu-id="6f4a0-196">Cuando **DaySpecified** es **false**, el valor se interpreta como un intervalo en lugar de un número entre 01 y 31.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-196">When **DaySpecified** is **FALSE**, then the value is interpreted as an interval rather than a number between 01 and 31.</span></span> <span data-ttu-id="6f4a0-197">Si se usa un intervalo en cualquier parte del valor [DateTime](datetime.md) de CIM, [**IsInterval**](swbemdatetime-isinterval.md) también se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-197">If an interval is used anywhere in the CIM [datetime](datetime.md) value, then [**IsInterval**](swbemdatetime-isinterval.md) is also set to **TRUE**.</span></span> <span data-ttu-id="6f4a0-198">El valor predeterminado es que un valor DateTime de CIM contenga una fecha en lugar de uno o más intervalos.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-198">The default is for a CIM datetime value to contain a date rather than one or more intervals.</span></span>

<span data-ttu-id="6f4a0-199">Por ejemplo, si [**SWbemDateTime. DaySpecified**](swbemdatetime-dayspecified.md) es **true**, [**SWbemDateTime. Value**](swbemdatetime-value.md) incluye el valor actual de [**SWbemDateTime. Day**](swbemdatetime-day.md); de lo contrario, es un valor comodín.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-199">For example, if [**SWbemDateTime.DaySpecified**](swbemdatetime-dayspecified.md) is **TRUE**, then [**SWbemDateTime.Value**](swbemdatetime-value.md) includes the current value of [**SWbemDateTime.Day**](swbemdatetime-day.md), otherwise it is a wildcard value.</span></span> <span data-ttu-id="6f4a0-200">La propiedad [**IsInterval**](swbemdatetime-isinterval.md) es **false** en cualquier caso.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-200">The [**IsInterval**](swbemdatetime-isinterval.md) property is **FALSE** in either case.</span></span>

## <a name="examples"></a><span data-ttu-id="6f4a0-201">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6f4a0-201">Examples</span></span>

<span data-ttu-id="6f4a0-202">En el ejemplo de código de script siguiente se muestra cómo usar un objeto **SWbemDateTime** para analizar un valor de propiedad DateTime leído del repositorio WMI, la propiedad **InstallDate** en el sistema [**\_ operativo Win32**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span><span class="sxs-lookup"><span data-stu-id="6f4a0-202">The following script code example shows how to use an **SWbemDateTime** object to parse a datetime property value read from the WMI repository, the **InstallDate** property in [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span>


```VB
' Create a new datetime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")

' Retrieve a WMI object that contains a datetime value.
for each os in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

    ' The InstallDate property is a CIM_DATETIME. 
    MsgBox os.InstallDate
    dateTime.Value = os.InstallDate

    ' Display the year of installation.
    MsgBox "This OS was installed in the year " & dateTime.Year

    ' Display the installation date using the VT_DATE format.
    MsgBox "Full installation date (VT_DATE format) is " _
    & dateTime.GetVarDate

    ' Display the installation date using the FILETIME format.
    MsgBox "Full installation date (FILETIME format) is " _
    & dateTime.GetFileTime 
next
Set datetime = Nothing
```



<span data-ttu-id="6f4a0-203">En el ejemplo siguiente se muestra cómo crear un objeto **SWbemDateTime** , cómo almacenar un valor de fecha en el objeto, cómo mostrar la fecha como hora universal coordinada (UTC) y cómo almacenar el valor en una clase y propiedad recién creadas.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-203">The following example shows how to create an **SWbemDateTime** object, store a date value in the object, display the date as local and Coordinated Universal Time (UTC), and store the value in a newly created class and property.</span></span> <span data-ttu-id="6f4a0-204">Para obtener más información sobre la constante **wbemCimtypeDatetime**, vea [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span><span class="sxs-lookup"><span data-stu-id="6f4a0-204">For more information about the constant **wbemCimtypeDatetime**, see [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span></span>


```VB
' Create an SWbemDateTime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
' Set the value 
Const wbemCimTypeDatetime = 101

' Construct a datetime value using the intrinsic VBScript CDate
' function interpreting this as a local date/time in
' the Pacific time zone (-8 hrs GMT). Convert to CIM datetime
' using SetVarDate method. The year defaults to current year.
dateTime.SetVarDate (CDate ("January 20 11:56:32"))

' The value in dateTime displays as 
' 20000120195632.000000-480. This is the equivalent time
' in GMT with the specified offset for PST of -8 hrs.
MsgBox "CIM datetime " & dateTime

' The value now displays as B=0/2000 11:56:32 AM because the
' parameter contains the default TRUE value causing the value to be
' interpreted as a local time.
MsgBox "Local datetime " & dateTime.GetVarDate ()

' The value now displays as B=0/2000 7:56:32 PM because the
' parameter value is FALSE, which indicates a GMT time.
' non-local time.
MsgBox "Datetime in GMT " & dateTime.GetVarDate (false)

' Create a new class and add a DateTime property value.
' SWbemServices.Get returns an empty SWbemObject
' which can become a new class. SWbemObject.Path_ returns an
' SWbemObjectPath object. 
set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "NewClass"

' Add a new property named "InterestingDate" to the NewObject class
' and define its datatype as a CIM datetime value.
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value of the SWbemDateTime object in the InterestingDate
' property.
NewObject.InterestingDate = dateTime.Value
MsgBox "Datetime in new object " & NewObject.InterestingDate

' Write the new class (named "NewClass") containing
' the SWbemDateTime object to the repository.
NewObject.Put_
WScript.Echo "NewClass is now in WMI repository"

' Clean up the example by deleting the new class from the repository
NewObject.Delete_
```



<span data-ttu-id="6f4a0-205">En el ejemplo de código de script siguiente se muestra cómo usar un objeto **SWbemDateTime** para modificar un valor de intervalo en una propiedad que se lee desde el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-205">The following script code example shows how to use an **SWbemDateTime** object to modify an interval value on a property that is read from the WMI repository.</span></span>


```VB
' Construct an interval value of 100 days, 1 hour, and 3 seconds.
dateTime.IsInterval = true 
dateTime.Day = 100
dateTime.Hours = 1
dateTime.Seconds = 3

' The datetime displays as 00000100010003.000000:000.
MsgBox "Constructed interval value " & datetime

' Retrieve an empty WMI object and add a datetime property. 
Const wbemCimTypeDatetime = 101
Set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "Empty"
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value in the property and update. 
NewObject.InterestingDate = dateTime.Value
MsgBox "NewObject.InterestingDate = " & NewObject.InterestingDate

' Write the new SWbemDateTime object to the repository.
NewObject.Put_

' Delete the object.
NewObject.Delete_
```



<span data-ttu-id="6f4a0-206">En el ejemplo de código de script siguiente se muestra cómo usar un objeto **SWbemDate** para leer un valor de **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="6f4a0-206">The following script code example shows how to use an **SWbemDate** object to read a **FILETIME** value.</span></span>


```VB
' Create a new datetime object.
Set datetime = CreateObject("WbemScripting.SWbemDateTime")

' Set from a FILETIME value (non-local).
' Assume a timezone -7 hrs. GMT.
MsgBox "FILETIME value " & "126036951652030000"
datetime.SetFileTime "126036951652030000", false

' Displays as 5/24/2000 7:26:05 PM.
MsgBox "GMT time " & dateTime.GetVarDate   

' Set from a FILETIME value (local).
datetime.SetFileTime "126036951652030000"

' Displays as 5/25/2000 2:26:05 AM.
MsgBox "Same value in local time " & dateTime.GetVarDate
Set datetime = Nothing
```



<span data-ttu-id="6f4a0-207">El siguiente código de PowerShell crea una instancia de un objeto SWbemDateTime, recupera la fecha de instalación del sistema operativo y convierte la fecha a un formato diferente.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-207">The following PowerShell code creates an instance of a SWbemDateTime object, retrieves the OS install date, and converts the date to a different format</span></span>


```PowerShell
# Create swbemdatetime object
$datetime = New-Object -ComObject WbemScripting.SWbemDateTime

#  Get OS installation time and assign to datetime object
$os = Get-WmiObject -Class Win32_OperatingSystem
$dateTime.Value = $os.InstallDate

# Now display the time
"This OS was installed in the year {0}"           -f $dateTime.Year
"Full installation date (VT_DATE format) is {0}"  -f $dateTime.GetVarDate()
"Full installation date (FILETIME format) is {0}" -f $dateTime.GetFileTime() 
```



<span data-ttu-id="6f4a0-208">El siguiente código de PowerShell convierte el código en un formato listo para que lo consuma un proveedor CIM.</span><span class="sxs-lookup"><span data-stu-id="6f4a0-208">The following Powershell code translates the code into a format ready to be consumed by a CIM provider.</span></span>


```PowerShell
 $time = (Get-Date)
 $objScriptTime = New-Object -ComObject WbemScripting.SWbemDateTime
 $objScriptTime.SetVarDate($time)
 $cimTime = $objScriptTime.Value
```



## <a name="requirements"></a><span data-ttu-id="6f4a0-209">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f4a0-209">Requirements</span></span>



| <span data-ttu-id="6f4a0-210">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f4a0-210">Requirement</span></span> | <span data-ttu-id="6f4a0-211">Value</span><span class="sxs-lookup"><span data-stu-id="6f4a0-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f4a0-212">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f4a0-212">Minimum supported client</span></span><br/> | <span data-ttu-id="6f4a0-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f4a0-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f4a0-214">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f4a0-214">Minimum supported server</span></span><br/> | <span data-ttu-id="6f4a0-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f4a0-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f4a0-216">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f4a0-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f4a0-217"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f4a0-217"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f4a0-218">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6f4a0-218">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f4a0-219"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6f4a0-219"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6f4a0-220">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f4a0-220">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f4a0-221"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f4a0-221"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6f4a0-222">CLSID</span><span class="sxs-lookup"><span data-stu-id="6f4a0-222">CLSID</span></span><br/>                    | <span data-ttu-id="6f4a0-223">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="6f4a0-223">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="6f4a0-224">IID</span><span class="sxs-lookup"><span data-stu-id="6f4a0-224">IID</span></span><br/>                      | <span data-ttu-id="6f4a0-225">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="6f4a0-225">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="6f4a0-226">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f4a0-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f4a0-227">WbemCimtypeEnum</span><span class="sxs-lookup"><span data-stu-id="6f4a0-227">WbemCimtypeEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dt>

[<span data-ttu-id="6f4a0-228">DATETIME</span><span class="sxs-lookup"><span data-stu-id="6f4a0-228">DATETIME</span></span>](datetime.md)
</dt> <dt>

[<span data-ttu-id="6f4a0-229">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="6f4a0-229">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

