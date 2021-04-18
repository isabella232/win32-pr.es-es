---
description: La \_ clase CIM MemoryCheck especifica una condición para la cantidad mínima de memoria que debe estar disponible en un sistema.
ms.assetid: a7d22f31-a285-41c4-b069-47c54865ddf5
ms.tgt_platform: multiple
title: CIM_MemoryCheck (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryCheck
- CIM_MemoryCheck.CheckID
- CIM_MemoryCheck.Caption
- CIM_MemoryCheck.Description
- CIM_MemoryCheck.CheckMode
- CIM_MemoryCheck.Name
- CIM_MemoryCheck.TargetOperatingSystem
- CIM_MemoryCheck.Version
- CIM_MemoryCheck.SoftwareElementID
- CIM_MemoryCheck.SoftwareElementState
- CIM_MemoryCheck.MemorySize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4265b108bd57bcb91aa903fd163ff14bd91311ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659619"
---
# <a name="cim_memorycheck-class"></a><span data-ttu-id="079e2-103">\_Clase MemoryCheck de CIM</span><span class="sxs-lookup"><span data-stu-id="079e2-103">CIM\_MemoryCheck class</span></span>

<span data-ttu-id="079e2-104">La clase **CIM \_ MemoryCheck** especifica una condición para la cantidad mínima de memoria que debe estar disponible en un sistema.</span><span class="sxs-lookup"><span data-stu-id="079e2-104">The **CIM\_MemoryCheck** class specifies a condition for the minimum amount of memory that must be available on a system.</span></span> <span data-ttu-id="079e2-105">La cantidad se especifica en la propiedad **MemorySize** .</span><span class="sxs-lookup"><span data-stu-id="079e2-105">The amount is specified in the **MemorySize** property.</span></span> <span data-ttu-id="079e2-106">Los detalles de las comprobaciones se comparan con el valor de la propiedad **FreePhysicalMemory** del objeto [**\_ OperatingSystem de CIM**](cim-operatingsystem.md) al que hace referencia una asociación de [**CIM \_ instalado**](cim-installedos.md) para el objeto de [**\_ ComputerSystem de CIM**](cim-computersystem.md) que describe el entorno.</span><span class="sxs-lookup"><span data-stu-id="079e2-106">Details of the checks are compared with the value of the **FreePhysicalMemory** property of the [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by a [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="079e2-107">Cuando el valor de la propiedad **FreePhysicalMemory** es mayor o igual que el valor especificado en **MemorySize**, se cumple la condición.</span><span class="sxs-lookup"><span data-stu-id="079e2-107">When the value of the **FreePhysicalMemory** property is greater than or equal to the value specified in **MemorySize**, the condition is satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="079e2-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="079e2-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="079e2-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="079e2-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="079e2-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="079e2-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="079e2-111">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="079e2-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="079e2-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="079e2-112">Syntax</span></span>

``` syntax
[UUID("{DC0E96FE-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_MemoryCheck : CIM_Check
{
  string  CheckID;
  string  Caption;
  string  Description;
  boolean CheckMode;
  string  Name;
  uint16  TargetOperatingSystem;
  string  Version;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  uint64  MemorySize;
};
```

## <a name="members"></a><span data-ttu-id="079e2-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="079e2-113">Members</span></span>

<span data-ttu-id="079e2-114">La clase **CIM \_ MemoryCheck** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="079e2-114">The **CIM\_MemoryCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="079e2-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="079e2-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="079e2-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="079e2-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="079e2-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="079e2-117">Methods</span></span>

<span data-ttu-id="079e2-118">La clase **CIM \_ MemoryCheck** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="079e2-118">The **CIM\_MemoryCheck** class has these methods.</span></span>



| <span data-ttu-id="079e2-119">Método</span><span class="sxs-lookup"><span data-stu-id="079e2-119">Method</span></span>                                                   | <span data-ttu-id="079e2-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="079e2-120">Description</span></span>                                                   |
|:---------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="079e2-121">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="079e2-121">**Invoke**</span></span>](invoke-method-in-class-cim-memorycheck.md) | <span data-ttu-id="079e2-122">Toma una acción concreta.</span><span class="sxs-lookup"><span data-stu-id="079e2-122">Takes a particular action.</span></span> <span data-ttu-id="079e2-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="079e2-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="079e2-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="079e2-124">Properties</span></span>

<span data-ttu-id="079e2-125">La clase **CIM \_ MemoryCheck** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="079e2-125">The **CIM\_MemoryCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="079e2-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="079e2-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="079e2-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="079e2-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="079e2-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="079e2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="079e2-129">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="079e2-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="079e2-130">Breve descripción textual del sujeto.</span><span class="sxs-lookup"><span data-stu-id="079e2-130">A short textual description of the subject.</span></span>

<span data-ttu-id="079e2-131">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="079e2-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="079e2-132">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="079e2-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="079e2-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="079e2-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="079e2-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="079e2-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="079e2-135">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="079e2-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="079e2-136">Identificador que se usa junto con otras claves para identificar de forma única la comprobación.</span><span class="sxs-lookup"><span data-stu-id="079e2-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="079e2-137">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="079e2-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="079e2-138">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="079e2-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="079e2-139">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="079e2-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="079e2-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="079e2-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="079e2-141">Si es **true**, se espera que la condición exista en el entorno.</span><span class="sxs-lookup"><span data-stu-id="079e2-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="079e2-142">Por ejemplo, se espera que un archivo esté en un sistema, por lo que el método [**Invoke**](invoke-method-in-class-cim-check.md) debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="079e2-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="079e2-143">Si es **false**, no se espera que la condición exista.</span><span class="sxs-lookup"><span data-stu-id="079e2-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="079e2-144">Por ejemplo, un archivo no se encuentra en un sistema, por lo que el método [**Invoke**](invoke-method-in-class-cim-check.md) debe devolver **false**.</span><span class="sxs-lookup"><span data-stu-id="079e2-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="079e2-145">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="079e2-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="079e2-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="079e2-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="079e2-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="079e2-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="079e2-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="079e2-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="079e2-149">Descripción de los objetos.</span><span class="sxs-lookup"><span data-stu-id="079e2-149">A description of the objects.</span></span>

<span data-ttu-id="079e2-150">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="079e2-150">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="079e2-151">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="079e2-151">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="079e2-152">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="079e2-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="079e2-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="079e2-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="079e2-154">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**FreePhysicalMemory**"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="079e2-154">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**FreePhysicalMemory**"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="079e2-155">Cantidad de memoria que debe existir en el sistema del equipo para que un elemento de software se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="079e2-155">Amount of memory that needs to exist on a computer system for a software element to execute properly.</span></span>

<span data-ttu-id="079e2-156">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="079e2-156">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="079e2-157">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="079e2-157">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="079e2-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="079e2-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="079e2-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="079e2-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="079e2-160">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="079e2-160">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="079e2-161">Nombre usado para identificar el elemento de software</span><span class="sxs-lookup"><span data-stu-id="079e2-161">Name used to identify the software element</span></span>

<span data-ttu-id="079e2-162">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="079e2-162">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="079e2-163">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="079e2-163">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="079e2-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="079e2-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="079e2-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="079e2-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="079e2-166">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="079e2-166">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="079e2-167">Este es un identificador de este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="079e2-167">This is an identifier for this software element.</span></span>

<span data-ttu-id="079e2-168">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="079e2-168">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="079e2-169">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="079e2-169">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="079e2-170">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="079e2-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="079e2-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="079e2-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="079e2-172">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="079e2-172">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="079e2-173">El estado de elemento de software de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="079e2-173">The software element state of a software element.</span></span>

<span data-ttu-id="079e2-174">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="079e2-174">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="079e2-175"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>Se pueden **implementar** (0)</span><span class="sxs-lookup"><span data-stu-id="079e2-175"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-176">Describe los detalles necesarios para la distribución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado instalable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="079e2-176">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="079e2-177"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalable** (1)</span><span class="sxs-lookup"><span data-stu-id="079e2-177"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-178">Describe los detalles necesarios para una instalación correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado del archivo ejecutable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="079e2-178">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="079e2-179"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Archivo ejecutable** (2)</span><span class="sxs-lookup"><span data-stu-id="079e2-179"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-180">Describe los detalles necesarios para la ejecución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado de ejecución (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="079e2-180">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="079e2-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="079e2-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-182">Describe los detalles necesarios para supervisar y operar en un elemento de inicio.</span><span class="sxs-lookup"><span data-stu-id="079e2-182">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="079e2-183">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="079e2-183">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="079e2-184">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="079e2-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="079e2-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="079e2-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="079e2-186">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Información del componente de software de DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="079e2-186">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="079e2-187">Sistema operativo de destino del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="079e2-187">Target operating system of the software element.</span></span>

<span data-ttu-id="079e2-188">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="079e2-188">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="079e2-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="079e2-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="079e2-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="079e2-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="079e2-191"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="079e2-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-192">Mac OS</span><span class="sxs-lookup"><span data-stu-id="079e2-192">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="079e2-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="079e2-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-194">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="079e2-194">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="079e2-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="079e2-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="079e2-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="079e2-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="079e2-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="079e2-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="079e2-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="079e2-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-199">Abrir máquinas virtuales</span><span class="sxs-lookup"><span data-stu-id="079e2-199">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="079e2-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="079e2-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-201">HP-UX</span><span class="sxs-lookup"><span data-stu-id="079e2-201">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="079e2-202"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="079e2-202"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="079e2-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="079e2-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="079e2-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="079e2-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="079e2-205"><span id="OS_2"></span><span id="os_2"></span>**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="079e2-205"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="079e2-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="079e2-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-207">Máquina virtual (VM) de Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="079e2-207">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="079e2-208"><span id="MSDOS"></span><span id="msdos"></span>**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="079e2-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="079e2-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="079e2-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-210">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="079e2-210">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="079e2-211"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="079e2-211"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-212">Windows 95</span><span class="sxs-lookup"><span data-stu-id="079e2-212">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="079e2-213"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="079e2-213"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-214">Windows 98</span><span class="sxs-lookup"><span data-stu-id="079e2-214">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="079e2-215"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="079e2-215"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-216">Windows NT</span><span class="sxs-lookup"><span data-stu-id="079e2-216">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="079e2-217"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="079e2-217"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-218">Windows CE</span><span class="sxs-lookup"><span data-stu-id="079e2-218">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="079e2-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="079e2-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-220">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="079e2-220">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="079e2-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="079e2-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="079e2-222"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="079e2-222"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="079e2-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="079e2-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="079e2-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="079e2-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="079e2-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="079e2-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="079e2-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="079e2-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="079e2-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="079e2-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="079e2-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="079e2-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="079e2-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="079e2-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="079e2-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="079e2-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="079e2-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="079e2-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="079e2-232"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="079e2-232"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-233">Una serie</span><span class="sxs-lookup"><span data-stu-id="079e2-233">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="079e2-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="079e2-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-235">Tándem NSK</span><span class="sxs-lookup"><span data-stu-id="079e2-235">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="079e2-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="079e2-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-237">Tándem</span><span class="sxs-lookup"><span data-stu-id="079e2-237">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="079e2-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="079e2-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-239">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="079e2-239">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="079e2-240"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="079e2-240"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="079e2-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="079e2-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="079e2-242"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="079e2-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="079e2-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="079e2-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="079e2-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="079e2-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="079e2-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="079e2-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-246">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="079e2-246">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="079e2-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="079e2-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="079e2-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="079e2-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="079e2-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="079e2-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="079e2-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="079e2-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-251">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="079e2-251">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="079e2-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="079e2-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="079e2-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="079e2-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="079e2-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="079e2-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="079e2-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="079e2-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="079e2-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="079e2-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="079e2-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="079e2-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="079e2-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="079e2-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="079e2-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="079e2-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="079e2-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="079e2-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="079e2-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="079e2-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="079e2-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="079e2-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="079e2-263">Palm OS</span><span class="sxs-lookup"><span data-stu-id="079e2-263">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="079e2-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="079e2-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="079e2-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="079e2-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="079e2-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="079e2-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="079e2-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="079e2-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="079e2-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="079e2-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="079e2-269">**Versión**</span><span class="sxs-lookup"><span data-stu-id="079e2-269">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="079e2-270">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="079e2-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="079e2-271">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="079e2-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="079e2-272">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Versión**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="079e2-272">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="079e2-273">Versión de la operación.</span><span class="sxs-lookup"><span data-stu-id="079e2-273">Version of the operation.</span></span>

<span data-ttu-id="079e2-274">La versión de la operación debe estar en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="079e2-274">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="079e2-275"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="079e2-275"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="079e2-276"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="079e2-276"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="079e2-277">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="079e2-277">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="079e2-278">Observaciones</span><span class="sxs-lookup"><span data-stu-id="079e2-278">Remarks</span></span>

<span data-ttu-id="079e2-279">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="079e2-279">WMI does not implement this class.</span></span>

<span data-ttu-id="079e2-280">La clase **CIM \_ MemoryCheck** se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="079e2-280">The **CIM\_MemoryCheck** class is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<span data-ttu-id="079e2-281">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="079e2-281">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="079e2-282">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="079e2-282">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="079e2-283">Requisitos</span><span class="sxs-lookup"><span data-stu-id="079e2-283">Requirements</span></span>



| <span data-ttu-id="079e2-284">Requisito</span><span class="sxs-lookup"><span data-stu-id="079e2-284">Requirement</span></span> | <span data-ttu-id="079e2-285">Value</span><span class="sxs-lookup"><span data-stu-id="079e2-285">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="079e2-286">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="079e2-286">Minimum supported client</span></span><br/> | <span data-ttu-id="079e2-287">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="079e2-287">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="079e2-288">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="079e2-288">Minimum supported server</span></span><br/> | <span data-ttu-id="079e2-289">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="079e2-289">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="079e2-290">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="079e2-290">Namespace</span></span><br/>                | <span data-ttu-id="079e2-291">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="079e2-291">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="079e2-292">MOF</span><span class="sxs-lookup"><span data-stu-id="079e2-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="079e2-293"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="079e2-293"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="079e2-294">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="079e2-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="079e2-295"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="079e2-295"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="079e2-296">Vea también</span><span class="sxs-lookup"><span data-stu-id="079e2-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="079e2-297">**Comprobación de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="079e2-297">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

