---
description: Se utiliza para controlar la colección de métricas de un elemento o elementos administrados.
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: Método ControlMetrics de la clase Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b12fbf71b860571bb3bb5ee06cb58483e782f479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667838"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="05517-103">Método ControlMetrics de la \_ clase MetricService de MSVM</span><span class="sxs-lookup"><span data-stu-id="05517-103">ControlMetrics method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="05517-104">Se utiliza para controlar la colección de métricas de un elemento o elementos administrados.</span><span class="sxs-lookup"><span data-stu-id="05517-104">Used to control the collection of metrics for a managed element or elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="05517-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05517-105">Syntax</span></span>


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="05517-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05517-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05517-107">*Asunto* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05517-107">*Subject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05517-108">Instancia [**de \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que identifica los elementos administrados para los que se recopilarán las métricas.</span><span class="sxs-lookup"><span data-stu-id="05517-108">A [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) instance that identifies the managed elements for which metrics will be collected.</span></span> <span data-ttu-id="05517-109">Si este parámetro es **null**, se recopilarán las métricas de todos los elementos administrados asociados al parámetro de *definición* .</span><span class="sxs-lookup"><span data-stu-id="05517-109">If this parameter is **Null**, the metrics for all the managed elements associated with the *Definition* parameter will be collected.</span></span>

</dd> <dt>

<span data-ttu-id="05517-110">*Definición* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="05517-110">*Definition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05517-111">Una instancia de [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) que especifica qué métricas se van a recopilar.</span><span class="sxs-lookup"><span data-stu-id="05517-111">An [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance that specifies which metrics will be collected.</span></span> <span data-ttu-id="05517-112">Si este parámetro es **null**, se recopilarán las métricas de todas las definiciones asociadas al elemento administrado identificado por el parámetro de *asunto* .</span><span class="sxs-lookup"><span data-stu-id="05517-112">If this parameter is **Null**, the metrics for all the definitions associated with the managed element identified by the *Subject* parameter will be collected</span></span>

</dd> <dt>

<span data-ttu-id="05517-113">*MetricCollectionEnabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05517-113">*MetricCollectionEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05517-114">Especifica la operación que se va a realizar en la colección de métricas.</span><span class="sxs-lookup"><span data-stu-id="05517-114">Specifies the operation to perform on the metrics collection.</span></span> <span data-ttu-id="05517-115">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="05517-115">This must be one of the following values.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="05517-116"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Habilitar** (2)</span><span class="sxs-lookup"><span data-stu-id="05517-116"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="05517-117">Habilite la recopilación de métricas.</span><span class="sxs-lookup"><span data-stu-id="05517-117">Enable metrics collection.</span></span>

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="05517-118"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deshabilitar** (3)</span><span class="sxs-lookup"><span data-stu-id="05517-118"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (3)</span></span>


</dt> <dd>

<span data-ttu-id="05517-119">Deshabilite la recopilación de métricas.</span><span class="sxs-lookup"><span data-stu-id="05517-119">Disable metrics collection.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="05517-120"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (4)</span><span class="sxs-lookup"><span data-stu-id="05517-120"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (4)</span></span>


</dt> <dd>

<span data-ttu-id="05517-121">Restablezca los valores de las métricas.</span><span class="sxs-lookup"><span data-stu-id="05517-121">Reset metrics values.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="05517-122"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="05517-122"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="05517-123"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="05517-123"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="05517-124"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="05517-124"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="05517-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05517-125">Return value</span></span>

<span data-ttu-id="05517-126">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="05517-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="05517-127">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="05517-127">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="05517-128">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="05517-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="05517-129">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="05517-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="05517-130">**Método reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="05517-130">**Method Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="05517-131">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="05517-131">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="05517-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05517-132">Remarks</span></span>

<span data-ttu-id="05517-133">Este método producirá un error en las instancias siguientes:</span><span class="sxs-lookup"><span data-stu-id="05517-133">This method will fail in the following instances:</span></span>

-   <span data-ttu-id="05517-134">Los parámetros de *asunto* y *definición* son **null**.</span><span class="sxs-lookup"><span data-stu-id="05517-134">The *Subject* and *Definition* parameters are both **Null**.</span></span>
-   <span data-ttu-id="05517-135">Los parámetros de *asunto* y *definición* son no **null** y no hay una instancia de [**MSVM \_ MetricDefForME**](msvm-metricdefforme.md) que asocie las dos instancias.</span><span class="sxs-lookup"><span data-stu-id="05517-135">The *Subject* and *Definition* parameters are both non-**Null** and there is not an instance of [**Msvm\_MetricDefForME**](msvm-metricdefforme.md) that associates the two instances.</span></span>
-   <span data-ttu-id="05517-136">El parámetro *Definition* es una referencia a una instancia de [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) que no está asociada con [**MSVM \_ MetricService**](msvm-metricservice.md) a [**MSVM \_ ServiceAffectsElement**](msvm-serviceaffectselement.md).</span><span class="sxs-lookup"><span data-stu-id="05517-136">The *Definition* parameter is a reference to an instance of [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) that is not associated with the [**Msvm\_MetricService**](msvm-metricservice.md) through [**Msvm\_ServiceAffectsElement**](msvm-serviceaffectselement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05517-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05517-137">Requirements</span></span>



| <span data-ttu-id="05517-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="05517-138">Requirement</span></span> | <span data-ttu-id="05517-139">Value</span><span class="sxs-lookup"><span data-stu-id="05517-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05517-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05517-140">Minimum supported client</span></span><br/> | <span data-ttu-id="05517-141">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="05517-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="05517-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05517-142">Minimum supported server</span></span><br/> | <span data-ttu-id="05517-143">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="05517-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="05517-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="05517-144">Namespace</span></span><br/>                | <span data-ttu-id="05517-145">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="05517-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="05517-146">MOF</span><span class="sxs-lookup"><span data-stu-id="05517-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05517-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05517-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="05517-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="05517-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05517-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="05517-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="05517-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="05517-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05517-151">**MSVM \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="05517-151">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

