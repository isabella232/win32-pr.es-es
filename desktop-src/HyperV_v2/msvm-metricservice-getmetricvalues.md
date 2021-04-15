---
description: Obtiene los valores de métrica.
ms.assetid: 71c614ef-a005-45aa-9999-a19dc9f9c0df
title: Método GetMetricValues de la clase Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe3e32b21ec0baa497fcef781e1b48fae37fbf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669770"
---
# <a name="getmetricvalues-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="632eb-103">Método GetMetricValues de la \_ clase MetricService de MSVM</span><span class="sxs-lookup"><span data-stu-id="632eb-103">GetMetricValues method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="632eb-104">Obtiene los valores de métrica.</span><span class="sxs-lookup"><span data-stu-id="632eb-104">Gets metric values.</span></span>

## <a name="syntax"></a><span data-ttu-id="632eb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="632eb-105">Syntax</span></span>


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a><span data-ttu-id="632eb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="632eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="632eb-107">*Definición* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="632eb-107">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="632eb-108">Identifica un [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) para el que se devolverán las métricas.</span><span class="sxs-lookup"><span data-stu-id="632eb-108">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="632eb-109">*Intervalo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="632eb-109">*Range* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="632eb-110">Identifica cómo se seleccionan las instancias.</span><span class="sxs-lookup"><span data-stu-id="632eb-110">Identifies how the instances are selected.</span></span> <span data-ttu-id="632eb-111">El algoritmo para ordenar instancias de valor es específico de la definición de métricas.</span><span class="sxs-lookup"><span data-stu-id="632eb-111">The algorithm for ordering value instances is metric definition specific.</span></span>

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="632eb-112">**Mínimo** (2)</span><span class="sxs-lookup"><span data-stu-id="632eb-112">**Minimum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="632eb-113">**Máximo** (3)</span><span class="sxs-lookup"><span data-stu-id="632eb-113">**Maximum** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="632eb-114">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="632eb-114">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="632eb-115">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="632eb-115">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="632eb-116">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="632eb-116">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="632eb-117">Identifica el número máximo de instancias que debe devolver el método.</span><span class="sxs-lookup"><span data-stu-id="632eb-117">Identifies the maximum number of instances to be returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="632eb-118">*Valores* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="632eb-118">*Values* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="632eb-119">Tras la finalización correcta del método, contiene referencias a instancias [**de \_ BaseMetricValue de CIM**](cim-basemetricvalue.md), filtradas según los valores de los parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="632eb-119">Upon successful completion of the method, contains references to instances of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md), filtered according to the values of the input parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="632eb-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="632eb-120">Return value</span></span>

<span data-ttu-id="632eb-121">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="632eb-121">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="632eb-122">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="632eb-122">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="632eb-123">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="632eb-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="632eb-124">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="632eb-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="632eb-125">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="632eb-125">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="632eb-126">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="632eb-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="632eb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="632eb-127">Requirements</span></span>



| <span data-ttu-id="632eb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="632eb-128">Requirement</span></span> | <span data-ttu-id="632eb-129">Value</span><span class="sxs-lookup"><span data-stu-id="632eb-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="632eb-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="632eb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="632eb-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="632eb-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="632eb-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="632eb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="632eb-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="632eb-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="632eb-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="632eb-134">Namespace</span></span><br/>                | <span data-ttu-id="632eb-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="632eb-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="632eb-136">MOF</span><span class="sxs-lookup"><span data-stu-id="632eb-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="632eb-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="632eb-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="632eb-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="632eb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="632eb-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="632eb-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="632eb-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="632eb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="632eb-141">**MSVM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="632eb-141">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

 




