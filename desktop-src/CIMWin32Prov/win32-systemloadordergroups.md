---
description: La \_ clase WMI SystemLoadOrderGroups Association de Win32 relaciona un equipo y un grupo de pedidos de carga.
ms.assetid: fb637300-0f70-465a-a72b-f0ab3f246790
ms.tgt_platform: multiple
title: Win32_SystemLoadOrderGroups (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemLoadOrderGroups
- Win32_SystemLoadOrderGroups.GroupComponent
- Win32_SystemLoadOrderGroups.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 510acfbde2f562493a454abe80a4f7788377e556
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659725"
---
# <a name="win32_systemloadordergroups-class"></a><span data-ttu-id="6e672-103">\_Clase Win32 SystemLoadOrderGroups</span><span class="sxs-lookup"><span data-stu-id="6e672-103">Win32\_SystemLoadOrderGroups class</span></span>

<span data-ttu-id="6e672-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemLoadOrderGroups** Association de Win32 relaciona un equipo y un grupo de pedidos de carga.</span><span class="sxs-lookup"><span data-stu-id="6e672-104">The **Win32\_SystemLoadOrderGroups** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a load order group.</span></span>

<span data-ttu-id="6e672-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6e672-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6e672-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="6e672-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e672-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e672-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C503-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemLoadOrderGroups : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_LoadOrderGroup REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="6e672-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6e672-108">Members</span></span>

<span data-ttu-id="6e672-109">La **clase \_ SystemLoadOrderGroups de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6e672-109">The **Win32\_SystemLoadOrderGroups** class has these types of members:</span></span>

-   [<span data-ttu-id="6e672-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6e672-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6e672-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6e672-111">Properties</span></span>

<span data-ttu-id="6e672-112">La **clase \_ SystemLoadOrderGroups de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6e672-112">The **Win32\_SystemLoadOrderGroups** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e672-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="6e672-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e672-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="6e672-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="6e672-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6e672-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e672-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="6e672-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="6e672-117">Referencia a la instancia de que representa el sistema del equipo en el que existe el grupo de orden de carga.</span><span class="sxs-lookup"><span data-stu-id="6e672-117">Reference to the instance representing the computer system where the load order group exists.</span></span>

</dd> <dt>

<span data-ttu-id="6e672-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="6e672-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e672-119">Tipo de datos: **Win32 \_ LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="6e672-119">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="6e672-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6e672-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e672-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LoadOrderGroup")</span><span class="sxs-lookup"><span data-stu-id="6e672-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="6e672-122">Referencia a la instancia de que representa el grupo de orden de carga existente en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="6e672-122">Reference to the instance representing the load order group existing on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e672-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e672-123">Remarks</span></span>

<span data-ttu-id="6e672-124">La **clase \_ SystemLoadOrderGroups de Win32** se deriva de [**\_ SystemComponent de CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="6e672-124">The **Win32\_SystemLoadOrderGroups** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e672-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e672-125">Requirements</span></span>



| <span data-ttu-id="6e672-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e672-126">Requirement</span></span> | <span data-ttu-id="6e672-127">Value</span><span class="sxs-lookup"><span data-stu-id="6e672-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e672-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e672-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6e672-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e672-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6e672-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e672-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6e672-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e672-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6e672-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6e672-132">Namespace</span></span><br/>                | <span data-ttu-id="6e672-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6e672-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6e672-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6e672-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e672-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e672-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e672-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e672-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e672-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e672-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e672-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e672-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e672-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="6e672-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="6e672-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="6e672-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
