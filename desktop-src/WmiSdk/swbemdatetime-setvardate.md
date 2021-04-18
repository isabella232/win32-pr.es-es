---
description: Convierte una fecha del formato de fecha de VT \_ al formato de fecha y hora de CIM.
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: Método SWbemDateTime. SetVarDate (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetVarDate
- ISWbemDateTime.SetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8641bad2c59f100b689c74e23faf727bc80d2f49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361376"
---
# <a name="swbemdatetimesetvardate-method"></a><span data-ttu-id="d0e81-103">SWbemDateTime. SetVarDate, método</span><span class="sxs-lookup"><span data-stu-id="d0e81-103">SWbemDateTime.SetVarDate method</span></span>

<span data-ttu-id="d0e81-104">El método **SetVarDate** del objeto [**SWbemDateTime**](swbemdatetime.md) convierte una fecha en el formato de fecha de VT al formato de **\_ fecha** [y hora de CIM](date-and-time-format.md) .</span><span class="sxs-lookup"><span data-stu-id="d0e81-104">The **SetVarDate** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date in the **VT\_DATE** format to the [CIM datetime](date-and-time-format.md) format.</span></span>

<span data-ttu-id="d0e81-105">Un valor de **\_ fecha de VT** es un valor de fecha y hora Variant que Visual Basic y el uso de ActiveX.</span><span class="sxs-lookup"><span data-stu-id="d0e81-105">A **VT\_DATE** value is a variant datetime value that Visual Basic and ActiveX use.</span></span>

<span data-ttu-id="d0e81-106">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d0e81-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0e81-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0e81-107">Syntax</span></span>


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d0e81-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0e81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0e81-109">*vdate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0e81-109">*vdate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e81-110">Valor de fecha Variant para establecer el objeto.</span><span class="sxs-lookup"><span data-stu-id="d0e81-110">The variant date value to set the object.</span></span> <span data-ttu-id="d0e81-111">Este parámetro debe estar en el formato de **\_ fecha VT** .</span><span class="sxs-lookup"><span data-stu-id="d0e81-111">This parameter must be in the **VT\_DATE** format.</span></span>

</dd> <dt>

<span data-ttu-id="d0e81-112">*bIsLocal* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d0e81-112">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e81-113">Si es **true**, *vdate* se interpreta como una hora local y la propiedad hora universal coordinada (UTC) contiene la hora local que se convierte en el desplazamiento UTC correcto.</span><span class="sxs-lookup"><span data-stu-id="d0e81-113">If **TRUE**, *vdate* is interpreted as a local time, and the Coordinated Universal Time (UTC) property contains the local time that is converted to the correct UTC offset.</span></span> <span data-ttu-id="d0e81-114">Cuando *bIsLocal* es **false**, *vdate* se convierte directamente en un valor UTC con un desplazamiento de cero (0).</span><span class="sxs-lookup"><span data-stu-id="d0e81-114">When *bIsLocal* is **FALSE**, then *vdate* is converted directly into a UTC value with an offset of zero (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0e81-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0e81-115">Return value</span></span>

<span data-ttu-id="d0e81-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d0e81-116">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d0e81-117">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d0e81-117">Error codes</span></span>

<span data-ttu-id="d0e81-118">Después de completar el método **SetVarDate** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="d0e81-118">After completing the **SetVarDate** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d0e81-119">**wbemErrInvalidSyntax** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="d0e81-119">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="d0e81-120">El formato de *vdate* no es válido.</span><span class="sxs-lookup"><span data-stu-id="d0e81-120">The format of *vdate* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0e81-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0e81-121">Remarks</span></span>

<span data-ttu-id="d0e81-122">Después de una llamada correcta a **SetVarDate**, el valor de [**fecha y hora**](datetime.md) se interpreta como un valor de fecha y hora absoluto en lugar de un intervalo, y la propiedad [**IsInterval**](swbemdatetime-isinterval.md) se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="d0e81-122">After a successful call to **SetVarDate**, the [**DATETIME**](datetime.md) value is interpreted as an absolute datetime value instead of an interval, and the [**IsInterval**](swbemdatetime-isinterval.md) property is set to **FALSE**.</span></span>

<span data-ttu-id="d0e81-123">Las funciones intrínsecas Visual Basic o VBScript [CDate](/previous-versions//2dt118h2(v=vs.85)) proporcionan un valor [**DateTime**](datetime.md) en el formato de **\_ fecha de VT** para la entrada en **SetVarDate**.</span><span class="sxs-lookup"><span data-stu-id="d0e81-123">The intrinsic Visual Basic or VBScript function [CDate](/previous-versions//2dt118h2(v=vs.85)) provides a [**datetime**](datetime.md) value in the **VT\_DATE** format for input to **SetVarDate**.</span></span>

## <a name="examples"></a><span data-ttu-id="d0e81-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d0e81-124">Examples</span></span>

<span data-ttu-id="d0e81-125">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="d0e81-125">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="d0e81-126">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="d0e81-126">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

<span data-ttu-id="d0e81-127">El código de ejemplo de [conversión de fecha a WMI Date-Time formato](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) de VBScript de la galería de TechNet usa SetVarDate para convertir un valor de fecha y hora normal en el formato de fecha y hora UTC.</span><span class="sxs-lookup"><span data-stu-id="d0e81-127">The [Convert Date to WMI Date-Time Format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript code sample in the TechNet Gallery uses SetVarDate to convert a regular date-time value into the UTC date-time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0e81-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0e81-128">Requirements</span></span>



| <span data-ttu-id="d0e81-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0e81-129">Requirement</span></span> | <span data-ttu-id="d0e81-130">Value</span><span class="sxs-lookup"><span data-stu-id="d0e81-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e81-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0e81-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d0e81-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0e81-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0e81-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0e81-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d0e81-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0e81-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0e81-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0e81-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0e81-136"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0e81-136"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0e81-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d0e81-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="d0e81-138"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d0e81-138"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d0e81-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0e81-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0e81-140"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0e81-140"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d0e81-141">CLSID</span><span class="sxs-lookup"><span data-stu-id="d0e81-141">CLSID</span></span><br/>                    | <span data-ttu-id="d0e81-142">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="d0e81-142">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="d0e81-143">IID</span><span class="sxs-lookup"><span data-stu-id="d0e81-143">IID</span></span><br/>                      | <span data-ttu-id="d0e81-144">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="d0e81-144">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d0e81-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0e81-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0e81-146">**SWbemDateTime.SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="d0e81-146">**SWbemDateTime.SetFileTime**</span></span>](swbemdatetime-setfiletime.md)
</dt> <dt>

[<span data-ttu-id="d0e81-147">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="d0e81-147">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="d0e81-148">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="d0e81-148">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

