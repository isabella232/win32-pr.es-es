---
description: Obtiene o establece la fecha de CIM sin procesar en el formato DMTF (Distributed Management Task Force).
ms.assetid: 426a60d5-c364-406e-8346-049a13d59c7f
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. Value (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Value
- ISWbemDateTime.Value
- ISWbemDateTime.get_Value
- ISWbemDateTime.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2ecb3a42a865559ba9b3c3e5fbec7302f975fa0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155837"
---
# <a name="swbemdatetimevalue-property"></a><span data-ttu-id="17436-103">SWbemDateTime. Value (propiedad)</span><span class="sxs-lookup"><span data-stu-id="17436-103">SWbemDateTime.Value property</span></span>

<span data-ttu-id="17436-104">La propiedad **Value** del objeto [**SWbemDateTime**](swbemdatetime.md) obtiene o establece la fecha de CIM sin procesar en el formato DMTF (Distributed Management Task Force).</span><span class="sxs-lookup"><span data-stu-id="17436-104">The **Value** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets the raw CIM date in the DMTF (Distributed Management Task Force) format.</span></span> <span data-ttu-id="17436-105">El formato DMTF es una representación de cadena del valor [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="17436-105">The DMTF format is a string representation of the [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="17436-106">Esta propiedad es la propiedad predeterminada para los objetos **SWbemDateTime** .</span><span class="sxs-lookup"><span data-stu-id="17436-106">This property is the default property for **SWbemDateTime** objects.</span></span> <span data-ttu-id="17436-107">La propiedad **Value** tiene un valor predeterminado de 00000101000000.000000 + 000.</span><span class="sxs-lookup"><span data-stu-id="17436-107">The **Value** property has a default value of 00000101000000.000000+000.</span></span>

<span data-ttu-id="17436-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="17436-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="17436-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="17436-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="17436-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17436-110">Syntax</span></span>


```VB
SWbemDateTime.Value As String
```



## <a name="property-value"></a><span data-ttu-id="17436-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="17436-111">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="17436-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="17436-112">Error codes</span></span>

<span data-ttu-id="17436-113">Después de obtener o establecer la propiedad **Value** , el objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) puede contener el código de error siguiente.</span><span class="sxs-lookup"><span data-stu-id="17436-113">After you get or set the **Value** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="17436-114">**wbemErrInvalidSyntax** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="17436-114">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="17436-115">El formato de *strValue* no es válido.</span><span class="sxs-lookup"><span data-stu-id="17436-115">The format of *strValue* is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="17436-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="17436-116">Examples</span></span>

<span data-ttu-id="17436-117">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y [**hora**](datetime.md) de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="17436-117">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="17436-118">Para obtener una descripción del formato de fecha y hora **de CIM,** consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="17436-118">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17436-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17436-119">Requirements</span></span>



| <span data-ttu-id="17436-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="17436-120">Requirement</span></span> | <span data-ttu-id="17436-121">Value</span><span class="sxs-lookup"><span data-stu-id="17436-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17436-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17436-122">Minimum supported client</span></span><br/> | <span data-ttu-id="17436-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17436-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17436-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17436-124">Minimum supported server</span></span><br/> | <span data-ttu-id="17436-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17436-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17436-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17436-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="17436-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="17436-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="17436-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="17436-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="17436-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="17436-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="17436-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="17436-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17436-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17436-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="17436-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="17436-132">CLSID</span></span><br/>                    | <span data-ttu-id="17436-133">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="17436-133">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="17436-134">IID</span><span class="sxs-lookup"><span data-stu-id="17436-134">IID</span></span><br/>                      | <span data-ttu-id="17436-135">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="17436-135">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="17436-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="17436-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17436-137">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="17436-137">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="17436-138">**DATETIME**</span><span class="sxs-lookup"><span data-stu-id="17436-138">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

