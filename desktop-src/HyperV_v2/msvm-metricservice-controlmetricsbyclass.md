---
description: Controla las métricas por clase.
ms.assetid: f848fdec-561b-4be0-b1e9-a59e15196d1d
title: Método ControlMetricsByClass de la clase Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4149da6327edf774afda20e64f34ae0958f7c3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688566"
---
# <a name="controlmetricsbyclass-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="30027-103">Método ControlMetricsByClass de la \_ clase MetricService de MSVM</span><span class="sxs-lookup"><span data-stu-id="30027-103">ControlMetricsByClass method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="30027-104">Controla las métricas por clase.</span><span class="sxs-lookup"><span data-stu-id="30027-104">Controls metrics by class.</span></span>

## <a name="syntax"></a><span data-ttu-id="30027-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30027-105">Syntax</span></span>


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="30027-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30027-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30027-107">*Asunto* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="30027-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30027-108">Identifica la clase CIM cuyas métricas se van a controlar.</span><span class="sxs-lookup"><span data-stu-id="30027-108">Identifies the CIM class for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="30027-109">*Definición* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="30027-109">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30027-110">Identifica un [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) para el que se controlarán las métricas.</span><span class="sxs-lookup"><span data-stu-id="30027-110">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be controlled.</span></span>

</dd> <dt>

<span data-ttu-id="30027-111">*MetricCollectionEnabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="30027-111">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30027-112">Indica la operación deseada que se va a realizar en las métricas.</span><span class="sxs-lookup"><span data-stu-id="30027-112">Indicates the desired operation to perform on the metrics.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="30027-113">**Habilitar** (2)</span><span class="sxs-lookup"><span data-stu-id="30027-113">**Enable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="30027-114">**Deshabilitar** (3)</span><span class="sxs-lookup"><span data-stu-id="30027-114">**Disable** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="30027-115">**Restablecer** (4)</span><span class="sxs-lookup"><span data-stu-id="30027-115">**Reset** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="30027-116">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="30027-116">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="30027-117">**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="30027-117">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="30027-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="30027-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="30027-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30027-119">Return value</span></span>

<span data-ttu-id="30027-120">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="30027-120">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="30027-121">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="30027-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="30027-122">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="30027-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="30027-123">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="30027-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="30027-124">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="30027-124">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="30027-125">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="30027-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="30027-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30027-126">Requirements</span></span>



| <span data-ttu-id="30027-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="30027-127">Requirement</span></span> | <span data-ttu-id="30027-128">Value</span><span class="sxs-lookup"><span data-stu-id="30027-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30027-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30027-129">Minimum supported client</span></span><br/> | <span data-ttu-id="30027-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="30027-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="30027-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30027-131">Minimum supported server</span></span><br/> | <span data-ttu-id="30027-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="30027-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="30027-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="30027-133">Namespace</span></span><br/>                | <span data-ttu-id="30027-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="30027-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="30027-135">MOF</span><span class="sxs-lookup"><span data-stu-id="30027-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30027-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30027-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="30027-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="30027-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30027-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="30027-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="30027-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="30027-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30027-140">**MSVM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="30027-140">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




