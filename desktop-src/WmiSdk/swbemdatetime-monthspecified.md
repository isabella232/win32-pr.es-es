---
description: Valor booleano que indica si el componente de mes del valor DateTime de CIM contiene un intervalo o un valor de carácter comodín.
ms.assetid: 12dd94de-24be-4b13-bde5-2fc28be94efa
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. MonthSpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MonthSpecified
- ISWbemDateTime.MonthSpecified
- ISWbemDateTime.get_MonthSpecified
- ISWbemDateTime.put_MonthSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 52b44444a5810577289353778c2c00b1ebfb80fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706071"
---
# <a name="swbemdatetimemonthspecified-property"></a><span data-ttu-id="874ae-103">Propiedad SWbemDateTime. MonthSpecified</span><span class="sxs-lookup"><span data-stu-id="874ae-103">SWbemDateTime.MonthSpecified property</span></span>

<span data-ttu-id="874ae-104">La propiedad **MonthSpecified** del objeto [**SWbemDateTime**](swbemdatetime.md) es un valor booleano que indica si el componente de mes del valor DateTime de CIM contiene un intervalo o un valor de carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="874ae-104">The **MonthSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the month component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="874ae-105">Si **MonthSpecified** es **true** y [**IsInterval**](swbemdatetime-isinterval.md) es **false**, [**SWbemDateTime. month**](swbemdatetime-month.md) contiene un valor de fecha.</span><span class="sxs-lookup"><span data-stu-id="874ae-105">If **MonthSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Month**](swbemdatetime-month.md) contains a date value.</span></span> <span data-ttu-id="874ae-106">Un valor DateTime que contiene un intervalo no se puede convertir en el formato de **\_ fecha VT** o en el formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="874ae-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="874ae-107">Si **MonthSpecified** es **false** y **IsInterval** es **true**, **SWbemDateTime. month** contiene un intervalo.</span><span class="sxs-lookup"><span data-stu-id="874ae-107">If **MonthSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Month** contains an interval.</span></span>

<span data-ttu-id="874ae-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="874ae-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="874ae-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="874ae-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="874ae-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="874ae-110">Syntax</span></span>


```VB
SWbemDateTime.MonthSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="874ae-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="874ae-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="874ae-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="874ae-112">Examples</span></span>

<span data-ttu-id="874ae-113">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="874ae-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="874ae-114">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="874ae-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="874ae-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="874ae-115">Requirements</span></span>



| <span data-ttu-id="874ae-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="874ae-116">Requirement</span></span> | <span data-ttu-id="874ae-117">Value</span><span class="sxs-lookup"><span data-stu-id="874ae-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="874ae-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="874ae-118">Minimum supported client</span></span><br/> | <span data-ttu-id="874ae-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="874ae-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="874ae-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="874ae-120">Minimum supported server</span></span><br/> | <span data-ttu-id="874ae-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="874ae-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="874ae-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="874ae-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="874ae-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="874ae-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="874ae-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="874ae-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="874ae-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="874ae-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="874ae-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="874ae-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="874ae-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="874ae-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="874ae-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="874ae-128">CLSID</span></span><br/>                    | <span data-ttu-id="874ae-129">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="874ae-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="874ae-130">IID</span><span class="sxs-lookup"><span data-stu-id="874ae-130">IID</span></span><br/>                      | <span data-ttu-id="874ae-131">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="874ae-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="874ae-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="874ae-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="874ae-133">**SWbemDateTime. month**</span><span class="sxs-lookup"><span data-stu-id="874ae-133">**SWbemDateTime.Month**</span></span>](swbemdatetime-month.md)
</dt> <dt>

[<span data-ttu-id="874ae-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="874ae-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="874ae-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="874ae-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




