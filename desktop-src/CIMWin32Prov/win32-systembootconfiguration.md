---
description: La \_ clase WMI SystemBootConfiguration Association de Win32 relaciona un equipo con su configuración de arranque.
ms.assetid: 1c6bce81-84d9-4949-92da-6111b4ecc939
ms.tgt_platform: multiple
title: Win32_SystemBootConfiguration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBootConfiguration
- Win32_SystemBootConfiguration.Element
- Win32_SystemBootConfiguration.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 863e4103f7e87681e25ccf53679bfe006ed3ff75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907249"
---
# <a name="win32_systembootconfiguration-class"></a><span data-ttu-id="22a7e-103">\_Clase Win32 SystemBootConfiguration</span><span class="sxs-lookup"><span data-stu-id="22a7e-103">Win32\_SystemBootConfiguration class</span></span>

<span data-ttu-id="22a7e-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemBootConfiguration** Association de Win32 relaciona un equipo con su configuración de arranque.</span><span class="sxs-lookup"><span data-stu-id="22a7e-104">The **Win32\_SystemBootConfiguration** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its boot configuration.</span></span>

<span data-ttu-id="22a7e-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="22a7e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="22a7e-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="22a7e-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="22a7e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22a7e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C507-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBootConfiguration : Win32_SystemSetting
{
  Win32_ComputerSystem    REF Element;
  Win32_BootConfiguration REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="22a7e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="22a7e-108">Members</span></span>

<span data-ttu-id="22a7e-109">La **clase \_ SystemBootConfiguration de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="22a7e-109">The **Win32\_SystemBootConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="22a7e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="22a7e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="22a7e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="22a7e-111">Properties</span></span>

<span data-ttu-id="22a7e-112">La **clase \_ SystemBootConfiguration de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="22a7e-112">The **Win32\_SystemBootConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22a7e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="22a7e-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a7e-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="22a7e-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="22a7e-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22a7e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22a7e-116">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="22a7e-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="22a7e-117">Referencia a la instancia de que representa el sistema del equipo mediante la configuración de arranque.</span><span class="sxs-lookup"><span data-stu-id="22a7e-117">Reference to the instance representing the computer system using the boot configuration.</span></span>

</dd> <dt>

<span data-ttu-id="22a7e-118">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="22a7e-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a7e-119">Tipo de datos: **Win32 \_ BootConfiguration**</span><span class="sxs-lookup"><span data-stu-id="22a7e-119">Data type: **Win32\_BootConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="22a7e-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22a7e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22a7e-121">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ BootConfiguration")</span><span class="sxs-lookup"><span data-stu-id="22a7e-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_BootConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="22a7e-122">Referencia a la instancia de que representa la configuración de arranque del equipo.</span><span class="sxs-lookup"><span data-stu-id="22a7e-122">Reference to the instance representing the boot configuration for the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22a7e-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22a7e-123">Remarks</span></span>

<span data-ttu-id="22a7e-124">La **clase \_ SystemBootConfiguration de Win32** se deriva de [**\_ SystemSetting de Win32**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="22a7e-124">The **Win32\_SystemBootConfiguration** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22a7e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22a7e-125">Requirements</span></span>



| <span data-ttu-id="22a7e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="22a7e-126">Requirement</span></span> | <span data-ttu-id="22a7e-127">Value</span><span class="sxs-lookup"><span data-stu-id="22a7e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22a7e-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22a7e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="22a7e-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22a7e-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="22a7e-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22a7e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="22a7e-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22a7e-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="22a7e-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="22a7e-132">Namespace</span></span><br/>                | <span data-ttu-id="22a7e-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="22a7e-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="22a7e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="22a7e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22a7e-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22a7e-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="22a7e-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="22a7e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22a7e-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22a7e-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22a7e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="22a7e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22a7e-139">**Win32 \_ SystemSetting**</span><span class="sxs-lookup"><span data-stu-id="22a7e-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="22a7e-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="22a7e-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
