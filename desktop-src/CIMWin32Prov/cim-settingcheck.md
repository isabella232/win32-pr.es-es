---
description: La \_ clase CIM SettingCheck especifica la información necesaria para comprobar un archivo de configuración determinado para una entrada específica que contiene un valor igual al valor especificado. Se supone que todas las comparaciones no distinguen mayúsculas de minúsculas.
ms.assetid: 0e40276c-e794-4ea1-8937-c6d7f110f97d
ms.tgt_platform: multiple
title: CIM_SettingCheck (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingCheck
- CIM_SettingCheck.Caption
- CIM_SettingCheck.CheckID
- CIM_SettingCheck.CheckMode
- CIM_SettingCheck.CheckType
- CIM_SettingCheck.Description
- CIM_SettingCheck.EntryName
- CIM_SettingCheck.EntryValue
- CIM_SettingCheck.FileName
- CIM_SettingCheck.Name
- CIM_SettingCheck.SectionKey
- CIM_SettingCheck.SoftwareElementID
- CIM_SettingCheck.SoftwareElementState
- CIM_SettingCheck.TargetOperatingSystem
- CIM_SettingCheck.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4b360833f216d9feb839a4ed84a0e1ba4cd61ebf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659508"
---
# <a name="cim_settingcheck-class"></a><span data-ttu-id="ef989-104">\_Clase SettingCheck de CIM</span><span class="sxs-lookup"><span data-stu-id="ef989-104">CIM\_SettingCheck class</span></span>

<span data-ttu-id="ef989-105">La clase **CIM \_ SettingCheck** especifica la información necesaria para comprobar un archivo de configuración determinado para una entrada específica que contiene un valor igual al valor especificado.</span><span class="sxs-lookup"><span data-stu-id="ef989-105">The **CIM\_SettingCheck** class specifies information needed to check a particular setting file for a specific entry that contains a value equal to the value specified.</span></span> <span data-ttu-id="ef989-106">Se supone que todas las comparaciones no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ef989-106">All comparisons are assumed to be case insensitive.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ef989-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="ef989-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ef989-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ef989-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ef989-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ef989-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ef989-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="ef989-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef989-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef989-111">Syntax</span></span>

``` syntax
[UUID("{DC1D8140-DB30-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SettingCheck : CIM_Check
{
  string  Caption;
  string  CheckID;
  boolean CheckMode;
  uint16  CheckType;
  string  Description;
  string  EntryName;
  string  EntryValue;
  string  FileName;
  string  Name;
  string  SectionKey;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  uint16  TargetOperatingSystem;
  string  Version;
};
```

## <a name="members"></a><span data-ttu-id="ef989-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="ef989-112">Members</span></span>

<span data-ttu-id="ef989-113">La clase **CIM \_ SettingCheck** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ef989-113">The **CIM\_SettingCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="ef989-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="ef989-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="ef989-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ef989-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ef989-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="ef989-116">Methods</span></span>

<span data-ttu-id="ef989-117">La clase **CIM \_ SettingCheck** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ef989-117">The **CIM\_SettingCheck** class has these methods.</span></span>



| <span data-ttu-id="ef989-118">Método</span><span class="sxs-lookup"><span data-stu-id="ef989-118">Method</span></span>                                                    | <span data-ttu-id="ef989-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef989-119">Description</span></span>                                                   |
|:----------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="ef989-120">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="ef989-120">**Invoke**</span></span>](invoke-method-in-class-cim-settingcheck.md) | <span data-ttu-id="ef989-121">Toma una acción concreta.</span><span class="sxs-lookup"><span data-stu-id="ef989-121">Takes a particular action.</span></span> <span data-ttu-id="ef989-122">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="ef989-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ef989-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ef989-123">Properties</span></span>

<span data-ttu-id="ef989-124">La clase **CIM \_ SettingCheck** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ef989-124">The **CIM\_SettingCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef989-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ef989-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef989-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef989-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef989-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef989-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef989-128">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ef989-128">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ef989-129">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="ef989-129">Short textual description of the object.</span></span>

