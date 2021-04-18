---
description: Convierte una fecha en el formato de cadena FILETIME en el formato de fecha y hora de CIM.
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: Método SWbemDateTime. SetFileTime (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ca3e36a284e3700e166e86f6786218bada8f369e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155840"
---
# <a name="swbemdatetimesetfiletime-method"></a><span data-ttu-id="cf8e7-103">SWbemDateTime. SetFileTime, método</span><span class="sxs-lookup"><span data-stu-id="cf8e7-103">SWbemDateTime.SetFileTime method</span></span>

<span data-ttu-id="cf8e7-104">El método **SetFileTime** del objeto [**SWbemDateTime**](swbemdatetime.md) convierte una fecha en el formato de cadena **FILETIME** al formato de [fecha y hora de CIM](date-and-time-format.md) .</span><span class="sxs-lookup"><span data-stu-id="cf8e7-104">The **SetFileTime** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date in the string **FILETIME** format to the [CIM datetime](date-and-time-format.md) format.</span></span>

<span data-ttu-id="cf8e7-105">El formato **FILETIME** es una estructura datetime de 64 bits que representa el número de unidades de 100-nanosegundos desde el comienzo del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-105">The **FILETIME** format is a 64-bit datetime structure that represents the number of 100-nanosecond units since the beginning of January 1, 1601.</span></span> <span data-ttu-id="cf8e7-106">Instrumental de administración de Windows (WMI) trata los valores de **FILETIME** como representaciones de cadena de números de bits 64 sin signo.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-106">Windows Management Instrumentation (WMI) treats **FILETIME** values as string representations of unsigned 64-bit numbers.</span></span>

<span data-ttu-id="cf8e7-107">Para ver la explicación de la sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="cf8e7-107">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cf8e7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf8e7-108">Syntax</span></span>


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="cf8e7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf8e7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf8e7-110">*strFileTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cf8e7-110">*strFileTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf8e7-111">Valor de **FILETIME** que se usa para establecer el objeto.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-111">**FILETIME** value used to set the object.</span></span>

</dd> <dt>

<span data-ttu-id="cf8e7-112">*bIsLocal* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cf8e7-112">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cf8e7-113">Si es **true**, *strFileTime* se interpreta como una hora local.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-113">If **TRUE**, *strFileTime* is interpreted as a local time.</span></span> <span data-ttu-id="cf8e7-114">La propiedad hora universal coordinada (UTC) contiene la hora local convertida en el desplazamiento UTC correcto.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-114">The Coordinated Universal Time (UTC) property contains the local time converted to the correct UTC offset.</span></span> <span data-ttu-id="cf8e7-115">Cuando *bIsLocal* es **false**, *strFileTime* se convierte directamente en un valor UTC con un desplazamiento de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="cf8e7-115">When *bIsLocal* is **FALSE**, then *strFileTime* is converted directly into a UTC value with an offset of 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf8e7-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf8e7-116">Return value</span></span>

<span data-ttu-id="cf8e7-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-117">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cf8e7-118">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="cf8e7-118">Error codes</span></span>

<span data-ttu-id="cf8e7-119">Después de completar el método **SetFileTime** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-119">After completing the **SetFileTime** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="cf8e7-120">**wbemErrInvalidSyntax** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="cf8e7-120">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="cf8e7-121">El formato de *strFileTime* no es válido.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-121">The format of *strFileTime* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf8e7-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf8e7-122">Remarks</span></span>

<span data-ttu-id="cf8e7-123">Después de una llamada correcta a **SetFileTime**, el valor [**DateTime**](datetime.md) siempre se interpreta como un valor absoluto (**DateTime**) y [**IsInterval**](swbemdatetime-isinterval.md) se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="cf8e7-123">After a successful call to **SetFileTime**, the [**datetime**](datetime.md) value is always interpreted as an absolute (**datetime**) value, and [**IsInterval**](swbemdatetime-isinterval.md) is set to **FALSE**.</span></span>

## <a name="examples"></a><span data-ttu-id="cf8e7-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cf8e7-124">Examples</span></span>

<span data-ttu-id="cf8e7-125">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="cf8e7-125">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="cf8e7-126">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="cf8e7-126">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf8e7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf8e7-127">Requirements</span></span>



| <span data-ttu-id="cf8e7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf8e7-128">Requirement</span></span> | <span data-ttu-id="cf8e7-129">Value</span><span class="sxs-lookup"><span data-stu-id="cf8e7-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf8e7-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf8e7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cf8e7-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf8e7-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cf8e7-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf8e7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cf8e7-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf8e7-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cf8e7-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf8e7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf8e7-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf8e7-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf8e7-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="cf8e7-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="cf8e7-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cf8e7-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cf8e7-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cf8e7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf8e7-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf8e7-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cf8e7-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="cf8e7-140">CLSID</span></span><br/>                    | <span data-ttu-id="cf8e7-141">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="cf8e7-141">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="cf8e7-142">IID</span><span class="sxs-lookup"><span data-stu-id="cf8e7-142">IID</span></span><br/>                      | <span data-ttu-id="cf8e7-143">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="cf8e7-143">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="cf8e7-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf8e7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf8e7-145">**SWbemDateTime.SetVarDate**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-145">**SWbemDateTime.SetVarDate**</span></span>](swbemdatetime-setvardate.md)
</dt> <dt>

[<span data-ttu-id="cf8e7-146">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-146">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="cf8e7-147">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="cf8e7-147">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

