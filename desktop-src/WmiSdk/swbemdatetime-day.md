---
description: Obtiene o establece un valor que representa el componente de día del valor de fecha y hora.
ms.assetid: 60da99bc-560c-45bc-b787-f4bef8e5a509
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. Day (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Day
- ISWbemDateTime.Day
- ISWbemDateTime.get_Day
- ISWbemDateTime.put_Day
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1de77a8e5d616284c3dc13a19bce2526db371c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002825"
---
# <a name="swbemdatetimeday-property"></a><span data-ttu-id="21005-103">SWbemDateTime. Day (propiedad)</span><span class="sxs-lookup"><span data-stu-id="21005-103">SWbemDateTime.Day property</span></span>

<span data-ttu-id="21005-104">La propiedad **Day** del objeto [**SWbemDateTime**](swbemdatetime.md) obtiene o establece un valor que representa el componente de día del valor DateTime.</span><span class="sxs-lookup"><span data-stu-id="21005-104">The **Day** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the day component of the datetime value.</span></span> <span data-ttu-id="21005-105">El valor debe estar en el intervalo comprendido entre 1 y 31 si [**IsInterval**](swbemdatetime-isinterval.md) es **false**.</span><span class="sxs-lookup"><span data-stu-id="21005-105">The value must be in the range of 1 through 31 if [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**.</span></span> <span data-ttu-id="21005-106">Sin embargo, la comprobación de errores no es sensible al valor del mes.</span><span class="sxs-lookup"><span data-stu-id="21005-106">However, error checking is not sensitive to the month value.</span></span> <span data-ttu-id="21005-107">Por lo tanto, el valor en el intervalo de 31 no devolverá un error en los casos en los que el valor de [**SWbemDateTime. month**](swbemdatetime-month.md) sea para un mes de menos de 31 días (febrero, abril, junio, septiembre, noviembre).</span><span class="sxs-lookup"><span data-stu-id="21005-107">Thus, the in-range value of 31 will not return an error in the cases where the [**SWbemDateTime.Month**](swbemdatetime-month.md) value is for a month of fewer than 31 days (February, April, June, September, November).</span></span>

<span data-ttu-id="21005-108">El valor predeterminado para **Day** es 01.</span><span class="sxs-lookup"><span data-stu-id="21005-108">The default value for **Day** is 01.</span></span>

<span data-ttu-id="21005-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="21005-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="21005-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="21005-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="21005-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21005-111">Syntax</span></span>


```VB
SWbemDateTime.Day As Long
```



## <a name="property-value"></a><span data-ttu-id="21005-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="21005-112">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="21005-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="21005-113">Error codes</span></span>

<span data-ttu-id="21005-114">Después de obtener o establecer la propiedad **Day** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error siguiente.</span><span class="sxs-lookup"><span data-stu-id="21005-114">After you get or set the **Day** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="21005-115">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="21005-115">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="21005-116">Si [**IsInterval**](swbemdatetime-isinterval.md) es **true** y el intervalo de valores correctos supera de 0 a 99999999.</span><span class="sxs-lookup"><span data-stu-id="21005-116">If [**IsInterval**](swbemdatetime-isinterval.md) is **TRUE** and the range of correct values exceeds 0 through 99999999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="21005-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="21005-117">Examples</span></span>

<span data-ttu-id="21005-118">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="21005-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="21005-119">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="21005-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21005-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21005-120">Requirements</span></span>



| <span data-ttu-id="21005-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="21005-121">Requirement</span></span> | <span data-ttu-id="21005-122">Value</span><span class="sxs-lookup"><span data-stu-id="21005-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21005-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21005-123">Minimum supported client</span></span><br/> | <span data-ttu-id="21005-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21005-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="21005-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21005-125">Minimum supported server</span></span><br/> | <span data-ttu-id="21005-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21005-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="21005-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21005-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="21005-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="21005-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="21005-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="21005-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="21005-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="21005-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="21005-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="21005-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21005-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21005-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="21005-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="21005-133">CLSID</span></span><br/>                    | <span data-ttu-id="21005-134">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="21005-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="21005-135">IID</span><span class="sxs-lookup"><span data-stu-id="21005-135">IID</span></span><br/>                      | <span data-ttu-id="21005-136">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="21005-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="21005-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="21005-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21005-138">**SWbemDateTime.DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="21005-138">**SWbemDateTime.DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
</dt> <dt>

[<span data-ttu-id="21005-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="21005-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="21005-140">DATETIME</span><span class="sxs-lookup"><span data-stu-id="21005-140">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

