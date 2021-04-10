---
description: La \_ clase WMI SystemOperatingSystem Association de Win32 relaciona un equipo y su sistema operativo.
ms.assetid: dc71f80b-6fbd-4bc8-8783-3922d8050518
ms.tgt_platform: multiple
title: Win32_SystemOperatingSystem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemOperatingSystem
- Win32_SystemOperatingSystem.PrimaryOS
- Win32_SystemOperatingSystem.GroupComponent
- Win32_SystemOperatingSystem.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba3f8ac94ec882ee1df96da51d93d2c24fde9b3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153492"
---
# <a name="win32_systemoperatingsystem-class"></a><span data-ttu-id="3b0b2-103">\_Clase Win32 SystemOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3b0b2-103">Win32\_SystemOperatingSystem class</span></span>

<span data-ttu-id="3b0b2-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemOperatingSystem** Association de Win32 relaciona un equipo y su sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3b0b2-104">The **Win32\_SystemOperatingSystem** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its operating system.</span></span>

<span data-ttu-id="3b0b2-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3b0b2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3b0b2-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3b0b2-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b0b2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b0b2-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemOperatingSystem : CIM_InstalledOS
{
  boolean                   PrimaryOS;
  Win32_ComputerSystem  REF GroupComponent;
  Win32_OperatingSystem REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="3b0b2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3b0b2-108">Members</span></span>

<span data-ttu-id="3b0b2-109">La **clase \_ SystemOperatingSystem de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3b0b2-109">The **Win32\_SystemOperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="3b0b2-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3b0b2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b0b2-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3b0b2-111">Properties</span></span>

<span data-ttu-id="3b0b2-112">La **clase \_ SystemOperatingSystem de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3b0b2-112">The **Win32\_SystemOperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b0b2-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3b0b2-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b0b2-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="3b0b2-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="3b0b2-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b0b2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b0b2-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="3b0b2-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="3b0b2-117">Un [**\_ ComputerSystem de Win32**](win32-computersystemprocessor.md) que describe las propiedades del sistema del equipo en el que está instalado el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3b0b2-117">A [**Win32\_ComputerSystem**](win32-computersystemprocessor.md) that describes the properties of the computer system upon which the operating system is installed.</span></span>

</dd> <dt>

<span data-ttu-id="3b0b2-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3b0b2-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b0b2-119">Tipo de datos: **Win32 \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="3b0b2-119">Data type: **Win32\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="3b0b2-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b0b2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b0b2-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ OperatingSystem")</span><span class="sxs-lookup"><span data-stu-id="3b0b2-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_OperatingSystem")</span></span>
</dt> </dl>

<span data-ttu-id="3b0b2-122">Un [**\_ OperatingSystem de Win32**](win32-operatingsystem.md) que describe las propiedades del sistema operativo que se ejecuta en este equipo.</span><span class="sxs-lookup"><span data-stu-id="3b0b2-122">A [**Win32\_OperatingSystem**](win32-operatingsystem.md) that describes properties of the operating system running on this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="3b0b2-123">**Principalesos**</span><span class="sxs-lookup"><span data-stu-id="3b0b2-123">**PrimaryOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b0b2-124">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3b0b2-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b0b2-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b0b2-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b0b2-126">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sistema operativo DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="3b0b2-126">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operating System\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="3b0b2-127">Si es **true**, el sistema operativo instalado es el sistema operativo predeterminado del equipo.</span><span class="sxs-lookup"><span data-stu-id="3b0b2-127">If **TRUE**, the installed operating system is the default operating system for the computer system.</span></span>

<span data-ttu-id="3b0b2-128">Esta propiedad se hereda de [**los \_ instaladores de CIM**](cim-installedos.md).</span><span class="sxs-lookup"><span data-stu-id="3b0b2-128">This property is inherited from [**CIM\_InstalledOS**](cim-installedos.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b0b2-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b0b2-129">Remarks</span></span>

<span data-ttu-id="3b0b2-130">La **clase \_ SystemOperatingSystem de Win32** se deriva de los [**\_ instaladores de CIM**](cim-installedos.md).</span><span class="sxs-lookup"><span data-stu-id="3b0b2-130">The **Win32\_SystemOperatingSystem** class is derived from [**CIM\_InstalledOS**](cim-installedos.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b0b2-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b0b2-131">Requirements</span></span>



| <span data-ttu-id="3b0b2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b0b2-132">Requirement</span></span> | <span data-ttu-id="3b0b2-133">Value</span><span class="sxs-lookup"><span data-stu-id="3b0b2-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b0b2-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b0b2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3b0b2-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b0b2-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b0b2-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b0b2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3b0b2-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b0b2-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b0b2-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3b0b2-138">Namespace</span></span><br/>                | <span data-ttu-id="3b0b2-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3b0b2-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3b0b2-140">MOF</span><span class="sxs-lookup"><span data-stu-id="3b0b2-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b0b2-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b0b2-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b0b2-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b0b2-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b0b2-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b0b2-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b0b2-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b0b2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b0b2-145">**\_Instalado CIM**</span><span class="sxs-lookup"><span data-stu-id="3b0b2-145">**CIM\_InstalledOS**</span></span>](cim-installedos.md)
</dt> <dt>

[<span data-ttu-id="3b0b2-146">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3b0b2-146">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
