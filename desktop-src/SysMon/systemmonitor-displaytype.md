---
title: SystemMonitor. DisplayType (propiedad)
description: Recupera o establece el tipo de gráfico que se usa para representar gráficamente los datos del contador de rendimiento.
ms.assetid: a04545b1-920e-4fb3-909b-dc47e1374629
keywords:
- Propiedad DisplayType SysMon
- Propiedad DisplayType SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad DisplayType
topic_type:
- apiref
api_name:
- SystemMonitor.DisplayType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c0e96ff0da57ef9e5f580063dc4f693d672e15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150337"
---
# <a name="systemmonitordisplaytype-property"></a><span data-ttu-id="eca09-106">SystemMonitor. DisplayType (propiedad)</span><span class="sxs-lookup"><span data-stu-id="eca09-106">SystemMonitor.DisplayType property</span></span>

<span data-ttu-id="eca09-107">Recupera o establece el tipo de gráfico que se usa para representar gráficamente los datos del contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="eca09-107">Retrieves or sets the type of graph used to graph the performance counter data.</span></span>

<span data-ttu-id="eca09-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="eca09-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eca09-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eca09-109">Syntax</span></span>


```VB
Property DisplayType As DisplayTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="eca09-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="eca09-110">Property value</span></span>

<span data-ttu-id="eca09-111">Tipo de gráfico que se usa para representar gráficamente los datos del contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="eca09-111">Type of graph used to graph the performance counter data.</span></span> <span data-ttu-id="eca09-112">Para obtener los valores posibles, vea [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span><span class="sxs-lookup"><span data-stu-id="eca09-112">For possible values, see [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).</span></span>

## <a name="exceptions"></a><span data-ttu-id="eca09-113">Excepciones</span><span class="sxs-lookup"><span data-stu-id="eca09-113">Exceptions</span></span>



| <span data-ttu-id="eca09-114">Tipo de excepción</span><span class="sxs-lookup"><span data-stu-id="eca09-114">Exception type</span></span>               | <span data-ttu-id="eca09-115">Condición</span><span class="sxs-lookup"><span data-stu-id="eca09-115">Condition</span></span>                                         |
|------------------------------|---------------------------------------------------|
| <span data-ttu-id="eca09-116">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="eca09-116">**System.ArgumentException**</span></span> | <span data-ttu-id="eca09-117">El gráfico o valor de informe especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="eca09-117">The specified graph or report value is not valid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="eca09-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eca09-118">Requirements</span></span>



| <span data-ttu-id="eca09-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="eca09-119">Requirement</span></span> | <span data-ttu-id="eca09-120">Value</span><span class="sxs-lookup"><span data-stu-id="eca09-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eca09-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eca09-121">Minimum supported client</span></span><br/> | <span data-ttu-id="eca09-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="eca09-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="eca09-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eca09-123">Minimum supported server</span></span><br/> | <span data-ttu-id="eca09-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eca09-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eca09-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eca09-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eca09-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="eca09-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eca09-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="eca09-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eca09-128">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="eca09-128">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





