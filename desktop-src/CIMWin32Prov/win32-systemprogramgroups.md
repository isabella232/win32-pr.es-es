---
description: La \_ clase WMI SystemProgramGroups Association de Win32 relaciona un equipo y un grupo de programas lógicos.
ms.assetid: cbf810c8-a967-4d60-889c-e47c43b039ea
ms.tgt_platform: multiple
title: Win32_SystemProgramGroups (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProgramGroups
- Win32_SystemProgramGroups.Element
- Win32_SystemProgramGroups.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1a8ca556c24295e2c4b04ab851610ef35ec9b715
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153485"
---
# <a name="win32_systemprogramgroups-class"></a><span data-ttu-id="6135d-103">\_Clase Win32 SystemProgramGroups</span><span class="sxs-lookup"><span data-stu-id="6135d-103">Win32\_SystemProgramGroups class</span></span>

<span data-ttu-id="6135d-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemProgramGroups** Association de Win32 relaciona un equipo y un grupo de programas lógicos.</span><span class="sxs-lookup"><span data-stu-id="6135d-104">The **Win32\_SystemProgramGroups** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a logical program group.</span></span>

<span data-ttu-id="6135d-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6135d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6135d-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="6135d-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6135d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6135d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C505-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProgramGroups : Win32_SystemSetting
{
  Win32_ComputerSystem      REF Element;
  Win32_LogicalProgramGroup REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="6135d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6135d-108">Members</span></span>

<span data-ttu-id="6135d-109">La **clase \_ SystemProgramGroups de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6135d-109">The **Win32\_SystemProgramGroups** class has these types of members:</span></span>

-   [<span data-ttu-id="6135d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6135d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6135d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6135d-111">Properties</span></span>

<span data-ttu-id="6135d-112">La **clase \_ SystemProgramGroups de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6135d-112">The **Win32\_SystemProgramGroups** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6135d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6135d-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6135d-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="6135d-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="6135d-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6135d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6135d-116">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="6135d-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="6135d-117">Referencia a la instancia de que representa el sistema del equipo que contiene el grupo de programas lógicos.</span><span class="sxs-lookup"><span data-stu-id="6135d-117">Reference to the instance representing the computer system containing the logical program group.</span></span>

</dd> <dt>

<span data-ttu-id="6135d-118">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="6135d-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6135d-119">Tipo de datos: **Win32 \_ LogicalProgramGroup**</span><span class="sxs-lookup"><span data-stu-id="6135d-119">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="6135d-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6135d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6135d-121">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LogicalProgramGroup")</span><span class="sxs-lookup"><span data-stu-id="6135d-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="6135d-122">Referencia a la instancia de que representa el grupo de programas lógicos del equipo.</span><span class="sxs-lookup"><span data-stu-id="6135d-122">Reference to the instance representing the logical program group on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6135d-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6135d-123">Remarks</span></span>

<span data-ttu-id="6135d-124">La **clase \_ SystemProgramGroups de Win32** se deriva de [**\_ SystemSetting de Win32**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="6135d-124">The **Win32\_SystemProgramGroups** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6135d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6135d-125">Requirements</span></span>



| <span data-ttu-id="6135d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6135d-126">Requirement</span></span> | <span data-ttu-id="6135d-127">Value</span><span class="sxs-lookup"><span data-stu-id="6135d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6135d-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6135d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6135d-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6135d-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6135d-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6135d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6135d-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6135d-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6135d-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6135d-132">Namespace</span></span><br/>                | <span data-ttu-id="6135d-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6135d-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6135d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6135d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6135d-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6135d-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6135d-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6135d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6135d-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6135d-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6135d-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="6135d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6135d-139">**Win32 \_ SystemSetting**</span><span class="sxs-lookup"><span data-stu-id="6135d-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="6135d-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="6135d-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
