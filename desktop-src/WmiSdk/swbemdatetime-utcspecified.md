---
description: Valor booleano que indica si el componente de hora universal coordinada (UTC) del valor DateTime de CIM contiene un intervalo o un valor de carácter comodín.
ms.assetid: 9cb04351-294b-48ba-8d1c-2f28cb9ce463
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. UTCSpecified (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTCSpecified
- ISWbemDateTime.UTCSpecified
- ISWbemDateTime.get_UTCSpecified
- ISWbemDateTime.put_UTCSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2ada5bbbfa68e6cb63c0e060d6c3a12c0f771a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706648"
---
# <a name="swbemdatetimeutcspecified-property"></a><span data-ttu-id="8a37a-103">Propiedad SWbemDateTime. UTCSpecified</span><span class="sxs-lookup"><span data-stu-id="8a37a-103">SWbemDateTime.UTCSpecified property</span></span>

<span data-ttu-id="8a37a-104">La propiedad **UTCSpecified** del objeto [**SWbemDateTime**](swbemdatetime.md) es un valor booleano que indica si el componente de hora universal coordinada (UTC) del valor DateTime de CIM contiene un intervalo o un valor comodín.</span><span class="sxs-lookup"><span data-stu-id="8a37a-104">The **UTCSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the Universal Coordinated Time (UTC) component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="8a37a-105">Si **UTCSpecified** es **true** y [**IsInterval**](swbemdatetime-isinterval.md) es **false**, [**SWbemDateTime. UTC**](swbemdatetime-utc.md) contiene un valor [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="8a37a-105">If **UTCSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.UTC**](swbemdatetime-utc.md) contains a [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="8a37a-106">Un valor **DateTime** que contiene un intervalo no se puede convertir en el formato de **\_ fecha VT** o en el formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="8a37a-106">A **DATETIME** value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="8a37a-107">Si **UTCSpecified** es **false** y **IsInterval** es **true**, **SWbemDateTime. UTC** contiene un intervalo.</span><span class="sxs-lookup"><span data-stu-id="8a37a-107">If **UTCSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.UTC** contains an interval.</span></span>

<span data-ttu-id="8a37a-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8a37a-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="8a37a-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8a37a-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a37a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a37a-110">Syntax</span></span>


```VB
SWbemDateTime.UTCSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="8a37a-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8a37a-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="8a37a-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8a37a-112">Examples</span></span>

<span data-ttu-id="8a37a-113">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="8a37a-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="8a37a-114">Para obtener una descripción del formato de fecha y hora de CIM, consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="8a37a-114">For a description of the CIM datetime format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a37a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a37a-115">Requirements</span></span>



| <span data-ttu-id="8a37a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a37a-116">Requirement</span></span> | <span data-ttu-id="8a37a-117">Value</span><span class="sxs-lookup"><span data-stu-id="8a37a-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a37a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a37a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8a37a-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a37a-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a37a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a37a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8a37a-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a37a-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a37a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a37a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a37a-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a37a-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a37a-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8a37a-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="8a37a-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8a37a-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8a37a-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a37a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a37a-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a37a-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8a37a-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="8a37a-128">CLSID</span></span><br/>                    | <span data-ttu-id="8a37a-129">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="8a37a-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="8a37a-130">IID</span><span class="sxs-lookup"><span data-stu-id="8a37a-130">IID</span></span><br/>                      | <span data-ttu-id="8a37a-131">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="8a37a-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="8a37a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a37a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a37a-133">**SWbemDateTime. UTC**</span><span class="sxs-lookup"><span data-stu-id="8a37a-133">**SWbemDateTime.UTC**</span></span>](swbemdatetime-utc.md)
</dt> <dt>

[<span data-ttu-id="8a37a-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="8a37a-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="8a37a-135">DATETIME</span><span class="sxs-lookup"><span data-stu-id="8a37a-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