<span data-ttu-id="ef989-130">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="ef989-130">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef989-131">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="ef989-131">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef989-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef989-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef989-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef989-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef989-134">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ef989-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ef989-135">Identificador que se usa junto con otras claves para identificar de forma única la comprobación.</span><span class="sxs-lookup"><span data-stu-id="ef989-135">Identifier used in conjunction with other keys to uniquely identify the check.</span></span> <span data-ttu-id="ef989-136">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="ef989-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef989-137">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="ef989-137">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef989-138">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ef989-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef989-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef989-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef989-140">Si es **true**, se espera que la condición exista en el entorno (por ejemplo, si un archivo está en un sistema, el método [**Invoke**](invoke-method-in-class-cim-settingcheck.md) debe devolver **true**).</span><span class="sxs-lookup"><span data-stu-id="ef989-140">If **TRUE**, the condition is expected to exist in the environment (for example, if a file is on a system, the [**Invoke**](invoke-method-in-class-cim-settingcheck.md) method should return **TRUE**).</span></span> <span data-ttu-id="ef989-141">Si es **false**, la condición no debe existir (por ejemplo, si un archivo no se encuentra en un sistema, el método **Invoke** debe devolver **false**).</span><span class="sxs-lookup"><span data-stu-id="ef989-141">If **FALSE**, the condition should not exist (for example, if a file is not on a system, the **Invoke** method should return **FALSE**).</span></span>

<span data-ttu-id="ef989-142">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="ef989-142">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef989-143">**CheckType**</span><span class="sxs-lookup"><span data-stu-id="ef989-143">**CheckType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef989-144">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef989-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef989-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef989-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef989-146">Modo en el que se debe comparar el valor de configuración.</span><span class="sxs-lookup"><span data-stu-id="ef989-146">Way in which the setting value should be compared.</span></span>

<dt>

<span id="Matches"></span><span id="matches"></span><span id="MATCHES"></span>

<span data-ttu-id="ef989-147">**Coincide con** (0)</span><span class="sxs-lookup"><span data-stu-id="ef989-147">**Matches** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Contains"></span><span id="contains"></span><span id="CONTAINS"></span>

<span data-ttu-id="ef989-148">**Contains** (1)</span><span class="sxs-lookup"><span data-stu-id="ef989-148">**Contains** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef989-149">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ef989-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef989-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef989-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef989-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef989-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef989-152">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ef989-152">Description of the object.</span></span>

<span data-ttu-id="ef989-153">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="ef989-153">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef989-154">**EntryName**</span><span class="sxs-lookup"><span data-stu-id="ef989-154">**EntryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef989-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef989-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef989-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef989-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef989-157">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ef989-157">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ef989-158">Nombre de la entrada que se va a comprobar</span><span class="sxs-lookup"><span data-stu-id="ef989-158">Name of the entry to be checked</span></span>

</dd> <dt>

<span data-ttu-id="ef989-159">**EntryValue**</span><span class="sxs-lookup"><span data-stu-id="ef989-159">**EntryValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef989-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef989-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef989-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef989-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef989-162">Valor asociado a la entrada con nombre que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="ef989-162">Value that is associated with the named entry to check.</span></span>

</dd> <dt>

<span data-ttu-id="ef989-163">**FileName**</span><span class="sxs-lookup"><span data-stu-id="ef989-163">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef989-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef989-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef989-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef989-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef989-166">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="ef989-166">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="ef989-167">Nombre del archivo de configuración que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="ef989-167">File name of the setting file to check.</span></span>

</dd> <dt>

