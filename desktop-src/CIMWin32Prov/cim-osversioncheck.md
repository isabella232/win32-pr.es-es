---
description: La \_ clase CIM OSVersionCheck especifica las versiones del sistema operativo que pueden admitir un elemento de software.
ms.assetid: 6796cfc4-3b6f-43a4-b5f0-854a95284238
ms.tgt_platform: multiple
title: CIM_OSVersionCheck (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSVersionCheck
- CIM_OSVersionCheck.CheckID
- CIM_OSVersionCheck.Caption
- CIM_OSVersionCheck.Description
- CIM_OSVersionCheck.CheckMode
- CIM_OSVersionCheck.Name
- CIM_OSVersionCheck.TargetOperatingSystem
- CIM_OSVersionCheck.Version
- CIM_OSVersionCheck.SoftwareElementID
- CIM_OSVersionCheck.SoftwareElementState
- CIM_OSVersionCheck.MaximumVersion
- CIM_OSVersionCheck.MinimumVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c341b9038b5b40b559b4a121adb88fbb2d7b5205
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080214"
---
# <a name="cim_osversioncheck-class"></a><span data-ttu-id="014cd-103">\_Clase OSVersionCheck de CIM</span><span class="sxs-lookup"><span data-stu-id="014cd-103">CIM\_OSVersionCheck class</span></span>

<span data-ttu-id="014cd-104">La clase **CIM \_ OSVersionCheck** especifica las versiones del sistema operativo que pueden admitir un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="014cd-104">The **CIM\_OSVersionCheck** class specifies the versions of the operating system that can support a software element.</span></span> <span data-ttu-id="014cd-105">La comprobación se puede ejecutar para un determinado, un mínimo, un máximo o un intervalo de versiones del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="014cd-105">The check can be run for a specific, minimum, maximum, or a range of operating system releases.</span></span> <span data-ttu-id="014cd-106">Para especificar una versión específica del sistema operativo, las versiones mínima y máxima deben ser iguales.</span><span class="sxs-lookup"><span data-stu-id="014cd-106">To specify a specific operating system version, the minimum and maximum versions must be equal.</span></span> <span data-ttu-id="014cd-107">Para especificar la versión mínima, solo se debe especificar la versión mínima.</span><span class="sxs-lookup"><span data-stu-id="014cd-107">To specify the minimum version, the minimum version only must be specified.</span></span> <span data-ttu-id="014cd-108">Para especificar una versión máxima, solo es necesario especificar la versión máxima.</span><span class="sxs-lookup"><span data-stu-id="014cd-108">To specify a maximum version, the maximum version only needs to be specified.</span></span> <span data-ttu-id="014cd-109">Para especificar un intervalo, deben especificarse las versiones mínima y máxima.</span><span class="sxs-lookup"><span data-stu-id="014cd-109">To specify a range, both minimum and maximum versions must be specified.</span></span>

<span data-ttu-id="014cd-110">El tipo de sistema operativo se especifica en la propiedad **TargetOperatingSystem** del elemento de software propietario.</span><span class="sxs-lookup"><span data-stu-id="014cd-110">The type of operating system is specified in the **TargetOperatingSystem** property of the owning software element.</span></span> <span data-ttu-id="014cd-111">Los detalles de las comprobaciones se comparan con los detalles correspondientes que se encuentran en un objeto [**\_ OperatingSystem de CIM**](cim-operatingsystem.md) al que hace referencia una asociación de [**CIM \_ instalado**](cim-installedos.md) para el objeto de [**\_ ComputerSystem de CIM**](cim-computersystem.md) que describe el entorno.</span><span class="sxs-lookup"><span data-stu-id="014cd-111">Details of the checks are compared with the corresponding details found in a [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by a [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="014cd-112">Al menos una clase de sistema **\_ operativo CIM** debe cumplir los detalles de la condición para que se cumpla la comprobación.</span><span class="sxs-lookup"><span data-stu-id="014cd-112">At least one **CIM\_OperatingSystem** class must satisfy the details of the condition for the check to be satisfied.</span></span> <span data-ttu-id="014cd-113">En otras palabras, no todos los sistemas operativos del equipo correspondiente deben satisfacer la condición.</span><span class="sxs-lookup"><span data-stu-id="014cd-113">In other words, not all of the operating systems on the relevant computer system need to satisfy the condition.</span></span> <span data-ttu-id="014cd-114">Además, la propiedad **OSType** de la clase **CIM \_ OperatingSystem** debe coincidir con el tipo de la propiedad **TargetOperatingSystem** .</span><span class="sxs-lookup"><span data-stu-id="014cd-114">Also, the **OSType** property of the **CIM\_OperatingSystem** class must match the type of the **TargetOperatingSystem** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="014cd-115">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="014cd-115">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="014cd-116">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="014cd-116">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="014cd-117">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="014cd-117">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="014cd-118">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="014cd-118">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="014cd-119">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="014cd-119">Syntax</span></span>

``` syntax
[UUID("{FEE8368A-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_OSVersionCheck : CIM_Check
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
  string  MaximumVersion;
  string  MinimumVersion;
};
```

## <a name="members"></a><span data-ttu-id="014cd-120">Miembros</span><span class="sxs-lookup"><span data-stu-id="014cd-120">Members</span></span>

<span data-ttu-id="014cd-121">La clase **CIM \_ OSVersionCheck** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="014cd-121">The **CIM\_OSVersionCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="014cd-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="014cd-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="014cd-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="014cd-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="014cd-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="014cd-124">Methods</span></span>

<span data-ttu-id="014cd-125">La clase **CIM \_ OSVersionCheck** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="014cd-125">The **CIM\_OSVersionCheck** class has these methods.</span></span>



| <span data-ttu-id="014cd-126">Método</span><span class="sxs-lookup"><span data-stu-id="014cd-126">Method</span></span>                                                      | <span data-ttu-id="014cd-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="014cd-127">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="014cd-128">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="014cd-128">**Invoke**</span></span>](invoke-method-in-class-cim-osversioncheck.md) | <span data-ttu-id="014cd-129">Toma una acción concreta.</span><span class="sxs-lookup"><span data-stu-id="014cd-129">Takes a particular action.</span></span> <span data-ttu-id="014cd-130">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="014cd-130">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="014cd-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="014cd-131">Properties</span></span>

<span data-ttu-id="014cd-132">La clase **CIM \_ OSVersionCheck** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="014cd-132">The **CIM\_OSVersionCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="014cd-133">**Caption**</span><span class="sxs-lookup"><span data-stu-id="014cd-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="014cd-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="014cd-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="014cd-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="014cd-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="014cd-136">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="014cd-136">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="014cd-137">Breve descripción textual del sujeto.</span><span class="sxs-lookup"><span data-stu-id="014cd-137">A short textual description of the subject.</span></span>

<span data-ttu-id="014cd-138">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="014cd-138">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="014cd-139">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="014cd-139">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="014cd-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="014cd-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="014cd-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="014cd-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="014cd-142">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="014cd-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="014cd-143">Identificador que se usa junto con otras claves para identificar de forma única la comprobación.</span><span class="sxs-lookup"><span data-stu-id="014cd-143">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="014cd-144">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="014cd-144">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="014cd-145">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="014cd-145">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="014cd-146">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="014cd-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="014cd-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="014cd-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="014cd-148">Si es **true**, se espera que la condición exista en el entorno.</span><span class="sxs-lookup"><span data-stu-id="014cd-148">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="014cd-149">Por ejemplo, se espera que un archivo esté en un sistema, por lo que el método [**Invoke**](invoke-method-in-class-cim-check.md) debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="014cd-149">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="014cd-150">Si es **false**, no se espera que la condición exista.</span><span class="sxs-lookup"><span data-stu-id="014cd-150">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="014cd-151">Por ejemplo, un archivo no se encuentra en un sistema, por lo que el método [**Invoke**](invoke-method-in-class-cim-check.md) debe devolver **false**.</span><span class="sxs-lookup"><span data-stu-id="014cd-151">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="014cd-152">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="014cd-152">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="014cd-153">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="014cd-153">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="014cd-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="014cd-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="014cd-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="014cd-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="014cd-156">Descripción de los objetos.</span><span class="sxs-lookup"><span data-stu-id="014cd-156">A description of the objects.</span></span>

<span data-ttu-id="014cd-157">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="014cd-157">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="014cd-158">**MaximumVersion**</span><span class="sxs-lookup"><span data-stu-id="014cd-158">**MaximumVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="014cd-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="014cd-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="014cd-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="014cd-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="014cd-161">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Versión**")</span><span class="sxs-lookup"><span data-stu-id="014cd-161">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="014cd-162">Versión máxima del sistema operativo requerido.</span><span class="sxs-lookup"><span data-stu-id="014cd-162">Maximum version of the required operating system.</span></span>

<span data-ttu-id="014cd-163">El valor se codifica en una de las formas siguientes:</span><span class="sxs-lookup"><span data-stu-id="014cd-163">The value is encoded in one of the following forms:</span></span>

-   <span data-ttu-id="014cd-164"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="014cd-164"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="014cd-165"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="014cd-165"><major>.<minor><letter><revision></span></span>

</dd> <dt>

<span data-ttu-id="014cd-166">**MinimumVersion**</span><span class="sxs-lookup"><span data-stu-id="014cd-166">**MinimumVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="014cd-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="014cd-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="014cd-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="014cd-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="014cd-169">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Versión**")</span><span class="sxs-lookup"><span data-stu-id="014cd-169">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="014cd-170">Versión mínima del sistema operativo requerido.</span><span class="sxs-lookup"><span data-stu-id="014cd-170">Minimum version of the required operating system.</span></span>

<span data-ttu-id="014cd-171">El valor se codifica en una de las formas siguientes:</span><span class="sxs-lookup"><span data-stu-id="014cd-171">The value is encoded in one of the following forms:</span></span>

-   <span data-ttu-id="014cd-172"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="014cd-172"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="014cd-173"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="014cd-173"><major>.<minor><letter><revision></span></span>

</dd> <dt>

<span data-ttu-id="014cd-174">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="014cd-174">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="014cd-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="014cd-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="014cd-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="014cd-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="014cd-177">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nombre**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="014cd-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="014cd-178">Nombre usado para identificar el elemento de software</span><span class="sxs-lookup"><span data-stu-id="014cd-178">Name used to identify the software element</span></span>

<span data-ttu-id="014cd-179">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="014cd-179">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="014cd-180">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="014cd-180">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="014cd-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="014cd-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="014cd-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="014cd-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="014cd-183">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="014cd-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="014cd-184">Este es un identificador de este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="014cd-184">This is an identifier for this software element.</span></span>

<span data-ttu-id="014cd-185">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="014cd-185">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="014cd-186">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="014cd-186">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="014cd-187">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="014cd-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="014cd-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="014cd-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="014cd-189">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="014cd-189">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="014cd-190">El estado de elemento de software de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="014cd-190">The software element state of a software element.</span></span>

<span data-ttu-id="014cd-191">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="014cd-191">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="014cd-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>Se pueden **implementar** (0)</span><span class="sxs-lookup"><span data-stu-id="014cd-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-193">Describe los detalles necesarios para la distribución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado instalable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="014cd-193">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="014cd-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalable** (1)</span><span class="sxs-lookup"><span data-stu-id="014cd-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-195">Describe los detalles necesarios para una instalación correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado del archivo ejecutable (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="014cd-195">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="014cd-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Archivo ejecutable** (2)</span><span class="sxs-lookup"><span data-stu-id="014cd-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-197">Describe los detalles necesarios para la ejecución correcta y los detalles (condiciones y acciones) necesarios para crear un elemento de software en el estado de ejecución (es decir, el siguiente estado).</span><span class="sxs-lookup"><span data-stu-id="014cd-197">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="014cd-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="014cd-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-199">Describe los detalles necesarios para supervisar y operar en un elemento de inicio.</span><span class="sxs-lookup"><span data-stu-id="014cd-199">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="014cd-200">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="014cd-200">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="014cd-201">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="014cd-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="014cd-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="014cd-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="014cd-203">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Información del componente de software de DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="014cd-203">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="014cd-204">Sistema operativo de destino del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="014cd-204">Target operating system of the software element.</span></span>

<span data-ttu-id="014cd-205">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="014cd-205">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="014cd-206"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="014cd-206"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="014cd-207"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="014cd-207"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="014cd-208"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="014cd-208"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-209">Mac OS</span><span class="sxs-lookup"><span data-stu-id="014cd-209">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="014cd-210"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="014cd-210"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-211">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="014cd-211">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="014cd-212"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="014cd-212"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="014cd-213"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="014cd-213"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="014cd-214"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="014cd-214"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="014cd-215"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="014cd-215"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-216">Abrir máquinas virtuales</span><span class="sxs-lookup"><span data-stu-id="014cd-216">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="014cd-217"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="014cd-217"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-218">HP-UX</span><span class="sxs-lookup"><span data-stu-id="014cd-218">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="014cd-219"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="014cd-219"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="014cd-220"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="014cd-220"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="014cd-221"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="014cd-221"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="014cd-222"><span id="OS_2"></span><span id="os_2"></span>**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="014cd-222"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="014cd-223"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="014cd-223"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-224">Máquina virtual (VM) de Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="014cd-224">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="014cd-225"><span id="MSDOS"></span><span id="msdos"></span>**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="014cd-225"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="014cd-226"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="014cd-226"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-227">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="014cd-227">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="014cd-228"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="014cd-228"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-229">Windows 95</span><span class="sxs-lookup"><span data-stu-id="014cd-229">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="014cd-230"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="014cd-230"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-231">Windows 98</span><span class="sxs-lookup"><span data-stu-id="014cd-231">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="014cd-232"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="014cd-232"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-233">Windows NT</span><span class="sxs-lookup"><span data-stu-id="014cd-233">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="014cd-234"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="014cd-234"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-235">Windows CE</span><span class="sxs-lookup"><span data-stu-id="014cd-235">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="014cd-236"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="014cd-236"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-237">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="014cd-237">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="014cd-238"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="014cd-238"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="014cd-239"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="014cd-239"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="014cd-240"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="014cd-240"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="014cd-241"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="014cd-241"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="014cd-242"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="014cd-242"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="014cd-243"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="014cd-243"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="014cd-244"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="014cd-244"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="014cd-245"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="014cd-245"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="014cd-246"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="014cd-246"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="014cd-247"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="014cd-247"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="014cd-248"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="014cd-248"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="014cd-249"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="014cd-249"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-250">Una serie</span><span class="sxs-lookup"><span data-stu-id="014cd-250">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="014cd-251"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="014cd-251"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-252">Tándem NSK</span><span class="sxs-lookup"><span data-stu-id="014cd-252">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="014cd-253"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="014cd-253"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-254">Tándem</span><span class="sxs-lookup"><span data-stu-id="014cd-254">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="014cd-255"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="014cd-255"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-256">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="014cd-256">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="014cd-257"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="014cd-257"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="014cd-258"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="014cd-258"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="014cd-259"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="014cd-259"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="014cd-260"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="014cd-260"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="014cd-261"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="014cd-261"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="014cd-262"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="014cd-262"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-263">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="014cd-263">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="014cd-264"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="014cd-264"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="014cd-265"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="014cd-265"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="014cd-266"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="014cd-266"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="014cd-267"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="014cd-267"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-268">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="014cd-268">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="014cd-269"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="014cd-269"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="014cd-270"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="014cd-270"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="014cd-271"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="014cd-271"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="014cd-272"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="014cd-272"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="014cd-273"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="014cd-273"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="014cd-274"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="014cd-274"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="014cd-275"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="014cd-275"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="014cd-276"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="014cd-276"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="014cd-277"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="014cd-277"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="014cd-278"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="014cd-278"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="014cd-279"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="014cd-279"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="014cd-280">Palm OS</span><span class="sxs-lookup"><span data-stu-id="014cd-280">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="014cd-281"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="014cd-281"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="014cd-282"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="014cd-282"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="014cd-283"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="014cd-283"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="014cd-284"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="014cd-284"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="014cd-285"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="014cd-285"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="014cd-286">**Versión**</span><span class="sxs-lookup"><span data-stu-id="014cd-286">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="014cd-287">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="014cd-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="014cd-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="014cd-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="014cd-289">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Versión**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="014cd-289">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="014cd-290">Versión de la operación.</span><span class="sxs-lookup"><span data-stu-id="014cd-290">Version of the operation.</span></span>

<span data-ttu-id="014cd-291">La versión de la operación debe estar en una de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="014cd-291">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="014cd-292"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="014cd-292"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="014cd-293"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="014cd-293"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="014cd-294">Esta propiedad se hereda de [**la \_ comprobación CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="014cd-294">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="014cd-295">Observaciones</span><span class="sxs-lookup"><span data-stu-id="014cd-295">Remarks</span></span>

<span data-ttu-id="014cd-296">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="014cd-296">WMI does not implement this class.</span></span>

<span data-ttu-id="014cd-297">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="014cd-297">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="014cd-298">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="014cd-298">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="014cd-299">Requisitos</span><span class="sxs-lookup"><span data-stu-id="014cd-299">Requirements</span></span>



| <span data-ttu-id="014cd-300">Requisito</span><span class="sxs-lookup"><span data-stu-id="014cd-300">Requirement</span></span> | <span data-ttu-id="014cd-301">Value</span><span class="sxs-lookup"><span data-stu-id="014cd-301">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="014cd-302">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="014cd-302">Minimum supported client</span></span><br/> | <span data-ttu-id="014cd-303">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="014cd-303">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="014cd-304">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="014cd-304">Minimum supported server</span></span><br/> | <span data-ttu-id="014cd-305">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="014cd-305">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="014cd-306">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="014cd-306">Namespace</span></span><br/>                | <span data-ttu-id="014cd-307">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="014cd-307">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="014cd-308">MOF</span><span class="sxs-lookup"><span data-stu-id="014cd-308">MOF</span></span><br/>                      | <dl> <span data-ttu-id="014cd-309"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="014cd-309"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="014cd-310">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="014cd-310">DLL</span></span><br/>                      | <dl> <span data-ttu-id="014cd-311"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="014cd-311"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="014cd-312">Vea también</span><span class="sxs-lookup"><span data-stu-id="014cd-312">See also</span></span>

<dl> <dt>

[<span data-ttu-id="014cd-313">**Comprobación de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="014cd-313">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

