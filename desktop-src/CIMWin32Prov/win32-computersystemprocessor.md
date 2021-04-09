---
description: La \_ clase WMI ComputerSystemProcessor Association de Win32 relaciona un equipo y un procesador que se ejecutan en ese sistema.
ms.assetid: e630ebea-19bf-43c7-a8a0-7acfda3a752b
ms.tgt_platform: multiple
title: Win32_ComputerSystemProcessor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProcessor
- Win32_ComputerSystemProcessor.PartComponent
- Win32_ComputerSystemProcessor.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2f836d8f5e9053029763c38d2c4f2116987b08fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152919"
---
# <a name="win32_computersystemprocessor-class"></a><span data-ttu-id="28eac-103">\_Clase Win32 ComputerSystemProcessor</span><span class="sxs-lookup"><span data-stu-id="28eac-103">Win32\_ComputerSystemProcessor class</span></span>

<span data-ttu-id="28eac-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ComputerSystemProcessor** Association de Win32 relaciona un equipo y un procesador que se ejecutan en ese sistema.</span><span class="sxs-lookup"><span data-stu-id="28eac-104">The **Win32\_ComputerSystemProcessor** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a computer system and a processor running on that system.</span></span>

<span data-ttu-id="28eac-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="28eac-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="28eac-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="28eac-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="28eac-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28eac-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{719A6839-C124-11d2-85E8-0000F8102E5F}"), AMENDMENT]
class Win32_ComputerSystemProcessor : Win32_SystemDevices
{
  Win32_Processor      REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="28eac-108">Members</span><span class="sxs-lookup"><span data-stu-id="28eac-108">Members</span></span>

<span data-ttu-id="28eac-109">La **clase \_ ComputerSystemProcessor de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="28eac-109">The **Win32\_ComputerSystemProcessor** class has these types of members:</span></span>

-   [<span data-ttu-id="28eac-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="28eac-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="28eac-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="28eac-111">Properties</span></span>

<span data-ttu-id="28eac-112">La **clase \_ ComputerSystemProcessor de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="28eac-112">The **Win32\_ComputerSystemProcessor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="28eac-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="28eac-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28eac-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="28eac-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="28eac-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="28eac-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28eac-116">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="28eac-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="28eac-117">Un **\_ ComputerSystem de Win32** que describe las propiedades del equipo en el que se está ejecutando el procesador.</span><span class="sxs-lookup"><span data-stu-id="28eac-117">A **Win32\_ComputerSystem** that describes the properties of the computer system on which the processor is running.</span></span>

</dd> <dt>

<span data-ttu-id="28eac-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="28eac-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28eac-119">Tipo de datos **: \_ procesador Win32**</span><span class="sxs-lookup"><span data-stu-id="28eac-119">Data type: **Win32\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="28eac-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="28eac-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28eac-121">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| procesador Win32 de WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="28eac-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Processor")</span></span>
</dt> </dl>

<span data-ttu-id="28eac-122">[**\_ Procesador Win32**](win32-processor.md) que describe las propiedades de un procesador que ejecuta el sistema informático.</span><span class="sxs-lookup"><span data-stu-id="28eac-122">A [**Win32\_Processor**](win32-processor.md) that describes the properties of a processor which is running the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28eac-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28eac-123">Remarks</span></span>

<span data-ttu-id="28eac-124">La **clase \_ ComputerSystemProcessor de Win32** se deriva de [**\_ SystemDevices de Win32**](win32-systemdevices.md).</span><span class="sxs-lookup"><span data-stu-id="28eac-124">The **Win32\_ComputerSystemProcessor** class is derived from [**Win32\_SystemDevices**](win32-systemdevices.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="28eac-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28eac-125">Requirements</span></span>



| <span data-ttu-id="28eac-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="28eac-126">Requirement</span></span> | <span data-ttu-id="28eac-127">Value</span><span class="sxs-lookup"><span data-stu-id="28eac-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28eac-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28eac-128">Minimum supported client</span></span><br/> | <span data-ttu-id="28eac-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28eac-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="28eac-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28eac-130">Minimum supported server</span></span><br/> | <span data-ttu-id="28eac-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28eac-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="28eac-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="28eac-132">Namespace</span></span><br/>                | <span data-ttu-id="28eac-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="28eac-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="28eac-134">MOF</span><span class="sxs-lookup"><span data-stu-id="28eac-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28eac-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28eac-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="28eac-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28eac-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28eac-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28eac-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28eac-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="28eac-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28eac-139">**Win32 \_ SystemDevices**</span><span class="sxs-lookup"><span data-stu-id="28eac-139">**Win32\_SystemDevices**</span></span>](win32-systemdevices.md)
</dt> <dt>

<span data-ttu-id="28eac-140">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="28eac-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

