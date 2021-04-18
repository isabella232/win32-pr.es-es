---
description: Representa el valor de instancia de una métrica definida por una instancia de CIM \_ AggregationMetricDefinition.
ms.assetid: 663ef18a-0238-416f-9682-8809b271b4fc
title: CIM_AggregationMetricValue (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricValue
- CIM_AggregationMetricValue.AggregationTimeStamp
- CIM_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0af264b66838e7c039ef3f99a4f365ebab55c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666917"
---
# <a name="cim_aggregationmetricvalue-class"></a><span data-ttu-id="abcda-103">\_Clase AggregationMetricValue de CIM</span><span class="sxs-lookup"><span data-stu-id="abcda-103">CIM\_AggregationMetricValue class</span></span>

<span data-ttu-id="abcda-104">Representa el valor de instancia de una métrica definida por una instancia de **CIM \_ AggregationMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="abcda-104">Represents the instance value of a metric defined by an instance of **CIM\_AggregationMetricDefinition**.</span></span>

## <a name="syntax"></a><span data-ttu-id="abcda-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="abcda-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricValue : CIM_BaseMetricValue
{
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a><span data-ttu-id="abcda-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="abcda-106">Members</span></span>

<span data-ttu-id="abcda-107">La clase **CIM \_ AggregationMetricValue** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="abcda-107">The **CIM\_AggregationMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="abcda-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="abcda-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="abcda-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="abcda-109">Properties</span></span>

<span data-ttu-id="abcda-110">La clase **CIM \_ AggregationMetricValue** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="abcda-110">The **CIM\_AggregationMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abcda-111">**AggregationDuration**</span><span class="sxs-lookup"><span data-stu-id="abcda-111">**AggregationDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-112">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="abcda-112">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="abcda-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abcda-114">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricValue**.**AggregationTimeStamp**")</span><span class="sxs-lookup"><span data-stu-id="abcda-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricValue**.**AggregationTimeStamp**")</span></span>
</dt> </dl>

<span data-ttu-id="abcda-115">Representa la duración de tiempo en la que se calculó la agregación.</span><span class="sxs-lookup"><span data-stu-id="abcda-115">Represents the time duration over which the aggregation was computed.</span></span> <span data-ttu-id="abcda-116">El inicio de un intervalo de supervisión sobre el que se aplica la función de agregación se determina restando el valor de **AggregationDuration** del valor de **AggregationTimestamp** .</span><span class="sxs-lookup"><span data-stu-id="abcda-116">The start of a monitoring interval over which the aggregation function is applied is determined by subtracting the **AggregationDuration** value from the **AggregationTimestamp** value.</span></span>

</dd> <dt>

<span data-ttu-id="abcda-117">**AggregationTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="abcda-117">**AggregationTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abcda-118">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="abcda-118">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="abcda-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="abcda-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abcda-120">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricValue**.**Duration**")</span><span class="sxs-lookup"><span data-stu-id="abcda-120">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="abcda-121">Hora a la que se aplicó la función de agregación para determinar el valor de la instancia de métrica.</span><span class="sxs-lookup"><span data-stu-id="abcda-121">The time when the aggregation function was applied to determine the value of the metric instance.</span></span> <span data-ttu-id="abcda-122">Esto es diferente del momento en que se crea la instancia.</span><span class="sxs-lookup"><span data-stu-id="abcda-122">This is different from the time when the instance is created.</span></span> <span data-ttu-id="abcda-123">El valor **AggregationTimeStamp** cambia cada vez que se aplica la función de agregación para calcular el valor.</span><span class="sxs-lookup"><span data-stu-id="abcda-123">The **AggregationTimeStamp** value changes whenever the aggregation function is applied to calculate the value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abcda-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abcda-124">Requirements</span></span>



| <span data-ttu-id="abcda-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="abcda-125">Requirement</span></span> | <span data-ttu-id="abcda-126">Value</span><span class="sxs-lookup"><span data-stu-id="abcda-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abcda-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abcda-127">Minimum supported client</span></span><br/> | <span data-ttu-id="abcda-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="abcda-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="abcda-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abcda-129">Minimum supported server</span></span><br/> | <span data-ttu-id="abcda-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="abcda-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="abcda-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="abcda-131">Namespace</span></span><br/>                | <span data-ttu-id="abcda-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="abcda-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="abcda-133">MOF</span><span class="sxs-lookup"><span data-stu-id="abcda-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abcda-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abcda-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="abcda-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="abcda-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abcda-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="abcda-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="abcda-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="abcda-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abcda-138">**\_BASEMETRICVALUE CIM**</span><span class="sxs-lookup"><span data-stu-id="abcda-138">**CIM\_BaseMetricValue**</span></span>](cim-basemetricvalue.md)
</dt> </dl>

 

