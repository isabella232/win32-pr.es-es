---
description: Valor booleano que indica si cualquier campo de un valor DateTime de CIM debe interpretarse como un intervalo.
ms.assetid: ba5fcf17-7c26-4960-9da9-e380d90e5f3e
ms.tgt_platform: multiple
title: Propiedad SWbemDateTime. IsInterval (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.IsInterval
- ISWbemDateTime.IsInterval
- ISWbemDateTime.get_IsInterval
- ISWbemDateTime.put_IsInterval
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 468ea16de4f1206a9a15c58c2c7891df8afd4c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279292"
---
# <a name="swbemdatetimeisinterval-property"></a><span data-ttu-id="a6829-103">Propiedad SWbemDateTime. IsInterval</span><span class="sxs-lookup"><span data-stu-id="a6829-103">SWbemDateTime.IsInterval property</span></span>

<span data-ttu-id="a6829-104">La propiedad **IsInterval** del objeto [**SWbemDateTime**](swbemdatetime.md) es un valor booleano que indica si cualquier campo de un valor DateTime de CIM debe interpretarse como un intervalo.</span><span class="sxs-lookup"><span data-stu-id="a6829-104">The **IsInterval** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether any field in a CIM datetime value should be interpreted as an interval.</span></span>

<span data-ttu-id="a6829-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a6829-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="a6829-106">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a6829-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6829-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6829-107">Syntax</span></span>


```VB
SWbemDateTime.IsInterval As boolean
```



## <a name="property-value"></a><span data-ttu-id="a6829-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a6829-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="a6829-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a6829-109">Examples</span></span>

<span data-ttu-id="a6829-110">Para obtener ejemplos del uso del objeto [**SWbemDateTime**](swbemdatetime.md) para convertir valores de fecha y hora de CIM en el formato **FILETIME** o en el formato de **\_ fecha de VT** , vea [tareas de WMI: fechas y horas](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="a6829-110">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM datetime values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="a6829-111">Para obtener una descripción del formato de fecha y hora de CIM, consulte [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="a6829-111">For a description of the CIM datetime format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6829-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6829-112">Requirements</span></span>



| <span data-ttu-id="a6829-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6829-113">Requirement</span></span> | <span data-ttu-id="a6829-114">Value</span><span class="sxs-lookup"><span data-stu-id="a6829-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6829-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6829-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a6829-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a6829-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a6829-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6829-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a6829-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6829-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a6829-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6829-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6829-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6829-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6829-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a6829-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="a6829-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a6829-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a6829-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a6829-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6829-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6829-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a6829-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="a6829-125">CLSID</span></span><br/>                    | <span data-ttu-id="a6829-126">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="a6829-126">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="a6829-127">IID</span><span class="sxs-lookup"><span data-stu-id="a6829-127">IID</span></span><br/>                      | <span data-ttu-id="a6829-128">\_ISWBEMDATETIME IID</span><span class="sxs-lookup"><span data-stu-id="a6829-128">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="a6829-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6829-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6829-130">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="a6829-130">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="a6829-131">Formato de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="a6829-131">Date and Time Format</span></span>](date-and-time-format.md)
</dt> </dl>

 

 




