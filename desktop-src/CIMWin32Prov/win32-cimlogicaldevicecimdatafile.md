---
description: La \_ clase WMI CIMLogicalDeviceCIMDataFile Association de Win32 relaciona los dispositivos lógicos y los archivos de datos, que indican los archivos de controlador utilizados por el dispositivo. Esta clase se usa para detectar los controladores de dispositivo que usa un dispositivo.
ms.assetid: 892272de-920d-4fa0-adbc-f584ed6e8748
ms.tgt_platform: multiple
title: Win32_CIMLogicalDeviceCIMDataFile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CIMLogicalDeviceCIMDataFile
- Win32_CIMLogicalDeviceCIMDataFile.Dependent
- Win32_CIMLogicalDeviceCIMDataFile.Antecedent
- Win32_CIMLogicalDeviceCIMDataFile.Purpose
- Win32_CIMLogicalDeviceCIMDataFile.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15db6209360cbd150a722dc98b6255afd696cbe9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539153"
---
# <a name="win32_cimlogicaldevicecimdatafile-class"></a><span data-ttu-id="e4b86-104">\_Clase Win32 CIMLogicalDeviceCIMDataFile</span><span class="sxs-lookup"><span data-stu-id="e4b86-104">Win32\_CIMLogicalDeviceCIMDataFile class</span></span>

<span data-ttu-id="e4b86-105">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ CIMLogicalDeviceCIMDataFile** Association de Win32 relaciona los dispositivos lógicos y los archivos de datos, que indican los archivos de controlador utilizados por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4b86-105">The **Win32\_CIMLogicalDeviceCIMDataFile** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates logical devices and data files, indicating the driver files used by the device.</span></span> <span data-ttu-id="e4b86-106">Esta clase se usa para detectar los controladores de dispositivo que usa un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4b86-106">This class is used to discover which device drivers a device uses.</span></span>

<span data-ttu-id="e4b86-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e4b86-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e4b86-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="e4b86-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b86-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4b86-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C510-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CIMLogicalDeviceCIMDataFile : CIM_Dependency
{
  CIM_DataFile      REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint16                Purpose;
  string                PurposeDescription;
};
```

## <a name="members"></a><span data-ttu-id="e4b86-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="e4b86-110">Members</span></span>

<span data-ttu-id="e4b86-111">La **clase \_ CIMLogicalDeviceCIMDataFile de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e4b86-111">The **Win32\_CIMLogicalDeviceCIMDataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="e4b86-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4b86-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e4b86-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4b86-113">Properties</span></span>

<span data-ttu-id="e4b86-114">La **clase \_ CIMLogicalDeviceCIMDataFile de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e4b86-114">The **Win32\_CIMLogicalDeviceCIMDataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4b86-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="e4b86-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b86-116">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="e4b86-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="e4b86-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4b86-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4b86-118">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| lógico CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="e4b86-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="e4b86-119">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que representa las propiedades del dispositivo lógico utilizado por el archivo de datos.</span><span class="sxs-lookup"><span data-stu-id="e4b86-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the properties of the logical device that is being used by the data file.</span></span>

</dd> <dt>

<span data-ttu-id="e4b86-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="e4b86-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b86-121">Tipo de datos **: \_ archivo** de datos CIM</span><span class="sxs-lookup"><span data-stu-id="e4b86-121">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="e4b86-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4b86-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4b86-123">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM archivo de \_ archivos")</span><span class="sxs-lookup"><span data-stu-id="e4b86-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="e4b86-124">Un [**\_ archivo**](cim-datafile.md) de datos CIM que representa las propiedades del archivo de datos asignado al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="e4b86-124">A [**CIM\_DataFile**](cim-datafile.md) that represents the properties of the data file assigned to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="e4b86-125">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="e4b86-125">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b86-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e4b86-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e4b86-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4b86-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4b86-128">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span><span class="sxs-lookup"><span data-stu-id="e4b86-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span></span>
</dt> </dl>

<span data-ttu-id="e4b86-129">Rol que desempeña el archivo de datos con respecto a su dispositivo lógico asociado.</span><span class="sxs-lookup"><span data-stu-id="e4b86-129">Role that the data file plays with regard to its associated logical device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e4b86-130">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="e4b86-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e4b86-131">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="e4b86-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

<span data-ttu-id="e4b86-132">**Controlador** (2)</span><span class="sxs-lookup"><span data-stu-id="e4b86-132">**Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

<span data-ttu-id="e4b86-133">**Software de configuración** (3)</span><span class="sxs-lookup"><span data-stu-id="e4b86-133">**Configuration Software** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

<span data-ttu-id="e4b86-134">**Software de aplicación** (4)</span><span class="sxs-lookup"><span data-stu-id="e4b86-134">**Application Software** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

<span data-ttu-id="e4b86-135">**Instrumentación** (5)</span><span class="sxs-lookup"><span data-stu-id="e4b86-135">**Instrumentation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

<span data-ttu-id="e4b86-136">**Firmware** (6)</span><span class="sxs-lookup"><span data-stu-id="e4b86-136">**Firmware** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e4b86-137">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="e4b86-137">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b86-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e4b86-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4b86-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e4b86-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4b86-140">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span><span class="sxs-lookup"><span data-stu-id="e4b86-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span></span>
</dt> </dl>

<span data-ttu-id="e4b86-141">Extiende el valor de la propiedad **purpose** de esta clase.</span><span class="sxs-lookup"><span data-stu-id="e4b86-141">Extends the value of the **Purpose** property of this class.</span></span>

<span data-ttu-id="e4b86-142">Ejemplo: "controlador de disquete"</span><span class="sxs-lookup"><span data-stu-id="e4b86-142">Example: "Floppy Disk Driver"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4b86-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4b86-143">Remarks</span></span>

<span data-ttu-id="e4b86-144">La **clase \_ CIMLogicalDeviceCIMDataFile de Win32** se deriva de la [**\_ dependencia CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="e4b86-144">The **Win32\_CIMLogicalDeviceCIMDataFile** class is derived from [**CIM\_Dependency**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4b86-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4b86-145">Requirements</span></span>



| <span data-ttu-id="e4b86-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4b86-146">Requirement</span></span> | <span data-ttu-id="e4b86-147">Value</span><span class="sxs-lookup"><span data-stu-id="e4b86-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b86-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4b86-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b86-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4b86-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e4b86-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4b86-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b86-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4b86-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e4b86-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e4b86-152">Namespace</span></span><br/>                | <span data-ttu-id="e4b86-153">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e4b86-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e4b86-154">MOF</span><span class="sxs-lookup"><span data-stu-id="e4b86-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4b86-155"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4b86-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4b86-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e4b86-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4b86-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4b86-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4b86-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4b86-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b86-159">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e4b86-159">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="e4b86-160">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e4b86-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

