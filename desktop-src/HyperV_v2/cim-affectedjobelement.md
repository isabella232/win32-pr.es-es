---
description: Representa una asociación entre un trabajo y los objetos de ManagedElement de CIM \_ que pueden verse afectados por su ejecución.
ms.assetid: 94c5e602-214c-4003-921c-8955c3859738
title: CIM_AffectedJobElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AffectedJobElement
- CIM_AffectedJobElement.AffectedElement
- CIM_AffectedJobElement.AffectingElement
- CIM_AffectedJobElement.ElementEffects
- CIM_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 830e798ff12dc87c88126375736f116c044de731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156061"
---
# <a name="cim_affectedjobelement-class"></a><span data-ttu-id="65547-103">\_Clase AffectedJobElement de CIM</span><span class="sxs-lookup"><span data-stu-id="65547-103">CIM\_AffectedJobElement class</span></span>

<span data-ttu-id="65547-104">Representa una asociación entre un trabajo y los objetos de **\_ ManagedElement de CIM** que pueden verse afectados por su ejecución.</span><span class="sxs-lookup"><span data-stu-id="65547-104">Represents an association between a job and the **CIM\_ManagedElement** objects that may be affected by its execution.</span></span> <span data-ttu-id="65547-105">Puede que no sea factible para el trabajo describir todos los elementos afectados.</span><span class="sxs-lookup"><span data-stu-id="65547-105">It may not be feasible for the job to describe all of the affected elements.</span></span> <span data-ttu-id="65547-106">El propósito principal de esta asociación es proporcionar información cuando un trabajo requiere el uso exclusivo de los elementos administrados afectados o al describir los efectos secundarios que se pueden producir.</span><span class="sxs-lookup"><span data-stu-id="65547-106">The main purpose of this association is to provide information when a job requires exclusive use of the affected managed elements or when describing the side effects that may result.</span></span>

## <a name="syntax"></a><span data-ttu-id="65547-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65547-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.15.0"), UMLPackagePath("CIM::System::Processing"), AMENDMENT]
class CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Job            REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="65547-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="65547-108">Members</span></span>

<span data-ttu-id="65547-109">La clase **CIM \_ AffectedJobElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="65547-109">The **CIM\_AffectedJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="65547-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="65547-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65547-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="65547-111">Properties</span></span>

<span data-ttu-id="65547-112">La clase **CIM \_ AffectedJobElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="65547-112">The **CIM\_AffectedJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65547-113">**AffectedElement**</span><span class="sxs-lookup"><span data-stu-id="65547-113">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65547-114">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="65547-114">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="65547-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65547-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65547-116">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="65547-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="65547-117">Elemento administrado que se ve afectado por la ejecución del trabajo.</span><span class="sxs-lookup"><span data-stu-id="65547-117">The managed element affected by the execution of the job.</span></span>

</dd> <dt>

<span data-ttu-id="65547-118">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="65547-118">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65547-119">Tipo de datos **: \_ trabajo CIM**</span><span class="sxs-lookup"><span data-stu-id="65547-119">Data type: **CIM\_Job**</span></span>
</dt> <dt>

<span data-ttu-id="65547-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65547-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65547-121">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="65547-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="65547-122">El trabajo que afecta al elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="65547-122">The job that is affecting the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="65547-123">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="65547-123">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65547-124">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="65547-124">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="65547-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65547-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65547-126">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AffectedJobElement**.**OtherElementEffectsDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="65547-126">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AffectedJobElement**.**OtherElementEffectsDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="65547-127">El efecto que tiene el trabajo en el elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="65547-127">The effect the job has on the managed element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="65547-128">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="65547-128">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="65547-129">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="65547-129">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

<span data-ttu-id="65547-130">**Uso exclusivo** (2)</span><span class="sxs-lookup"><span data-stu-id="65547-130">**Exclusive Use** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

<span data-ttu-id="65547-131">**Impacto** en el rendimiento (3)</span><span class="sxs-lookup"><span data-stu-id="65547-131">**Performance Impact** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

<span data-ttu-id="65547-132">**Integridad de elementos** (4)</span><span class="sxs-lookup"><span data-stu-id="65547-132">**Element Integrity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="65547-133">**Crear** (5)</span><span class="sxs-lookup"><span data-stu-id="65547-133">**Create** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="65547-134">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="65547-134">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65547-135">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="65547-135">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="65547-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65547-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65547-137">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AffectedJobElement**.**ElementEffects**")</span><span class="sxs-lookup"><span data-stu-id="65547-137">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AffectedJobElement**.**ElementEffects**")</span></span>
</dt> </dl>

<span data-ttu-id="65547-138">Detalles adicionales de los "1" (otros) valores correspondientes de la matriz **ElementEffects** .</span><span class="sxs-lookup"><span data-stu-id="65547-138">Additional details for corresponding "1" (Other) values in the **ElementEffects** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65547-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65547-139">Requirements</span></span>



| <span data-ttu-id="65547-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="65547-140">Requirement</span></span> | <span data-ttu-id="65547-141">Value</span><span class="sxs-lookup"><span data-stu-id="65547-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65547-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65547-142">Minimum supported client</span></span><br/> | <span data-ttu-id="65547-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="65547-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="65547-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65547-144">Minimum supported server</span></span><br/> | <span data-ttu-id="65547-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65547-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="65547-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="65547-146">Namespace</span></span><br/>                | <span data-ttu-id="65547-147">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="65547-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="65547-148">MOF</span><span class="sxs-lookup"><span data-stu-id="65547-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65547-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65547-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="65547-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65547-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65547-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="65547-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

