---
description: Muestra las métricas por clase.
ms.assetid: a08c0749-b60b-4b8a-996f-b3bbaf1fb2d3
title: Método ShowMetricsByClass de la clase Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 93f132b24c6c20826b1551e979c128b1aa38c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667165"
---
# <a name="showmetricsbyclass-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="9c1fd-103">Método ShowMetricsByClass de la \_ clase MetricService de MSVM</span><span class="sxs-lookup"><span data-stu-id="9c1fd-103">ShowMetricsByClass method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="9c1fd-104">Muestra las métricas por clase.</span><span class="sxs-lookup"><span data-stu-id="9c1fd-104">Shows metrics by class.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c1fd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c1fd-105">Syntax</span></span>


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a><span data-ttu-id="9c1fd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c1fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c1fd-107">*Asunto* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9c1fd-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c1fd-108">Identifica una clase CIM para la que el método devuelve referencias a instancias [**de \_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) que definen las métricas que están disponibles para ser capturadas para todas las instancias de la clase.</span><span class="sxs-lookup"><span data-stu-id="9c1fd-108">Identifies a CIM class for which the method returns references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics that are available to be captured for all instances of the class.</span></span>

</dd> <dt>

<span data-ttu-id="9c1fd-109">*Definición* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9c1fd-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c1fd-110">Identifica una instancia de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="9c1fd-110">Identifies an instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).</span></span> <span data-ttu-id="9c1fd-111">El método devuelve referencias a instancias de [**CIM \_ de CIM**](cim-managedelement.md) para las que se pueden recopilar las métricas definidas por la instancia de **\_ BaseMetricDefinition de CIM** .</span><span class="sxs-lookup"><span data-stu-id="9c1fd-111">The method returns references to instances of [**CIM\_ManagedElement**](cim-managedelement.md) for which metrics defined by the instance of **CIM\_BaseMetricDefinition** are available to be collected.</span></span>

</dd> <dt>

<span data-ttu-id="9c1fd-112">*DefinitionList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9c1fd-112">*DefinitionList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c1fd-113">Tras la finalización correcta del método, puede contener referencias a instancias [**de \_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) que definan las métricas disponibles para la recopilación para el [**\_ ManagedElement de CIM**](cim-managedelement.md) identificado por el parámetro de *asunto* .</span><span class="sxs-lookup"><span data-stu-id="9c1fd-113">Upon successful completion of the method, may contain references to instances of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that define metrics available for collection for the [**CIM\_ManagedElement**](cim-managedelement.md) identified by the *Subject* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9c1fd-114">*MetricNames* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9c1fd-114">*MetricNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c1fd-115">Tras la finalización correcta del método, cada índice de matriz contiene el valor de la propiedad **Name** para la instancia de [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) a la que hace referencia el índice de matriz correspondiente del parámetro *DefinitionList* .</span><span class="sxs-lookup"><span data-stu-id="9c1fd-115">Upon successful completion of the method, each array index contains the value of the **Name** property for the instance of [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) referenced by the corresponding array index of the *DefinitionList* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9c1fd-116">*MetricCollectionEnabled* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9c1fd-116">*MetricCollectionEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c1fd-117">Indica si se va a recopilar una métrica para todas las instancias de una clase de elementos administrados.</span><span class="sxs-lookup"><span data-stu-id="9c1fd-117">Indicates whether a metric is being collected for all instances of a class of managed elements.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9c1fd-118">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="9c1fd-118">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9c1fd-119">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="9c1fd-119">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="9c1fd-120">**Reservado** (4)</span><span class="sxs-lookup"><span data-stu-id="9c1fd-120">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="9c1fd-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9c1fd-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="9c1fd-122">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="9c1fd-122">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="9c1fd-123"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9c1fd-123"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="9c1fd-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c1fd-124">Return value</span></span>

<span data-ttu-id="9c1fd-125">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="9c1fd-125">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="9c1fd-126">**Correcto** ()</span><span class="sxs-lookup"><span data-stu-id="9c1fd-126">**Success** ()</span></span>
</dt> <dt>

<span data-ttu-id="9c1fd-127">**No compatible** ()</span><span class="sxs-lookup"><span data-stu-id="9c1fd-127">**Not Supported** ()</span></span>
</dt> <dt>

<span data-ttu-id="9c1fd-128">**Error** ()</span><span class="sxs-lookup"><span data-stu-id="9c1fd-128">**Failed** ()</span></span>
</dt> <dt>

<span data-ttu-id="9c1fd-129">**Método reservado** ()</span><span class="sxs-lookup"><span data-stu-id="9c1fd-129">**Method Reserved** ()</span></span>
</dt> <dt>

<span data-ttu-id="9c1fd-130">**Específico del proveedor** ()</span><span class="sxs-lookup"><span data-stu-id="9c1fd-130">**Vendor Specific** ()</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9c1fd-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c1fd-131">Requirements</span></span>



| <span data-ttu-id="9c1fd-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c1fd-132">Requirement</span></span> | <span data-ttu-id="9c1fd-133">Value</span><span class="sxs-lookup"><span data-stu-id="9c1fd-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c1fd-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c1fd-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9c1fd-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9c1fd-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="9c1fd-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c1fd-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9c1fd-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9c1fd-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="9c1fd-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9c1fd-138">Namespace</span></span><br/>                | <span data-ttu-id="9c1fd-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9c1fd-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9c1fd-140">MOF</span><span class="sxs-lookup"><span data-stu-id="9c1fd-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c1fd-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c1fd-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c1fd-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9c1fd-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c1fd-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9c1fd-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9c1fd-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c1fd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c1fd-145">**MSVM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="9c1fd-145">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




