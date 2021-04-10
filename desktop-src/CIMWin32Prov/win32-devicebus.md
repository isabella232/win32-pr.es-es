---
description: La \_ clase WMI DeviceBus Association de Win32 relaciona un bus del sistema y un dispositivo lógico mediante el bus. Esta clase se usa para detectar qué dispositivos están en cada bus.
ms.assetid: 2d7d83a5-c058-40c0-aab3-7700f4067a16
ms.tgt_platform: multiple
title: Win32_DeviceBus (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceBus
- Win32_DeviceBus.Dependent
- Win32_DeviceBus.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2dde01ee6b3f3be026dbc19f8c4b8e2c238f4ff2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153548"
---
# <a name="win32_devicebus-class"></a><span data-ttu-id="8f88d-104">\_Clase Win32 DeviceBus</span><span class="sxs-lookup"><span data-stu-id="8f88d-104">Win32\_DeviceBus class</span></span>

<span data-ttu-id="8f88d-105">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DeviceBus** Association de Win32 relaciona un bus del sistema y un dispositivo lógico mediante el bus.</span><span class="sxs-lookup"><span data-stu-id="8f88d-105">The **Win32\_DeviceBus** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a system bus and a logical device using the bus.</span></span> <span data-ttu-id="8f88d-106">Esta clase se usa para detectar qué dispositivos están en cada bus.</span><span class="sxs-lookup"><span data-stu-id="8f88d-106">This class is used to discover which devices are on which bus.</span></span>

<span data-ttu-id="8f88d-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8f88d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8f88d-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="8f88d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f88d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f88d-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceBus : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  Win32_Bus         REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="8f88d-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="8f88d-110">Members</span></span>

<span data-ttu-id="8f88d-111">La **clase \_ DeviceBus de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8f88d-111">The **Win32\_DeviceBus** class has these types of members:</span></span>

-   [<span data-ttu-id="8f88d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8f88d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f88d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8f88d-113">Properties</span></span>

<span data-ttu-id="8f88d-114">La **clase \_ DeviceBus de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8f88d-114">The **Win32\_DeviceBus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f88d-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="8f88d-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-116">Tipo de datos **: \_ bus Win32**</span><span class="sxs-lookup"><span data-stu-id="8f88d-116">Data type: **Win32\_Bus**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f88d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-118">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| bus Win32 de WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="8f88d-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Bus")</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-119">Un [**\_ bus Win32**](win32-bus.md) que describe las propiedades del bus del sistema que usa el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8f88d-119">A [**Win32\_Bus**](win32-bus.md) that describes the properties of the system bus that is used by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="8f88d-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-121">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="8f88d-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8f88d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-123">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| lógico CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="8f88d-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-124">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe las propiedades del dispositivo lógico que usa el bus del sistema.</span><span class="sxs-lookup"><span data-stu-id="8f88d-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the properties of the logical device that is using the system bus.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f88d-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f88d-125">Remarks</span></span>

<span data-ttu-id="8f88d-126">La **clase \_ DeviceBus de Win32** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="8f88d-126">The **Win32\_DeviceBus** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f88d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f88d-127">Requirements</span></span>



| <span data-ttu-id="8f88d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f88d-128">Requirement</span></span> | <span data-ttu-id="8f88d-129">Value</span><span class="sxs-lookup"><span data-stu-id="8f88d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f88d-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f88d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8f88d-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f88d-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f88d-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f88d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8f88d-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f88d-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f88d-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8f88d-134">Namespace</span></span><br/>                | <span data-ttu-id="8f88d-135">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8f88d-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f88d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="8f88d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f88d-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f88d-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8f88d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f88d-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f88d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f88d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f88d-141">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="8f88d-141">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="8f88d-142">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="8f88d-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

