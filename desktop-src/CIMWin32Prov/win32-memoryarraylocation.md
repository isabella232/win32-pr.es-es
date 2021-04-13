---
description: La \_ clase WMI MemoryArrayLocation Association de Win32 relaciona una matriz de memoria lógica y la matriz de memoria física en la que existe.
ms.assetid: 455daeee-ad67-4599-84d6-fa3f4ac593aa
ms.tgt_platform: multiple
title: Win32_MemoryArrayLocation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArrayLocation
- Win32_MemoryArrayLocation.Dependent
- Win32_MemoryArrayLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62aae3bf672b12bdb947ff8ce6b76f919eaa11b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539231"
---
# <a name="win32_memoryarraylocation-class"></a><span data-ttu-id="0e222-103">\_Clase Win32 MemoryArrayLocation</span><span class="sxs-lookup"><span data-stu-id="0e222-103">Win32\_MemoryArrayLocation class</span></span>

<span data-ttu-id="0e222-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MemoryArrayLocation** Association de Win32 relaciona una matriz de memoria lógica y la matriz de memoria física en la que existe.</span><span class="sxs-lookup"><span data-stu-id="0e222-104">The **Win32\_MemoryArrayLocation** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical memory array and the physical memory array on which it exists.</span></span>

<span data-ttu-id="0e222-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0e222-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0e222-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="0e222-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e222-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e222-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF561-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryArrayLocation : CIM_Realizes
{
  Win32_MemoryArray         REF Dependent;
  Win32_PhysicalMemoryArray REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="0e222-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0e222-108">Members</span></span>

<span data-ttu-id="0e222-109">La **clase \_ MemoryArrayLocation de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0e222-109">The **Win32\_MemoryArrayLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="0e222-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0e222-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e222-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0e222-111">Properties</span></span>

<span data-ttu-id="0e222-112">La **clase \_ MemoryArrayLocation de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0e222-112">The **Win32\_MemoryArrayLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e222-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="0e222-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e222-114">Tipo de datos: **Win32 \_ PhysicalMemoryArray**</span><span class="sxs-lookup"><span data-stu-id="0e222-114">Data type: **Win32\_PhysicalMemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="0e222-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e222-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e222-116">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ PhysicalMemoryArray")</span><span class="sxs-lookup"><span data-stu-id="0e222-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_PhysicalMemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="0e222-117">[**\_ PhysicalMemoryArray de Win32**](win32-physicalmemoryarray.md) que describe la matriz de memoria física que implementa la matriz de memoria lógica.</span><span class="sxs-lookup"><span data-stu-id="0e222-117">A [**Win32\_PhysicalMemoryArray**](win32-physicalmemoryarray.md) that describes the physical memory array that implements the logical memory array.</span></span>

</dd> <dt>

<span data-ttu-id="0e222-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="0e222-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e222-119">Tipo de datos: **Win32 \_ MemoryArray**</span><span class="sxs-lookup"><span data-stu-id="0e222-119">Data type: **Win32\_MemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="0e222-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0e222-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e222-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryArray")</span><span class="sxs-lookup"><span data-stu-id="0e222-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="0e222-122">[**\_ MemoryArray de Win32**](win32-memoryarray.md) que describe la matriz de memoria lógica implementada por la matriz de memoria física.</span><span class="sxs-lookup"><span data-stu-id="0e222-122">A [**Win32\_MemoryArray**](win32-memoryarray.md) that describes the logical memory array implemented by the physical memory array.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e222-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e222-123">Remarks</span></span>

<span data-ttu-id="0e222-124">La **clase \_ MemoryArrayLocation de Win32** se deriva de los [**\_ beneficios de CIM**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="0e222-124">The **Win32\_MemoryArrayLocation** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e222-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e222-125">Requirements</span></span>



| <span data-ttu-id="0e222-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e222-126">Requirement</span></span> | <span data-ttu-id="0e222-127">Value</span><span class="sxs-lookup"><span data-stu-id="0e222-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e222-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e222-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0e222-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e222-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e222-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e222-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0e222-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e222-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e222-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0e222-132">Namespace</span></span><br/>                | <span data-ttu-id="0e222-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0e222-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0e222-134">MOF</span><span class="sxs-lookup"><span data-stu-id="0e222-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e222-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e222-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e222-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0e222-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e222-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e222-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e222-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e222-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e222-139">**Contrataciones \_ de CIM**</span><span class="sxs-lookup"><span data-stu-id="0e222-139">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dt>

[<span data-ttu-id="0e222-140">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="0e222-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

