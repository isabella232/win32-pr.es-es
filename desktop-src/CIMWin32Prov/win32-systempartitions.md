---
description: La \_ clase WMI SystemPartitions Association de Win32 relaciona un equipo y una partición de disco en ese sistema.
ms.assetid: e8f02cd0-9446-4258-b476-5dc6c72c80d4
ms.tgt_platform: multiple
title: Win32_SystemPartitions (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemPartitions
- Win32_SystemPartitions.GroupComponent
- Win32_SystemPartitions.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deae8129772e5d854f05b5b953ec66a12bd5bcaf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907247"
---
# <a name="win32_systempartitions-class"></a><span data-ttu-id="1df10-103">\_Clase Win32 SystemPartitions</span><span class="sxs-lookup"><span data-stu-id="1df10-103">Win32\_SystemPartitions class</span></span>

<span data-ttu-id="1df10-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemPartitions** Association de Win32 relaciona un equipo y una partición de disco en ese sistema.</span><span class="sxs-lookup"><span data-stu-id="1df10-104">The **Win32\_SystemPartitions** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a disk partition on that system.</span></span>

<span data-ttu-id="1df10-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1df10-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1df10-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="1df10-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1df10-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1df10-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemPartitions : Win32_SystemDevices
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_DiskPartition  REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="1df10-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1df10-108">Members</span></span>

<span data-ttu-id="1df10-109">La **clase \_ SystemPartitions de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1df10-109">The **Win32\_SystemPartitions** class has these types of members:</span></span>

-   [<span data-ttu-id="1df10-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1df10-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1df10-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1df10-111">Properties</span></span>

<span data-ttu-id="1df10-112">La **clase \_ SystemPartitions de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1df10-112">The **Win32\_SystemPartitions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1df10-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="1df10-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1df10-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="1df10-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="1df10-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1df10-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1df10-116">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="1df10-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="1df10-117">Referencia a la instancia de que representa las propiedades del sistema del equipo donde se encuentra la partición de disco.</span><span class="sxs-lookup"><span data-stu-id="1df10-117">Reference to the instance representing the properties of the computer system where the disk partition is located.</span></span>

</dd> <dt>

<span data-ttu-id="1df10-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="1df10-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1df10-119">Tipo de datos: **Win32 \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="1df10-119">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="1df10-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1df10-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1df10-121">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ DiskPartition")</span><span class="sxs-lookup"><span data-stu-id="1df10-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="1df10-122">Referencia a la instancia de que representa las propiedades de una partición de disco que existe en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="1df10-122">Reference to the instance representing the properties of a disk partition that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1df10-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1df10-123">Remarks</span></span>

<span data-ttu-id="1df10-124">La **clase \_ SystemPartitions de Win32** se deriva de [**\_ SystemDevices de Win32**](win32-systemdevices.md).</span><span class="sxs-lookup"><span data-stu-id="1df10-124">The **Win32\_SystemPartitions** class is derived from [**Win32\_SystemDevices**](win32-systemdevices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1df10-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1df10-125">Requirements</span></span>



| <span data-ttu-id="1df10-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1df10-126">Requirement</span></span> | <span data-ttu-id="1df10-127">Value</span><span class="sxs-lookup"><span data-stu-id="1df10-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1df10-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1df10-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1df10-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1df10-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1df10-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1df10-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1df10-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1df10-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1df10-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1df10-132">Namespace</span></span><br/>                | <span data-ttu-id="1df10-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1df10-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1df10-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1df10-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1df10-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1df10-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1df10-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1df10-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1df10-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1df10-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1df10-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="1df10-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df10-139">**Win32 \_ SystemDevices**</span><span class="sxs-lookup"><span data-stu-id="1df10-139">**Win32\_SystemDevices**</span></span>](win32-systemdevices.md)
</dt> <dt>

[<span data-ttu-id="1df10-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="1df10-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
