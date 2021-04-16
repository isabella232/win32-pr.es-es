---
description: Valor booleano que indica si el componente de año del valor DateTime de CIM contiene un intervalo o un valor de carácter comodín.
ms.assetid: afac0a08-7bd0-42f1-b5a7-8664f9db8615
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. YearSpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.YearSpecified
- ISWbemDateTime.YearSpecified
- ISWbemDateTime.get_YearSpecified
- ISWbemDateTime.put_YearSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3ad6ae5b120c2b38d7b6170951ef30b3b19f5295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706067"
---
# <a name="swbemdatetimeyearspecified-property"></a><span data-ttu-id="3c255-103">Propiedad SWbemDateTime. YearSpecified</span><span class="sxs-lookup"><span data-stu-id="3c255-103">SWbemDateTime.YearSpecified property</span></span>

<span data-ttu-id="3c255-104">La propiedad **YearSpecified** del objeto [**SWbemDateTime**](swbemdatetime.md) es un valor booleano que indica si el componente de año del valor DateTime de CIM contiene un intervalo o un valor de carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="3c255-104">The **YearSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the year component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="3c255-105">Si **YearSpecified** es **true** y [**IsInterval**](swbemdatetime-isinterval.md) es **false**, [**SWbemDateTime. Year**](swbemdatetime-year.md) contiene un valor DateTime.</span><span class="sxs-lookup"><span data-stu-id="3c255-105">If **YearSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Year**](swbemdatetime-year.md) contains a datetime value.</span></span> <span data-ttu-id="3c255-106">Un valor DateTime que contiene un intervalo no se puede convertir en el formato de **\_ fecha VT** o en el formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="3c255-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="3c255-107">Si **YearSpecified** es **false** y **IsInterval** es **true**, **SWbemDateTime. Year** contiene un intervalo.</span><span class="sxs-lookup"><span data-stu-id="3c255-107">If **YearSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Year** contains an interval.</span></span>

<span data-ttu-id="3c255-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3c255-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="3c255-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3c255-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c255-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c255-110">Syntax</span></span>


```VB
SWbemDateTime.YearSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="3c255-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3c255-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="3c255-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3c255-112">Examples</span></span>

<span data-ttu-id="3c255-113">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="3c255-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="3c255-114">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="3c255-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c255-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c255-115">Requirements</span></span>



| <span data-ttu-id="3c255-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c255-116">Requirement</span></span> | <span data-ttu-id="3c255-117">Value</span><span class="sxs-lookup"><span data-stu-id="3c255-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c255-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c255-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3c255-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c255-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3c255-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c255-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3c255-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c255-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c255-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c255-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c255-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c255-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c255-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3c255-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="3c255-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3c255-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3c255-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c255-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c255-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c255-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3c255-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="3c255-128">CLSID</span></span><br/>                    | <span data-ttu-id="3c255-129">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="3c255-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="3c255-130">IID</span><span class="sxs-lookup"><span data-stu-id="3c255-130">IID</span></span><br/>                      | <span data-ttu-id="3c255-131">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="3c255-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="3c255-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c255-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c255-133">**SWbemDateTime. Year**</span><span class="sxs-lookup"><span data-stu-id="3c255-133">**SWbemDateTime.Year**</span></span>](swbemdatetime-year.md)
</dt> <dt>

[<span data-ttu-id="3c255-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="3c255-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="3c255-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="3c255-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




