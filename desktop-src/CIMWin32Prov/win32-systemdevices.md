---
description: La \_ clase WMI SystemDevices Association de Win32 relaciona un equipo y un dispositivo lógico instalado en ese sistema.
ms.assetid: 84dfcb75-3b44-4b27-8eee-779be522eb1f
ms.tgt_platform: multiple
title: Win32_SystemDevices (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDevices
- Win32_SystemDevices.GroupComponent
- Win32_SystemDevices.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2b28c11e10318e3bca562baf93bc20df9b756cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907452"
---
# <a name="win32_systemdevices-class"></a><span data-ttu-id="f6edc-103">\_Clase Win32 SystemDevices</span><span class="sxs-lookup"><span data-stu-id="f6edc-103">Win32\_SystemDevices class</span></span>

<span data-ttu-id="f6edc-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemDevices** Association de Win32 relaciona un equipo y un dispositivo lógico instalado en ese sistema.</span><span class="sxs-lookup"><span data-stu-id="f6edc-104">The **Win32\_SystemDevices** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a logical device installed on that system.</span></span>

<span data-ttu-id="f6edc-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f6edc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f6edc-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f6edc-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6edc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6edc-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDevices : CIM_SystemDevice
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_LogicalDevice    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="f6edc-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f6edc-108">Members</span></span>

<span data-ttu-id="f6edc-109">La **clase \_ SystemDevices de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f6edc-109">The **Win32\_SystemDevices** class has these types of members:</span></span>

-   [<span data-ttu-id="f6edc-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6edc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6edc-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6edc-111">Properties</span></span>

<span data-ttu-id="f6edc-112">La **clase \_ SystemDevices de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f6edc-112">The **Win32\_SystemDevices** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6edc-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="f6edc-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6edc-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="f6edc-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="f6edc-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6edc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6edc-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="f6edc-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="f6edc-117">Referencia a la instancia de que representa las propiedades del sistema del equipo en el que existe el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f6edc-117">Reference to the instance representing the properties of the computer system where the logical device exists.</span></span>

</dd> <dt>

<span data-ttu-id="f6edc-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="f6edc-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6edc-119">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="f6edc-119">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="f6edc-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6edc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6edc-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| lógico CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="f6edc-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="f6edc-122">Referencia a la instancia de que representa las propiedades de un dispositivo lógico que existe en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="f6edc-122">Reference to the instance representing the properties of a logical device that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6edc-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6edc-123">Remarks</span></span>

<span data-ttu-id="f6edc-124">La **clase \_ SystemDevices de Win32** se deriva de [**\_ SystemDevice de CIM**](cim-systemdevice.md).</span><span class="sxs-lookup"><span data-stu-id="f6edc-124">The **Win32\_SystemDevices** class is derived from [**CIM\_SystemDevice**](cim-systemdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6edc-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6edc-125">Requirements</span></span>



| <span data-ttu-id="f6edc-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6edc-126">Requirement</span></span> | <span data-ttu-id="f6edc-127">Value</span><span class="sxs-lookup"><span data-stu-id="f6edc-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6edc-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6edc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f6edc-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6edc-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f6edc-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6edc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f6edc-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6edc-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f6edc-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f6edc-132">Namespace</span></span><br/>                | <span data-ttu-id="f6edc-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f6edc-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f6edc-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f6edc-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6edc-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6edc-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6edc-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6edc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6edc-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6edc-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6edc-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6edc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6edc-139">**\_SYSTEMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="f6edc-139">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dt>

[<span data-ttu-id="f6edc-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f6edc-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
