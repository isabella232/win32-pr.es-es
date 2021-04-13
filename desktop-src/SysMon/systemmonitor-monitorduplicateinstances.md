---
title: Propiedad SystemMonitor. MonitorDuplicateInstances
description: Recupera o establece un valor que determina si se pueden supervisar varias instancias de un contador.
ms.assetid: fe8d6074-eb29-4093-9f79-39e6171a3a3f
keywords:
- Propiedad MonitorDuplicateInstances SysMon
- Propiedad MonitorDuplicateInstances SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad MonitorDuplicateInstances
topic_type:
- apiref
api_name:
- SystemMonitor.MonitorDuplicateInstances
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6ae53d0a1dcf3f67a43dab7959bb42619ace6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422211"
---
# <a name="systemmonitormonitorduplicateinstances-property"></a><span data-ttu-id="f51e7-106">Propiedad SystemMonitor. MonitorDuplicateInstances</span><span class="sxs-lookup"><span data-stu-id="f51e7-106">SystemMonitor.MonitorDuplicateInstances property</span></span>

<span data-ttu-id="f51e7-107">Recupera o establece un valor que determina si se pueden supervisar varias instancias de un contador.</span><span class="sxs-lookup"><span data-stu-id="f51e7-107">Retrieves or sets a value that determines whether multiple instances of a counter can be monitored.</span></span>

<span data-ttu-id="f51e7-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f51e7-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f51e7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f51e7-109">Syntax</span></span>


```VB
Property MonitorDuplicateInstances As Boolean
```



## <a name="property-value"></a><span data-ttu-id="f51e7-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f51e7-110">Property value</span></span>

<span data-ttu-id="f51e7-111">True indica que se pueden supervisar varias instancias de un contador (true es el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="f51e7-111">True indicates that multiple instances of a counter can be monitored (True is the default).</span></span> <span data-ttu-id="f51e7-112">False indica que solo se puede supervisar una instancia de un contador.</span><span class="sxs-lookup"><span data-stu-id="f51e7-112">False indicates that only one instance of a counter can be monitored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f51e7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f51e7-113">Remarks</span></span>

<span data-ttu-id="f51e7-114">El monitor de sistema anexa \# n a cada nombre de instancia, excepto el primero, si existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="f51e7-114">System Monitor appends \#n to every instance name, except the first, if multiple instances exist.</span></span> <span data-ttu-id="f51e7-115">El número de serie, n, comienza con uno y se incrementa en uno por cada nueva instancia.</span><span class="sxs-lookup"><span data-stu-id="f51e7-115">The serial number, n, begins with one and is incremented by one for each new instance.</span></span> <span data-ttu-id="f51e7-116">Por ejemplo, si especifica " \\ Process ( \* ) \\ % Processor Time", la colección de contadores debe contener varias instancias de svchost.</span><span class="sxs-lookup"><span data-stu-id="f51e7-116">For example, if you specify "\\Process(\*)\\% Processor Time", the counter collection should contain multiple instances of svchost.</span></span> <span data-ttu-id="f51e7-117">La primera vez será svchost, la siguiente repetición será svchost \# 1, etc.</span><span class="sxs-lookup"><span data-stu-id="f51e7-117">The first occurrence will be svchost, the next occurrence will be svchost\#1, and so on.</span></span>

<span data-ttu-id="f51e7-118">Las instancias duplicadas se supervisan solo si se usa el carácter comodín ( \* ) para el nombre de instancia.</span><span class="sxs-lookup"><span data-stu-id="f51e7-118">Duplicate instances are monitored only if you use the wildcard character (\*) for the instance name.</span></span> <span data-ttu-id="f51e7-119">Si especificó " \\ Process (svchost) \\ % Processor Time", se supervisará la primera instancia encontrada de svchost, no todas las instancias de svchost.</span><span class="sxs-lookup"><span data-stu-id="f51e7-119">If you specified "\\Process(svchost)\\% Processor Time" only the first instance found of svchost is monitored, not all instances of svchost.</span></span>

## <a name="requirements"></a><span data-ttu-id="f51e7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f51e7-120">Requirements</span></span>



| <span data-ttu-id="f51e7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f51e7-121">Requirement</span></span> | <span data-ttu-id="f51e7-122">Value</span><span class="sxs-lookup"><span data-stu-id="f51e7-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f51e7-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f51e7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f51e7-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f51e7-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f51e7-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f51e7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f51e7-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f51e7-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f51e7-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f51e7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f51e7-128"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f51e7-128"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f51e7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f51e7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f51e7-130">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="f51e7-130">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





