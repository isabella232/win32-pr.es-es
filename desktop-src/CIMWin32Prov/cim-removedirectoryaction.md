---
description: La \_ clase RemoveDirectoryAction de CIM quita los directorios de los elementos de software.
ms.assetid: e403baa8-3704-42a6-970a-8159e7cd72a7
ms.tgt_platform: multiple
title: CIM_RemoveDirectoryAction (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoveDirectoryAction
- CIM_RemoveDirectoryAction.ActionID
- CIM_RemoveDirectoryAction.Caption
- CIM_RemoveDirectoryAction.Description
- CIM_RemoveDirectoryAction.Direction
- CIM_RemoveDirectoryAction.Name
- CIM_RemoveDirectoryAction.SoftwareElementID
- CIM_RemoveDirectoryAction.SoftwareElementState
- CIM_RemoveDirectoryAction.TargetOperatingSystem
- CIM_RemoveDirectoryAction.Version
- CIM_RemoveDirectoryAction.DirectoryName
- CIM_RemoveDirectoryAction.MustBeEmpty
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5960c0f72bdea28bd431c11d23ccffa0ea19ead
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998169"
---
# <a name="cim_removedirectoryaction-class"></a><span data-ttu-id="243a6-103">\_Clase RemoveDirectoryAction de CIM</span><span class="sxs-lookup"><span data-stu-id="243a6-103">CIM\_RemoveDirectoryAction class</span></span>

<span data-ttu-id="243a6-104">La **clase \_ RemoveDirectoryAction de CIM** quita los directorios de los elementos de software.</span><span class="sxs-lookup"><span data-stu-id="243a6-104">The **CIM\_RemoveDirectoryAction** class removes directories for software elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="243a6-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="243a6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="243a6-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="243a6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="243a6-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="243a6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="243a6-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="243a6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="243a6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="243a6-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{B272D2EA-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RemoveDirectoryAction : CIM_DirectoryAction
{
  string  ActionID;
  string  Caption;
  string  Description;
  uint16  Direction;
  string  Name;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  uint16  TargetOperatingSystem;
  string  Version;
  string  DirectoryName;
  boolean MustBeEmpty;
};
```

## <a name="members"></a><span data-ttu-id="243a6-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="243a6-110">Members</span></span>

<span data-ttu-id="243a6-111">La clase **CIM \_ RemoveDirectoryAction** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="243a6-111">The **CIM\_RemoveDirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="243a6-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="243a6-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="243a6-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="243a6-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="243a6-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="243a6-114">Methods</span></span>

<span data-ttu-id="243a6-115">La clase **CIM \_ RemoveDirectoryAction** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="243a6-115">The **CIM\_RemoveDirectoryAction** class has these methods.</span></span>



| <span data-ttu-id="243a6-116">Método</span><span class="sxs-lookup"><span data-stu-id="243a6-116">Method</span></span>                                                             | <span data-ttu-id="243a6-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="243a6-117">Description</span></span>                                                   |
|:-------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="243a6-118">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="243a6-118">**Invoke**</span></span>](invoke-method-in-class-cim-removedirectoryaction.md) | <span data-ttu-id="243a6-119">Toma una acción concreta.</span><span class="sxs-lookup"><span data-stu-id="243a6-119">Takes a particular action.</span></span> <span data-ttu-id="243a6-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="243a6-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="243a6-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="243a6-121">Properties</span></span>

<span data-ttu-id="243a6-122">La clase **CIM \_ RemoveDirectoryAction** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="243a6-122">The **CIM\_RemoveDirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="243a6-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="243a6-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="243a6-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="243a6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="243a6-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="243a6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="243a6-126">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="243a6-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="243a6-127">Identificador único asignado a una acción determinada para un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="243a6-127">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="243a6-128">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="243a6-128">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="243a6-129">**Caption**</span><span class="sxs-lookup"><span data-stu-id="243a6-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="243a6-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="243a6-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="243a6-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="243a6-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="243a6-132">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="243a6-132">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="243a6-133">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="243a6-133">Short textual description of the object.</span></span>

<span data-ttu-id="243a6-134">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="243a6-134">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="243a6-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="243a6-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="243a6-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="243a6-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="243a6-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="243a6-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="243a6-138">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="243a6-138">Description of the object.</span></span>

<span data-ttu-id="243a6-139">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="243a6-139">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="243a6-140">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="243a6-140">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="243a6-141">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="243a6-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="243a6-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="243a6-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="243a6-143">Indica si un objeto [**de \_ acción de CIM**](cim-action.md) determinado forma parte de una secuencia de acciones para pasar el elemento de software actual al siguiente estado, como "instalar", o para quitar el elemento de software actual, como "desinstalar".</span><span class="sxs-lookup"><span data-stu-id="243a6-143">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="243a6-144">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="243a6-144">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="243a6-145">**Instalar** (0)</span><span class="sxs-lookup"><span data-stu-id="243a6-145">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="243a6-146">**Desinstalar** (1)</span><span class="sxs-lookup"><span data-stu-id="243a6-146">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="243a6-147">**DirectoryName**</span><span class="sxs-lookup"><span data-stu-id="243a6-147">**DirectoryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="243a6-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="243a6-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="243a6-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="243a6-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="243a6-150">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="243a6-150">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="243a6-151">Nombre del directorio al que se aplica la acción.</span><span class="sxs-lookup"><span data-stu-id="243a6-151">Name of the directory to which the action applies.</span></span>

<span data-ttu-id="243a6-152">Esta propiedad se hereda de [**\_ DirectoryAction CIM**](cim-directoryaction.md).</span><span class="sxs-lookup"><span data-stu-id="243a6-152">This property is inherited from [**CIM\_DirectoryAction**](cim-directoryaction.md).</span></span>

</dd> <dt>

<span data-ttu-id="243a6-153">**MustBeEmpty**</span><span class="sxs-lookup"><span data-stu-id="243a6-153">**MustBeEmpty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="243a6-154">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="243a6-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="243a6-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="243a6-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="243a6-156">Si **es true**, el directorio debe estar vacío para quitarse.</span><span class="sxs-lookup"><span data-stu-id="243a6-156">If **TRUE**, the directory must be empty to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="243a6-157">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="243a6-157">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="243a6-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="243a6-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="243a6-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="243a6-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="243a6-160">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="243a6-160">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="243a6-161">Identifica el elemento de software.</span><span class="sxs-lookup"><span data-stu-id="243a6-161">Identifies the software element.</span></span>

<span data-ttu-id="243a6-162">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="243a6-162">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="243a6-163">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="243a6-163">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="243a6-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="243a6-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="243a6-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="243a6-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="243a6-166">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="243a6-166">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="243a6-167">Identificador del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="243a6-167">Identifier for the software element.</span></span>

<span data-ttu-id="243a6-168">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="243a6-168">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="243a6-169">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="243a6-169">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="243a6-170">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="243a6-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="243a6-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="243a6-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="243a6-172">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="243a6-172">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="243a6-173">Estado de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="243a6-173">State of a software element.</span></span>

<span data-ttu-id="243a6-174">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="243a6-174">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="243a6-175"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>Se pueden **implementar** (0)</span><span class="sxs-lookup"><span data-stu-id="243a6-175"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-176">Describe los detalles necesarios para la distribución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado instalable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="243a6-176">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="243a6-177"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalable** (1)</span><span class="sxs-lookup"><span data-stu-id="243a6-177"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-178">Describe los detalles necesarios para una instalación correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado del archivo ejecutable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="243a6-178">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="243a6-179"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Archivo ejecutable** (2)</span><span class="sxs-lookup"><span data-stu-id="243a6-179"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-180">Describe los detalles necesarios para la ejecución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado de ejecución (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="243a6-180">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="243a6-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="243a6-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-182">Describe los detalles necesarios para supervisar y operar en un elemento de inicio.</span><span class="sxs-lookup"><span data-stu-id="243a6-182">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="243a6-183">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="243a6-183">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="243a6-184">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="243a6-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="243a6-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="243a6-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="243a6-186">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Información del componente de software de DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="243a6-186">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="243a6-187">Sistema operativo de destino del elemento de software propietario.</span><span class="sxs-lookup"><span data-stu-id="243a6-187">Target operating system of the owning software element.</span></span>

<span data-ttu-id="243a6-188">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="243a6-188">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="243a6-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="243a6-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="243a6-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="243a6-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="243a6-191"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="243a6-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-192">Mac OS</span><span class="sxs-lookup"><span data-stu-id="243a6-192">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="243a6-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="243a6-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="243a6-194"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="243a6-194"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="243a6-195"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="243a6-195"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="243a6-196"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="243a6-196"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="243a6-197"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="243a6-197"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-198">Abrir máquinas virtuales</span><span class="sxs-lookup"><span data-stu-id="243a6-198">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="243a6-199"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="243a6-199"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-200">HP-UX</span><span class="sxs-lookup"><span data-stu-id="243a6-200">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="243a6-201"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="243a6-201"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="243a6-202"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="243a6-202"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="243a6-203"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="243a6-203"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="243a6-204"><span id="OS_2"></span><span id="os_2"></span>**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="243a6-204"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="243a6-205"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="243a6-205"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-206">Máquina virtual (VM) de Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="243a6-206">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="243a6-207"><span id="MSDOS"></span><span id="msdos"></span>**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="243a6-207"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="243a6-208"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="243a6-208"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-209">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="243a6-209">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="243a6-210"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="243a6-210"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-211">Windows 95</span><span class="sxs-lookup"><span data-stu-id="243a6-211">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="243a6-212"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="243a6-212"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-213">Windows 98</span><span class="sxs-lookup"><span data-stu-id="243a6-213">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="243a6-214"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="243a6-214"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-215">Windows NT</span><span class="sxs-lookup"><span data-stu-id="243a6-215">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="243a6-216"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="243a6-216"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-217">Windows CE</span><span class="sxs-lookup"><span data-stu-id="243a6-217">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="243a6-218"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="243a6-218"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-219">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="243a6-219">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="243a6-220"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="243a6-220"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="243a6-221"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="243a6-221"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="243a6-222"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="243a6-222"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="243a6-223"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="243a6-223"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="243a6-224"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="243a6-224"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="243a6-225"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="243a6-225"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="243a6-226"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="243a6-226"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="243a6-227"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="243a6-227"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="243a6-228"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="243a6-228"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="243a6-229"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="243a6-229"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="243a6-230"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="243a6-230"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="243a6-231"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="243a6-231"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-232">Una serie</span><span class="sxs-lookup"><span data-stu-id="243a6-232">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="243a6-233"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="243a6-233"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-234">Tándem NSK</span><span class="sxs-lookup"><span data-stu-id="243a6-234">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="243a6-235"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="243a6-235"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-236">Tándem</span><span class="sxs-lookup"><span data-stu-id="243a6-236">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="243a6-237"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="243a6-237"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-238">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="243a6-238">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="243a6-239"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="243a6-239"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="243a6-240"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="243a6-240"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="243a6-241"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="243a6-241"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="243a6-242"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="243a6-242"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="243a6-243"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="243a6-243"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="243a6-244"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="243a6-244"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-245">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="243a6-245">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="243a6-246"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="243a6-246"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="243a6-247"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="243a6-247"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="243a6-248"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="243a6-248"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="243a6-249"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="243a6-249"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-250">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="243a6-250">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="243a6-251"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="243a6-251"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="243a6-252"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="243a6-252"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="243a6-253"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="243a6-253"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="243a6-254"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="243a6-254"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="243a6-255"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="243a6-255"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="243a6-256"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="243a6-256"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="243a6-257"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="243a6-257"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="243a6-258"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="243a6-258"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-259">Ser so</span><span class="sxs-lookup"><span data-stu-id="243a6-259">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="243a6-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="243a6-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="243a6-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="243a6-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="243a6-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="243a6-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="243a6-263">Palm OS</span><span class="sxs-lookup"><span data-stu-id="243a6-263">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="243a6-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="243a6-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="243a6-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="243a6-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="243a6-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="243a6-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="243a6-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="243a6-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="243a6-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="243a6-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="243a6-269">**Versión**</span><span class="sxs-lookup"><span data-stu-id="243a6-269">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="243a6-270">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="243a6-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="243a6-271">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="243a6-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="243a6-272">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Versión**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="243a6-272">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="243a6-273">Versión de la operación.</span><span class="sxs-lookup"><span data-stu-id="243a6-273">Version of the operation.</span></span>

<span data-ttu-id="243a6-274">La versión de la operación debe estar en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="243a6-274">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="243a6-275"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="243a6-275"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="243a6-276"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="243a6-276"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="243a6-277">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="243a6-277">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="243a6-278">Observaciones</span><span class="sxs-lookup"><span data-stu-id="243a6-278">Remarks</span></span>

<span data-ttu-id="243a6-279">La clase **CIM \_ RemoveDirectoryAction** se deriva de [**\_ DirectoryAction de CIM**](cim-directoryaction.md).</span><span class="sxs-lookup"><span data-stu-id="243a6-279">The **CIM\_RemoveDirectoryAction** class is derived from [**CIM\_DirectoryAction**](cim-directoryaction.md).</span></span>

<span data-ttu-id="243a6-280">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="243a6-280">WMI does not implement this class.</span></span>

<span data-ttu-id="243a6-281">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="243a6-281">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="243a6-282">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="243a6-282">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="243a6-283">Requisitos</span><span class="sxs-lookup"><span data-stu-id="243a6-283">Requirements</span></span>



| <span data-ttu-id="243a6-284">Requisito</span><span class="sxs-lookup"><span data-stu-id="243a6-284">Requirement</span></span> | <span data-ttu-id="243a6-285">Value</span><span class="sxs-lookup"><span data-stu-id="243a6-285">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="243a6-286">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="243a6-286">Minimum supported client</span></span><br/> | <span data-ttu-id="243a6-287">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="243a6-287">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="243a6-288">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="243a6-288">Minimum supported server</span></span><br/> | <span data-ttu-id="243a6-289">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="243a6-289">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="243a6-290">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="243a6-290">Namespace</span></span><br/>                | <span data-ttu-id="243a6-291">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="243a6-291">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="243a6-292">MOF</span><span class="sxs-lookup"><span data-stu-id="243a6-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="243a6-293"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="243a6-293"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="243a6-294">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="243a6-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="243a6-295"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="243a6-295"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="243a6-296">Vea también</span><span class="sxs-lookup"><span data-stu-id="243a6-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="243a6-297">**\_DIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="243a6-297">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> </dl>

 