<span data-ttu-id="ef989-168">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="ef989-168">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef989-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef989-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef989-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef989-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef989-171">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ef989-171">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ef989-172">Nombre usado para identificar el elemento de software.</span><span class="sxs-lookup"><span data-stu-id="ef989-172">Name used to identify the software element.</span></span> <span data-ttu-id="ef989-173">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="ef989-173">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef989-174">**SectionKey**</span><span class="sxs-lookup"><span data-stu-id="ef989-174">**SectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef989-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef989-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef989-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef989-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef989-177">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ef989-177">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ef989-178">Clave de la sección que contiene la configuración que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="ef989-178">Key of section that contains the settings to check.</span></span>

</dd> <dt>

<span data-ttu-id="ef989-179">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="ef989-179">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef989-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef989-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef989-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef989-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef989-182">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ef989-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ef989-183">Identificador del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="ef989-183">Identifier for the software element.</span></span>

<span data-ttu-id="ef989-184">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="ef989-184">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef989-185">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="ef989-185">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef989-186">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef989-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef989-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef989-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef989-188">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ef989-188">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ef989-189">Estado de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="ef989-189">State of a software element.</span></span>

<span data-ttu-id="ef989-190">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="ef989-190">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="ef989-191"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>Se pueden **implementar** (0)</span><span class="sxs-lookup"><span data-stu-id="ef989-191"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-192">Describe los detalles necesarios para la distribución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado instalable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="ef989-192">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="ef989-193"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalable** (1)</span><span class="sxs-lookup"><span data-stu-id="ef989-193"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-194">Describe los detalles necesarios para una instalación correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado del archivo ejecutable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="ef989-194">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="ef989-195"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Archivo ejecutable** (2)</span><span class="sxs-lookup"><span data-stu-id="ef989-195"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-196">Describe los detalles necesarios para la ejecución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado de ejecución (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="ef989-196">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="ef989-197"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="ef989-197"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-198">Describe los detalles necesarios para supervisar y operar en un elemento de inicio.</span><span class="sxs-lookup"><span data-stu-id="ef989-198">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ef989-199">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="ef989-199">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef989-200">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef989-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef989-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef989-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef989-202">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Información del componente de software de DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="ef989-202">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="ef989-203">Sistema operativo de destino del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="ef989-203">Target operating system of the software element.</span></span>

