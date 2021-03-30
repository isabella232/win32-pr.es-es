---
description: 'Notifica lo siguiente: las métricas disponibles que se van a recopilar para todas las instancias de una clase CIM, las clases CIM para las que una métrica definida por una instancia de CIM \_ BaseMetricDefinition se pueden recopilar y si una métrica determinada se está recopilando actualmente para un elemento administrado.'
ms.assetid: 0115a5b5-2824-4c43-a8dc-757524c5d3dd
title: Método ShowMetricsByClass de la clase CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f843c835e6c92e39c4ac1f9628d0479b94a691bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910158"
---
# <a name="showmetricsbyclass-method-of-the-cim_metricservice-class"></a><span data-ttu-id="1e4e7-103">Método ShowMetricsByClass de la \_ clase MetricService de CIM</span><span class="sxs-lookup"><span data-stu-id="1e4e7-103">ShowMetricsByClass method of the CIM\_MetricService class</span></span>

<span data-ttu-id="1e4e7-104">Notifica lo siguiente: las métricas disponibles que se van a recopilar para todas las instancias de una clase CIM, las clases CIM para las que una métrica definida por una instancia de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) se pueden recopilar y si una métrica determinada se está recopilando actualmente para un elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="1e4e7-104">Reports the following: the metrics available to be collected for all instances of a CIM class, The CIM classes for which a metric defined by an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) is available to be collected, and whether or not a particular metric is currently being collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e4e7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e4e7-105">Syntax</span></span>


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="1e4e7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e4e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e4e7-107">*Asunto* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1e4e7-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e4e7-108">Identifica una clase CIM para la que el método devuelve referencias a instancias [**de \_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) que definen las métricas que están disponibles para ser capturadas para todas las instancias de la clase.</span><span class="sxs-lookup"><span data-stu-id="1e4e7-108">Identifies a CIM class for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are available to be captured for all instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="1e4e7-109">*Definición* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1e4e7-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e4e7-110">Identifica una instancia de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="1e4e7-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="1e4e7-111">El método devuelve referencias a instancias de [**CIM \_ de CIM**](cim-managedelement.md) para las que se pueden recopilar las métricas definidas por la instancia de **\_ BaseMetricDefinition de CIM** .</span><span class="sxs-lookup"><span data-stu-id="1e4e7-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="1e4e7-112">*DefinitionList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1e4e7-112">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e4e7-113">Si se ejecuta correctamente, puede contener referencias a instancias de objetos [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) que definen las métricas disponibles para la recopilación de los [**\_ ManagedElement de CIM**](cim-managedelement.md) identificados por el parámetro de *asunto* .</span><span class="sxs-lookup"><span data-stu-id="1e4e7-113">On success, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) objects that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1e4e7-114">*MetricNames* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1e4e7-114">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e4e7-115">Si se ejecuta correctamente, cada índice de matriz contendrá el valor de la propiedad **Name** para la instancia de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a la que hace referencia el índice de matriz correspondiente del parámetro *DefinitionList* .</span><span class="sxs-lookup"><span data-stu-id="1e4e7-115">On success, each array index shall contain the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1e4e7-116">*MetricCollectionEnabled* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1e4e7-116">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e4e7-117">Indica si se va a recopilar una métrica para todas las instancias de una clase de elementos administrados.</span><span class="sxs-lookup"><span data-stu-id="1e4e7-117">Indicates whether a metric is being collected for all instances of a class of managed elements.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1e4e7-118">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="1e4e7-118">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1e4e7-119">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="1e4e7-119">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="1e4e7-120">**Reservado** (4)</span><span class="sxs-lookup"><span data-stu-id="1e4e7-120">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1e4e7-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1e4e7-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="1e4e7-122">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="1e4e7-122">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="1e4e7-123"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1e4e7-123"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="1e4e7-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e4e7-124">Return value</span></span>

<span data-ttu-id="1e4e7-125">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="1e4e7-125">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="1e4e7-126">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="1e4e7-126">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1e4e7-127">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="1e4e7-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1e4e7-128">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="1e4e7-128">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1e4e7-129">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1e4e7-129">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1e4e7-130">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="1e4e7-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1e4e7-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e4e7-131">Requirements</span></span>



| <span data-ttu-id="1e4e7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e4e7-132">Requirement</span></span> | <span data-ttu-id="1e4e7-133">Value</span><span class="sxs-lookup"><span data-stu-id="1e4e7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e4e7-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e4e7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1e4e7-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1e4e7-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1e4e7-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e4e7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1e4e7-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1e4e7-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1e4e7-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1e4e7-138">Namespace</span></span><br/>                | <span data-ttu-id="1e4e7-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1e4e7-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1e4e7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="1e4e7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e4e7-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e4e7-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e4e7-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e4e7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e4e7-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1e4e7-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1e4e7-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e4e7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e4e7-145">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="1e4e7-145">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




