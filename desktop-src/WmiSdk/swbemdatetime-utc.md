---
description: Obtiene o establece la representación de hora universal coordinada (UTC) del valor de fecha y hora.
ms.assetid: 43d9d0c8-5521-410f-825b-6b00c3dd0039
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. UTC (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTC
- ISWbemDateTime.UTC
- ISWbemDateTime.get_UTC
- ISWbemDateTime.put_UTC
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 80a4c32e47b94289f66999fdbf1f7daf5f9f03cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706069"
---
# <a name="swbemdatetimeutc-property"></a><span data-ttu-id="612c3-103">Propiedad SWbemDateTime. UTC</span><span class="sxs-lookup"><span data-stu-id="612c3-103">SWbemDateTime.UTC property</span></span>

<span data-ttu-id="612c3-104">La propiedad **UTC** del objeto [**SWbemDateTime**](swbemdatetime.md) obtiene o establece la representación de hora universal coordinada (UTC) del valor **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="612c3-104">The **UTC** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets the Coordinated Universal Times (UTC) representation of the **datetime** value.</span></span> <span data-ttu-id="612c3-105">UTC es el tiempo establecido por el estándar de hora mundial.</span><span class="sxs-lookup"><span data-stu-id="612c3-105">UTC is the time as set by the World Time Standard.</span></span> <span data-ttu-id="612c3-106">La hora UTC ha reemplazado a la hora del meridiano de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="612c3-106">UTC has replaced Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="612c3-107">Un valor UTC con un desplazamiento de cero es igual que GMT con un desplazamiento de cero.</span><span class="sxs-lookup"><span data-stu-id="612c3-107">A UTC value with a zero offset is the same as GMT with a zero offset.</span></span> <span data-ttu-id="612c3-108">El número con signo debe estar en el intervalo de-720 a 720 o se devuelve el error **wbemErrValueOutOfRange** .</span><span class="sxs-lookup"><span data-stu-id="612c3-108">The signed number must be in the range of -720 through 720 or the error **wbemErrValueOutOfRange** is returned.</span></span>

<span data-ttu-id="612c3-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="612c3-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="612c3-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="612c3-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="612c3-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="612c3-111">Syntax</span></span>


```VB
SWbemDateTime.UTC As Long
```



## <a name="property-value"></a><span data-ttu-id="612c3-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="612c3-112">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="612c3-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="612c3-113">Error codes</span></span>

<span data-ttu-id="612c3-114">Después de obtener o establecer la propiedad **UTC** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error siguiente.</span><span class="sxs-lookup"><span data-stu-id="612c3-114">After you get or set the **UTC** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="612c3-115">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="612c3-115">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="612c3-116">El valor no estaba en el intervalo de-720 a 720.</span><span class="sxs-lookup"><span data-stu-id="612c3-116">The value was not in the range of -720 through 720.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="612c3-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="612c3-117">Examples</span></span>

<span data-ttu-id="612c3-118">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="612c3-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="612c3-119">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="612c3-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="612c3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="612c3-120">Requirements</span></span>



| <span data-ttu-id="612c3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="612c3-121">Requirement</span></span> | <span data-ttu-id="612c3-122">Value</span><span class="sxs-lookup"><span data-stu-id="612c3-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="612c3-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="612c3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="612c3-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="612c3-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="612c3-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="612c3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="612c3-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="612c3-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="612c3-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="612c3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="612c3-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="612c3-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="612c3-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="612c3-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="612c3-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="612c3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="612c3-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="612c3-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="612c3-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="612c3-133">CLSID</span></span><br/>                    | <span data-ttu-id="612c3-134">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="612c3-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="612c3-135">IID</span><span class="sxs-lookup"><span data-stu-id="612c3-135">IID</span></span><br/>                      | <span data-ttu-id="612c3-136">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="612c3-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="612c3-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="612c3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="612c3-138">**SWbemDateTime.UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="612c3-138">**SWbemDateTime.UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)
</dt> <dt>

[<span data-ttu-id="612c3-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="612c3-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="612c3-140">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="612c3-140">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

