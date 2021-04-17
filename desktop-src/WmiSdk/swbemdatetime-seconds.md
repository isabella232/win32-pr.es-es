---
description: Obtiene o establece un valor que representa el componente de segundos del valor de fecha y hora.
ms.assetid: 194d4309-6abf-4c5f-99f8-60d2c835af6c
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. seconds (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Seconds
- ISWbemDateTime.Seconds
- ISWbemDateTime.get_Seconds
- ISWbemDateTime.put_Seconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0ef4ef15f13bf3d8dfc9272b2a3b734c3678f8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715743"
---
# <a name="swbemdatetimeseconds-property"></a><span data-ttu-id="6d9e7-103">Propiedad SWbemDateTime. seconds</span><span class="sxs-lookup"><span data-stu-id="6d9e7-103">SWbemDateTime.Seconds property</span></span>

<span data-ttu-id="6d9e7-104">La propiedad **seconds** del objeto [**SWbemDateTime**](swbemdatetime.md) obtiene o establece un valor que representa el componente de segundos del valor DateTime.</span><span class="sxs-lookup"><span data-stu-id="6d9e7-104">The **Seconds** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the seconds component of the datetime value.</span></span>

<span data-ttu-id="6d9e7-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6d9e7-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="6d9e7-106">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="6d9e7-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d9e7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d9e7-107">Syntax</span></span>


```VB
SWbemDateTime.Seconds As Long
```



## <a name="property-value"></a><span data-ttu-id="6d9e7-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6d9e7-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="6d9e7-109">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="6d9e7-109">Error codes</span></span>

<span data-ttu-id="6d9e7-110">Después de obtener o establecer la propiedad **segundos** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error siguiente.</span><span class="sxs-lookup"><span data-stu-id="6d9e7-110">After you get or set the **Seconds** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="6d9e7-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="6d9e7-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="6d9e7-112">El valor no estaba en el intervalo comprendido entre 0 y 59.</span><span class="sxs-lookup"><span data-stu-id="6d9e7-112">The value was not in the range of 0 through 59.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d9e7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d9e7-113">Remarks</span></span>

<span data-ttu-id="6d9e7-114">La propiedad **SWbemDateTime. seconds** puede contener un valor incorrecto si la propiedad [**SWbemDateTime. minutes**](swbemdatetime-minutes.md) se ha establecido en 1.</span><span class="sxs-lookup"><span data-stu-id="6d9e7-114">The **SWbemDateTime.Seconds** property may contain an incorrect value if the [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) property has been set to 1.</span></span> <span data-ttu-id="6d9e7-115">Contiene un valor que se desplaza en un segundo debido a un error de redondeo que se produce cuando un valor [**DateTime**](datetime.md) de CIM se convierte en un valor de **\_ fecha de VT** .</span><span class="sxs-lookup"><span data-stu-id="6d9e7-115">It contains a value that is offset by one second because of a rounding error that occurs when a CIM [**DATETIME**](datetime.md) value is translated to a **VT\_DATE** value.</span></span> <span data-ttu-id="6d9e7-116">Si en su lugar la propiedad **minutes** está establecida en 0 (cero), la propiedad **seconds** devuelve el valor correcto.</span><span class="sxs-lookup"><span data-stu-id="6d9e7-116">If the **Minutes** property is set to 0 (zero) instead, then the **Seconds** property returns the correct value.</span></span>

## <a name="examples"></a><span data-ttu-id="6d9e7-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6d9e7-117">Examples</span></span>

<span data-ttu-id="6d9e7-118">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="6d9e7-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="6d9e7-119">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="6d9e7-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d9e7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d9e7-120">Requirements</span></span>



| <span data-ttu-id="6d9e7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d9e7-121">Requirement</span></span> | <span data-ttu-id="6d9e7-122">Value</span><span class="sxs-lookup"><span data-stu-id="6d9e7-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d9e7-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d9e7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6d9e7-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d9e7-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6d9e7-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d9e7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6d9e7-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d9e7-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6d9e7-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d9e7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d9e7-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d9e7-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6d9e7-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6d9e7-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="6d9e7-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6d9e7-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6d9e7-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6d9e7-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d9e7-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d9e7-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6d9e7-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="6d9e7-133">CLSID</span></span><br/>                    | <span data-ttu-id="6d9e7-134">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="6d9e7-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="6d9e7-135">IID</span><span class="sxs-lookup"><span data-stu-id="6d9e7-135">IID</span></span><br/>                      | <span data-ttu-id="6d9e7-136">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="6d9e7-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="6d9e7-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d9e7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d9e7-138">**SWbemDateTime.SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="6d9e7-138">**SWbemDateTime.SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
</dt> <dt>

[<span data-ttu-id="6d9e7-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="6d9e7-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="6d9e7-140">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="6d9e7-140">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

