---
description: La \_ relación DeviceSoftware de CIM identifica el software que está asociado a un dispositivo, como controladores, software de la aplicación o de configuración, o firmware.
ms.assetid: 831d0014-2a01-49f4-9642-fae5682f0388
ms.tgt_platform: multiple
title: CIM_DeviceSoftware (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSoftware
- CIM_DeviceSoftware.Dependent
- CIM_DeviceSoftware.Antecedent
- CIM_DeviceSoftware.Purpose
- CIM_DeviceSoftware.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 467fa670e8bb3f7d6ee967e6dd422102a2026a57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539069"
---
# <a name="cim_devicesoftware-class"></a><span data-ttu-id="bf783-103">\_Clase DeviceSoftware de CIM</span><span class="sxs-lookup"><span data-stu-id="bf783-103">CIM\_DeviceSoftware class</span></span>

<span data-ttu-id="bf783-104">La **relación \_ DeviceSoftware de CIM** identifica el software que está asociado a un dispositivo, como controladores, software de la aplicación o de configuración, o firmware.</span><span class="sxs-lookup"><span data-stu-id="bf783-104">The **CIM\_DeviceSoftware** relationship identifies software that is associated with a device, such as drivers, configuration or application software, or firmware.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf783-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="bf783-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bf783-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bf783-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bf783-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="bf783-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bf783-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="bf783-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf783-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf783-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{36363AAA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceSoftware : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_SoftwareElement REF Antecedent;
  uint16                  Purpose;
  string                  PurposeDescription;
};
```

## <a name="members"></a><span data-ttu-id="bf783-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="bf783-110">Members</span></span>

<span data-ttu-id="bf783-111">La clase **CIM \_ DeviceSoftware** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bf783-111">The **CIM\_DeviceSoftware** class has these types of members:</span></span>

-   [<span data-ttu-id="bf783-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf783-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf783-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf783-113">Properties</span></span>

<span data-ttu-id="bf783-114">La clase **CIM \_ DeviceSoftware** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bf783-114">The **CIM\_DeviceSoftware** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf783-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="bf783-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf783-116">Tipo de datos: **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="bf783-116">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="bf783-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf783-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf783-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="bf783-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="bf783-119">Un [**\_ SoftwareElement de CIM**](cim-softwareelement.md) que describe el elemento de software.</span><span class="sxs-lookup"><span data-stu-id="bf783-119">A [**CIM\_SoftwareElement**](cim-softwareelement.md) that describes the software element.</span></span>

</dd> <dt>

<span data-ttu-id="bf783-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="bf783-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf783-121">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="bf783-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="bf783-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf783-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf783-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="bf783-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="bf783-124">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe el dispositivo lógico que requiere o utiliza el software.</span><span class="sxs-lookup"><span data-stu-id="bf783-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device that requires or uses the software.</span></span>

</dd> <dt>

<span data-ttu-id="bf783-125">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="bf783-125">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf783-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bf783-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bf783-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf783-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf783-128">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DeviceSoftware**.**PurposeDescription**")</span><span class="sxs-lookup"><span data-stu-id="bf783-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DeviceSoftware**.**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="bf783-129">Rol que el software toma con respecto a su dispositivo asociado.</span><span class="sxs-lookup"><span data-stu-id="bf783-129">Role that the software takes regarding its associated device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bf783-130"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="bf783-130"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bf783-131">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="bf783-131">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bf783-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="bf783-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bf783-133">Otros.</span><span class="sxs-lookup"><span data-stu-id="bf783-133">Other.</span></span>

</dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

<span data-ttu-id="bf783-134"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>**Controlador** (2)</span><span class="sxs-lookup"><span data-stu-id="bf783-134"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>**Driver** (2)</span></span>


</dt> <dd>

<span data-ttu-id="bf783-135">Dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf783-135">Driver.</span></span>

</dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

<span data-ttu-id="bf783-136"><span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>**Software de configuración** (3)</span><span class="sxs-lookup"><span data-stu-id="bf783-136"><span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>**Configuration Software** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bf783-137">Software de configuración.</span><span class="sxs-lookup"><span data-stu-id="bf783-137">Configuration software.</span></span>

</dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

<span data-ttu-id="bf783-138"><span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>**Software de aplicación** (4)</span><span class="sxs-lookup"><span data-stu-id="bf783-138"><span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>**Application Software** (4)</span></span>


</dt> <dd>

<span data-ttu-id="bf783-139">Software de aplicación.</span><span class="sxs-lookup"><span data-stu-id="bf783-139">Application software.</span></span>

</dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

<span data-ttu-id="bf783-140"><span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>**Instrumentación** (5)</span><span class="sxs-lookup"><span data-stu-id="bf783-140"><span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>**Instrumentation** (5)</span></span>


</dt> <dd>

<span data-ttu-id="bf783-141">Instrumentación.</span><span class="sxs-lookup"><span data-stu-id="bf783-141">Instrumentation.</span></span>

</dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

<span data-ttu-id="bf783-142"><span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>**Firmware** (6)</span><span class="sxs-lookup"><span data-stu-id="bf783-142"><span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>**Firmware** (6)</span></span>


</dt> <dd>

<span data-ttu-id="bf783-143">Firmware.</span><span class="sxs-lookup"><span data-stu-id="bf783-143">Firmware.</span></span>

</dd> <dt>

<span id="BIOS"></span><span id="bios"></span>

<span data-ttu-id="bf783-144"><span id="BIOS"></span><span id="bios"></span>**BIOS** (7)</span><span class="sxs-lookup"><span data-stu-id="bf783-144"><span id="BIOS"></span><span id="bios"></span>**BIOS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="bf783-145">BIOS.</span><span class="sxs-lookup"><span data-stu-id="bf783-145">BIOS.</span></span>

</dd> <dt>

<span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>

<span data-ttu-id="bf783-146"><span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>**ROM de arranque** (8)</span><span class="sxs-lookup"><span data-stu-id="bf783-146"><span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>**Boot ROM** (8)</span></span>


</dt> <dd>

<span data-ttu-id="bf783-147">ROM de arranque.</span><span class="sxs-lookup"><span data-stu-id="bf783-147">Boot ROM.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf783-148">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="bf783-148">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf783-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bf783-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf783-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf783-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf783-151">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DeviceSoftware**.**Propósito**")</span><span class="sxs-lookup"><span data-stu-id="bf783-151">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DeviceSoftware**.**Purpose**")</span></span>
</dt> </dl>

<span data-ttu-id="bf783-152">Cadena de forma libre que proporciona más información para la propiedad **propósito** , por ejemplo, "software de aplicación".</span><span class="sxs-lookup"><span data-stu-id="bf783-152">Free-form string that provides more information for the **Purpose** property, for example, "Application Software".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf783-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf783-153">Remarks</span></span>

<span data-ttu-id="bf783-154">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="bf783-154">WMI does not implement this class.</span></span>

<span data-ttu-id="bf783-155">La clase **CIM \_ DeviceSoftware** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="bf783-155">The **CIM\_DeviceSoftware** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="bf783-156">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="bf783-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bf783-157">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="bf783-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf783-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf783-158">Requirements</span></span>



| <span data-ttu-id="bf783-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf783-159">Requirement</span></span> | <span data-ttu-id="bf783-160">Value</span><span class="sxs-lookup"><span data-stu-id="bf783-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf783-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf783-161">Minimum supported client</span></span><br/> | <span data-ttu-id="bf783-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf783-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bf783-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf783-163">Minimum supported server</span></span><br/> | <span data-ttu-id="bf783-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf783-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bf783-165">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bf783-165">Namespace</span></span><br/>                | <span data-ttu-id="bf783-166">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bf783-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bf783-167">MOF</span><span class="sxs-lookup"><span data-stu-id="bf783-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf783-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf783-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf783-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bf783-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf783-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf783-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf783-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf783-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf783-172">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="bf783-172">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

