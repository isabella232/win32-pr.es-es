---
description: Define la asociación entre un \_ BaseMetricDefinition MSVM y un \_ ManagedElement CIM para definir las métricas de este último. La definición de métricas se proporciona en el contexto mediante ManagedElement, que es el motivo por el que la definición depende del elemento.
ms.assetid: 528d9b1a-089d-48ae-b5a6-40bc9d09191c
title: Msvm_MetricDefForME (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricDefForME
- Msvm_MetricDefForME.Antecedent
- Msvm_MetricDefForME.Dependent
- Msvm_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afd5146e3b1222b2b0febbcb098c24d53c22f85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667166"
---
# <a name="msvm_metricdefforme-class"></a><span data-ttu-id="e25b4-104">MSVM \_ MetricDefForME (clase)</span><span class="sxs-lookup"><span data-stu-id="e25b4-104">Msvm\_MetricDefForME class</span></span>

<span data-ttu-id="e25b4-105">Define la asociación entre un [**\_ BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md) y un [**\_ ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) para definir las métricas de este último.</span><span class="sxs-lookup"><span data-stu-id="e25b4-105">Defines the association between an [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) and a [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) to define metrics for the latter.</span></span> <span data-ttu-id="e25b4-106">La definición de métricas se proporciona en el contexto mediante ManagedElement, que es el motivo por el que la definición depende del elemento.</span><span class="sxs-lookup"><span data-stu-id="e25b4-106">The metrics definition is given context by the ManagedElement, which is why the definition is dependent on the element.</span></span>

<span data-ttu-id="e25b4-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e25b4-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e25b4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e25b4-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricDefForME : CIM_MetricDefForME
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a><span data-ttu-id="e25b4-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="e25b4-109">Members</span></span>

<span data-ttu-id="e25b4-110">La clase **MSVM \_ MetricDefForME** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e25b4-110">The **Msvm\_MetricDefForME** class has these types of members:</span></span>

-   [<span data-ttu-id="e25b4-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e25b4-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e25b4-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e25b4-112">Properties</span></span>

<span data-ttu-id="e25b4-113">La clase **MSVM \_ MetricDefForME** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e25b4-113">The **Msvm\_MetricDefForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e25b4-114">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="e25b4-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e25b4-115">Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="e25b4-115">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="e25b4-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e25b4-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e25b4-117">Referencia a una instancia de la clase [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que representa el elemento administrado que puede tener métricas del tipo definido por **dependent** .</span><span class="sxs-lookup"><span data-stu-id="e25b4-117">A reference to an instance of the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the managed element that can have metrics of the type defined by **Dependent** applied to it.</span></span> <span data-ttu-id="e25b4-118">Esta propiedad se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="e25b4-118">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="e25b4-119">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="e25b4-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e25b4-120">Tipo de datos: **[ **CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="e25b4-120">Data type: **[**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="e25b4-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e25b4-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e25b4-122">Referencia a una instancia de la clase [**\_ BaseMetricDefinition de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que representa la definición de métricas a la que puede aplicarse el **antecedente** .</span><span class="sxs-lookup"><span data-stu-id="e25b4-122">A reference to an instance of the [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class that represents the metric definition that the **Antecedent** can have applied to it.</span></span> <span data-ttu-id="e25b4-123">Esta propiedad se hereda de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="e25b4-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="e25b4-124">**MetricCollectionEnabled**</span><span class="sxs-lookup"><span data-stu-id="e25b4-124">**MetricCollectionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e25b4-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e25b4-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e25b4-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e25b4-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e25b4-127">Indica si se va a recopilar la métrica definida por **dependent** para el **antecedente**.</span><span class="sxs-lookup"><span data-stu-id="e25b4-127">Indicates whether the metric defined by **Dependent** is being collected for the **Antecedent**.</span></span> <span data-ttu-id="e25b4-128">Será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e25b4-128">This will be one of the following values.</span></span>



| <span data-ttu-id="e25b4-129">Value</span><span class="sxs-lookup"><span data-stu-id="e25b4-129">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="e25b4-130">Significado</span><span class="sxs-lookup"><span data-stu-id="e25b4-130">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="e25b4-131"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e25b4-131"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                         | <span data-ttu-id="e25b4-132">Se está recopilando la métrica.</span><span class="sxs-lookup"><span data-stu-id="e25b4-132">The metric is being collected.</span></span><br/>                                |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="e25b4-133"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e25b4-133"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                     | <span data-ttu-id="e25b4-134">No se está recopilando la métrica.</span><span class="sxs-lookup"><span data-stu-id="e25b4-134">The metric is not being collected.</span></span><br/>                            |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <span data-ttu-id="e25b4-135"><dt>**Reservado**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e25b4-135"><dt>**Reserved**</dt> <dt>4</dt></span></span> </dl>                                     |                                                                          |
| <span id="PartiallyEnabled"></span><span id="partiallyenabled"></span><span id="PARTIALLYENABLED"></span><dl> <span data-ttu-id="e25b4-136"><dt>**PartiallyEnabled**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="e25b4-136"><dt>**PartiallyEnabled**</dt> <dt>32768</dt></span></span> </dl> | <span data-ttu-id="e25b4-137">La métrica se está recopilando para algunos dispositivos, pero no para todos.</span><span class="sxs-lookup"><span data-stu-id="e25b4-137">The metric is being collected for some, but not all, devices.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e25b4-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e25b4-138">Requirements</span></span>



| <span data-ttu-id="e25b4-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e25b4-139">Requirement</span></span> | <span data-ttu-id="e25b4-140">Value</span><span class="sxs-lookup"><span data-stu-id="e25b4-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e25b4-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e25b4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e25b4-142">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e25b4-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e25b4-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e25b4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e25b4-144">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e25b4-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e25b4-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e25b4-145">Namespace</span></span><br/>                | <span data-ttu-id="e25b4-146">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e25b4-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e25b4-147">MOF</span><span class="sxs-lookup"><span data-stu-id="e25b4-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e25b4-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e25b4-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e25b4-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e25b4-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e25b4-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e25b4-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

