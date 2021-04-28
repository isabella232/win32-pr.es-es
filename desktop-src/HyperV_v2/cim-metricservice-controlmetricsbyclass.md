---
description: 'Método ControlMetricsByClass de la clase CIM_MetricService: habilita y deshabilita la colección de métricas.'
ms.assetid: 1a53c7a7-c0fc-49d7-ad1b-d185d776ede5
title: Método ControlMetricsByClass de la CIM_MetricService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fda8407d49ed3eec7ff86abc94ced6b63d2d77c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109713"
---
# <a name="controlmetricsbyclass-method-of-the-cim_metricservice-class"></a><span data-ttu-id="2371a-103">Método ControlMetricsByClass de la clase \_ MetricService de CIM</span><span class="sxs-lookup"><span data-stu-id="2371a-103">ControlMetricsByClass method of the CIM\_MetricService class</span></span>

<span data-ttu-id="2371a-104">Habilita y deshabilita la recopilación de métricas. **ControlMetricsByClass** se usa para controlar la colección de cada tipo de métrica para todas las instancias de una clase o la colección de una métrica específica para todas las instancias de una clase.</span><span class="sxs-lookup"><span data-stu-id="2371a-104">Enables and disables the collection of metrics.**ControlMetricsByClass** is used to control the collection of each type of metric for all instances of a class or the collection of a specific metric for all instances of a class.</span></span>

## <a name="syntax"></a><span data-ttu-id="2371a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2371a-105">Syntax</span></span>


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="2371a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2371a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2371a-107">*Asunto* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2371a-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2371a-108">Identifica la clase [**\_ ManagedElement de CIM**](cim-managedelement.md) para la que se controlarán las métricas.</span><span class="sxs-lookup"><span data-stu-id="2371a-108">Identifies the [**CIM\_ManagedElement**](cim-managedelement.md) class for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="2371a-109">*Definición* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2371a-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2371a-110">Identifica una [**\_ baseMetricDefinition de CIM**](cim-basemetricdefinition.md) para la que se controlarán las métricas.</span><span class="sxs-lookup"><span data-stu-id="2371a-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="2371a-111">*MetricCollectionEnabled* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2371a-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2371a-112">Indica la operación deseada que se realizará en las métricas.</span><span class="sxs-lookup"><span data-stu-id="2371a-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="2371a-113">**Habilitar** (2)</span><span class="sxs-lookup"><span data-stu-id="2371a-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="2371a-114">**Deshabilitar** (3)</span><span class="sxs-lookup"><span data-stu-id="2371a-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="2371a-115">**Restablecimiento** (4)</span><span class="sxs-lookup"><span data-stu-id="2371a-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2371a-116">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2371a-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2371a-117">**Vendor Reserved** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="2371a-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="2371a-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2371a-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="2371a-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2371a-119">Return value</span></span>

<span data-ttu-id="2371a-120">Devuelve un valor 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="2371a-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="2371a-121">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="2371a-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2371a-122">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="2371a-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2371a-123">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="2371a-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2371a-124">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2371a-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2371a-125">**Específico del** proveedor (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="2371a-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2371a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2371a-126">Requirements</span></span>



| <span data-ttu-id="2371a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2371a-127">Requirement</span></span> | <span data-ttu-id="2371a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="2371a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2371a-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2371a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2371a-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2371a-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2371a-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2371a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2371a-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2371a-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2371a-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2371a-133">Namespace</span></span><br/>                | <span data-ttu-id="2371a-134">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="2371a-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2371a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="2371a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2371a-136"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="2371a-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2371a-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2371a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2371a-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2371a-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2371a-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2371a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2371a-140">**CIM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="2371a-140">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




