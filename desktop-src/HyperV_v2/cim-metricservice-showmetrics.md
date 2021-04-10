---
description: 'Notifica lo siguiente: las métricas disponibles que se van a recopilar para un elemento administrado, los elementos administrados para los que se puede recopilar una métrica definida por una instancia de BaseMetricDefinition de CIM \_ y si una métrica determinada se está recopilando actualmente para un elemento administrado.'
ms.assetid: 5af430d2-9ab3-4bee-ad51-d9045b51172a
title: Método ShowMetrics de la clase CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1e0e062adaefd6c6d9bdabe6f168bd64e789acc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156593"
---
# <a name="showmetrics-method-of-the-cim_metricservice-class"></a><span data-ttu-id="4ccb6-103">Método ShowMetrics de la \_ clase MetricService de CIM</span><span class="sxs-lookup"><span data-stu-id="4ccb6-103">ShowMetrics method of the CIM\_MetricService class</span></span>

<span data-ttu-id="4ccb6-104">Notifica lo siguiente: las métricas disponibles que se van a recopilar para un elemento administrado, los elementos administrados para los que se puede recopilar una métrica definida por una instancia de [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) y si una métrica determinada se está recopilando actualmente para un elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="4ccb6-104">Reports the following: the metrics available to be collected for a managed element, the managed elements for which a metric defined by an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) is available to be collected, and whether or not a particular metric is currently being collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ccb6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ccb6-105">Syntax</span></span>


```mof
uint32 ShowMetrics(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_ManagedElement       REF ManagedElements[],
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="4ccb6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ccb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ccb6-107">*Asunto* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ccb6-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccb6-108">Identifica una instancia de [**CIM \_ de CIM**](cim-managedelement.md) para la que el método devuelve referencias a instancias de [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) que definen métricas que se capturan para el **\_ ManagedElement de CIM**.</span><span class="sxs-lookup"><span data-stu-id="4ccb6-108">Identifies an instance of [**CIM\_ManagedElement**](cim-managedelement.md) for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are being captured for the **CIM\_ManagedElement**.</span></span>

</dd> <dt>

<span data-ttu-id="4ccb6-109">*Definición* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4ccb6-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccb6-110">Identifica una instancia de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="4ccb6-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="4ccb6-111">El método devuelve referencias a instancias de [**CIM \_ de CIM**](cim-managedelement.md) para las que se pueden recopilar las métricas definidas por la instancia de **\_ BaseMetricDefinition de CIM** .</span><span class="sxs-lookup"><span data-stu-id="4ccb6-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="4ccb6-112">*ManagedElements* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4ccb6-112">*ManagedElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccb6-113">Si se ejecuta correctamente, puede contener referencias a objetos de [**\_ ManagedElement de CIM**](cim-managedelement.md) para los que la métrica identificada por el parámetro de *definición* está disponible para la colección.</span><span class="sxs-lookup"><span data-stu-id="4ccb6-113">On success, may contain references to [**CIM\_ManagedElement**](cim-managedelement.md) objects for which the metric identified by the *Definition* parameter is available for collection.</span></span>

</dd> <dt>

<span data-ttu-id="4ccb6-114">*DefinitionList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4ccb6-114">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccb6-115">Si se ejecuta correctamente, puede contener referencias a instancias de objetos [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) que definen las métricas disponibles para la recopilación de los [**\_ ManagedElement de CIM**](cim-managedelement.md) identificados por el parámetro de *asunto* .</span><span class="sxs-lookup"><span data-stu-id="4ccb6-115">On success, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) objects that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4ccb6-116">*MetricNames* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4ccb6-116">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccb6-117">Si se ejecuta correctamente, cada índice de matriz contendrá el valor de la propiedad **Name** para la instancia de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a la que hace referencia el índice de matriz correspondiente del parámetro *DefinitionList* .</span><span class="sxs-lookup"><span data-stu-id="4ccb6-117">On success, each array index shall contain the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4ccb6-118">*MetricCollectionEnabled* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4ccb6-118">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccb6-119">Indica si se va a recopilar una métrica para un elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="4ccb6-119">Indicates whether a metric is being collected for a managed element.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="4ccb6-120">**Habilitar** (2)</span><span class="sxs-lookup"><span data-stu-id="4ccb6-120">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="4ccb6-121">**Deshabilitar** (3)</span><span class="sxs-lookup"><span data-stu-id="4ccb6-121">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="4ccb6-122">**Reservado** (4)</span><span class="sxs-lookup"><span data-stu-id="4ccb6-122">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4ccb6-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="4ccb6-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="4ccb6-124">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="4ccb6-124">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="4ccb6-125"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4ccb6-125"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="4ccb6-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ccb6-126">Return value</span></span>

<span data-ttu-id="4ccb6-127">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="4ccb6-127">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="4ccb6-128">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="4ccb6-128">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4ccb6-129">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="4ccb6-129">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4ccb6-130">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="4ccb6-130">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4ccb6-131">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="4ccb6-131">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4ccb6-132">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="4ccb6-132">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4ccb6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ccb6-133">Requirements</span></span>



| <span data-ttu-id="4ccb6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ccb6-134">Requirement</span></span> | <span data-ttu-id="4ccb6-135">Value</span><span class="sxs-lookup"><span data-stu-id="4ccb6-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ccb6-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ccb6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4ccb6-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4ccb6-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4ccb6-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ccb6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4ccb6-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4ccb6-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4ccb6-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4ccb6-140">Namespace</span></span><br/>                | <span data-ttu-id="4ccb6-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4ccb6-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4ccb6-142">MOF</span><span class="sxs-lookup"><span data-stu-id="4ccb6-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ccb6-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ccb6-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ccb6-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4ccb6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ccb6-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4ccb6-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4ccb6-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ccb6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ccb6-147">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="4ccb6-147">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




