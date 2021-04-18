---
description: Proporciona la capacidad de devolver una lista filtrada de \_ las instancias de BaseMetricValue de CIM.
ms.assetid: c207a0ef-11f1-42c4-af77-3dcf3fbff8a7
title: Método GetMetricValues de la clase CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3c84ae9f5128edecfd3dd4cb591f811fdbd86010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667568"
---
# <a name="getmetricvalues-method-of-the-cim_metricservice-class"></a><span data-ttu-id="84f66-103">Método GetMetricValues de la \_ clase MetricService de CIM</span><span class="sxs-lookup"><span data-stu-id="84f66-103">GetMetricValues method of the CIM\_MetricService class</span></span>

<span data-ttu-id="84f66-104">Proporciona la capacidad de devolver una lista filtrada de las instancias de [**\_ BaseMetricValue de CIM**](cim-basemetricvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="84f66-104">Provides the ability to return a filtered list of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f66-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84f66-105">Syntax</span></span>


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a><span data-ttu-id="84f66-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84f66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84f66-107">*Definición* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="84f66-107">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84f66-108">Identifica un [**\_ BaseMetricDefinition de CIM**](cim-basemetricdefinition.md) para el que se devolverán las métricas.</span><span class="sxs-lookup"><span data-stu-id="84f66-108">Identifies a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) for which metrics will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="84f66-109">*Intervalo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="84f66-109">*Range* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84f66-110">Identifica cómo se seleccionan las instancias.</span><span class="sxs-lookup"><span data-stu-id="84f66-110">Identifies how the instances are selected.</span></span> <span data-ttu-id="84f66-111">El algoritmo para ordenar instancias de valor es específico de la definición de métricas.</span><span class="sxs-lookup"><span data-stu-id="84f66-111">The algorithm for ordering value instances is metric-definition specific.</span></span>

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="84f66-112">**Mínimo** (2)</span><span class="sxs-lookup"><span data-stu-id="84f66-112">**Minimum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="84f66-113">**Máximo** (3)</span><span class="sxs-lookup"><span data-stu-id="84f66-113">**Maximum** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="84f66-114">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="84f66-114">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="84f66-115">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="84f66-115">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="84f66-116">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="84f66-116">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84f66-117">Identifica el número máximo de instancias que debe devolver el método.</span><span class="sxs-lookup"><span data-stu-id="84f66-117">Identifies the maximum number of instances to be returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="84f66-118">*Valores* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="84f66-118">*Values* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84f66-119">Tras la finalización correcta del método, contiene referencias a instancias [**de \_ BaseMetricValue de CIM**](cim-basemetricvalue.md), filtradas según los valores de los parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="84f66-119">Upon successful completion of the method, contains references to instances of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md), filtered according to the values of the input parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84f66-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84f66-120">Return value</span></span>

<span data-ttu-id="84f66-121">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="84f66-121">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="84f66-122">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="84f66-122">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84f66-123">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="84f66-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84f66-124">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="84f66-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84f66-125">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="84f66-125">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="84f66-126">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="84f66-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="84f66-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84f66-127">Requirements</span></span>



| <span data-ttu-id="84f66-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="84f66-128">Requirement</span></span> | <span data-ttu-id="84f66-129">Value</span><span class="sxs-lookup"><span data-stu-id="84f66-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84f66-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84f66-130">Minimum supported client</span></span><br/> | <span data-ttu-id="84f66-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="84f66-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="84f66-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84f66-132">Minimum supported server</span></span><br/> | <span data-ttu-id="84f66-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="84f66-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="84f66-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="84f66-134">Namespace</span></span><br/>                | <span data-ttu-id="84f66-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="84f66-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="84f66-136">MOF</span><span class="sxs-lookup"><span data-stu-id="84f66-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84f66-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84f66-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84f66-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="84f66-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84f66-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84f66-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84f66-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="84f66-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f66-141">**\_METRICSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="84f66-141">**CIM\_MetricService**</span></span>](cim-metricservice.md)
</dt> </dl>

 

 




