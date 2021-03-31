---
description: Muestra las métricas especificadas.
ms.assetid: 3716b5e6-b360-4719-a0f3-60b8d39deb31
title: Método ShowMetrics de la clase Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9823ea61864b0d87245ebe8b171195a2fd3c411a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913125"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="ab006-103">Método ShowMetrics de la \_ clase MetricService de MSVM</span><span class="sxs-lookup"><span data-stu-id="ab006-103">ShowMetrics method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="ab006-104">Muestra las métricas especificadas.</span><span class="sxs-lookup"><span data-stu-id="ab006-104">Shows the specified metrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab006-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab006-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ab006-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab006-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab006-107">*Asunto* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab006-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab006-108">El parámetro Subject identifica una instancia de [**CIM de CIM \_**](cim-managedelement.md) para la que el método devuelve referencias a instancias de [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) que definen métricas que se capturan para el **\_ ManagedElement de CIM**.</span><span class="sxs-lookup"><span data-stu-id="ab006-108">The Subject parameter identifies an instance of [**CIM\_ManagedElement**](cim-managedelement.md) for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are being captured for the **CIM\_ManagedElement**.</span></span>

</dd> <dt>

<span data-ttu-id="ab006-109">*Definición* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ab006-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab006-110">El parámetro de definición identifica una instancia de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="ab006-110">The Definition parameter identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="ab006-111">El método devuelve referencias a instancias de [**CIM \_ de CIM**](cim-managedelement.md) para las que se pueden recopilar las métricas definidas por la instancia de **\_ BaseMetricDefinition de CIM** .</span><span class="sxs-lookup"><span data-stu-id="ab006-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="ab006-112">*ManagedElements* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab006-112">*ManagedElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab006-113">Tras la finalización correcta del método, el parámetro *ManagedElements* \[ \] puede contener referencias a un [**\_ ManagedElement de CIM**](cim-managedelement.md) para el que la métrica identificada por el parámetro de *definición* está disponible para la recopilación.</span><span class="sxs-lookup"><span data-stu-id="ab006-113">Upon successful completion of the method, the *ManagedElements*\[\] parameter may contain references to [**CIM\_ManagedElement**](cim-managedelement.md) for which the metric identified by *Definition* parameter is available for collection.</span></span>

</dd> <dt>

<span data-ttu-id="ab006-114">*DefinitionList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab006-114">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab006-115">Tras la finalización correcta del método, el parámetro *DefinitionList* puede contener referencias a instancias [**de \_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) que definen las métricas disponibles para la recopilación para el [**\_ ManagedElement de CIM**](cim-managedelement.md) identificado por el parámetro de *asunto* .</span><span class="sxs-lookup"><span data-stu-id="ab006-115">Upon successful completion of the method, the *DefinitionList* parameter may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab006-116">*MetricNames* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab006-116">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab006-117">Tras completar correctamente el método, cada índice de matriz del parámetro *MetricNames* contendrá el valor de la propiedad Name de la instancia de [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) a la que hace referencia el índice de matriz correspondiente del parámetro *DefinitionList* .</span><span class="sxs-lookup"><span data-stu-id="ab006-117">Upon successful completion of the method, each array index of the *MetricNames* parameter shall contain the value of the Name property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ab006-118">*MetricCollectionEnabled* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ab006-118">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab006-119">El parámetro *MetricCollectionEnabled* indica si se va a recopilar una métrica para un elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="ab006-119">The *MetricCollectionEnabled* parameter indicates whether a metric is being collected for a managed element.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="ab006-120">**Habilitar** (2)</span><span class="sxs-lookup"><span data-stu-id="ab006-120">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="ab006-121">**Deshabilitar** (3)</span><span class="sxs-lookup"><span data-stu-id="ab006-121">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="ab006-122">**Reservado** (4)</span><span class="sxs-lookup"><span data-stu-id="ab006-122">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ab006-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ab006-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ab006-124">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="ab006-124">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="ab006-125"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ab006-125"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="ab006-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab006-126">Return value</span></span>

<span data-ttu-id="ab006-127">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ab006-127">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ab006-128">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="ab006-128">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ab006-129">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="ab006-129">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ab006-130">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="ab006-130">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ab006-131">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ab006-131">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ab006-132">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="ab006-132">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ab006-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab006-133">Requirements</span></span>



| <span data-ttu-id="ab006-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab006-134">Requirement</span></span> | <span data-ttu-id="ab006-135">Value</span><span class="sxs-lookup"><span data-stu-id="ab006-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab006-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab006-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ab006-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ab006-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ab006-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab006-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ab006-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ab006-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ab006-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ab006-140">Namespace</span></span><br/>                | <span data-ttu-id="ab006-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ab006-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ab006-142">MOF</span><span class="sxs-lookup"><span data-stu-id="ab006-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab006-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab006-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab006-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab006-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab006-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ab006-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ab006-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab006-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab006-147">**MSVM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="ab006-147">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




