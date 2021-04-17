---
description: Convierte un valor de fecha y hora en el formato de fecha y hora de CIM en el formato de fecha de VT \_ .
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: Método SWbemDateTime. Getvardate ((Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d0c71e4748774eacab4b234092178179a4a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715746"
---
# <a name="swbemdatetimegetvardate-method"></a><span data-ttu-id="35062-103">SWbemDateTime. Getvardate (, método</span><span class="sxs-lookup"><span data-stu-id="35062-103">SWbemDateTime.GetVarDate method</span></span>

<span data-ttu-id="35062-104">El método **getvardate (** del objeto [**SWbemDateTime**](swbemdatetime.md) convierte un valor de fecha y hora en el formato de fecha y hora [**de CIM al**](datetime.md) formato de **\_ fecha de VT** .</span><span class="sxs-lookup"><span data-stu-id="35062-104">The **GetVarDate** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date and time value in the CIM [**DATETIME**](datetime.md) format to the **VT\_DATE** format.</span></span>

<span data-ttu-id="35062-105">El formato de **\_ fecha VT** es un valor [**DateTime**](datetime.md) de la variante de automatización que Visual Basic y el uso de ActiveX.</span><span class="sxs-lookup"><span data-stu-id="35062-105">The **VT\_DATE** format is an automation variant [**DATETIME**](datetime.md) value that Visual Basic and ActiveX use.</span></span>

<span data-ttu-id="35062-106">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="35062-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="35062-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35062-107">Syntax</span></span>


```VB
vdate = .GetVarDate( _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="35062-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35062-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35062-109">*bIsLocal* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="35062-109">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="35062-110">Indica si el valor devuelto se interpreta como hora local.</span><span class="sxs-lookup"><span data-stu-id="35062-110">Indicates whether the returned value is interpreted as local time.</span></span> <span data-ttu-id="35062-111">La propiedad hora universal coordinada (UTC) contiene la hora local convertida en el desplazamiento UTC correcto.</span><span class="sxs-lookup"><span data-stu-id="35062-111">The Coordinated Universal Time (UTC) property contains the local time converted to the correct UTC offset.</span></span> <span data-ttu-id="35062-112">Si el valor es **false**, el valor se interpreta como UTC con un desplazamiento de cero (0).</span><span class="sxs-lookup"><span data-stu-id="35062-112">If the value is **FALSE**, then the value is interpreted as UTC with a zero (0) offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35062-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35062-113">Return value</span></span>

<span data-ttu-id="35062-114">Valor de fecha y hora en el formato de **\_ fecha de VT** .</span><span class="sxs-lookup"><span data-stu-id="35062-114">The date and time value in the **VT\_DATE** format.</span></span>

## <a name="remarks"></a><span data-ttu-id="35062-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35062-115">Remarks</span></span>

<span data-ttu-id="35062-116">**VT \_** Los valores Date y **FILETIME** no pueden contener campos comodín.</span><span class="sxs-lookup"><span data-stu-id="35062-116">**VT\_DATE** and **FILETIME** values cannot contain wildcard fields.</span></span>

<span data-ttu-id="35062-117">Se produce un error en el método **getvardate (** (**wbemErrFailed**) si alguna de las siguientes propiedades es **falsa**:</span><span class="sxs-lookup"><span data-stu-id="35062-117">The **GetVarDate** method fails (**wbemErrFailed**) if any of the following properties are **FALSE**:</span></span>

-   [<span data-ttu-id="35062-118">**YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="35062-118">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
-   [<span data-ttu-id="35062-119">**MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="35062-119">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
-   [<span data-ttu-id="35062-120">**DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="35062-120">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
-   [<span data-ttu-id="35062-121">**HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="35062-121">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
-   [<span data-ttu-id="35062-122">**MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="35062-122">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
-   [<span data-ttu-id="35062-123">**SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="35062-123">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
-   [<span data-ttu-id="35062-124">**MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="35062-124">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
-   [<span data-ttu-id="35062-125">**UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="35062-125">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)

<span data-ttu-id="35062-126">Todas estas propiedades se establecen en **true** si se devuelve correctamente desde [**SetVarDate**](swbemdatetime-setvardate.md).</span><span class="sxs-lookup"><span data-stu-id="35062-126">On successful return from [**SetVarDate**](swbemdatetime-setvardate.md), all of these properties are set to **TRUE**.</span></span>

<span data-ttu-id="35062-127">Después de una llamada correcta a [**SetVarDate**](swbemdatetime-setvardate.md), el valor [**DateTime**](datetime.md) siempre se interpreta como un valor de **fecha y hora** absoluto en lugar de un intervalo, y [**IsInterval**](swbemdatetime-isinterval.md) se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="35062-127">After a successful call to [**SetVarDate**](swbemdatetime-setvardate.md), the [**DATETIME**](datetime.md) value is always interpreted as an absolute **DATETIME** value instead of an interval, and the [**IsInterval**](swbemdatetime-isinterval.md) is set to **FALSE**.</span></span>

<span data-ttu-id="35062-128">Si [**IsInterval**](swbemdatetime-isinterval.md) se establece en **true**, una llamada a **getvardate (** produce el error **wbemErrFailed** .</span><span class="sxs-lookup"><span data-stu-id="35062-128">If [**IsInterval**](swbemdatetime-isinterval.md) is set to **TRUE**, then a call to **GetVarDate** results in the **wbemErrFailed** error.</span></span>

<span data-ttu-id="35062-129">Se produce una pérdida de precisión cuando se llama a **getvardate (**, ya que los valores [DateTime](datetime.md) tienen una resolución de un microsegundo (s) y los valores de **\_ fecha de VT** tienen una resolución de 500 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="35062-129">Some loss of precision occurs when you call **GetVarDate**, because [datetime](datetime.md) values have a one microsecond ( s) resolution, and **VT\_DATE** values have a 500 millisecond resolution.</span></span>

## <a name="examples"></a><span data-ttu-id="35062-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="35062-130">Examples</span></span>

<span data-ttu-id="35062-131">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM a y desde el formato de **\_ fecha** de **FILETIME** o VT, vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="35062-131">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="35062-132">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="35062-132">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35062-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35062-133">Requirements</span></span>



| <span data-ttu-id="35062-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="35062-134">Requirement</span></span> | <span data-ttu-id="35062-135">Value</span><span class="sxs-lookup"><span data-stu-id="35062-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35062-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35062-136">Minimum supported client</span></span><br/> | <span data-ttu-id="35062-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35062-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35062-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35062-138">Minimum supported server</span></span><br/> | <span data-ttu-id="35062-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35062-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35062-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35062-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="35062-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="35062-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="35062-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="35062-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="35062-143"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35062-143"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35062-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35062-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35062-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35062-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="35062-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="35062-146">CLSID</span></span><br/>                    | <span data-ttu-id="35062-147">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="35062-147">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="35062-148">IID</span><span class="sxs-lookup"><span data-stu-id="35062-148">IID</span></span><br/>                      | <span data-ttu-id="35062-149">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="35062-149">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="35062-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="35062-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35062-151">**SWbemDateTime.GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="35062-151">**SWbemDateTime.GetFileTime**</span></span>](swbemdatetime-getfiletime.md)
</dt> <dt>

[<span data-ttu-id="35062-152">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="35062-152">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="35062-153">DATETIME</span><span class="sxs-lookup"><span data-stu-id="35062-153">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




