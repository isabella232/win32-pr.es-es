---
description: La \_ clase WMI SystemProcesses Association de Win32 relaciona un equipo y un proceso que se ejecutan en ese sistema.
ms.assetid: 0d8c3ec6-265e-4486-8e94-f5acd2845cf5
ms.tgt_platform: multiple
title: Win32_SystemProcesses (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProcesses
- Win32_SystemProcesses.GroupComponent
- Win32_SystemProcesses.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b963aea5d9c651e27dc4380200e40dd3dcb9a77
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080203"
---
# <a name="win32_systemprocesses-class"></a><span data-ttu-id="ec7e4-103">\_Clase Win32 SystemProcesses</span><span class="sxs-lookup"><span data-stu-id="ec7e4-103">Win32\_SystemProcesses class</span></span>

<span data-ttu-id="ec7e4-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemProcesses** Association de Win32 relaciona un equipo y un proceso que se ejecutan en ese sistema.</span><span class="sxs-lookup"><span data-stu-id="ec7e4-104">The **Win32\_SystemProcesses** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a process running on that system.</span></span>

<span data-ttu-id="ec7e4-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ec7e4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ec7e4-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="ec7e4-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec7e4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec7e4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProcesses : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_Process        REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="ec7e4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ec7e4-108">Members</span></span>

<span data-ttu-id="ec7e4-109">La **clase \_ SystemProcesses de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ec7e4-109">The **Win32\_SystemProcesses** class has these types of members:</span></span>

-   [<span data-ttu-id="ec7e4-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ec7e4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec7e4-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ec7e4-111">Properties</span></span>

<span data-ttu-id="ec7e4-112">La **clase \_ SystemProcesses de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ec7e4-112">The **Win32\_SystemProcesses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec7e4-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="ec7e4-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec7e4-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="ec7e4-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="ec7e4-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ec7e4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec7e4-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="ec7e4-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="ec7e4-117">Referencia a la instancia de que representa el sistema del equipo en el que se está ejecutando el proceso.</span><span class="sxs-lookup"><span data-stu-id="ec7e4-117">Reference to the instance representing the computer system upon which the process is running.</span></span>

</dd> <dt>

<span data-ttu-id="ec7e4-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="ec7e4-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec7e4-119">Tipo de datos **: \_ proceso Win32**</span><span class="sxs-lookup"><span data-stu-id="ec7e4-119">Data type: **Win32\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="ec7e4-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ec7e4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec7e4-121">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Process")</span><span class="sxs-lookup"><span data-stu-id="ec7e4-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Process")</span></span>
</dt> </dl>

<span data-ttu-id="ec7e4-122">Referencia a la instancia de que representa el proceso que se está ejecutando en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="ec7e4-122">Reference to the instance representing the process running on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec7e4-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec7e4-123">Remarks</span></span>

<span data-ttu-id="ec7e4-124">La **clase \_ SystemProcesses de Win32** se deriva de [**\_ SystemComponent de CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="ec7e4-124">The **Win32\_SystemProcesses** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec7e4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec7e4-125">Requirements</span></span>



| <span data-ttu-id="ec7e4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec7e4-126">Requirement</span></span> | <span data-ttu-id="ec7e4-127">Value</span><span class="sxs-lookup"><span data-stu-id="ec7e4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7e4-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec7e4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ec7e4-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec7e4-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ec7e4-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec7e4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ec7e4-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec7e4-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ec7e4-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ec7e4-132">Namespace</span></span><br/>                | <span data-ttu-id="ec7e4-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ec7e4-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ec7e4-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ec7e4-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec7e4-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec7e4-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec7e4-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ec7e4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec7e4-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec7e4-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec7e4-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec7e4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec7e4-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="ec7e4-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="ec7e4-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="ec7e4-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
