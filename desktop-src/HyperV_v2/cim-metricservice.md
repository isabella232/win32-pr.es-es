---
description: Administra las métricas de los elementos administrados.
ms.assetid: df249d0c-960b-47d6-9590-f0fd08ddec18
title: CIM_MetricService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 41c4ab5e947fe22434e38006c5169711701915a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667567"
---
# <a name="cim_metricservice-class"></a><span data-ttu-id="e7cdb-103">\_Clase MetricService de CIM</span><span class="sxs-lookup"><span data-stu-id="e7cdb-103">CIM\_MetricService class</span></span>

<span data-ttu-id="e7cdb-104">Administra las métricas de los elementos administrados.</span><span class="sxs-lookup"><span data-stu-id="e7cdb-104">Manages metrics for managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7cdb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7cdb-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="e7cdb-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e7cdb-106">Members</span></span>

<span data-ttu-id="e7cdb-107">La clase **CIM \_ MetricService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e7cdb-107">The **CIM\_MetricService** class has these types of members:</span></span>

-   [<span data-ttu-id="e7cdb-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="e7cdb-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e7cdb-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e7cdb-109">Methods</span></span>

<span data-ttu-id="e7cdb-110">La clase **CIM \_ MetricService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e7cdb-110">The **CIM\_MetricService** class has these methods.</span></span>



| <span data-ttu-id="e7cdb-111">Método</span><span class="sxs-lookup"><span data-stu-id="e7cdb-111">Method</span></span>                                                                   | <span data-ttu-id="e7cdb-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7cdb-112">Description</span></span>                                                                                                                                                                         |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7cdb-113">**ControlMetrics**</span><span class="sxs-lookup"><span data-stu-id="e7cdb-113">**ControlMetrics**</span></span>](cim-metricservice-controlmetrics.md)               | <span data-ttu-id="e7cdb-114">Habilita y deshabilita la recopilación de métricas.</span><span class="sxs-lookup"><span data-stu-id="e7cdb-114">Enables and disables the collection of metrics.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="e7cdb-115">**ControlMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="e7cdb-115">**ControlMetricsByClass**</span></span>](cim-metricservice-controlmetricsbyclass.md) | <span data-ttu-id="e7cdb-116">Habilita y deshabilita la colección de métricas de una clase.</span><span class="sxs-lookup"><span data-stu-id="e7cdb-116">Enables and disables the collection of metrics for a class.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="e7cdb-117">**ControlSampleTimes**</span><span class="sxs-lookup"><span data-stu-id="e7cdb-117">**ControlSampleTimes**</span></span>](cim-metricservice-controlsampletimes.md)       | <span data-ttu-id="e7cdb-118">Especifica cuándo se recopilan las métricas.</span><span class="sxs-lookup"><span data-stu-id="e7cdb-118">Specifies when metrics are gathered.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="e7cdb-119">**GetMetricValues**</span><span class="sxs-lookup"><span data-stu-id="e7cdb-119">**GetMetricValues**</span></span>](cim-metricservice-getmetricvalues.md)             | <span data-ttu-id="e7cdb-120">Recupera una lista filtrada de valores de métricas.</span><span class="sxs-lookup"><span data-stu-id="e7cdb-120">Retrieves a filtered list of metric values.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="e7cdb-121">**ShowMetrics**</span><span class="sxs-lookup"><span data-stu-id="e7cdb-121">**ShowMetrics**</span></span>](cim-metricservice-showmetrics.md)                     | <span data-ttu-id="e7cdb-122">Indica si la colección de métricas está habilitada para los elementos administrados especificados e indica las métricas que están disponibles para la colección para cada elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="e7cdb-122">Indicates whether metric collection is enabled for the specified managed elements, and indicates the metrics that are available for collection for each managed element.</span></span><br/> |
| [<span data-ttu-id="e7cdb-123">**ShowMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="e7cdb-123">**ShowMetricsByClass**</span></span>](cim-metricservice-showmetricsbyclass.md)       | <span data-ttu-id="e7cdb-124">Indica qué métricas están disponibles para la recopilación para todas las instancias de una clase CIM.</span><span class="sxs-lookup"><span data-stu-id="e7cdb-124">Indicates which metrics are available for collection for all instances of a CIM class.</span></span><br/>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="e7cdb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7cdb-125">Requirements</span></span>



| <span data-ttu-id="e7cdb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7cdb-126">Requirement</span></span> | <span data-ttu-id="e7cdb-127">Value</span><span class="sxs-lookup"><span data-stu-id="e7cdb-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7cdb-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7cdb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e7cdb-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e7cdb-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e7cdb-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7cdb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e7cdb-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e7cdb-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e7cdb-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e7cdb-132">Namespace</span></span><br/>                | <span data-ttu-id="e7cdb-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e7cdb-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e7cdb-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e7cdb-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7cdb-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7cdb-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7cdb-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e7cdb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7cdb-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e7cdb-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e7cdb-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7cdb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7cdb-139">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="e7cdb-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




