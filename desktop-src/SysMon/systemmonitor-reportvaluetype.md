---
title: Propiedad SystemMonitor. ReportValueType
description: Recupera o establece un valor que determina si el histograma y las vistas de informe representan el último valor muestreado durante el intervalo de muestreo o un valor calculado del muestreo, como el valor del contador promedio o mínimo.
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- Propiedad ReportValueType SysMon
- Propiedad ReportValueType SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad ReportValueType
topic_type:
- apiref
api_name:
- SystemMonitor.ReportValueType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc340516f1d99bb77dcc5a31c03eb189d2d70a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996350"
---
# <a name="systemmonitorreportvaluetype-property"></a><span data-ttu-id="d0007-106">Propiedad SystemMonitor. ReportValueType</span><span class="sxs-lookup"><span data-stu-id="d0007-106">SystemMonitor.ReportValueType property</span></span>

<span data-ttu-id="d0007-107">Recupera o establece un valor que determina si el histograma y las vistas de informe representan el último valor muestreado durante el intervalo de muestreo o un valor calculado del muestreo, como el valor del contador promedio o mínimo.</span><span class="sxs-lookup"><span data-stu-id="d0007-107">Retrieves or sets a value that determines if the Histogram and Report views graph the last value sampled during the sampling interval or a calculated value from the sampling, such as the average or minimum counter value.</span></span>

<span data-ttu-id="d0007-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d0007-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0007-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0007-109">Syntax</span></span>


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a><span data-ttu-id="d0007-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d0007-110">Property value</span></span>

<span data-ttu-id="d0007-111">Determina si el histograma y las vistas de informe representan el último valor muestreado durante el intervalo de muestreo o un valor calculado del intervalo de muestreo.</span><span class="sxs-lookup"><span data-stu-id="d0007-111">Determines if the Histogram and Report views graph the last value sampled during the sampling interval or a calculated value from the sampling interval.</span></span> <span data-ttu-id="d0007-112">Para obtener los valores posibles, vea [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="d0007-112">For possible values, see [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).</span></span>

## <a name="remarks"></a><span data-ttu-id="d0007-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0007-113">Remarks</span></span>

<span data-ttu-id="d0007-114">SYSMON omite este valor y usa [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) si [**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) no es [**DisplayTypeConstants.sysmonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) o **DisplayTypeConstants.sysmonReport**.</span><span class="sxs-lookup"><span data-stu-id="d0007-114">SYSMON ignores this value and uses [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) if [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) is not [**DisplayTypeConstants.sysmonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) or **DisplayTypeConstants.sysmonReport**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0007-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0007-115">Requirements</span></span>



| <span data-ttu-id="d0007-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0007-116">Requirement</span></span> | <span data-ttu-id="d0007-117">Value</span><span class="sxs-lookup"><span data-stu-id="d0007-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0007-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0007-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d0007-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d0007-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d0007-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0007-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d0007-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d0007-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0007-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0007-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0007-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="d0007-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0007-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0007-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0007-125">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="d0007-125">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





