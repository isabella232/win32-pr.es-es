---
description: Obtiene o establece un valor que representa el componente de minutos del valor de fecha y hora.
ms.assetid: a52a66c2-f7ab-48d0-bdee-a07984ed3bc2
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. minutes (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Minutes
- ISWbemDateTime.Minutes
- ISWbemDateTime.get_Minutes
- ISWbemDateTime.put_Minutes
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cce55d731916d0e8180de1bde495566d4ed22c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707350"
---
# <a name="swbemdatetimeminutes-property"></a><span data-ttu-id="85bc9-103">Propiedad SWbemDateTime. minutes</span><span class="sxs-lookup"><span data-stu-id="85bc9-103">SWbemDateTime.Minutes property</span></span>

<span data-ttu-id="85bc9-104">La propiedad **minutes** del objeto [**SWbemDateTime**](swbemdatetime.md) obtiene o establece un valor que representa el componente de minutos del valor DateTime.</span><span class="sxs-lookup"><span data-stu-id="85bc9-104">The **Minutes** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the minutes component of the datetime value.</span></span>

<span data-ttu-id="85bc9-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="85bc9-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="85bc9-106">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="85bc9-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="85bc9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85bc9-107">Syntax</span></span>


```VB
SWbemDateTime.Minutes As Long
```



## <a name="property-value"></a><span data-ttu-id="85bc9-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="85bc9-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="85bc9-109">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="85bc9-109">Error codes</span></span>

<span data-ttu-id="85bc9-110">Después de obtener o establecer la propiedad **minutes** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error siguiente.</span><span class="sxs-lookup"><span data-stu-id="85bc9-110">After you get or set the **Minutes** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="85bc9-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="85bc9-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="85bc9-112">El valor no estaba en el intervalo comprendido entre 0 y 59.</span><span class="sxs-lookup"><span data-stu-id="85bc9-112">The value was not in the range of 0 through 59.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85bc9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85bc9-113">Remarks</span></span>

<span data-ttu-id="85bc9-114">Si la propiedad **SWbemDateTime. minutes** está establecida en 1, la propiedad [**SWbemDateTime. seconds**](swbemdatetime-seconds.md) contiene un valor que se desplaza por un segundo un error de redondeo que se produce cuando un valor **DateTime** de CIM se convierte en un valor de **\_ fecha de VT** .</span><span class="sxs-lookup"><span data-stu-id="85bc9-114">If the **SWbemDateTime.Minutes** property is set to 1, then the [**SWbemDateTime.Seconds**](swbemdatetime-seconds.md) property contains a value that is offset by one second a rounding error that occurs when a CIM **datetime** value is translated to a **VT\_DATE** value.</span></span> <span data-ttu-id="85bc9-115">Si en su lugar la propiedad **minutes** está establecida en 0, la propiedad **seconds** devuelve el valor correcto.</span><span class="sxs-lookup"><span data-stu-id="85bc9-115">If the **Minutes** property is set to 0 instead, then the **Seconds** property returns the correct value.</span></span>

## <a name="examples"></a><span data-ttu-id="85bc9-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="85bc9-116">Examples</span></span>

<span data-ttu-id="85bc9-117">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="85bc9-117">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="85bc9-118">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="85bc9-118">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85bc9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85bc9-119">Requirements</span></span>



| <span data-ttu-id="85bc9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="85bc9-120">Requirement</span></span> | <span data-ttu-id="85bc9-121">Value</span><span class="sxs-lookup"><span data-stu-id="85bc9-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85bc9-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85bc9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="85bc9-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85bc9-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="85bc9-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85bc9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="85bc9-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85bc9-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="85bc9-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85bc9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="85bc9-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="85bc9-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="85bc9-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="85bc9-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="85bc9-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="85bc9-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="85bc9-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85bc9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85bc9-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85bc9-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="85bc9-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="85bc9-132">CLSID</span></span><br/>                    | <span data-ttu-id="85bc9-133">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="85bc9-133">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="85bc9-134">IID</span><span class="sxs-lookup"><span data-stu-id="85bc9-134">IID</span></span><br/>                      | <span data-ttu-id="85bc9-135">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="85bc9-135">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="85bc9-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="85bc9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85bc9-137">**SWbemDateTime.MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="85bc9-137">**SWbemDateTime.MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
</dt> <dt>

[<span data-ttu-id="85bc9-138">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="85bc9-138">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="85bc9-139">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="85bc9-139">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

