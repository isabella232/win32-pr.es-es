---
description: Valor booleano que indica si el componente de segundos del valor DATETIME de CIM contiene un intervalo o un valor de carácter comodín.
ms.assetid: 9f9b75c3-ae08-49a6-b747-294831601a62
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. SecondsSpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SecondsSpecified
- ISWbemDateTime.SecondsSpecified
- ISWbemDateTime.get_SecondsSpecified
- ISWbemDateTime.put_SecondsSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e0cf97eff544d6e244890014108506f39b1934b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913006"
---
# <a name="swbemdatetimesecondsspecified-property"></a><span data-ttu-id="629e2-103">Propiedad SWbemDateTime. SecondsSpecified</span><span class="sxs-lookup"><span data-stu-id="629e2-103">SWbemDateTime.SecondsSpecified property</span></span>

<span data-ttu-id="629e2-104">La propiedad **SecondsSpecified** del objeto [**SWbemDateTime**](swbemdatetime.md) es un valor booleano que indica si el componente de segundos del valor [**DateTime**](datetime.md) de CIM contiene un intervalo o un valor de carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="629e2-104">The **SecondsSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the seconds component in the CIM [**DATETIME**](datetime.md) value contains an interval or a wildcard value.</span></span> <span data-ttu-id="629e2-105">Si **SecondsSpecified** es **true** y [**IsInterval**](swbemdatetime-isinterval.md) es **false**, [**SWbemDateTime. seconds**](swbemdatetime-seconds.md) contiene un valor de fecha.</span><span class="sxs-lookup"><span data-stu-id="629e2-105">If **SecondsSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Seconds**](swbemdatetime-seconds.md) contains a date value.</span></span> <span data-ttu-id="629e2-106">Un valor DateTime que contiene un intervalo no se puede convertir en el formato de **\_ fecha VT** o en el formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="629e2-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="629e2-107">Si **SecondsSpecified** es **false** y **IsInterval** es **true**, **SWbemDateTime. seconds** contiene un intervalo.</span><span class="sxs-lookup"><span data-stu-id="629e2-107">If **SecondsSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Seconds** contains an interval.</span></span>

<span data-ttu-id="629e2-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="629e2-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="629e2-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="629e2-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="629e2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="629e2-110">Syntax</span></span>


```VB
SWbemDateTime.SecondsSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="629e2-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="629e2-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="629e2-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="629e2-112">Examples</span></span>

<span data-ttu-id="629e2-113">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="629e2-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="629e2-114">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="629e2-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="629e2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="629e2-115">Requirements</span></span>



| <span data-ttu-id="629e2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="629e2-116">Requirement</span></span> | <span data-ttu-id="629e2-117">Value</span><span class="sxs-lookup"><span data-stu-id="629e2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="629e2-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="629e2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="629e2-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="629e2-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="629e2-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="629e2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="629e2-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="629e2-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="629e2-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="629e2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="629e2-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="629e2-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="629e2-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="629e2-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="629e2-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="629e2-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="629e2-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="629e2-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="629e2-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="629e2-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="629e2-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="629e2-128">CLSID</span></span><br/>                    | <span data-ttu-id="629e2-129">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="629e2-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="629e2-130">IID</span><span class="sxs-lookup"><span data-stu-id="629e2-130">IID</span></span><br/>                      | <span data-ttu-id="629e2-131">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="629e2-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="629e2-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="629e2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="629e2-133">**SWbemDateTime. segundos**</span><span class="sxs-lookup"><span data-stu-id="629e2-133">**SWbemDateTime.Seconds**</span></span>](swbemdatetime-seconds.md)
</dt> <dt>

[<span data-ttu-id="629e2-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="629e2-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="629e2-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="629e2-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




