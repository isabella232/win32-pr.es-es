---
description: Habilita y deshabilita la recopilación de métricas.
ms.assetid: afb90863-e70a-46e5-b1b7-d959dcacc306
title: Método ControlMetrics de la clase CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 60a7d0b34227594cf7146a988aa7e0d232f2d6cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277055"
---
# <a name="controlmetrics-method-of-the-cim_metricservice-class"></a><span data-ttu-id="6b0fa-103">Método ControlMetrics de la \_ clase MetricService de CIM</span><span class="sxs-lookup"><span data-stu-id="6b0fa-103">ControlMetrics method of the CIM\_MetricService class</span></span>

<span data-ttu-id="6b0fa-104">Habilita y deshabilita la recopilación de métricas. **ControlMetrics** se utiliza para controlar la colección de cada tipo de métrica para un [**\_ ManagedElement CIM**](cim-managedelement.md), la colección de un tipo de métrica determinado para todos los elementos administrados o la colección de una métrica específica para un elemento administrado concreto.</span><span class="sxs-lookup"><span data-stu-id="6b0fa-104">Enables and disables the collection of metrics.**ControlMetrics** is used to control the collection of each type of metric for a [**CIM\_ManagedElement**](cim-managedelement.md), the collection of a given type of metric for all managed elements, or the collection of a specific metric for a specific managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b0fa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b0fa-105">Syntax</span></span>


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="6b0fa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b0fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b0fa-107">*Asunto* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6b0fa-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b0fa-108">Un [**elemento \_ ManagedElement de CIM**](cim-managedelement.md) que identifica los elementos administrados para los que se controlarán las métricas.</span><span class="sxs-lookup"><span data-stu-id="6b0fa-108">A [**CIM\_ManagedElement**](cim-managedelement.md) that identifies managed element(s) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="6b0fa-109">*Definición* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6b0fa-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b0fa-110">Identifica un [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) para el que se controlarán las métricas.</span><span class="sxs-lookup"><span data-stu-id="6b0fa-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="6b0fa-111">*MetricCollectionEnabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6b0fa-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b0fa-112">Indica la operación deseada que se va a realizar en las métricas.</span><span class="sxs-lookup"><span data-stu-id="6b0fa-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="6b0fa-113">**Habilitar** (2)</span><span class="sxs-lookup"><span data-stu-id="6b0fa-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="6b0fa-114">**Deshabilitar** (3)</span><span class="sxs-lookup"><span data-stu-id="6b0fa-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="6b0fa-115">**Restablecer** (4)</span><span class="sxs-lookup"><span data-stu-id="6b0fa-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6b0fa-116">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="6b0fa-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="6b0fa-117">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="6b0fa-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="6b0fa-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6b0fa-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="6b0fa-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b0fa-119">Return value</span></span>

<span data-ttu-id="6b0fa-120">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="6b0fa-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="6b0fa-121">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="6b0fa-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6b0fa-122">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="6b0fa-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6b0fa-123">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="6b0fa-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6b0fa-124">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="6b0fa-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6b0fa-125">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="6b0fa-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6b0fa-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b0fa-126">Requirements</span></span>



| <span data-ttu-id="6b0fa-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b0fa-127">Requirement</span></span> | <span data-ttu-id="6b0fa-128">Value</span><span class="sxs-lookup"><span data-stu-id="6b0fa-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b0fa-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b0fa-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6b0fa-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6b0fa-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6b0fa-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b0fa-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6b0fa-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6b0fa-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6b0fa-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6b0fa-133">Namespace</span></span><br/>                | <span data-ttu-id="6b0fa-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="6b0fa-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6b0fa-135">MOF</span><span class="sxs-lookup"><span data-stu-id="6b0fa-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b0fa-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b0fa-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b0fa-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6b0fa-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b0fa-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6b0fa-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6b0fa-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b0fa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b0fa-140">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="6b0fa-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




