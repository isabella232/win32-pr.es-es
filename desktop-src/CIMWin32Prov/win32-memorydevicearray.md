---
description: La \_ clase WMI MemoryDeviceArray Association de Win32 relaciona un dispositivo de memoria y la matriz de memoria en la que reside.
ms.assetid: 39ea6333-2352-488b-99e4-97594bea7dcd
ms.tgt_platform: multiple
title: Win32_MemoryDeviceArray (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceArray
- Win32_MemoryDeviceArray.GroupComponent
- Win32_MemoryDeviceArray.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e527f77183c3bdc09d464f6fed4808e45adefa5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907014"
---
# <a name="win32_memorydevicearray-class"></a><span data-ttu-id="5d92b-103">\_Clase Win32 MemoryDeviceArray</span><span class="sxs-lookup"><span data-stu-id="5d92b-103">Win32\_MemoryDeviceArray class</span></span>

<span data-ttu-id="5d92b-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MemoryDeviceArray** Association de Win32 relaciona un dispositivo de memoria y la matriz de memoria en la que reside.</span><span class="sxs-lookup"><span data-stu-id="5d92b-104">The **Win32\_MemoryDeviceArray** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a memory device and the memory array in which it resides.</span></span>

<span data-ttu-id="5d92b-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5d92b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5d92b-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="5d92b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d92b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d92b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF563-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryDeviceArray : CIM_Component
{
  Win32_MemoryArray  REF GroupComponent;
  Win32_MemoryDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="5d92b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5d92b-108">Members</span></span>

<span data-ttu-id="5d92b-109">La **clase \_ MemoryDeviceArray de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5d92b-109">The **Win32\_MemoryDeviceArray** class has these types of members:</span></span>

-   [<span data-ttu-id="5d92b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5d92b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d92b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5d92b-111">Properties</span></span>

<span data-ttu-id="5d92b-112">La **clase \_ MemoryDeviceArray de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5d92b-112">The **Win32\_MemoryDeviceArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d92b-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="5d92b-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d92b-114">Tipo de datos: **Win32 \_ MemoryArray**</span><span class="sxs-lookup"><span data-stu-id="5d92b-114">Data type: **Win32\_MemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="5d92b-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d92b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d92b-116">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryArray")</span><span class="sxs-lookup"><span data-stu-id="5d92b-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="5d92b-117">[**\_ MemoryArray de Win32**](win32-memoryarray.md) que representa la parte de la matriz de memoria de la \_ Asociación MemoryDeviceArray de Win32.</span><span class="sxs-lookup"><span data-stu-id="5d92b-117">A [**Win32\_MemoryArray**](win32-memoryarray.md) that represents the memory array part of the Win32\_MemoryDeviceArray association.</span></span>

</dd> <dt>

<span data-ttu-id="5d92b-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="5d92b-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d92b-119">Tipo de datos: **Win32 \_ MemoryDevice**</span><span class="sxs-lookup"><span data-stu-id="5d92b-119">Data type: **Win32\_MemoryDevice**</span></span>
</dt> <dt>

<span data-ttu-id="5d92b-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5d92b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d92b-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryDevice")</span><span class="sxs-lookup"><span data-stu-id="5d92b-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryDevice")</span></span>
</dt> </dl>

<span data-ttu-id="5d92b-122">[**\_ MemoryDevice de Win32**](win32-memorydevice.md) que representa una parte del dispositivo de memoria de la \_ Asociación MemoryDeviceArray de Win32.</span><span class="sxs-lookup"><span data-stu-id="5d92b-122">A [**Win32\_MemoryDevice**](win32-memorydevice.md) that represents a memory device part of the Win32\_MemoryDeviceArray association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d92b-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d92b-123">Remarks</span></span>

<span data-ttu-id="5d92b-124">La **clase \_ MemoryDeviceArray de Win32** se deriva [**del \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="5d92b-124">The **Win32\_MemoryDeviceArray** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d92b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d92b-125">Requirements</span></span>



| <span data-ttu-id="5d92b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d92b-126">Requirement</span></span> | <span data-ttu-id="5d92b-127">Value</span><span class="sxs-lookup"><span data-stu-id="5d92b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d92b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d92b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5d92b-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d92b-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d92b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d92b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5d92b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d92b-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d92b-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5d92b-132">Namespace</span></span><br/>                | <span data-ttu-id="5d92b-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5d92b-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5d92b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5d92b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d92b-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d92b-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d92b-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5d92b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d92b-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d92b-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d92b-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d92b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d92b-139">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="5d92b-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="5d92b-140">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="5d92b-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

