---
description: Representa una asociación en la que se recopilan los valores de métrica para un elemento administrado.
ms.assetid: 00752751-bc27-463b-a4ac-4db8e5040077
title: CIM_MetricForME (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricForME
- CIM_MetricForME.Antecedent
- CIM_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89c119ad622b778d0402100a64ff15befe623685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687856"
---
# <a name="cim_metricforme-class"></a><span data-ttu-id="5d3b2-103">\_Clase MetricForME de CIM</span><span class="sxs-lookup"><span data-stu-id="5d3b2-103">CIM\_MetricForME class</span></span>

<span data-ttu-id="5d3b2-104">Representa una asociación en la que se recopilan los valores de métrica para un elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="5d3b2-104">Represents an association in which a metric values are collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d3b2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d3b2-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricForME : CIM_Dependency
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5d3b2-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="5d3b2-106">Members</span></span>

<span data-ttu-id="5d3b2-107">La clase **CIM \_ MetricForME** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5d3b2-107">The **CIM\_MetricForME** class has these types of members:</span></span>

-   [<span data-ttu-id="5d3b2-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5d3b2-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d3b2-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5d3b2-109">Properties</span></span>

<span data-ttu-id="5d3b2-110">La clase **CIM \_ MetricForME** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5d3b2-110">The **CIM\_MetricForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d3b2-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="5d3b2-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d3b2-112">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="5d3b2-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="5d3b2-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d3b2-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d3b2-114">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="5d3b2-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5d3b2-115">Elemento administrado en la asociación.</span><span class="sxs-lookup"><span data-stu-id="5d3b2-115">The managed element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="5d3b2-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="5d3b2-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d3b2-117">Tipo de datos: **CIM \_ BaseMetricValue**</span><span class="sxs-lookup"><span data-stu-id="5d3b2-117">Data type: **CIM\_BaseMetricValue**</span></span>
</dt> <dt>

<span data-ttu-id="5d3b2-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d3b2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d3b2-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="5d3b2-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5d3b2-120">Valor de métrica de la asociación.</span><span class="sxs-lookup"><span data-stu-id="5d3b2-120">The metric value in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d3b2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d3b2-121">Requirements</span></span>



| <span data-ttu-id="5d3b2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d3b2-122">Requirement</span></span> | <span data-ttu-id="5d3b2-123">Value</span><span class="sxs-lookup"><span data-stu-id="5d3b2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d3b2-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d3b2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5d3b2-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5d3b2-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5d3b2-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d3b2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5d3b2-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5d3b2-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5d3b2-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5d3b2-128">Namespace</span></span><br/>                | <span data-ttu-id="5d3b2-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="5d3b2-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5d3b2-130">MOF</span><span class="sxs-lookup"><span data-stu-id="5d3b2-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d3b2-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d3b2-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d3b2-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5d3b2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d3b2-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5d3b2-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5d3b2-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d3b2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d3b2-135">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="5d3b2-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

