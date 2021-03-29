---
description: La \_ clase CIM ModifySettingAction representa la información para modificar un archivo de configuración concreto, para una entrada específica, con un valor específico.
ms.assetid: 6d22bc11-f798-4634-8688-797d4a4a4bee
ms.tgt_platform: multiple
title: CIM_ModifySettingAction (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ModifySettingAction
- CIM_ModifySettingAction.ActionID
- CIM_ModifySettingAction.Caption
- CIM_ModifySettingAction.Description
- CIM_ModifySettingAction.Direction
- CIM_ModifySettingAction.Name
- CIM_ModifySettingAction.SoftwareElementID
- CIM_ModifySettingAction.SoftwareElementState
- CIM_ModifySettingAction.TargetOperatingSystem
- CIM_ModifySettingAction.Version
- CIM_ModifySettingAction.ActionType
- CIM_ModifySettingAction.EntryName
- CIM_ModifySettingAction.EntryValue
- CIM_ModifySettingAction.FileName
- CIM_ModifySettingAction.SectionKey
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 450e73eaa6f405e47d79cbf3840932e0f106a4b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807669"
---
# <a name="cim_modifysettingaction-class"></a><span data-ttu-id="2e941-103">\_Clase ModifySettingAction de CIM</span><span class="sxs-lookup"><span data-stu-id="2e941-103">CIM\_ModifySettingAction class</span></span>

<span data-ttu-id="2e941-104">La clase **CIM \_ ModifySettingAction** representa la información para modificar un archivo de configuración concreto, para una entrada específica, con un valor específico.</span><span class="sxs-lookup"><span data-stu-id="2e941-104">The **CIM\_ModifySettingAction** class represents the information for modifying a specific setting file, for a specific entry, with a specific value.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e941-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="2e941-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2e941-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2e941-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2e941-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2e941-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2e941-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2e941-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e941-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e941-109">Syntax</span></span>

``` syntax
[UUID("{ECDE0B90-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ModifySettingAction : CIM_Action
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
  uint16 ActionType;
  string EntryName;
  string EntryValue;
  string FileName;
  string SectionKey;
};
```

## <a name="members"></a><span data-ttu-id="2e941-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="2e941-110">Members</span></span>

<span data-ttu-id="2e941-111">La clase **CIM \_ ModifySettingAction** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2e941-111">The **CIM\_ModifySettingAction** class has these types of members:</span></span>

-   [<span data-ttu-id="2e941-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e941-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2e941-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2e941-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2e941-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e941-114">Methods</span></span>

<span data-ttu-id="2e941-115">La clase **CIM \_ ModifySettingAction** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2e941-115">The **CIM\_ModifySettingAction** class has these methods.</span></span>



| <span data-ttu-id="2e941-116">Método</span><span class="sxs-lookup"><span data-stu-id="2e941-116">Method</span></span>                                                           | <span data-ttu-id="2e941-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e941-117">Description</span></span>                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="2e941-118">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="2e941-118">**Invoke**</span></span>](invoke-method-in-class-cim-modifysettingaction.md) | <span data-ttu-id="2e941-119">Toma una acción específica.</span><span class="sxs-lookup"><span data-stu-id="2e941-119">Takes a specific action.</span></span> <span data-ttu-id="2e941-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2e941-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2e941-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2e941-121">Properties</span></span>

<span data-ttu-id="2e941-122">La clase **CIM \_ ModifySettingAction** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2e941-122">The **CIM\_ModifySettingAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e941-123">**ActionID**</span><span class="sxs-lookup"><span data-stu-id="2e941-123">**ActionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e941-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e941-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e941-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e941-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e941-126">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2e941-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2e941-127">Identificador único asignado a una acción determinada para un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="2e941-127">Unique identifier assigned to a particular action for a software element.</span></span>

<span data-ttu-id="2e941-128">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="2e941-128">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e941-129">**ActionType**</span><span class="sxs-lookup"><span data-stu-id="2e941-129">**ActionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e941-130">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e941-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e941-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e941-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e941-132">Tipo de acción que se va a realizar en la entrada de configuración especificada.</span><span class="sxs-lookup"><span data-stu-id="2e941-132">Type of action to perform on the specified setting entry.</span></span> <span data-ttu-id="2e941-133">Se supone que las adiciones distinguen mayúsculas de minúsculas; sin embargo, se supone que las eliminaciones no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2e941-133">Additions are assumed to be case sensitive; however, removals are assumed to be case insensitive.</span></span>

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="2e941-134"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>**Crear** (0)</span><span class="sxs-lookup"><span data-stu-id="2e941-134"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>**Create** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-135">Crea la entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="2e941-135">Creates the specified entry.</span></span>

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

<span data-ttu-id="2e941-136"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Eliminar** (1)</span><span class="sxs-lookup"><span data-stu-id="2e941-136"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Delete** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-137">Elimina la entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="2e941-137">Deletes the specified entry.</span></span>

</dd> <dt>

<span id="Append"></span><span id="append"></span><span id="APPEND"></span>

<span data-ttu-id="2e941-138"><span id="Append"></span><span id="append"></span><span id="APPEND"></span>**Append** (2)</span><span class="sxs-lookup"><span data-stu-id="2e941-138"><span id="Append"></span><span id="append"></span><span id="APPEND"></span>**Append** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-139">Anexa al final de la entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="2e941-139">Appends to the end of the specified entry.</span></span>

</dd> <dt>

<span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>

<span data-ttu-id="2e941-140"><span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>**Quitar** (3)</span><span class="sxs-lookup"><span data-stu-id="2e941-140"><span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>**Remove** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-141">Quita el valor de la entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="2e941-141">Removes the value from the specified entry.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e941-142">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2e941-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e941-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e941-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e941-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e941-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e941-145">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2e941-145">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2e941-146">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2e941-146">Short textual description of the object.</span></span>

<span data-ttu-id="2e941-147">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="2e941-147">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e941-148">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e941-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e941-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e941-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e941-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e941-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e941-151">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="2e941-151">Description of the object.</span></span>

<span data-ttu-id="2e941-152">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="2e941-152">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e941-153">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="2e941-153">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e941-154">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e941-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e941-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e941-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e941-156">Indica si un objeto [**de \_ acción de CIM**](cim-action.md) determinado forma parte de una secuencia de acciones para pasar el elemento de software actual al siguiente estado, como "instalar", o para quitar el elemento de software actual, como "desinstalar".</span><span class="sxs-lookup"><span data-stu-id="2e941-156">Indicates whether a particular [**CIM\_Action**](cim-action.md) object is part of a sequence of actions to transition the current software element to its next state, such as "Install", or to remove the current software element, such as "Uninstall".</span></span>

<span data-ttu-id="2e941-157">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="2e941-157">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Install"></span><span id="install"></span><span id="INSTALL"></span>

<span data-ttu-id="2e941-158">**Instalar** (0)</span><span class="sxs-lookup"><span data-stu-id="2e941-158">**Install** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Uninstall"></span><span id="uninstall"></span><span id="UNINSTALL"></span>

<span data-ttu-id="2e941-159">**Desinstalar** (1)</span><span class="sxs-lookup"><span data-stu-id="2e941-159">**Uninstall** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2e941-160">**EntryName**</span><span class="sxs-lookup"><span data-stu-id="2e941-160">**EntryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e941-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e941-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e941-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e941-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e941-163">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2e941-163">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2e941-164">Nombre de la entrada que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="2e941-164">Name of the entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="2e941-165">**EntryValue**</span><span class="sxs-lookup"><span data-stu-id="2e941-165">**EntryValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e941-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e941-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e941-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e941-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e941-168">Valor que se va a agregar, anexar o para reemplazar la configuración especificada.</span><span class="sxs-lookup"><span data-stu-id="2e941-168">Value to add, append, or to replace the specified setting.</span></span>

</dd> <dt>

<span data-ttu-id="2e941-169">**FileName**</span><span class="sxs-lookup"><span data-stu-id="2e941-169">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e941-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e941-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e941-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e941-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e941-172">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="2e941-172">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="2e941-173">Nombre de archivo de la entrada del archivo de configuración que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="2e941-173">File name of the setting file entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="2e941-174">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="2e941-174">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e941-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e941-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e941-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e941-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e941-177">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2e941-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2e941-178">Identifica el elemento de software.</span><span class="sxs-lookup"><span data-stu-id="2e941-178">Identifies the software element.</span></span>

<span data-ttu-id="2e941-179">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="2e941-179">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e941-180">**SectionKey**</span><span class="sxs-lookup"><span data-stu-id="2e941-180">**SectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e941-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e941-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e941-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e941-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e941-183">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2e941-183">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2e941-184">Clave de la sección de la entrada de configuración que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="2e941-184">Section key of the setting entry to modify.</span></span>

</dd> <dt>

<span data-ttu-id="2e941-185">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="2e941-185">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e941-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e941-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e941-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e941-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e941-188">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2e941-188">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2e941-189">Identificador del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="2e941-189">Identifier for the software element.</span></span>

<span data-ttu-id="2e941-190">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="2e941-190">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e941-191">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="2e941-191">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e941-192">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e941-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e941-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e941-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e941-194">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2e941-194">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2e941-195">Estado de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="2e941-195">State of a software element.</span></span>

<span data-ttu-id="2e941-196">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="2e941-196">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="2e941-197"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>Se pueden **implementar** (0)</span><span class="sxs-lookup"><span data-stu-id="2e941-197"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-198">Describe los detalles necesarios para la distribución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado instalable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="2e941-198">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="2e941-199"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalable** (1)</span><span class="sxs-lookup"><span data-stu-id="2e941-199"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-200">Describe los detalles necesarios para una instalación correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado del archivo ejecutable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="2e941-200">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="2e941-201"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Archivo ejecutable** (2)</span><span class="sxs-lookup"><span data-stu-id="2e941-201"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-202">Describe los detalles necesarios para la ejecución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado de ejecución (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="2e941-202">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="2e941-203"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="2e941-203"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-204">Describe los detalles necesarios para supervisar y operar en un elemento de inicio.</span><span class="sxs-lookup"><span data-stu-id="2e941-204">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e941-205">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="2e941-205">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e941-206">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e941-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e941-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e941-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e941-208">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Información del componente de software de DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="2e941-208">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="2e941-209">Sistema operativo de destino del elemento de software propietario.</span><span class="sxs-lookup"><span data-stu-id="2e941-209">Target operating system of the owning software element.</span></span>

<span data-ttu-id="2e941-210">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="2e941-210">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e941-211"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2e941-211"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2e941-212"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2e941-212"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="2e941-213"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="2e941-213"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-214">Mac OS</span><span class="sxs-lookup"><span data-stu-id="2e941-214">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="2e941-215"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="2e941-215"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="2e941-216"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="2e941-216"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="2e941-217"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="2e941-217"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="2e941-218"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="2e941-218"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="2e941-219"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="2e941-219"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-220">Abrir máquinas virtuales</span><span class="sxs-lookup"><span data-stu-id="2e941-220">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="2e941-221"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="2e941-221"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-222">HP-UX</span><span class="sxs-lookup"><span data-stu-id="2e941-222">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="2e941-223"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="2e941-223"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="2e941-224"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="2e941-224"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="2e941-225"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="2e941-225"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="2e941-226"><span id="OS_2"></span><span id="os_2"></span>**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="2e941-226"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="2e941-227"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="2e941-227"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-228">Máquina virtual (VM) de Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="2e941-228">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="2e941-229"><span id="MSDOS"></span><span id="msdos"></span>**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="2e941-229"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="2e941-230"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="2e941-230"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-231">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="2e941-231">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="2e941-232"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="2e941-232"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-233">Windows 95</span><span class="sxs-lookup"><span data-stu-id="2e941-233">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="2e941-234"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="2e941-234"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-235">Windows 98</span><span class="sxs-lookup"><span data-stu-id="2e941-235">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="2e941-236"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="2e941-236"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-237">Windows NT</span><span class="sxs-lookup"><span data-stu-id="2e941-237">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="2e941-238"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="2e941-238"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-239">Windows CE</span><span class="sxs-lookup"><span data-stu-id="2e941-239">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="2e941-240"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="2e941-240"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-241">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="2e941-241">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="2e941-242"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="2e941-242"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="2e941-243"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="2e941-243"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="2e941-244"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="2e941-244"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="2e941-245"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="2e941-245"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="2e941-246"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="2e941-246"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="2e941-247"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="2e941-247"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="2e941-248"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="2e941-248"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="2e941-249"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="2e941-249"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="2e941-250"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="2e941-250"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="2e941-251"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="2e941-251"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="2e941-252"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="2e941-252"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="2e941-253"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="2e941-253"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-254">Una serie</span><span class="sxs-lookup"><span data-stu-id="2e941-254">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="2e941-255"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="2e941-255"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-256">Tándem NSK</span><span class="sxs-lookup"><span data-stu-id="2e941-256">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="2e941-257"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="2e941-257"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-258">Tándem</span><span class="sxs-lookup"><span data-stu-id="2e941-258">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="2e941-259"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="2e941-259"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-260">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="2e941-260">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="2e941-261"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="2e941-261"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="2e941-262"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="2e941-262"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="2e941-263"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="2e941-263"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="2e941-264"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="2e941-264"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="2e941-265"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="2e941-265"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="2e941-266"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="2e941-266"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-267">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="2e941-267">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="2e941-268"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="2e941-268"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="2e941-269"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="2e941-269"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="2e941-270"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="2e941-270"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="2e941-271"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="2e941-271"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-272">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="2e941-272">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="2e941-273"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="2e941-273"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="2e941-274"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="2e941-274"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="2e941-275"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="2e941-275"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="2e941-276"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="2e941-276"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="2e941-277"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="2e941-277"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="2e941-278"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="2e941-278"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="2e941-279"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="2e941-279"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="2e941-280"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="2e941-280"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-281">Ser so</span><span class="sxs-lookup"><span data-stu-id="2e941-281">Be OS</span></span>

</dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="2e941-282"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="2e941-282"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="2e941-283"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="2e941-283"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="2e941-284"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="2e941-284"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="2e941-285">Palm OS</span><span class="sxs-lookup"><span data-stu-id="2e941-285">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="2e941-286"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="2e941-286"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="2e941-287"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="2e941-287"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="2e941-288"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="2e941-288"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="2e941-289"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="2e941-289"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="2e941-290"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="2e941-290"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2e941-291">**Versión**</span><span class="sxs-lookup"><span data-stu-id="2e941-291">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e941-292">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e941-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e941-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e941-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e941-294">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Versión**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="2e941-294">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="2e941-295">Versión de la operación.</span><span class="sxs-lookup"><span data-stu-id="2e941-295">Version of the operation.</span></span>

<span data-ttu-id="2e941-296">La versión de la operación debe estar en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="2e941-296">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="2e941-297"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="2e941-297"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="2e941-298"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="2e941-298"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="2e941-299">Esta propiedad se hereda de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="2e941-299">This property is inherited from [**CIM\_Action**](cim-action.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e941-300">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e941-300">Remarks</span></span>

<span data-ttu-id="2e941-301">La clase **CIM \_ ModifySettingAction** se deriva de [**la \_ acción CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="2e941-301">The **CIM\_ModifySettingAction** class is derived from [**CIM\_Action**](cim-action.md).</span></span>

<span data-ttu-id="2e941-302">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="2e941-302">WMI does not implement this class.</span></span>

<span data-ttu-id="2e941-303">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="2e941-303">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2e941-304">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="2e941-304">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e941-305">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e941-305">Requirements</span></span>



| <span data-ttu-id="2e941-306">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e941-306">Requirement</span></span> | <span data-ttu-id="2e941-307">Value</span><span class="sxs-lookup"><span data-stu-id="2e941-307">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e941-308">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e941-308">Minimum supported client</span></span><br/> | <span data-ttu-id="2e941-309">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e941-309">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e941-310">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e941-310">Minimum supported server</span></span><br/> | <span data-ttu-id="2e941-311">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e941-311">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e941-312">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2e941-312">Namespace</span></span><br/>                | <span data-ttu-id="2e941-313">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2e941-313">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2e941-314">MOF</span><span class="sxs-lookup"><span data-stu-id="2e941-314">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e941-315"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e941-315"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e941-316">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e941-316">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e941-317"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e941-317"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e941-318">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e941-318">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e941-319">**Acción de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2e941-319">**CIM\_Action**</span></span>](cim-action.md)
</dt> </dl>

 

