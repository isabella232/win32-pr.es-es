---
description: La \_ clase WMI SystemBIOS Association de Win32 relaciona un equipo con (incluidos los datos, como las propiedades de inicio, las zonas horarias, las configuraciones de arranque o las contraseñas administrativas) y un BIOS del sistema (servicios, idiomas y propiedades de administración del sistema).
ms.assetid: 92747b1b-ef28-40ab-868a-6755aee8c723
ms.tgt_platform: multiple
title: Win32_SystemBIOS (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBIOS
- Win32_SystemBIOS.PartComponent
- Win32_SystemBIOS.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc8ec1f3526e2faefe0e63c9dea357accd025c13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907453"
---
# <a name="win32_systembios-class"></a><span data-ttu-id="68cac-103">\_Clase Win32 SystemBIOS</span><span class="sxs-lookup"><span data-stu-id="68cac-103">Win32\_SystemBIOS class</span></span>

<span data-ttu-id="68cac-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemBIOS** Association de Win32 relaciona un equipo con (incluidos los datos, como las propiedades de inicio, las zonas horarias, las configuraciones de arranque o las contraseñas administrativas) y un BIOS del sistema (servicios, idiomas y propiedades de administración del sistema).</span><span class="sxs-lookup"><span data-stu-id="68cac-104">The **Win32\_SystemBIOS** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system (including data such as startup properties, time zones, boot configurations, or administrative passwords), and a system BIOS (services, languages, and system management properties).</span></span>

<span data-ttu-id="68cac-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="68cac-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="68cac-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="68cac-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68cac-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68cac-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBIOS : CIM_SystemComponent
{
  Win32_BIOS           REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="68cac-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="68cac-108">Members</span></span>

<span data-ttu-id="68cac-109">La **clase \_ SystemBIOS de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="68cac-109">The **Win32\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="68cac-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="68cac-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68cac-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="68cac-111">Properties</span></span>

<span data-ttu-id="68cac-112">La **clase \_ SystemBIOS de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="68cac-112">The **Win32\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68cac-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="68cac-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68cac-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="68cac-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="68cac-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68cac-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68cac-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="68cac-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="68cac-117">El [**\_ ComputerSystem de Win32**](win32-computersystemprocessor.md) que contiene el BIOS de la asociación.</span><span class="sxs-lookup"><span data-stu-id="68cac-117">The [**Win32\_ComputerSystem**](win32-computersystemprocessor.md) containing the BIOS of the association.</span></span>

</dd> <dt>

<span data-ttu-id="68cac-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="68cac-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68cac-119">Tipo de datos **: \_ BIOS Win32**</span><span class="sxs-lookup"><span data-stu-id="68cac-119">Data type: **Win32\_BIOS**</span></span>
</dt> <dt>

<span data-ttu-id="68cac-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68cac-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68cac-121">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ BIOS")</span><span class="sxs-lookup"><span data-stu-id="68cac-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_BIOS")</span></span>
</dt> </dl>

<span data-ttu-id="68cac-122">[**\_ BIOS Win32**](win32-bios.md) incluido en el sistema del equipo de esta asociación.</span><span class="sxs-lookup"><span data-stu-id="68cac-122">A [**Win32\_BIOS**](win32-bios.md) contained in the computer system of this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68cac-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68cac-123">Remarks</span></span>

<span data-ttu-id="68cac-124">La **clase \_ SystemBIOS de Win32** se deriva de [**\_ SystemComponent de CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="68cac-124">The **Win32\_SystemBIOS** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68cac-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68cac-125">Requirements</span></span>



| <span data-ttu-id="68cac-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="68cac-126">Requirement</span></span> | <span data-ttu-id="68cac-127">Value</span><span class="sxs-lookup"><span data-stu-id="68cac-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68cac-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68cac-128">Minimum supported client</span></span><br/> | <span data-ttu-id="68cac-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68cac-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68cac-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68cac-130">Minimum supported server</span></span><br/> | <span data-ttu-id="68cac-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68cac-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68cac-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="68cac-132">Namespace</span></span><br/>                | <span data-ttu-id="68cac-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="68cac-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68cac-134">MOF</span><span class="sxs-lookup"><span data-stu-id="68cac-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68cac-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68cac-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68cac-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68cac-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68cac-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68cac-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68cac-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="68cac-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68cac-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="68cac-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="68cac-140">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="68cac-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
