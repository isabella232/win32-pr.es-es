---
description: Valor booleano que indica si el componente de día del valor DATETIME de CIM contiene un intervalo o un valor de carácter comodín.
ms.assetid: a713378b-3953-49d8-9c6a-44aa9337eae2
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. DaySpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.DaySpecified
- ISWbemDateTime.DaySpecified
- ISWbemDateTime.get_DaySpecified
- ISWbemDateTime.put_DaySpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f295d33940f36212fde4fe821af8d5df24d4f75f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715747"
---
# <a name="swbemdatetimedayspecified-property"></a><span data-ttu-id="dc880-103">Propiedad SWbemDateTime. DaySpecified</span><span class="sxs-lookup"><span data-stu-id="dc880-103">SWbemDateTime.DaySpecified property</span></span>

<span data-ttu-id="dc880-104">La propiedad **DaySpecified** del objeto [**SWbemDateTime**](swbemdatetime.md) es un valor booleano que indica si el componente de día del valor [**DateTime**](datetime.md) de CIM contiene un intervalo o un valor de carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="dc880-104">The **DaySpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the day component in the CIM [**DATETIME**](datetime.md) value contains an interval or a wildcard value.</span></span> <span data-ttu-id="dc880-105">Si **DaySpecified** es **true** y [**IsInterval**](swbemdatetime-isinterval.md) es **false**, [**SWbemDateTime. Day**](swbemdatetime-day.md) contiene un valor DateTime.</span><span class="sxs-lookup"><span data-stu-id="dc880-105">If **DaySpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Day**](swbemdatetime-day.md) contains a datetime value.</span></span> <span data-ttu-id="dc880-106">Un valor [**DateTime**](datetime.md) que contiene un intervalo no se puede convertir en el formato de **\_ fecha VT** o en el formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="dc880-106">A [**DATETIME**](datetime.md) value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="dc880-107">Si **DaySpecified** es **false** y **IsInterval** es **true**, **SWbemDateTime. Day** contiene un intervalo.</span><span class="sxs-lookup"><span data-stu-id="dc880-107">If **DaySpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Day** contains an interval.</span></span>

<span data-ttu-id="dc880-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="dc880-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="dc880-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="dc880-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc880-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc880-110">Syntax</span></span>


```VB
SWbemDateTime.DaySpecified As BOOLEAN
```



## <a name="property-value"></a><span data-ttu-id="dc880-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="dc880-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="dc880-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dc880-112">Examples</span></span>

<span data-ttu-id="dc880-113">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="dc880-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="dc880-114">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="dc880-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc880-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc880-115">Requirements</span></span>



| <span data-ttu-id="dc880-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc880-116">Requirement</span></span> | <span data-ttu-id="dc880-117">Value</span><span class="sxs-lookup"><span data-stu-id="dc880-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc880-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc880-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dc880-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc880-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc880-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc880-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dc880-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc880-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc880-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc880-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc880-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc880-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc880-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="dc880-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="dc880-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dc880-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dc880-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc880-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc880-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc880-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dc880-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="dc880-128">CLSID</span></span><br/>                    | <span data-ttu-id="dc880-129">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="dc880-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="dc880-130">IID</span><span class="sxs-lookup"><span data-stu-id="dc880-130">IID</span></span><br/>                      | <span data-ttu-id="dc880-131">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="dc880-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="dc880-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc880-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc880-133">**SWbemDateTime. Day**</span><span class="sxs-lookup"><span data-stu-id="dc880-133">**SWbemDateTime.Day**</span></span>](swbemdatetime-day.md)
</dt> <dt>

[<span data-ttu-id="dc880-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="dc880-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="dc880-135">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="dc880-135">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

 




