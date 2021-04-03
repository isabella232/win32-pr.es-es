---
description: La \_ clase WMI SystemTimeZone Association de Win32 relaciona un equipo y una zona horaria.
ms.assetid: 53c74a61-c91d-4daa-933e-4cc7b9583d98
ms.tgt_platform: multiple
title: Win32_SystemTimeZone (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemTimeZone
- Win32_SystemTimeZone.Element
- Win32_SystemTimeZone.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ec294600fdc81f085bf29f5e664bcbec961417c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907244"
---
# <a name="win32_systemtimezone-class"></a><span data-ttu-id="6e6e8-103">\_Clase Win32 SystemTimeZone</span><span class="sxs-lookup"><span data-stu-id="6e6e8-103">Win32\_SystemTimeZone class</span></span>

<span data-ttu-id="6e6e8-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemTimeZone** Association de Win32 relaciona un equipo y una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="6e6e8-104">The **Win32\_SystemTimeZone** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a time zone.</span></span>

<span data-ttu-id="6e6e8-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6e6e8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6e6e8-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="6e6e8-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e6e8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e6e8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C504-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemTimeZone : Win32_SystemSetting
{
  Win32_ComputerSystem REF Element;
  Win32_TimeZone       REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="6e6e8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6e6e8-108">Members</span></span>

<span data-ttu-id="6e6e8-109">La **clase \_ SystemTimeZone de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6e6e8-109">The **Win32\_SystemTimeZone** class has these types of members:</span></span>

-   [<span data-ttu-id="6e6e8-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6e6e8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6e6e8-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6e6e8-111">Properties</span></span>

<span data-ttu-id="6e6e8-112">La **clase \_ SystemTimeZone de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6e6e8-112">The **Win32\_SystemTimeZone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e6e8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6e6e8-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e6e8-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="6e6e8-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="6e6e8-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6e6e8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e6e8-116">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="6e6e8-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="6e6e8-117">Referencia a la instancia de que representa el sistema del equipo que realiza el seguimiento de la zona horaria del sistema.</span><span class="sxs-lookup"><span data-stu-id="6e6e8-117">Reference to the instance representing the computer system keeping track of the system time zone.</span></span>

</dd> <dt>

<span data-ttu-id="6e6e8-118">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="6e6e8-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e6e8-119">Tipo de datos **: \_ zona horaria de Win32**</span><span class="sxs-lookup"><span data-stu-id="6e6e8-119">Data type: **Win32\_TimeZone**</span></span>
</dt> <dt>

<span data-ttu-id="6e6e8-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6e6e8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e6e8-121">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ TimeZone")</span><span class="sxs-lookup"><span data-stu-id="6e6e8-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_TimeZone")</span></span>
</dt> </dl>

<span data-ttu-id="6e6e8-122">Referencia a la instancia de que representa las propiedades de zona horaria cuyo seguimiento realiza el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="6e6e8-122">Reference to the instance representing the time zone properties tracked by the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e6e8-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e6e8-123">Remarks</span></span>

<span data-ttu-id="6e6e8-124">La **clase \_ SystemTimeZone de Win32** se deriva de [**\_ SystemSetting de Win32**](win32-systemsetting.md).</span><span class="sxs-lookup"><span data-stu-id="6e6e8-124">The **Win32\_SystemTimeZone** class is derived from [**Win32\_SystemSetting**](win32-systemsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e6e8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e6e8-125">Requirements</span></span>



| <span data-ttu-id="6e6e8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e6e8-126">Requirement</span></span> | <span data-ttu-id="6e6e8-127">Value</span><span class="sxs-lookup"><span data-stu-id="6e6e8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e6e8-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e6e8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6e6e8-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e6e8-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6e6e8-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e6e8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6e6e8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e6e8-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6e6e8-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6e6e8-132">Namespace</span></span><br/>                | <span data-ttu-id="6e6e8-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6e6e8-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6e6e8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6e6e8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e6e8-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e6e8-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e6e8-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e6e8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e6e8-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e6e8-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e6e8-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e6e8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e6e8-139">**Win32 \_ SystemSetting**</span><span class="sxs-lookup"><span data-stu-id="6e6e8-139">**Win32\_SystemSetting**</span></span>](win32-systemsetting.md)
</dt> <dt>

[<span data-ttu-id="6e6e8-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="6e6e8-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
