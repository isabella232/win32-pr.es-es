---
description: La \_ clase CIM VersionCompatibilityCheck especifica si se permite crear el siguiente estado de un elemento de software.
ms.assetid: 3a04c489-e44e-44c7-8945-d6047ba0d6df
ms.tgt_platform: multiple
title: CIM_VersionCompatibilityCheck (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VersionCompatibilityCheck
- CIM_VersionCompatibilityCheck.CheckID
- CIM_VersionCompatibilityCheck.Caption
- CIM_VersionCompatibilityCheck.Description
- CIM_VersionCompatibilityCheck.CheckMode
- CIM_VersionCompatibilityCheck.Name
- CIM_VersionCompatibilityCheck.TargetOperatingSystem
- CIM_VersionCompatibilityCheck.Version
- CIM_VersionCompatibilityCheck.SoftwareElementID
- CIM_VersionCompatibilityCheck.SoftwareElementState
- CIM_VersionCompatibilityCheck.AllowDownVersion
- CIM_VersionCompatibilityCheck.AllowMultipleVersions
- CIM_VersionCompatibilityCheck.Reinstall
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 00a37d52add8c9697371fd0ee8d0a24d9c487f61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000553"
---
# <a name="cim_versioncompatibilitycheck-class"></a><span data-ttu-id="86198-103">\_Clase VersionCompatibilityCheck de CIM</span><span class="sxs-lookup"><span data-stu-id="86198-103">CIM\_VersionCompatibilityCheck class</span></span>

<span data-ttu-id="86198-104">La clase **CIM \_ VersionCompatibilityCheck** especifica si se permite crear el siguiente estado de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="86198-104">The **CIM\_VersionCompatibilityCheck** class specifies whether it is permissible to create the next state of a software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="86198-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="86198-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="86198-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="86198-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="86198-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="86198-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="86198-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="86198-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="86198-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86198-109">Syntax</span></span>

``` syntax
[UUID("{D368CA4A-DB31-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VersionCompatibilityCheck : CIM_Check
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
  boolean AllowDownVersion;
  boolean AllowMultipleVersions;
  boolean Reinstall;
};
```

## <a name="members"></a><span data-ttu-id="86198-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="86198-110">Members</span></span>

<span data-ttu-id="86198-111">La clase **CIM \_ VersionCompatibilityCheck** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="86198-111">The **CIM\_VersionCompatibilityCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="86198-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="86198-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="86198-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="86198-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="86198-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="86198-114">Methods</span></span>

<span data-ttu-id="86198-115">La clase **CIM \_ VersionCompatibilityCheck** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="86198-115">The **CIM\_VersionCompatibilityCheck** class has these methods.</span></span>



| <span data-ttu-id="86198-116">Método</span><span class="sxs-lookup"><span data-stu-id="86198-116">Method</span></span>                                                                 | <span data-ttu-id="86198-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="86198-117">Description</span></span>                                                   |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="86198-118">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="86198-118">**Invoke**</span></span>](invoke-method-in-class-cim-versioncompatibilitycheck.md) | <span data-ttu-id="86198-119">Toma una acción concreta.</span><span class="sxs-lookup"><span data-stu-id="86198-119">Takes a particular action.</span></span> <span data-ttu-id="86198-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="86198-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="86198-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="86198-121">Properties</span></span>

<span data-ttu-id="86198-122">La clase **CIM \_ VersionCompatibilityCheck** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="86198-122">The **CIM\_VersionCompatibilityCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="86198-123">**AllowDownVersion**</span><span class="sxs-lookup"><span data-stu-id="86198-123">**AllowDownVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86198-124">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="86198-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86198-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86198-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86198-126">Si **es true**, el elemento de software puede pasar a su siguiente estado si ya existe una versión superior o posterior del elemento de software en el entorno.</span><span class="sxs-lookup"><span data-stu-id="86198-126">If **TRUE**, the software element can transition to its next state whether or not if a higher or latter version of the software element already exists in the environment.</span></span>

</dd> <dt>

<span data-ttu-id="86198-127">**AllowMultipleVersions**</span><span class="sxs-lookup"><span data-stu-id="86198-127">**AllowMultipleVersions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86198-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="86198-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86198-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86198-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86198-130">Controla la capacidad de configurar varias versiones de un producto en un sistema.</span><span class="sxs-lookup"><span data-stu-id="86198-130">Controls the ability to configure multiple versions of a product on a system.</span></span>

</dd> <dt>

<span data-ttu-id="86198-131">**Caption**</span><span class="sxs-lookup"><span data-stu-id="86198-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86198-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86198-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86198-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86198-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86198-134">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="86198-134">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="86198-135">Breve descripción textual del sujeto.</span><span class="sxs-lookup"><span data-stu-id="86198-135">A short textual description of the subject.</span></span>

<span data-ttu-id="86198-136">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="86198-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="86198-137">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="86198-137">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86198-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86198-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86198-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86198-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86198-140">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="86198-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="86198-141">Identificador que se usa junto con otras claves para identificar de forma única la comprobación.</span><span class="sxs-lookup"><span data-stu-id="86198-141">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="86198-142">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="86198-142">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="86198-143">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="86198-143">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86198-144">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="86198-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86198-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86198-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86198-146">Si es **true**, se espera que la condición exista en el entorno.</span><span class="sxs-lookup"><span data-stu-id="86198-146">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="86198-147">Por ejemplo, se espera que un archivo esté en un sistema, por lo que el método [**Invoke**](invoke-method-in-class-cim-check.md) debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="86198-147">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="86198-148">Si es **false**, no se espera que la condición exista.</span><span class="sxs-lookup"><span data-stu-id="86198-148">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="86198-149">Por ejemplo, un archivo no se encuentra en un sistema, por lo que el método [**Invoke**](invoke-method-in-class-cim-check.md) debe devolver **false**.</span><span class="sxs-lookup"><span data-stu-id="86198-149">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="86198-150">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="86198-150">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="86198-151">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86198-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86198-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86198-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86198-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86198-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86198-154">Descripción de los objetos.</span><span class="sxs-lookup"><span data-stu-id="86198-154">A description of the objects.</span></span>

<span data-ttu-id="86198-155">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="86198-155">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="86198-156">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="86198-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86198-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86198-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86198-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86198-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86198-159">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="86198-159">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="86198-160">Nombre usado para identificar el elemento de software</span><span class="sxs-lookup"><span data-stu-id="86198-160">Name used to identify the software element</span></span>

<span data-ttu-id="86198-161">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="86198-161">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="86198-162">**Reinstalación**</span><span class="sxs-lookup"><span data-stu-id="86198-162">**Reinstall**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86198-163">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="86198-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="86198-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86198-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86198-165">Si **es true**, el elemento de software puede pasar a su siguiente estado si ya existe o no un elemento de software de la misma versión en el entorno.</span><span class="sxs-lookup"><span data-stu-id="86198-165">If **TRUE**, the software element can transition to its next state whether or not a software element of the same version already exists in the environment.</span></span>

</dd> <dt>

<span data-ttu-id="86198-166">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="86198-166">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86198-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86198-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86198-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86198-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86198-169">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="86198-169">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="86198-170">Este es un identificador de este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="86198-170">This is an identifier for this software element.</span></span>

<span data-ttu-id="86198-171">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="86198-171">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="86198-172">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="86198-172">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86198-173">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86198-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86198-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86198-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86198-175">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="86198-175">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="86198-176">El estado de elemento de software de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="86198-176">The software element state of a software element.</span></span>

<span data-ttu-id="86198-177">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="86198-177">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="86198-178"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>Se pueden **implementar** (0)</span><span class="sxs-lookup"><span data-stu-id="86198-178"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="86198-179"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalable** (1)</span><span class="sxs-lookup"><span data-stu-id="86198-179"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="86198-180"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Archivo ejecutable** (2)</span><span class="sxs-lookup"><span data-stu-id="86198-180"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="86198-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="86198-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="86198-182">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="86198-182">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86198-183">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86198-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86198-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86198-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86198-185">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Información del componente de software de DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="86198-185">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="86198-186">Sistema operativo de destino del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="86198-186">Target operating system of the software element.</span></span>

<span data-ttu-id="86198-187">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="86198-187">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="86198-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="86198-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="86198-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="86198-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="86198-190"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="86198-190"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="86198-191">Mac OS</span><span class="sxs-lookup"><span data-stu-id="86198-191">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="86198-192"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="86198-192"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="86198-193">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="86198-193">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="86198-194"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="86198-194"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="86198-195"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="86198-195"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="86198-196"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="86198-196"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="86198-197"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="86198-197"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="86198-198">Abrir máquinas virtuales</span><span class="sxs-lookup"><span data-stu-id="86198-198">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="86198-199"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="86198-199"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="86198-200">HP-UX</span><span class="sxs-lookup"><span data-stu-id="86198-200">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="86198-201"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="86198-201"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="86198-202"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="86198-202"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="86198-203"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="86198-203"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="86198-204"><span id="OS_2"></span><span id="os_2"></span>**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="86198-204"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="86198-205"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="86198-205"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="86198-206">Máquina virtual (VM) de Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="86198-206">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="86198-207"><span id="MSDOS"></span><span id="msdos"></span>**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="86198-207"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="86198-208"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="86198-208"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="86198-209">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="86198-209">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="86198-210"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="86198-210"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="86198-211">Windows 95</span><span class="sxs-lookup"><span data-stu-id="86198-211">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="86198-212"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="86198-212"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="86198-213">Windows 98</span><span class="sxs-lookup"><span data-stu-id="86198-213">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="86198-214"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="86198-214"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="86198-215">Windows NT</span><span class="sxs-lookup"><span data-stu-id="86198-215">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="86198-216"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="86198-216"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="86198-217">Windows CE</span><span class="sxs-lookup"><span data-stu-id="86198-217">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="86198-218"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="86198-218"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="86198-219">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="86198-219">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="86198-220"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="86198-220"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="86198-221"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="86198-221"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="86198-222"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="86198-222"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="86198-223"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="86198-223"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="86198-224"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="86198-224"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="86198-225"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="86198-225"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="86198-226"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="86198-226"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="86198-227"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="86198-227"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="86198-228"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="86198-228"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="86198-229"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="86198-229"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="86198-230"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="86198-230"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="86198-231"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="86198-231"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="86198-232">Una serie</span><span class="sxs-lookup"><span data-stu-id="86198-232">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="86198-233"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="86198-233"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="86198-234">Tándem NSK</span><span class="sxs-lookup"><span data-stu-id="86198-234">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="86198-235"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="86198-235"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="86198-236">Tándem</span><span class="sxs-lookup"><span data-stu-id="86198-236">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="86198-237"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="86198-237"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="86198-238">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="86198-238">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="86198-239"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="86198-239"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="86198-240"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="86198-240"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="86198-241"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="86198-241"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="86198-242"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="86198-242"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="86198-243"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="86198-243"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="86198-244"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="86198-244"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="86198-245">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="86198-245">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="86198-246"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="86198-246"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="86198-247"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="86198-247"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="86198-248"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="86198-248"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="86198-249"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="86198-249"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="86198-250">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="86198-250">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="86198-251"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="86198-251"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="86198-252"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="86198-252"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="86198-253"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="86198-253"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="86198-254"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="86198-254"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="86198-255"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="86198-255"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="86198-256"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="86198-256"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="86198-257"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="86198-257"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="86198-258"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="86198-258"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="86198-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="86198-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="86198-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="86198-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="86198-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="86198-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="86198-262">Palm OS</span><span class="sxs-lookup"><span data-stu-id="86198-262">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="86198-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="86198-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="86198-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="86198-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="86198-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="86198-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="86198-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="86198-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="86198-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="86198-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="86198-268">**Versión**</span><span class="sxs-lookup"><span data-stu-id="86198-268">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86198-269">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="86198-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86198-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="86198-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86198-271">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Versión**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="86198-271">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="86198-272">Versión de la operación.</span><span class="sxs-lookup"><span data-stu-id="86198-272">Version of the operation.</span></span>

<span data-ttu-id="86198-273">La versión de la operación debe estar en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="86198-273">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="86198-274"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="86198-274"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="86198-275"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="86198-275"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="86198-276">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="86198-276">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86198-277">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86198-277">Remarks</span></span>

<span data-ttu-id="86198-278">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="86198-278">WMI does not implement this class.</span></span>

<span data-ttu-id="86198-279">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="86198-279">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="86198-280">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="86198-280">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="86198-281">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86198-281">Requirements</span></span>



| <span data-ttu-id="86198-282">Requisito</span><span class="sxs-lookup"><span data-stu-id="86198-282">Requirement</span></span> | <span data-ttu-id="86198-283">Value</span><span class="sxs-lookup"><span data-stu-id="86198-283">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86198-284">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86198-284">Minimum supported client</span></span><br/> | <span data-ttu-id="86198-285">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86198-285">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86198-286">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86198-286">Minimum supported server</span></span><br/> | <span data-ttu-id="86198-287">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86198-287">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86198-288">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="86198-288">Namespace</span></span><br/>                | <span data-ttu-id="86198-289">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="86198-289">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="86198-290">MOF</span><span class="sxs-lookup"><span data-stu-id="86198-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86198-291"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86198-291"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="86198-292">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="86198-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86198-293"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86198-293"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86198-294">Vea también</span><span class="sxs-lookup"><span data-stu-id="86198-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86198-295">**Comprobación de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="86198-295">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

