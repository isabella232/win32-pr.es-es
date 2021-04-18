---
description: Obtiene o establece un valor que representa el componente de mes del valor de fecha y hora.
ms.assetid: 05818f0a-7e15-4ddd-a6a7-9d16ae82cd3c
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. month (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Month
- ISWbemDateTime.Month
- ISWbemDateTime.get_Month
- ISWbemDateTime.put_Month
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 73769d73cffc5b9731cfd55785e2fa087182b33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707349"
---
# <a name="swbemdatetimemonth-property"></a><span data-ttu-id="e23d1-103">Propiedad SWbemDateTime. month</span><span class="sxs-lookup"><span data-stu-id="e23d1-103">SWbemDateTime.Month property</span></span>

<span data-ttu-id="e23d1-104">La propiedad **Month** del objeto [**SWbemDateTime**](swbemdatetime.md) obtiene o establece un valor que representa el componente de mes del valor DateTime.</span><span class="sxs-lookup"><span data-stu-id="e23d1-104">The **Month** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the month component of the datetime value.</span></span> <span data-ttu-id="e23d1-105">El número debe estar en el intervalo comprendido entre 01 y 12 o se devuelve el error **wbemValueOutOfRange** .</span><span class="sxs-lookup"><span data-stu-id="e23d1-105">The number must be in the range of 01 through 12 or the error **wbemValueOutOfRange** is returned.</span></span>

<span data-ttu-id="e23d1-106">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e23d1-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="e23d1-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e23d1-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e23d1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e23d1-108">Syntax</span></span>


```VB
SWbemDateTime.Month As Long
```



## <a name="property-value"></a><span data-ttu-id="e23d1-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e23d1-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="e23d1-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e23d1-110">Examples</span></span>

<span data-ttu-id="e23d1-111">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="e23d1-111">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="e23d1-112">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="e23d1-112">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e23d1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e23d1-113">Requirements</span></span>



| <span data-ttu-id="e23d1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e23d1-114">Requirement</span></span> | <span data-ttu-id="e23d1-115">Value</span><span class="sxs-lookup"><span data-stu-id="e23d1-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e23d1-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e23d1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e23d1-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e23d1-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e23d1-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e23d1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e23d1-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e23d1-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e23d1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e23d1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e23d1-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e23d1-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e23d1-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e23d1-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="e23d1-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e23d1-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e23d1-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e23d1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e23d1-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e23d1-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e23d1-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="e23d1-126">CLSID</span></span><br/>                    | <span data-ttu-id="e23d1-127">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="e23d1-127">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="e23d1-128">IID</span><span class="sxs-lookup"><span data-stu-id="e23d1-128">IID</span></span><br/>                      | <span data-ttu-id="e23d1-129">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="e23d1-129">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="e23d1-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e23d1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e23d1-131">**SWbemDateTime.MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="e23d1-131">**SWbemDateTime.MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
</dt> <dt>

[<span data-ttu-id="e23d1-132">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="e23d1-132">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="e23d1-133">DATETIME</span><span class="sxs-lookup"><span data-stu-id="e23d1-133">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




