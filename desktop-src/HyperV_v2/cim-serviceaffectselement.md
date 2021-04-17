---
description: Representa una asociación entre un servicio y un elemento administrado que podría verse afectado por su ejecución.
ms.assetid: 2fd9199f-9ab0-4c42-9708-d6cd6911f77a
title: CIM_ServiceAffectsElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAffectsElement
- CIM_ServiceAffectsElement.AffectedElement
- CIM_ServiceAffectsElement.AffectingElement
- CIM_ServiceAffectsElement.ElementEffects
- CIM_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e4dd4fe00d1ee4a537741ce69240413e78aca85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666565"
---
# <a name="cim_serviceaffectselement-class"></a><span data-ttu-id="46112-103">\_Clase ServiceAffectsElement de CIM</span><span class="sxs-lookup"><span data-stu-id="46112-103">CIM\_ServiceAffectsElement class</span></span>

<span data-ttu-id="46112-104">Representa una asociación entre un servicio y un elemento administrado que podría verse afectado por su ejecución.</span><span class="sxs-lookup"><span data-stu-id="46112-104">Represents an association between a service and a managed element that might be affected by its execution.</span></span>

## <a name="syntax"></a><span data-ttu-id="46112-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46112-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="46112-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="46112-106">Members</span></span>

<span data-ttu-id="46112-107">La clase **CIM \_ ServiceAffectsElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="46112-107">The **CIM\_ServiceAffectsElement** class has these types of members:</span></span>

