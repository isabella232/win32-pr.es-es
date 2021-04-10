---
description: La \_ clase de comprobación CIM representa una condición o característica que se espera que sea verdadera en un entorno definido o en el ámbito de una instancia de una clase de ComputerSystem de CIM \_ .
ms.assetid: f7862fe5-4412-4d57-b5fa-03c939ddba02
ms.tgt_platform: multiple
title: CIM_Check (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Check
- CIM_Check.CheckID
- CIM_Check.Caption
- CIM_Check.Description
- CIM_Check.CheckMode
- CIM_Check.Name
- CIM_Check.TargetOperatingSystem
- CIM_Check.Version
- CIM_Check.SoftwareElementID
- CIM_Check.SoftwareElementState
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cbe742fb4cd2510ec4c502f89b3b3b1eb79bc47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907340"
---
# <a name="cim_check-class"></a><span data-ttu-id="a9c4e-103">\_Clase de comprobación CIM</span><span class="sxs-lookup"><span data-stu-id="a9c4e-103">CIM\_Check class</span></span>

<span data-ttu-id="a9c4e-104">La clase de **\_ comprobación CIM** representa una condición o característica que se espera que sea verdadera en un entorno definido o en el ámbito de una instancia de una clase de [**\_ ComputerSystem de CIM**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="a9c4e-104">The **CIM\_Check** class represents a condition or characteristic that is expected to be true in an environment defined or scoped by an instance of a [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span> <span data-ttu-id="a9c4e-105">Las comprobaciones asociadas a un elemento de software determinado se organizan en uno de dos grupos mediante la propiedad **Phase** de la Asociación [**\_ SoftwareElementChecks de CIM**](cim-softwareelementchecks.md) .</span><span class="sxs-lookup"><span data-stu-id="a9c4e-105">The checks associated with a particular software element are organized into one of two groups using the **Phase** property of the [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association.</span></span>

<span data-ttu-id="a9c4e-106">Las condiciones que se espera que se cumplan cuando un elemento de software está en un entorno determinado se conocen como condiciones en estado.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-106">Conditions that are expected to be satisfied when a software element is in a particular environment are known as in-state conditions.</span></span> <span data-ttu-id="a9c4e-107">Las condiciones que deben satisfacerse para realizar la transición del elemento de software actual al estado siguiente se conocen como condiciones de estado siguiente.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-107">Conditions that must be satisfied to transition the current software element to its next state are known as next-state conditions.</span></span>

<span data-ttu-id="a9c4e-108">Un [**objeto \_ ComputerSystem de CIM**](cim-computersystem.md) representa el entorno en el que ya está instalado un [**\_ SoftwareElement de CIM**](cim-softwareelement.md) o en el que se instalará un **\_ SoftwareElement de CIM** .</span><span class="sxs-lookup"><span data-stu-id="a9c4e-108">A [**CIM\_ComputerSystem**](cim-computersystem.md) object represents the environment in which a [**CIM\_SoftwareElement**](cim-softwareelement.md) is already installed, or in which a **CIM\_SoftwareElement** will be installed.</span></span> <span data-ttu-id="a9c4e-109">En el caso en el que ya se haya instalado un elemento de software, la Asociación [**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) se usa para identificar el objeto **\_ ComputerSystem de CIM** que representa el "entorno".</span><span class="sxs-lookup"><span data-stu-id="a9c4e-109">For the case in which a software element is already installed, the [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) association is used to identify the **CIM\_ComputerSystem** object that represents the "environment."</span></span> <span data-ttu-id="a9c4e-110">Cuando un elemento de software se distribuye e instala en un equipo diferente, el objeto de **\_ ComputerSystem de CIM** para el sistema de destino es el entorno.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-110">When a software element is being distributed and installed on a different computer, the **CIM\_ComputerSystem** object for the targeted system is the environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a9c4e-111">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a9c4e-112">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a9c4e-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a9c4e-113">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a9c4e-114">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9c4e-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9c4e-115">Syntax</span></span>

``` syntax
[UUID("{7A9135CA-DB21-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_Check
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
};
```

## <a name="members"></a><span data-ttu-id="a9c4e-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="a9c4e-116">Members</span></span>

<span data-ttu-id="a9c4e-117">La clase de **\_ comprobación CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a9c4e-117">The **CIM\_Check** class has these types of members:</span></span>

-   [<span data-ttu-id="a9c4e-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="a9c4e-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="a9c4e-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a9c4e-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a9c4e-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="a9c4e-120">Methods</span></span>

<span data-ttu-id="a9c4e-121">La clase de **\_ comprobación CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-121">The **CIM\_Check** class has these methods.</span></span>



| <span data-ttu-id="a9c4e-122">Método</span><span class="sxs-lookup"><span data-stu-id="a9c4e-122">Method</span></span>                                             | <span data-ttu-id="a9c4e-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9c4e-123">Description</span></span>                                                   |
|:---------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="a9c4e-124">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-124">**Invoke**</span></span>](invoke-method-in-class-cim-check.md) | <span data-ttu-id="a9c4e-125">Toma una acción concreta.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-125">Takes a particular action.</span></span> <span data-ttu-id="a9c4e-126">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a9c4e-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a9c4e-127">Properties</span></span>

<span data-ttu-id="a9c4e-128">La clase de **\_ comprobación CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-128">The **CIM\_Check** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9c4e-129">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9c4e-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9c4e-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9c4e-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9c4e-132">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-132">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a9c4e-133">Breve descripción textual del sujeto.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-133">A short textual description of the subject.</span></span>

</dd> <dt>

<span data-ttu-id="a9c4e-134">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-134">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9c4e-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9c4e-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9c4e-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9c4e-137">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a9c4e-138">Identificador que se usa junto con otras claves para identificar de forma única la comprobación.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-138">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

</dd> <dt>

<span data-ttu-id="a9c4e-139">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-139">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9c4e-140">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a9c4e-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9c4e-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9c4e-142">Si es **true**, se espera que la condición exista en el entorno.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-142">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="a9c4e-143">Por ejemplo, se espera que un archivo esté en un sistema, por lo que el método [**Invoke**](invoke-method-in-class-cim-check.md) debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-143">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="a9c4e-144">Si es **false**, no se espera que la condición exista.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-144">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="a9c4e-145">Por ejemplo, un archivo no se encuentra en un sistema, por lo que el método [**Invoke**](invoke-method-in-class-cim-check.md) debe devolver **false**.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-145">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a9c4e-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9c4e-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9c4e-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9c4e-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9c4e-149">Descripción de los objetos.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-149">A description of the objects.</span></span>

</dd> <dt>

<span data-ttu-id="a9c4e-150">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-150">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9c4e-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9c4e-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9c4e-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9c4e-153">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-153">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a9c4e-154">Nombre usado para identificar el elemento de software.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-154">Name used to identify the software element.</span></span>

</dd> <dt>

<span data-ttu-id="a9c4e-155">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-155">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9c4e-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9c4e-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9c4e-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9c4e-158">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-158">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a9c4e-159">Este es un identificador de este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-159">This is an identifier for this software element.</span></span>

</dd> <dt>

<span data-ttu-id="a9c4e-160">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-160">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9c4e-161">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9c4e-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9c4e-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9c4e-163">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-163">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a9c4e-164">El estado de elemento de software de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-164">The software element state of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="a9c4e-165"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>Se pueden **implementar** (0)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-165"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-166">Describe los detalles necesarios para la distribución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado instalable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="a9c4e-166">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="a9c4e-167"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalable** (1)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-167"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-168">Describe los detalles necesarios para una instalación correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado del archivo ejecutable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="a9c4e-168">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="a9c4e-169"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Archivo ejecutable** (2)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-169"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-170">Describe los detalles necesarios para la ejecución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado de ejecución (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="a9c4e-170">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="a9c4e-171"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-171"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-172">Describe los detalles necesarios para supervisar y operar en un elemento de inicio.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-172">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a9c4e-173">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-173">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9c4e-174">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a9c4e-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9c4e-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9c4e-176">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Información del componente de software de DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="a9c4e-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="a9c4e-177">Sistema operativo de destino del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-177">Target operating system of the software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a9c4e-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a9c4e-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="a9c4e-180"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-180"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-181">Mac OS</span><span class="sxs-lookup"><span data-stu-id="a9c4e-181">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="a9c4e-182"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-182"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-183">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="a9c4e-183">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="a9c4e-184"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-184"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="a9c4e-185"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-185"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="a9c4e-186"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-186"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="a9c4e-187"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-187"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-188">Abrir máquinas virtuales</span><span class="sxs-lookup"><span data-stu-id="a9c4e-188">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="a9c4e-189"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-189"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-190">HP-UX</span><span class="sxs-lookup"><span data-stu-id="a9c4e-190">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="a9c4e-191"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-191"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="a9c4e-192"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-192"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="a9c4e-193"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-193"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="a9c4e-194"><span id="OS_2"></span><span id="os_2"></span>**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-194"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="a9c4e-195"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-195"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-196">Máquina virtual (VM) de Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="a9c4e-196">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="a9c4e-197"><span id="MSDOS"></span><span id="msdos"></span>**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-197"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="a9c4e-198"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-198"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-199">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="a9c4e-199">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="a9c4e-200"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-200"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-201">Windows 95</span><span class="sxs-lookup"><span data-stu-id="a9c4e-201">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="a9c4e-202"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-202"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-203">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a9c4e-203">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="a9c4e-204"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-204"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-205">Windows NT</span><span class="sxs-lookup"><span data-stu-id="a9c4e-205">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="a9c4e-206"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-206"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-207">Windows CE</span><span class="sxs-lookup"><span data-stu-id="a9c4e-207">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="a9c4e-208"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-208"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-209">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="a9c4e-209">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="a9c4e-210"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-210"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="a9c4e-211"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-211"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="a9c4e-212"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-212"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="a9c4e-213"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-213"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="a9c4e-214"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-214"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="a9c4e-215"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-215"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="a9c4e-216"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-216"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="a9c4e-217"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-217"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="a9c4e-218"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-218"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="a9c4e-219"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-219"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="a9c4e-220"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-220"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="a9c4e-221"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-221"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-222">Una serie</span><span class="sxs-lookup"><span data-stu-id="a9c4e-222">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="a9c4e-223"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-223"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-224">Tándem NSK</span><span class="sxs-lookup"><span data-stu-id="a9c4e-224">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="a9c4e-225"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-225"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-226">Tándem</span><span class="sxs-lookup"><span data-stu-id="a9c4e-226">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="a9c4e-227"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-227"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-228">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="a9c4e-228">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="a9c4e-229"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-229"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="a9c4e-230"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-230"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="a9c4e-231"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-231"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="a9c4e-232"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-232"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="a9c4e-233"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-233"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="a9c4e-234"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-234"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-235">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="a9c4e-235">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="a9c4e-236"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-236"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="a9c4e-237"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-237"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="a9c4e-238"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-238"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="a9c4e-239"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-239"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-240">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="a9c4e-240">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="a9c4e-241"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-241"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="a9c4e-242"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-242"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="a9c4e-243"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-243"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="a9c4e-244"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-244"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="a9c4e-245"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-245"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="a9c4e-246"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-246"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="a9c4e-247"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-247"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="a9c4e-248"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-248"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="a9c4e-249"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-249"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="a9c4e-250"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-250"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="a9c4e-251"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-251"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="a9c4e-252">Palm OS</span><span class="sxs-lookup"><span data-stu-id="a9c4e-252">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="a9c4e-253"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-253"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="a9c4e-254"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-254"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="a9c4e-255"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-255"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="a9c4e-256"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-256"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="a9c4e-257"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="a9c4e-257"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a9c4e-258">**Versión**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-258">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9c4e-259">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a9c4e-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9c4e-260">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a9c4e-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9c4e-261">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Versión**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="a9c4e-261">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="a9c4e-262">Versión de la operación.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-262">Version of the operation.</span></span>

<span data-ttu-id="a9c4e-263">La versión de la operación debe estar en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="a9c4e-263">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="a9c4e-264"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="a9c4e-264"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="a9c4e-265"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="a9c4e-265"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9c4e-266">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9c4e-266">Remarks</span></span>

<span data-ttu-id="a9c4e-267">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-267">WMI does not implement this class.</span></span> <span data-ttu-id="a9c4e-268">Para obtener más información sobre las clases derivadas de la **\_ comprobación CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a9c4e-268">For more information about classes derived from **CIM\_Check**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a9c4e-269">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-269">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a9c4e-270">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="a9c4e-270">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9c4e-271">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9c4e-271">Requirements</span></span>



| <span data-ttu-id="a9c4e-272">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9c4e-272">Requirement</span></span> | <span data-ttu-id="a9c4e-273">Value</span><span class="sxs-lookup"><span data-stu-id="a9c4e-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c4e-274">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9c4e-274">Minimum supported client</span></span><br/> | <span data-ttu-id="a9c4e-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9c4e-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9c4e-276">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9c4e-276">Minimum supported server</span></span><br/> | <span data-ttu-id="a9c4e-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9c4e-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9c4e-278">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a9c4e-278">Namespace</span></span><br/>                | <span data-ttu-id="a9c4e-279">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a9c4e-279">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a9c4e-280">MOF</span><span class="sxs-lookup"><span data-stu-id="a9c4e-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9c4e-281"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9c4e-281"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9c4e-282">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a9c4e-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9c4e-283"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9c4e-283"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