<span data-ttu-id="ef989-204">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="ef989-204">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef989-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="ef989-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ef989-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="ef989-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="ef989-207"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="ef989-207"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-208">Mac OS</span><span class="sxs-lookup"><span data-stu-id="ef989-208">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="ef989-209"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="ef989-209"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-210">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="ef989-210">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="ef989-211"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="ef989-211"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="ef989-212"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="ef989-212"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="ef989-213"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="ef989-213"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="ef989-214"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="ef989-214"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-215">Abrir máquinas virtuales</span><span class="sxs-lookup"><span data-stu-id="ef989-215">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="ef989-216"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="ef989-216"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-217">HP-UX</span><span class="sxs-lookup"><span data-stu-id="ef989-217">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="ef989-218"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="ef989-218"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="ef989-219"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="ef989-219"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="ef989-220"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="ef989-220"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="ef989-221"><span id="OS_2"></span><span id="os_2"></span>**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="ef989-221"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="ef989-222"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="ef989-222"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-223">Máquina virtual (VM) de Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="ef989-223">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="ef989-224"><span id="MSDOS"></span><span id="msdos"></span>**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="ef989-224"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="ef989-225"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="ef989-225"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-226">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="ef989-226">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="ef989-227"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="ef989-227"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-228">Windows 95</span><span class="sxs-lookup"><span data-stu-id="ef989-228">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="ef989-229"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="ef989-229"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-230">Windows 98</span><span class="sxs-lookup"><span data-stu-id="ef989-230">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="ef989-231"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="ef989-231"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-232">Windows NT</span><span class="sxs-lookup"><span data-stu-id="ef989-232">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="ef989-233"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="ef989-233"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-234">Windows CE</span><span class="sxs-lookup"><span data-stu-id="ef989-234">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="ef989-235"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="ef989-235"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-236">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="ef989-236">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="ef989-237"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="ef989-237"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="ef989-238"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="ef989-238"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="ef989-239"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="ef989-239"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="ef989-240"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="ef989-240"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="ef989-241"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="ef989-241"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="ef989-242"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="ef989-242"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="ef989-243"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="ef989-243"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="ef989-244"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="ef989-244"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="ef989-245"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="ef989-245"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="ef989-246"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="ef989-246"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="ef989-247"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="ef989-247"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="ef989-248"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="ef989-248"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-249">Una serie</span><span class="sxs-lookup"><span data-stu-id="ef989-249">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="ef989-250"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="ef989-250"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-251">Tándem NSK</span><span class="sxs-lookup"><span data-stu-id="ef989-251">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="ef989-252"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="ef989-252"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-253">Tándem</span><span class="sxs-lookup"><span data-stu-id="ef989-253">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="ef989-254"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="ef989-254"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-255">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="ef989-255">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="ef989-256"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="ef989-256"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="ef989-257"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="ef989-257"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="ef989-258"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="ef989-258"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="ef989-259"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="ef989-259"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="ef989-260"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="ef989-260"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="ef989-261"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="ef989-261"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-262">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="ef989-262">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="ef989-263"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="ef989-263"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="ef989-264"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="ef989-264"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="ef989-265"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="ef989-265"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="ef989-266"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="ef989-266"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-267">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="ef989-267">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="ef989-268"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="ef989-268"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="ef989-269"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="ef989-269"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="ef989-270"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="ef989-270"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="ef989-271"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="ef989-271"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="ef989-272"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="ef989-272"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="ef989-273"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="ef989-273"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="ef989-274"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="ef989-274"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="ef989-275"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="ef989-275"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="ef989-276"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="ef989-276"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="ef989-277"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="ef989-277"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="ef989-278"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="ef989-278"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="ef989-279">Palm OS</span><span class="sxs-lookup"><span data-stu-id="ef989-279">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="ef989-280"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="ef989-280"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="ef989-281"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="ef989-281"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="ef989-282"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="ef989-282"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="ef989-283"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="ef989-283"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="ef989-284"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="ef989-284"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef989-285">**Versión**</span><span class="sxs-lookup"><span data-stu-id="ef989-285">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef989-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ef989-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef989-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ef989-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef989-288">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Versión**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="ef989-288">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="ef989-289">Versión de la operación.</span><span class="sxs-lookup"><span data-stu-id="ef989-289">Version of the operation.</span></span>

<span data-ttu-id="ef989-290">La versión de la operación debe estar en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="ef989-290">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="ef989-291"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="ef989-291"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="ef989-292"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="ef989-292"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="ef989-293">Esta propiedad se hereda de la clase de [**\_ comprobación CIM**](cim-check.md) .</span><span class="sxs-lookup"><span data-stu-id="ef989-293">This property is inherited from the [**CIM\_Check**](cim-check.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef989-294">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef989-294">Remarks</span></span>

<span data-ttu-id="ef989-295">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="ef989-295">WMI does not implement this class.</span></span>

<span data-ttu-id="ef989-296">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="ef989-296">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ef989-297">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="ef989-297">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef989-298">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef989-298">Requirements</span></span>



| <span data-ttu-id="ef989-299">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef989-299">Requirement</span></span> | <span data-ttu-id="ef989-300">Value</span><span class="sxs-lookup"><span data-stu-id="ef989-300">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef989-301">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef989-301">Minimum supported client</span></span><br/> | <span data-ttu-id="ef989-302">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef989-302">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef989-303">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef989-303">Minimum supported server</span></span><br/> | <span data-ttu-id="ef989-304">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef989-304">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef989-305">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ef989-305">Namespace</span></span><br/>                | <span data-ttu-id="ef989-306">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ef989-306">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ef989-307">MOF</span><span class="sxs-lookup"><span data-stu-id="ef989-307">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef989-308"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef989-308"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef989-309">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef989-309">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef989-310"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef989-310"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef989-311">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef989-311">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef989-312">**Comprobación de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ef989-312">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

