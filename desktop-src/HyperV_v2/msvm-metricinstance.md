---
description: Representa una asociación de objetos de valor de métrica con sus definiciones de métricas.
ms.assetid: 98ad9390-78b4-4c18-b068-d05efa2f1866
title: Msvm_MetricInstance (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricInstance
- Msvm_MetricInstance.Antecedent
- Msvm_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab17dce339e866fb22654a0bd75c6f3945d320a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687478"
---
# <a name="msvm_metricinstance-class"></a><span data-ttu-id="5e846-103">MSVM \_ MetricInstance (clase)</span><span class="sxs-lookup"><span data-stu-id="5e846-103">Msvm\_MetricInstance class</span></span>

<span data-ttu-id="5e846-104">Representa una asociación de objetos de valor de métrica con sus definiciones de métricas.</span><span class="sxs-lookup"><span data-stu-id="5e846-104">Represents an association of metric value objects with their metrics definitions.</span></span> <span data-ttu-id="5e846-105">Esta asociación asocia una instancia de [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) a su [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="5e846-105">This association ties an instance of [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) to its [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span>

<span data-ttu-id="5e846-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5e846-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e846-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e846-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricInstance : CIM_MetricInstance
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5e846-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5e846-108">Members</span></span>

<span data-ttu-id="5e846-109">La clase **MSVM \_ MetricInstance** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5e846-109">The **Msvm\_MetricInstance** class has these types of members:</span></span>

-   [<span data-ttu-id="5e846-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5e846-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e846-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5e846-111">Properties</span></span>

<span data-ttu-id="5e846-112">La clase **MSVM \_ MetricInstance** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5e846-112">The **Msvm\_MetricInstance** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e846-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="5e846-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e846-114">Tipo de datos: \* \* \* \* CIM \_ ManagedElement \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5e846-114">Data type: \*\*\*\*CIM\_ManagedElement\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="5e846-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e846-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e846-116">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="5e846-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5e846-117">Una referencia a una instancia de la clase [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) que representa las definiciones de las métricas.</span><span class="sxs-lookup"><span data-stu-id="5e846-117">A reference to an instance of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) class that represents the metrics definitions.</span></span>

</dd> <dt>

<span data-ttu-id="5e846-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="5e846-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e846-119">Tipo de datos: \* \* \* \* CIM \_ ManagedElement \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5e846-119">Data type: \*\*\*\*CIM\_ManagedElement\*\*\*\*</span></span>
</dt> <dt>

<span data-ttu-id="5e846-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5e846-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e846-121">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="5e846-121">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5e846-122">Referencia a una instancia de la clase [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) que representa las métricas que dependen del **antecedente**.</span><span class="sxs-lookup"><span data-stu-id="5e846-122">A reference to an instance of the [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) class that represents the metrics that are dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e846-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e846-123">Requirements</span></span>



| <span data-ttu-id="5e846-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e846-124">Requirement</span></span> | <span data-ttu-id="5e846-125">Value</span><span class="sxs-lookup"><span data-stu-id="5e846-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e846-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e846-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5e846-127">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e846-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5e846-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e846-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5e846-129">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e846-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5e846-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5e846-130">Namespace</span></span><br/>                | <span data-ttu-id="5e846-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="5e846-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5e846-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5e846-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e846-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e846-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e846-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e846-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e846-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5e846-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




