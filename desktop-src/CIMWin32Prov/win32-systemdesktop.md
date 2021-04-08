---
description: La \_ clase WMI SystemDesktop Association de Win32 relaciona un equipo con la configuración del escritorio.
ms.assetid: 2b024660-d707-4463-8207-73df74bfa7d6
ms.tgt_platform: multiple
title: Win32_SystemDesktop (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDesktop
- Win32_SystemDesktop.Element
- Win32_SystemDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e14cab58a445fd645b9d59c1aea713bf6c40ac0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000786"
---
# <a name="win32_systemdesktop-class"></a><span data-ttu-id="1a108-103">\_Clase Win32 SystemDesktop</span><span class="sxs-lookup"><span data-stu-id="1a108-103">Win32\_SystemDesktop class</span></span>

<span data-ttu-id="1a108-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemDesktop** Association de Win32 relaciona un equipo con la configuración del escritorio.</span><span class="sxs-lookup"><span data-stu-id="1a108-104">The **Win32\_SystemDesktop** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and its desktop configuration.</span></span>

<span data-ttu-id="1a108-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1a108-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1a108-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="1a108-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a108-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a108-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C506-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDesktop : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_Desktop        REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="1a108-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1a108-108">Members</span></span>

<span data-ttu-id="1a108-109">La **clase \_ SystemDesktop de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1a108-109">The **Win32\_SystemDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="1a108-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a108-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a108-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a108-111">Properties</span></span>

<span data-ttu-id="1a108-112">La **clase \_ SystemDesktop de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1a108-112">The **Win32\_SystemDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a108-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1a108-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a108-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="1a108-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="1a108-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a108-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a108-116">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="1a108-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="1a108-117">Referencia a la instancia de que representa el sistema del equipo en el que existe la configuración de escritorio.</span><span class="sxs-lookup"><span data-stu-id="1a108-117">Reference to the instance representing the computer system where the desktop configuration exists.</span></span>

</dd> <dt>

<span data-ttu-id="1a108-118">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="1a108-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a108-119">Tipo de datos **: \_ escritorio Win32**</span><span class="sxs-lookup"><span data-stu-id="1a108-119">Data type: **Win32\_Desktop**</span></span>
</dt> <dt>

<span data-ttu-id="1a108-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a108-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a108-121">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Desktop")</span><span class="sxs-lookup"><span data-stu-id="1a108-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="1a108-122">Referencia a la instancia de que representa la configuración existente en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="1a108-122">Reference to the instance representing the configuration existing on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a108-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a108-123">Remarks</span></span>

<span data-ttu-id="1a108-124">La **clase \_ SystemDesktop de Win32** se deriva de [**\_ SystemSetting de Win32**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="1a108-124">The **Win32\_SystemDesktop** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a108-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a108-125">Requirements</span></span>



| <span data-ttu-id="1a108-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a108-126">Requirement</span></span> | <span data-ttu-id="1a108-127">Value</span><span class="sxs-lookup"><span data-stu-id="1a108-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a108-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a108-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1a108-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a108-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1a108-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a108-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1a108-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a108-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1a108-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1a108-132">Namespace</span></span><br/>                | <span data-ttu-id="1a108-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1a108-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1a108-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1a108-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a108-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a108-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a108-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1a108-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a108-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a108-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a108-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a108-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a108-139">**Win32 \_ SystemSetting**</span><span class="sxs-lookup"><span data-stu-id="1a108-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="1a108-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="1a108-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
