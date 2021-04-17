---
description: Convierte un valor de fecha y hora en el formato de fecha y hora de CIM al formato FILETIME.
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: Método SWbemDateTime. GetFileTime (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3f8a8c85cb4c78be578187b1f55afce078fe7bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498052"
---
# <a name="swbemdatetimegetfiletime-method"></a><span data-ttu-id="101bb-103">SWbemDateTime. GetFileTime, método</span><span class="sxs-lookup"><span data-stu-id="101bb-103">SWbemDateTime.GetFileTime method</span></span>

<span data-ttu-id="101bb-104">El método **GetFileTime** del objeto [**SWbemDateTime**](swbemdatetime.md) convierte un valor de fecha y hora en el formato de fecha y hora [de CIM al](datetime.md) formato FILETIME.</span><span class="sxs-lookup"><span data-stu-id="101bb-104">The **GetFileTime** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date and time value in the CIM [DATETIME](datetime.md) format to the FILETIME format.</span></span>

<span data-ttu-id="101bb-105">Si el parámetro se establece en **true**, el valor devuelto representa una hora local para el cliente.</span><span class="sxs-lookup"><span data-stu-id="101bb-105">If the parameter is set to **TRUE**, then the return value represents a local time for the client.</span></span> <span data-ttu-id="101bb-106">De lo contrario, el valor devuelto es una hora UTC (hora universal coordinada).</span><span class="sxs-lookup"><span data-stu-id="101bb-106">Otherwise, the return value is a Coordinated Universal Time (UTC) time.</span></span> <span data-ttu-id="101bb-107">Una estructura de [fecha y hora](datetime.md) de **FILETIME** es un valor de 64 bits que representa el número de unidades de 100-nanosegundos desde el comienzo del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="101bb-107">A **FILETIME** [DATETIME](datetime.md) structure is a 64-bit value that represents the number of 100-nanosecond units since the beginning of January 1, 1601.</span></span> <span data-ttu-id="101bb-108">Instrumental de administración de Windows (WMI) trata los valores de **FILETIME** como representaciones de cadena de números de bits 64 sin signo.</span><span class="sxs-lookup"><span data-stu-id="101bb-108">Windows Management Instrumentation (WMI) treats **FILETIME** values as string representations of unsigned 64-bit numbers.</span></span>

<span data-ttu-id="101bb-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="101bb-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="101bb-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="101bb-110">Syntax</span></span>


```VB
vDate = .GetFileTime( _
  [ ByVal bIsLocaL ] _
)
```



## <a name="parameters"></a><span data-ttu-id="101bb-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="101bb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="101bb-112">*bIsLocaL* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="101bb-112">*bIsLocaL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="101bb-113">Indica si el valor devuelto se interpreta como hora local.</span><span class="sxs-lookup"><span data-stu-id="101bb-113">Indicates whether the returned value is interpreted as local time.</span></span> <span data-ttu-id="101bb-114">A continuación, la propiedad UTC contiene la hora local convertida en el desplazamiento correcto de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="101bb-114">The UTC property then contains the local time converted to the correct Coordinated Universal Times (UTC) offset.</span></span> <span data-ttu-id="101bb-115">Si el valor es **false**, el valor se interpreta como UTC con un desplazamiento de cero (0).</span><span class="sxs-lookup"><span data-stu-id="101bb-115">If the value is **FALSE**, then the value is interpreted as UTC with a zero (0) offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="101bb-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="101bb-116">Return value</span></span>

<span data-ttu-id="101bb-117">Fecha y hora en formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="101bb-117">The date and time in the **FILETIME** format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="101bb-118">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="101bb-118">Error codes</span></span>

<span data-ttu-id="101bb-119">Después de completar el método **GetFileTime** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="101bb-119">After completing the **GetFileTime** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="101bb-120">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="101bb-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="101bb-121">Se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="101bb-121">The call failed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="101bb-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="101bb-122">Remarks</span></span>

<span data-ttu-id="101bb-123">**VT \_** Los valores Date y **FILETIME** no pueden contener campos comodín.</span><span class="sxs-lookup"><span data-stu-id="101bb-123">**VT\_DATE** and **FILETIME** values cannot contain wildcard fields.</span></span>

<span data-ttu-id="101bb-124">Se produce un error en el método **GetFileTime** (wbemErrFailed) si alguna de las siguientes propiedades es **falsa**:</span><span class="sxs-lookup"><span data-stu-id="101bb-124">The **GetFileTime** method fails (wbemErrFailed) if any of the following properties are **FALSE**:</span></span>

-   [<span data-ttu-id="101bb-125">**YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="101bb-125">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
-   [<span data-ttu-id="101bb-126">**MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="101bb-126">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
-   [<span data-ttu-id="101bb-127">**DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="101bb-127">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
-   [<span data-ttu-id="101bb-128">**HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="101bb-128">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
-   [<span data-ttu-id="101bb-129">**MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="101bb-129">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
-   [<span data-ttu-id="101bb-130">**SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="101bb-130">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
-   [<span data-ttu-id="101bb-131">**MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="101bb-131">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
-   [<span data-ttu-id="101bb-132">**UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="101bb-132">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)

<span data-ttu-id="101bb-133">En una devolución correcta de [**SetFileTime**](swbemdatetime-setfiletime.md), todas estas propiedades se establecen en **true**.</span><span class="sxs-lookup"><span data-stu-id="101bb-133">On a successful return from [**SetFileTime**](swbemdatetime-setfiletime.md), all of these properties are set to **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="101bb-134">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="101bb-134">Examples</span></span>

<span data-ttu-id="101bb-135">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="101bb-135">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="101bb-136">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="101bb-136">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="101bb-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="101bb-137">Requirements</span></span>



| <span data-ttu-id="101bb-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="101bb-138">Requirement</span></span> | <span data-ttu-id="101bb-139">Value</span><span class="sxs-lookup"><span data-stu-id="101bb-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="101bb-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="101bb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="101bb-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="101bb-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="101bb-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="101bb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="101bb-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="101bb-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="101bb-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="101bb-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="101bb-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="101bb-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="101bb-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="101bb-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="101bb-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="101bb-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="101bb-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="101bb-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="101bb-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="101bb-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="101bb-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="101bb-150">CLSID</span></span><br/>                    | <span data-ttu-id="101bb-151">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="101bb-151">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="101bb-152">IID</span><span class="sxs-lookup"><span data-stu-id="101bb-152">IID</span></span><br/>                      | <span data-ttu-id="101bb-153">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="101bb-153">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="101bb-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="101bb-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="101bb-155">**SWbemDateTime. Getvardate (**</span><span class="sxs-lookup"><span data-stu-id="101bb-155">**SWbemDateTime.GetVarDate**</span></span>](swbemdatetime-getvardate.md)
</dt> <dt>

[<span data-ttu-id="101bb-156">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="101bb-156">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="101bb-157">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="101bb-157">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