-   [<span data-ttu-id="46112-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="46112-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46112-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="46112-109">Properties</span></span>

<span data-ttu-id="46112-110">La clase **CIM \_ ServiceAffectsElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="46112-110">The **CIM\_ServiceAffectsElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46112-111">**AffectedElement**</span><span class="sxs-lookup"><span data-stu-id="46112-111">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46112-112">Tipo de datos: **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="46112-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="46112-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="46112-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46112-114">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="46112-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="46112-115">Elemento administrado que se ve afectado por el servicio.</span><span class="sxs-lookup"><span data-stu-id="46112-115">The managed element that is affected by the service.</span></span>

</dd> <dt>

<span data-ttu-id="46112-116">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="46112-116">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46112-117">Tipo de datos **: \_ servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="46112-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="46112-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="46112-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46112-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="46112-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="46112-120">El servicio que está afectando al elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="46112-120">The service that is affecting the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="46112-121">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="46112-121">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46112-122">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46112-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="46112-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="46112-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46112-124">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ServiceAffectsElement**.**OtherElementEffectsDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="46112-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ServiceAffectsElement**.**OtherElementEffectsDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="46112-125">Efecto en el elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="46112-125">The effect on the managed element.</span></span> <span data-ttu-id="46112-126">Esta matriz corresponde a la matriz **OtherElementEffectsDescriptions** .</span><span class="sxs-lookup"><span data-stu-id="46112-126">This array corresponds to the **OtherElementEffectsDescriptions** array.</span></span>

<span data-ttu-id="46112-127">\- Uso exclusivo (2): ningún otro servicio puede tener esta asociación al elemento.</span><span class="sxs-lookup"><span data-stu-id="46112-127">\- Exclusive Use (2): No other Service may have this association to the element.</span></span>

<span data-ttu-id="46112-128">\- Impacto en el rendimiento (3): desusado en favor de "consume", "mejora el rendimiento" o "degrada el rendimiento".</span><span class="sxs-lookup"><span data-stu-id="46112-128">\- Performance Impact (3): Deprecated in favor of "Consumes", "Enhances Performance", or "Degrades Performance".</span></span> <span data-ttu-id="46112-129">La ejecución del servicio puede mejorar o degradar el rendimiento del elemento.</span><span class="sxs-lookup"><span data-stu-id="46112-129">Execution of the Service may enhance or degrade the performance of the element.</span></span> <span data-ttu-id="46112-130">Esto puede ser un efecto secundario de la ejecución o como una consecuencia prevista de los métodos proporcionados por el servicio.</span><span class="sxs-lookup"><span data-stu-id="46112-130">This may be as a side-effect of execution or as an intended consequence of methods provided by the Service.</span></span>

<span data-ttu-id="46112-131">\- Integridad de elemento (4): desusado en favor de "consume", "mejora la integridad" o "degrada la integridad".</span><span class="sxs-lookup"><span data-stu-id="46112-131">\- Element Integrity (4): Deprecated in favor of "Consumes", "Enhances Integrity", or "Degrades Integrity".</span></span> <span data-ttu-id="46112-132">La ejecución del servicio puede mejorar o degradar la integridad del elemento.</span><span class="sxs-lookup"><span data-stu-id="46112-132">Execution of the Service may enhance or degrade the integrity of the element.</span></span> <span data-ttu-id="46112-133">Esto puede ser un efecto secundario de la ejecución o como una consecuencia prevista de los métodos proporcionados por el servicio.</span><span class="sxs-lookup"><span data-stu-id="46112-133">This may be as a side-effect of execution or as an intended consequence of methods provided by the Service.</span></span>

<span data-ttu-id="46112-134">\- Administra (5): el servicio administra el elemento.</span><span class="sxs-lookup"><span data-stu-id="46112-134">\- Manages (5): The Service manages the element.</span></span>

<span data-ttu-id="46112-135">\- Consume (6): la ejecución del servicio consume parte o todo el elemento asociado como consecuencia de la ejecución del servicio.</span><span class="sxs-lookup"><span data-stu-id="46112-135">\- Consumes (6): Execution of the Service consumes some or all of the associated element as a consequence of running the Service.</span></span> <span data-ttu-id="46112-136">Por ejemplo, el servicio puede consumir ciclos de CPU, lo que puede afectar al rendimiento o al almacenamiento, lo que puede afectar al rendimiento y a la integridad.</span><span class="sxs-lookup"><span data-stu-id="46112-136">For example, the Service may consume CPU cycles, which may affect performance, or Storage which may affect both performance and integrity.</span></span> <span data-ttu-id="46112-137">(Por ejemplo, la falta de almacenamiento libre puede degradar la integridad reduciendo la capacidad de guardar el estado.</span><span class="sxs-lookup"><span data-stu-id="46112-137">(For instance, the lack of free storage can degrade integrity by reducing the ability to save state.</span></span> <span data-ttu-id="46112-138">) "Consumes" se puede usar solo o junto con otros valores, en particular, "degrada el rendimiento" y "degrada la integridad".</span><span class="sxs-lookup"><span data-stu-id="46112-138">) "Consumes" may be used alone or in conjunction with other values, in particular, "Degrades Performance" and "Degrades Integrity".</span></span>

<span data-ttu-id="46112-139">"Administra" y no "consumes" se debe usar para reflejar los servicios de asignación que puede proporcionar un servicio.</span><span class="sxs-lookup"><span data-stu-id="46112-139">"Manages" and not "Consumes" should be used to reflect allocation services that may be provided by a Service.</span></span>

<span data-ttu-id="46112-140">\- Mejora la integridad (7): el servicio puede mejorar la integridad del elemento asociado.</span><span class="sxs-lookup"><span data-stu-id="46112-140">\- Enhances Integrity (7): The Service may enhance integrity of the associated element.</span></span>

<span data-ttu-id="46112-141">\- Degrada la integridad (8): el servicio puede degradar la integridad del elemento asociado.</span><span class="sxs-lookup"><span data-stu-id="46112-141">\- Degrades Integrity (8): The Service may degrade integrity of the associated element.</span></span>

<span data-ttu-id="46112-142">\- Mejora el rendimiento (9): el servicio puede mejorar el rendimiento del elemento asociado.</span><span class="sxs-lookup"><span data-stu-id="46112-142">\- Enhances Performance (9): The Service may enhance performance of the associated element.</span></span>

<span data-ttu-id="46112-143">\- Degrada el rendimiento (10): el servicio puede degradar el rendimiento del elemento asociado.</span><span class="sxs-lookup"><span data-stu-id="46112-143">\- Degrades Performance (10): The Service may degrade performance of the associated element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="46112-144">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="46112-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="46112-145">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="46112-145">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

<span data-ttu-id="46112-146">**Uso exclusivo** (2)</span><span class="sxs-lookup"><span data-stu-id="46112-146">**Exclusive Use** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

<span data-ttu-id="46112-147">**Impacto** en el rendimiento (3)</span><span class="sxs-lookup"><span data-stu-id="46112-147">**Performance Impact** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

<span data-ttu-id="46112-148">**Integridad de elementos** (4)</span><span class="sxs-lookup"><span data-stu-id="46112-148">**Element Integrity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Manages"></span><span id="manages"></span><span id="MANAGES"></span>

<span data-ttu-id="46112-149">**Administra** (5)</span><span class="sxs-lookup"><span data-stu-id="46112-149">**Manages** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Consumes"></span><span id="consumes"></span><span id="CONSUMES"></span>

<span data-ttu-id="46112-150">**Consume** (6)</span><span class="sxs-lookup"><span data-stu-id="46112-150">**Consumes** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhances_Integrity"></span><span id="enhances_integrity"></span><span id="ENHANCES_INTEGRITY"></span>

<span data-ttu-id="46112-151">**Mejora la integridad** (7)</span><span class="sxs-lookup"><span data-stu-id="46112-151">**Enhances Integrity** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Degrades_Integrity"></span><span id="degrades_integrity"></span><span id="DEGRADES_INTEGRITY"></span>

<span data-ttu-id="46112-152">**Degrada la integridad** (8)</span><span class="sxs-lookup"><span data-stu-id="46112-152">**Degrades Integrity** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhances_Performance"></span><span id="enhances_performance"></span><span id="ENHANCES_PERFORMANCE"></span>

<span data-ttu-id="46112-153">**Mejora el rendimiento** (9)</span><span class="sxs-lookup"><span data-stu-id="46112-153">**Enhances Performance** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degrades_Performance"></span><span id="degrades_performance"></span><span id="DEGRADES_PERFORMANCE"></span>

<span data-ttu-id="46112-154">**Degrada el rendimiento** (10)</span><span class="sxs-lookup"><span data-stu-id="46112-154">**Degrades Performance** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="46112-155">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="46112-155">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="46112-156">**Proveedor reservado** (0x8000... 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="46112-156">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="46112-157">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="46112-157">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46112-158">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="46112-158">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="46112-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="46112-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46112-160">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ServiceAffectsElement**.**ElementEffects**")</span><span class="sxs-lookup"><span data-stu-id="46112-160">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ServiceAffectsElement**.**ElementEffects**")</span></span>
</dt> </dl>

<span data-ttu-id="46112-161">Cada elemento de la matriz proporciona información adicional para el elemento correspondiente de la matriz **ElementEffects** .</span><span class="sxs-lookup"><span data-stu-id="46112-161">Each item in the array provides additional information for the corresponding item in the **ElementEffects** array.</span></span> <span data-ttu-id="46112-162">Se necesita una descripción para cualquier elemento de la matriz **ElementEffects** que esté establecido en **other** ("1").</span><span class="sxs-lookup"><span data-stu-id="46112-162">A description is required for any item in the **ElementEffects** array that is set to **Other** ("1").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46112-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46112-163">Requirements</span></span>



| <span data-ttu-id="46112-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="46112-164">Requirement</span></span> | <span data-ttu-id="46112-165">Value</span><span class="sxs-lookup"><span data-stu-id="46112-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46112-166">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46112-166">Minimum supported client</span></span><br/> | <span data-ttu-id="46112-167">Windows 8</span><span class="sxs-lookup"><span data-stu-id="46112-167">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="46112-168">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46112-168">Minimum supported server</span></span><br/> | <span data-ttu-id="46112-169">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="46112-169">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="46112-170">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="46112-170">Namespace</span></span><br/>                | <span data-ttu-id="46112-171">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="46112-171">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="46112-172">MOF</span><span class="sxs-lookup"><span data-stu-id="46112-172">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46112-173"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46112-173"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="46112-174">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="46112-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46112-175"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46112-175"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

