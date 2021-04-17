---
description: La \_ clase CIM CopyFileAction representa el traslado o la copia de archivos de un sistema informático a una nueva ubicación.
ms.assetid: c80b5002-d489-4b7e-b9a2-4460c3596958
ms.tgt_platform: multiple
title: CIM_CopyFileAction (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CopyFileAction
- CIM_CopyFileAction.ActionID
- CIM_CopyFileAction.Caption
- CIM_CopyFileAction.Description
- CIM_CopyFileAction.Direction
- CIM_CopyFileAction.Name
- CIM_CopyFileAction.SoftwareElementID
- CIM_CopyFileAction.SoftwareElementState
- CIM_CopyFileAction.TargetOperatingSystem
- CIM_CopyFileAction.Version
- CIM_CopyFileAction.DeleteAfterCopy
- CIM_CopyFileAction.Destination
- CIM_CopyFileAction.Source
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c0303f4696d1baa5129d93cd2e6a7703be611ed9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659609"
---
# <a name="cim_copyfileaction-class"></a><span data-ttu-id="12da2-103">\_Clase CopyFileAction de CIM</span><span class="sxs-lookup"><span data-stu-id="12da2-103">CIM\_CopyFileAction class</span></span>

<span data-ttu-id="12da2-104">La clase **CIM \_ CopyFileAction** representa el traslado o la copia de archivos de un sistema informático a una nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="12da2-104">The **CIM\_CopyFileAction** class represents moving or copying files from a computer system to a new location.</span></span>

<span data-ttu-id="12da2-105">La información de ubicación para copiar se especifica mediante las [**asociaciones \_ CIM ToDirectorySpecification**](cim-todirectoryspecification.md) y [**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) , o las asociaciones CIM [**\_ ToDirectoryAction**](cim-todirectoryaction.md) y [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) .</span><span class="sxs-lookup"><span data-stu-id="12da2-105">Location information for copying is specified by using either the [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) and [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) associations, or the [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) and [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) associations.</span></span> <span data-ttu-id="12da2-106">El primer conjunto se usa cuando el origen o el destino deben existir antes de que se realicen acciones.</span><span class="sxs-lookup"><span data-stu-id="12da2-106">The first set is used when the source or target are to exist before any actions are taken.</span></span> <span data-ttu-id="12da2-107">El segundo conjunto se utiliza cuando el origen o el destino se crean como parte de una acción anterior.</span><span class="sxs-lookup"><span data-stu-id="12da2-107">The second set is used when the source or target are created as a part of a previous action.</span></span> <span data-ttu-id="12da2-108">En el último caso, la acción para crear el directorio debe realizarse antes del objeto **CIM \_ CopyFileAction** .</span><span class="sxs-lookup"><span data-stu-id="12da2-108">In the latter case, the action to create the directory must occur prior to the **CIM\_CopyFileAction** object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12da2-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="12da2-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="12da2-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="12da2-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="12da2-111">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="12da2-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="12da2-112">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="12da2-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="12da2-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12da2-113">Syntax</span></span>

``` syntax
[UUID("{73553260-DB22-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_CopyFileAction : CIM_FileAction
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
  boolean DeleteAfterCopy;
  string  Destination;
  string  Source;
};
```

## <a name="members"></a><span data-ttu-id="12da2-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="12da2-114">Members</span></span>

<span data-ttu-id="12da2-115">La clase **CIM \_ CopyFileAction** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="12da2-115">The **CIM\_CopyFileAction** class has these types of members:</span></span>

-   [<span data-ttu-id="12da2-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="12da2-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="12da2-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="12da2-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="12da2-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="12da2-118">Methods</span></span>

<span data-ttu-id="12da2-119">La clase **CIM \_ CopyFileAction** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="12da2-119">The **CIM\_CopyFileAction** class has these methods.</span></span>



| <span data-ttu-id="12da2-120">Método</span><span class="sxs-lookup"><span data-stu-id="12da2-120">Method</span></span>                                                      | <span data-ttu-id="12da2-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="12da2-121">Description</span></span>                                                                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12da2-122">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="12da2-122">**Invoke**</span></span>](invoke-method-in-class-cim-copyfileaction.md) | <span data-ttu-id="12da2-123">Toma una acción concreta.</span><span class="sxs-lookup"><span data-stu-id="12da2-123">Takes a particular action.</span></span> <span data-ttu-id="12da2-124">Los detalles de cómo realiza la acción el método son específicos de la implementación.</span><span class="sxs-lookup"><span data-stu-id="12da2-124">The details of how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="12da2-125">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="12da2-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="12da2-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="12da2-126">Properties</span></span>

<span data-ttu-id="12da2-127">La clase **CIM \_ CopyFileAction** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="12da2-127">The **CIM\_CopyFileAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12da2-128">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="12da2-128">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12da2-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="12da2-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12da2-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12da2-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12da2-131">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="12da2-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="12da2-132">Identificador único asignado a una acción determinada para un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="12da2-132">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="12da2-133">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="12da2-133">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="12da2-134">**Caption**</span><span class="sxs-lookup"><span data-stu-id="12da2-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12da2-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="12da2-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12da2-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12da2-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12da2-137">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="12da2-137">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="12da2-138">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="12da2-138">Short textual description of the object.</span></span>

<span data-ttu-id="12da2-139">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="12da2-139">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="12da2-140">**DeleteAfterCopy**</span><span class="sxs-lookup"><span data-stu-id="12da2-140">**DeleteAfterCopy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12da2-141">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="12da2-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="12da2-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12da2-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12da2-143">Si es **true**, el archivo de código fuente se elimina después de la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="12da2-143">If **TRUE**, the source file is deleted after the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="12da2-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="12da2-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12da2-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="12da2-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12da2-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12da2-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12da2-147">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="12da2-147">Description of the object.</span></span>

<span data-ttu-id="12da2-148">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="12da2-148">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="12da2-149">**Destino**</span><span class="sxs-lookup"><span data-stu-id="12da2-149">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12da2-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="12da2-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12da2-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12da2-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12da2-152">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="12da2-152">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="12da2-153">Nombre completo del archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="12da2-153">Fully qualified destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="12da2-154">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="12da2-154">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12da2-155">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12da2-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12da2-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12da2-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12da2-157">Indica si un objeto [**de \_ acción de CIM**](cim-action.md) determinado forma parte de una secuencia de acciones para pasar el elemento de software actual al siguiente estado, como "instalar", o para quitar el elemento de software actual, como "desinstalar".</span><span class="sxs-lookup"><span data-stu-id="12da2-157">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="12da2-158">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="12da2-158">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="12da2-159">**Instalar** (0)</span><span class="sxs-lookup"><span data-stu-id="12da2-159">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="12da2-160">**Desinstalar** (1)</span><span class="sxs-lookup"><span data-stu-id="12da2-160">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12da2-161">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="12da2-161">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12da2-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="12da2-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12da2-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12da2-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12da2-164">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="12da2-164">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="12da2-165">Identifica el elemento de software.</span><span class="sxs-lookup"><span data-stu-id="12da2-165">Identifies the software element.</span></span>

<span data-ttu-id="12da2-166">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="12da2-166">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="12da2-167">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="12da2-167">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12da2-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="12da2-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12da2-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12da2-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12da2-170">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="12da2-170">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="12da2-171">Identificador del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="12da2-171">Identifier for the software element.</span></span>

<span data-ttu-id="12da2-172">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="12da2-172">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="12da2-173">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="12da2-173">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12da2-174">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12da2-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12da2-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12da2-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12da2-176">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12da2-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12da2-177">Estado de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="12da2-177">State of a software element.</span></span>

<span data-ttu-id="12da2-178">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="12da2-178">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="12da2-179"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>Se pueden **implementar** (0)</span><span class="sxs-lookup"><span data-stu-id="12da2-179"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-180">Describe los detalles necesarios para la distribución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado instalable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="12da2-180">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="12da2-181"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalable** (1)</span><span class="sxs-lookup"><span data-stu-id="12da2-181"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-182">Describe los detalles necesarios para una instalación correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado del archivo ejecutable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="12da2-182">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="12da2-183"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Archivo ejecutable** (2)</span><span class="sxs-lookup"><span data-stu-id="12da2-183"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-184">Describe los detalles necesarios para la ejecución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado de ejecución (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="12da2-184">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="12da2-185"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="12da2-185"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-186">Describe los detalles necesarios para supervisar y operar en un elemento de inicio.</span><span class="sxs-lookup"><span data-stu-id="12da2-186">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="12da2-187">**Origen**</span><span class="sxs-lookup"><span data-stu-id="12da2-187">**Source**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12da2-188">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="12da2-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12da2-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12da2-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12da2-190">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="12da2-190">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="12da2-191">Nombre completo del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="12da2-191">Fully qualified source file name.</span></span>

</dd> <dt>

<span data-ttu-id="12da2-192">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="12da2-192">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12da2-193">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="12da2-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="12da2-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12da2-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12da2-195">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Información del componente de software de DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="12da2-195">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="12da2-196">Sistema operativo de destino del elemento de software propietario.</span><span class="sxs-lookup"><span data-stu-id="12da2-196">Target operating system of the owning software element.</span></span>

<span data-ttu-id="12da2-197">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="12da2-197">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="12da2-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="12da2-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="12da2-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="12da2-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="12da2-200"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="12da2-200"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-201">Mac OS</span><span class="sxs-lookup"><span data-stu-id="12da2-201">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="12da2-202"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="12da2-202"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="12da2-203"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="12da2-203"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="12da2-204"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="12da2-204"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="12da2-205"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="12da2-205"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="12da2-206"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="12da2-206"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-207">Abrir máquinas virtuales</span><span class="sxs-lookup"><span data-stu-id="12da2-207">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="12da2-208"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="12da2-208"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-209">HP-UX</span><span class="sxs-lookup"><span data-stu-id="12da2-209">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="12da2-210"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="12da2-210"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="12da2-211"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="12da2-211"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="12da2-212"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="12da2-212"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="12da2-213"><span id="OS_2"></span><span id="os_2"></span>**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="12da2-213"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="12da2-214"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="12da2-214"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-215">Máquina virtual (VM) de Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="12da2-215">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="12da2-216"><span id="MSDOS"></span><span id="msdos"></span>**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="12da2-216"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="12da2-217"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="12da2-217"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-218">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="12da2-218">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="12da2-219"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="12da2-219"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-220">Windows 95</span><span class="sxs-lookup"><span data-stu-id="12da2-220">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="12da2-221"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="12da2-221"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-222">Windows 98</span><span class="sxs-lookup"><span data-stu-id="12da2-222">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="12da2-223"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="12da2-223"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-224">Windows NT</span><span class="sxs-lookup"><span data-stu-id="12da2-224">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="12da2-225"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="12da2-225"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-226">Windows CE</span><span class="sxs-lookup"><span data-stu-id="12da2-226">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="12da2-227"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="12da2-227"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-228">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="12da2-228">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="12da2-229"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="12da2-229"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="12da2-230"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="12da2-230"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="12da2-231"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="12da2-231"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="12da2-232"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="12da2-232"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="12da2-233"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="12da2-233"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="12da2-234"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="12da2-234"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="12da2-235"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="12da2-235"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="12da2-236"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="12da2-236"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="12da2-237"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="12da2-237"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="12da2-238"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="12da2-238"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="12da2-239"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="12da2-239"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="12da2-240"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="12da2-240"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-241">Una serie</span><span class="sxs-lookup"><span data-stu-id="12da2-241">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="12da2-242"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="12da2-242"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-243">Tándem NSK</span><span class="sxs-lookup"><span data-stu-id="12da2-243">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="12da2-244"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="12da2-244"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-245">Tándem</span><span class="sxs-lookup"><span data-stu-id="12da2-245">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="12da2-246"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="12da2-246"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-247">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="12da2-247">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="12da2-248"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="12da2-248"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="12da2-249"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="12da2-249"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="12da2-250"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="12da2-250"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="12da2-251"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="12da2-251"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="12da2-252"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="12da2-252"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="12da2-253"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="12da2-253"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-254">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="12da2-254">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="12da2-255"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="12da2-255"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="12da2-256"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="12da2-256"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="12da2-257"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="12da2-257"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="12da2-258"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="12da2-258"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-259">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="12da2-259">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="12da2-260"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="12da2-260"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="12da2-261"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="12da2-261"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="12da2-262"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="12da2-262"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="12da2-263"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="12da2-263"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="12da2-264"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="12da2-264"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="12da2-265"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="12da2-265"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="12da2-266"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="12da2-266"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="12da2-267"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="12da2-267"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-268">Ser so</span><span class="sxs-lookup"><span data-stu-id="12da2-268">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="12da2-269"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="12da2-269"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="12da2-270"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="12da2-270"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="12da2-271"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="12da2-271"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="12da2-272">Palm OS</span><span class="sxs-lookup"><span data-stu-id="12da2-272">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="12da2-273"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="12da2-273"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="12da2-274"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="12da2-274"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="12da2-275"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="12da2-275"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="12da2-276"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="12da2-276"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="12da2-277"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="12da2-277"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="12da2-278">**Versión**</span><span class="sxs-lookup"><span data-stu-id="12da2-278">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12da2-279">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="12da2-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12da2-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12da2-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12da2-281">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Versión**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="12da2-281">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="12da2-282">Versión de la operación.</span><span class="sxs-lookup"><span data-stu-id="12da2-282">Version of the operation.</span></span>

<span data-ttu-id="12da2-283">La versión de la operación debe estar en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="12da2-283">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="12da2-284"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="12da2-284"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="12da2-285"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="12da2-285"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="12da2-286">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="12da2-286">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12da2-287">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12da2-287">Remarks</span></span>

<span data-ttu-id="12da2-288">La clase **CIM \_ CopyFileAction** se deriva de [**\_ FileAction de CIM**](cim-fileaction.md).</span><span class="sxs-lookup"><span data-stu-id="12da2-288">The **CIM\_CopyFileAction** class is derived from [**CIM\_FileAction**](cim-fileaction.md).</span></span>

<span data-ttu-id="12da2-289">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="12da2-289">WMI does not implement this class.</span></span> <span data-ttu-id="12da2-290">Para obtener más información sobre las clases derivadas de **CIM \_ CopyFileAction**, vea [Win32 classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="12da2-290">For more information about classes derived from **CIM\_CopyFileAction**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="12da2-291">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="12da2-291">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="12da2-292">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="12da2-292">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="12da2-293">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12da2-293">Requirements</span></span>



| <span data-ttu-id="12da2-294">Requisito</span><span class="sxs-lookup"><span data-stu-id="12da2-294">Requirement</span></span> | <span data-ttu-id="12da2-295">Value</span><span class="sxs-lookup"><span data-stu-id="12da2-295">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12da2-296">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12da2-296">Minimum supported client</span></span><br/> | <span data-ttu-id="12da2-297">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12da2-297">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12da2-298">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12da2-298">Minimum supported server</span></span><br/> | <span data-ttu-id="12da2-299">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12da2-299">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12da2-300">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="12da2-300">Namespace</span></span><br/>                | <span data-ttu-id="12da2-301">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="12da2-301">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="12da2-302">MOF</span><span class="sxs-lookup"><span data-stu-id="12da2-302">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12da2-303"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12da2-303"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="12da2-304">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="12da2-304">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12da2-305"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12da2-305"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12da2-306">Vea también</span><span class="sxs-lookup"><span data-stu-id="12da2-306">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12da2-307">**\_FILEACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="12da2-307">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> </dl>

 

