---
description: Indica si el componente de minutos del valor DateTime de CIM contiene un intervalo o un valor de carácter comodín.
ms.assetid: de15f87e-0092-467e-b0d7-42ef447fa00a
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. MinutesSpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MinutesSpecified
- ISWbemDateTime.MinutesSpecified
- ISWbemDateTime.get_MinutesSpecified
- ISWbemDateTime.put_MinutesSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 62f64ad749ee020093008a308a3244e045f9995d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155841"
---
# <a name="swbemdatetimeminutesspecified-property"></a><span data-ttu-id="3ded1-103">Propiedad SWbemDateTime. MinutesSpecified</span><span class="sxs-lookup"><span data-stu-id="3ded1-103">SWbemDateTime.MinutesSpecified property</span></span>

<span data-ttu-id="3ded1-104">La propiedad **MinutesSpecified** del objeto [**SWbemDateTime**](swbemdatetime.md) es un valor booleano que indica si el componente de minutos del valor DateTime de CIM contiene un intervalo o un valor de carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="3ded1-104">The **MinutesSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the minutes component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="3ded1-105">Si **MinutesSpecified** es **true** y [**IsInterval**](swbemdatetime-isinterval.md) es **false** (lo que indica que el valor DateTime de CIM no tiene caracteres comodín), [**SWbemDateTime. minutes**](swbemdatetime-minutes.md) contiene un valor de fecha.</span><span class="sxs-lookup"><span data-stu-id="3ded1-105">If **MinutesSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE** (indicating that the CIM datetime value has no wildcards), then [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) contains a date value.</span></span> <span data-ttu-id="3ded1-106">Un valor DateTime que contiene un intervalo no se puede convertir en el formato de **\_ fecha VT** o en el formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="3ded1-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="3ded1-107">Si [**HoursSpecified**](swbemdatetime-hoursspecified.md) es **false** y **IsInterval** es **true**, **SWbemDateTime. minutes** contiene un intervalo.</span><span class="sxs-lookup"><span data-stu-id="3ded1-107">If [**HoursSpecified**](swbemdatetime-hoursspecified.md) is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Minutes** contains an interval.</span></span>

<span data-ttu-id="3ded1-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3ded1-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="3ded1-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3ded1-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ded1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ded1-110">Syntax</span></span>


```VB
SWbemDateTime.MinutesSpecified As boolean
```



## <a name="property-value"></a><span data-ttu-id="3ded1-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3ded1-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="3ded1-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3ded1-112">Examples</span></span>

<span data-ttu-id="3ded1-113">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="3ded1-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="3ded1-114">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="3ded1-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ded1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ded1-115">Requirements</span></span>



| <span data-ttu-id="3ded1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ded1-116">Requirement</span></span> | <span data-ttu-id="3ded1-117">Value</span><span class="sxs-lookup"><span data-stu-id="3ded1-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ded1-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ded1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3ded1-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ded1-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ded1-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ded1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3ded1-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ded1-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ded1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ded1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ded1-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ded1-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ded1-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3ded1-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="3ded1-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3ded1-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3ded1-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ded1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ded1-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ded1-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ded1-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="3ded1-128">CLSID</span></span><br/>                    | <span data-ttu-id="3ded1-129">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="3ded1-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="3ded1-130">IID</span><span class="sxs-lookup"><span data-stu-id="3ded1-130">IID</span></span><br/>                      | <span data-ttu-id="3ded1-131">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="3ded1-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="3ded1-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ded1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ded1-133">**SWbemDateTime. minutos**</span><span class="sxs-lookup"><span data-stu-id="3ded1-133">**SWbemDateTime.Minutes**</span></span>](swbemdatetime-minutes.md)
</dt> <dt>

[<span data-ttu-id="3ded1-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="3ded1-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="3ded1-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="3ded1-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




