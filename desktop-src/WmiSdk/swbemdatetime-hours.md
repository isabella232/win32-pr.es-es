---
description: Obtiene o establece un valor que representa el componente de horas del valor de fecha y hora.
ms.assetid: 83f084fa-57a5-4467-acea-7e19de82a91f
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. Hours (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Hours
- ISWbemDateTime.Hours
- ISWbemDateTime.get_Hours
- ISWbemDateTime.put_Hours
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 27edb3c209e2e95ae7aff20930d260f8f6d44427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278757"
---
# <a name="swbemdatetimehours-property"></a><span data-ttu-id="ede62-103">Propiedad SWbemDateTime. hours</span><span class="sxs-lookup"><span data-stu-id="ede62-103">SWbemDateTime.Hours property</span></span>

<span data-ttu-id="ede62-104">La propiedad **hours** del objeto [**SWbemDateTime**](swbemdatetime.md) obtiene o establece un valor que representa el componente de horas del valor DateTime.</span><span class="sxs-lookup"><span data-stu-id="ede62-104">The **Hours** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the hours component of the datetime value.</span></span>

<span data-ttu-id="ede62-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ede62-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="ede62-106">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ede62-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ede62-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ede62-107">Syntax</span></span>


```VB
SWbemDateTime.Hours As Long
```



## <a name="property-value"></a><span data-ttu-id="ede62-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ede62-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="ede62-109">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ede62-109">Error codes</span></span>

<span data-ttu-id="ede62-110">Después de obtener o establecer la propiedad **hours** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error siguiente.</span><span class="sxs-lookup"><span data-stu-id="ede62-110">After you get or set the **Hours** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="ede62-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="ede62-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="ede62-112">El valor no estaba en el intervalo comprendido entre 0 y 23.</span><span class="sxs-lookup"><span data-stu-id="ede62-112">The value was not in the range of 0 through 23.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ede62-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ede62-113">Examples</span></span>

<span data-ttu-id="ede62-114">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="ede62-114">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="ede62-115">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="ede62-115">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ede62-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ede62-116">Requirements</span></span>



| <span data-ttu-id="ede62-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ede62-117">Requirement</span></span> | <span data-ttu-id="ede62-118">Value</span><span class="sxs-lookup"><span data-stu-id="ede62-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ede62-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ede62-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ede62-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ede62-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ede62-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ede62-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ede62-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ede62-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ede62-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ede62-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ede62-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ede62-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ede62-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ede62-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="ede62-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ede62-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ede62-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ede62-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ede62-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ede62-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ede62-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="ede62-129">CLSID</span></span><br/>                    | <span data-ttu-id="ede62-130">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="ede62-130">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="ede62-131">IID</span><span class="sxs-lookup"><span data-stu-id="ede62-131">IID</span></span><br/>                      | <span data-ttu-id="ede62-132">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="ede62-132">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="ede62-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ede62-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ede62-134">**SWbemDateTime.HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="ede62-134">**SWbemDateTime.HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
</dt> <dt>

[<span data-ttu-id="ede62-135">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="ede62-135">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="ede62-136">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="ede62-136">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

