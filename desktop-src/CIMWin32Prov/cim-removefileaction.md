---
description: La \_ clase RemoveFileAction de CIM desinstala los archivos.
ms.assetid: 32d5e537-eee2-4f93-9b1f-ecee0d36c99a
ms.tgt_platform: multiple
title: CIM_RemoveFileAction (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoveFileAction
- CIM_RemoveFileAction.ActionID
- CIM_RemoveFileAction.Caption
- CIM_RemoveFileAction.Description
- CIM_RemoveFileAction.Direction
- CIM_RemoveFileAction.Name
- CIM_RemoveFileAction.SoftwareElementID
- CIM_RemoveFileAction.SoftwareElementState
- CIM_RemoveFileAction.TargetOperatingSystem
- CIM_RemoveFileAction.Version
- CIM_RemoveFileAction.File
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c9454f39e5389d61ea23c89e5e1aada7dc860ac9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907036"
---
# <a name="cim_removefileaction-class"></a><span data-ttu-id="6a003-103">\_Clase RemoveFileAction de CIM</span><span class="sxs-lookup"><span data-stu-id="6a003-103">CIM\_RemoveFileAction class</span></span>

<span data-ttu-id="6a003-104">La **clase \_ RemoveFileAction de CIM** desinstala los archivos.</span><span class="sxs-lookup"><span data-stu-id="6a003-104">The **CIM\_RemoveFileAction** class uninstalls files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a003-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="6a003-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6a003-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6a003-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6a003-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6a003-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6a003-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="6a003-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a003-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a003-109">Syntax</span></span>

``` syntax
[UUID("{C75D89F8-DB30-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_RemoveFileAction : CIM_FileAction
{
  string ActionID;
  string Caption;
  string Description;
  uint16 Direction;
  string Name;
  string SoftwareElementID;
  uint16 SoftwareElementState;
  uint16 TargetOperatingSystem;
  string Version;
  string File;
};
```

## <a name="members"></a><span data-ttu-id="6a003-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="6a003-110">Members</span></span>

<span data-ttu-id="6a003-111">La clase **CIM \_ RemoveFileAction** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6a003-111">The **CIM\_RemoveFileAction** class has these types of members:</span></span>

-   [<span data-ttu-id="6a003-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="6a003-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="6a003-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6a003-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6a003-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="6a003-114">Methods</span></span>

<span data-ttu-id="6a003-115">La clase **CIM \_ RemoveFileAction** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6a003-115">The **CIM\_RemoveFileAction** class has these methods.</span></span>



| <span data-ttu-id="6a003-116">Método</span><span class="sxs-lookup"><span data-stu-id="6a003-116">Method</span></span>                                                        | <span data-ttu-id="6a003-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a003-117">Description</span></span>                                                   |
|:--------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="6a003-118">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="6a003-118">**Invoke**</span></span>](invoke-method-in-class-cim-removefileaction.md) | <span data-ttu-id="6a003-119">Toma una acción concreta.</span><span class="sxs-lookup"><span data-stu-id="6a003-119">Takes a particular action.</span></span> <span data-ttu-id="6a003-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="6a003-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6a003-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6a003-121">Properties</span></span>

<span data-ttu-id="6a003-122">La clase **CIM \_ RemoveFileAction** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6a003-122">The **CIM\_RemoveFileAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6a003-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="6a003-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a003-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6a003-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a003-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a003-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a003-126">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6a003-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6a003-127">Identificador único asignado a una acción determinada para un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="6a003-127">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="6a003-128">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="6a003-128">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a003-129">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6a003-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a003-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6a003-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a003-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a003-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a003-132">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6a003-132">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6a003-133">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="6a003-133">Short textual description of the object.</span></span>

<span data-ttu-id="6a003-134">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="6a003-134">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a003-135">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6a003-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a003-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6a003-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a003-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a003-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a003-138">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="6a003-138">Description of the object.</span></span>

<span data-ttu-id="6a003-139">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="6a003-139">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a003-140">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="6a003-140">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a003-141">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a003-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6a003-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a003-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a003-143">Indica si un objeto [**de \_ acción de CIM**](cim-action.md) determinado forma parte de una secuencia de acciones para pasar el elemento de software actual al siguiente estado, como "instalar", o para quitar el elemento de software actual, como "desinstalar".</span><span class="sxs-lookup"><span data-stu-id="6a003-143">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="6a003-144">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="6a003-144">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="6a003-145">**Instalar** (0)</span><span class="sxs-lookup"><span data-stu-id="6a003-145">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="6a003-146">**Desinstalar** (1)</span><span class="sxs-lookup"><span data-stu-id="6a003-146">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6a003-147">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="6a003-147">**File**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a003-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6a003-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a003-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a003-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a003-150">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="6a003-150">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="6a003-151">Nombre del archivo que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="6a003-151">Name of the file to remove.</span></span>

</dd> <dt>

<span data-ttu-id="6a003-152">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="6a003-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a003-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6a003-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a003-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a003-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a003-155">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6a003-155">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6a003-156">Identifica el elemento de software.</span><span class="sxs-lookup"><span data-stu-id="6a003-156">Identifies the software element.</span></span>

<span data-ttu-id="6a003-157">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="6a003-157">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a003-158">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="6a003-158">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a003-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6a003-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a003-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a003-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a003-161">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6a003-161">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6a003-162">Identificador del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="6a003-162">Identifier for the software element.</span></span>

<span data-ttu-id="6a003-163">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="6a003-163">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a003-164">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="6a003-164">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a003-165">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a003-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6a003-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a003-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a003-167">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6a003-167">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6a003-168">Estado de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="6a003-168">State of a software element.</span></span>

<span data-ttu-id="6a003-169">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="6a003-169">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="6a003-170"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>Se pueden **implementar** (0)</span><span class="sxs-lookup"><span data-stu-id="6a003-170"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-171">Describe los detalles necesarios para la distribución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado instalable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="6a003-171">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="6a003-172"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalable** (1)</span><span class="sxs-lookup"><span data-stu-id="6a003-172"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-173">Describe los detalles necesarios para una instalación correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado del archivo ejecutable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="6a003-173">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="6a003-174"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Archivo ejecutable** (2)</span><span class="sxs-lookup"><span data-stu-id="6a003-174"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-175">Describe los detalles necesarios para la ejecución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado de ejecución (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="6a003-175">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="6a003-176"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="6a003-176"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-177">Describe los detalles necesarios para supervisar y operar en un elemento de inicio.</span><span class="sxs-lookup"><span data-stu-id="6a003-177">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6a003-178">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="6a003-178">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a003-179">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a003-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6a003-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a003-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a003-181">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Información del componente de software de DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="6a003-181">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="6a003-182">Sistema operativo de destino del elemento de software propietario.</span><span class="sxs-lookup"><span data-stu-id="6a003-182">Target operating system of the owning software element.</span></span>

<span data-ttu-id="6a003-183">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="6a003-183">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6a003-184"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="6a003-184"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6a003-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="6a003-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="6a003-186"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="6a003-186"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-187">Mac OS</span><span class="sxs-lookup"><span data-stu-id="6a003-187">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="6a003-188"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="6a003-188"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="6a003-189"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="6a003-189"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="6a003-190"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="6a003-190"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="6a003-191"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="6a003-191"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="6a003-192"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="6a003-192"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-193">Abrir máquinas virtuales</span><span class="sxs-lookup"><span data-stu-id="6a003-193">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="6a003-194"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="6a003-194"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-195">HP-UX</span><span class="sxs-lookup"><span data-stu-id="6a003-195">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="6a003-196"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="6a003-196"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="6a003-197"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="6a003-197"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="6a003-198"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="6a003-198"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="6a003-199"><span id="OS_2"></span><span id="os_2"></span>**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="6a003-199"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="6a003-200"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="6a003-200"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-201">Máquina virtual (VM) de Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="6a003-201">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="6a003-202"><span id="MSDOS"></span><span id="msdos"></span>**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="6a003-202"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="6a003-203"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="6a003-203"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-204">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="6a003-204">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="6a003-205"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="6a003-205"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-206">Windows 95</span><span class="sxs-lookup"><span data-stu-id="6a003-206">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="6a003-207"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="6a003-207"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-208">Windows 98</span><span class="sxs-lookup"><span data-stu-id="6a003-208">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="6a003-209"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="6a003-209"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-210">Windows NT</span><span class="sxs-lookup"><span data-stu-id="6a003-210">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="6a003-211"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="6a003-211"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-212">Windows CE</span><span class="sxs-lookup"><span data-stu-id="6a003-212">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="6a003-213"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="6a003-213"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-214">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="6a003-214">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="6a003-215"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="6a003-215"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="6a003-216"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="6a003-216"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="6a003-217"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="6a003-217"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="6a003-218"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="6a003-218"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="6a003-219"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="6a003-219"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="6a003-220"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="6a003-220"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="6a003-221"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="6a003-221"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="6a003-222"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="6a003-222"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="6a003-223"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="6a003-223"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="6a003-224"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="6a003-224"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="6a003-225"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="6a003-225"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="6a003-226"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="6a003-226"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-227">Una serie</span><span class="sxs-lookup"><span data-stu-id="6a003-227">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="6a003-228"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="6a003-228"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-229">Tándem NSK</span><span class="sxs-lookup"><span data-stu-id="6a003-229">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="6a003-230"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="6a003-230"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-231">Tándem</span><span class="sxs-lookup"><span data-stu-id="6a003-231">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="6a003-232"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="6a003-232"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-233">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="6a003-233">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="6a003-234"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="6a003-234"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="6a003-235"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="6a003-235"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="6a003-236"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="6a003-236"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="6a003-237"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="6a003-237"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="6a003-238"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="6a003-238"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="6a003-239"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="6a003-239"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-240">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="6a003-240">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="6a003-241"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="6a003-241"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="6a003-242"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="6a003-242"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="6a003-243"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="6a003-243"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="6a003-244"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="6a003-244"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-245">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="6a003-245">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="6a003-246"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="6a003-246"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="6a003-247"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="6a003-247"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="6a003-248"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="6a003-248"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="6a003-249"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="6a003-249"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="6a003-250"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="6a003-250"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="6a003-251"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="6a003-251"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="6a003-252"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="6a003-252"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="6a003-253"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="6a003-253"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-254">Ser so</span><span class="sxs-lookup"><span data-stu-id="6a003-254">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="6a003-255"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="6a003-255"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="6a003-256"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="6a003-256"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="6a003-257"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="6a003-257"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="6a003-258">Palm OS</span><span class="sxs-lookup"><span data-stu-id="6a003-258">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="6a003-259"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="6a003-259"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="6a003-260"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="6a003-260"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="6a003-261"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="6a003-261"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="6a003-262"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="6a003-262"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="6a003-263"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="6a003-263"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6a003-264">**Versión**</span><span class="sxs-lookup"><span data-stu-id="6a003-264">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a003-265">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6a003-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a003-266">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6a003-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a003-267">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Versión**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="6a003-267">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="6a003-268">Versión de la operación.</span><span class="sxs-lookup"><span data-stu-id="6a003-268">Version of the operation.</span></span>

<span data-ttu-id="6a003-269">La versión de la operación debe estar en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="6a003-269">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="6a003-270"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="6a003-270"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="6a003-271"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="6a003-271"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="6a003-272">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="6a003-272">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a003-273">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a003-273">Remarks</span></span>

<span data-ttu-id="6a003-274">La clase **CIM \_ RemoveFileAction** se deriva de [**\_ FileAction de CIM**](cim-fileaction.md).</span><span class="sxs-lookup"><span data-stu-id="6a003-274">The **CIM\_RemoveFileAction** class is derived from [**CIM\_FileAction**](cim-fileaction.md).</span></span>

<span data-ttu-id="6a003-275">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="6a003-275">WMI does not implement this class.</span></span>

<span data-ttu-id="6a003-276">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="6a003-276">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6a003-277">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="6a003-277">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a003-278">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a003-278">Requirements</span></span>



| <span data-ttu-id="6a003-279">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a003-279">Requirement</span></span> | <span data-ttu-id="6a003-280">Value</span><span class="sxs-lookup"><span data-stu-id="6a003-280">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a003-281">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a003-281">Minimum supported client</span></span><br/> | <span data-ttu-id="6a003-282">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a003-282">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a003-283">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a003-283">Minimum supported server</span></span><br/> | <span data-ttu-id="6a003-284">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a003-284">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a003-285">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6a003-285">Namespace</span></span><br/>                | <span data-ttu-id="6a003-286">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6a003-286">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6a003-287">MOF</span><span class="sxs-lookup"><span data-stu-id="6a003-287">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a003-288"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a003-288"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a003-289">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6a003-289">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a003-290"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a003-290"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a003-291">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a003-291">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a003-292">**\_FILEACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="6a003-292">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> </dl>

 

