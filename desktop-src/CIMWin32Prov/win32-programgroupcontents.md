---
description: La \_ clase WMI ProgramGroupContents Association de Win32 relaciona un orden de grupo de programas y un grupo de programas o un elemento individual que contiene.
ms.assetid: 687794d1-acc1-498a-9886-0c9ac762ebf4
ms.tgt_platform: multiple
title: Win32_ProgramGroupContents (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupContents
- Win32_ProgramGroupContents.GroupComponent
- Win32_ProgramGroupContents.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f77a61052357f7c67009ee7a89da018abeadda8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080126"
---
# <a name="win32_programgroupcontents-class"></a><span data-ttu-id="a2768-103">\_Clase Win32 ProgramGroupContents</span><span class="sxs-lookup"><span data-stu-id="a2768-103">Win32\_ProgramGroupContents class</span></span>

<span data-ttu-id="a2768-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ ProgramGroupContents** Association de Win32 relaciona un orden de grupo de programas y un grupo de programas o un elemento individual que contiene.</span><span class="sxs-lookup"><span data-stu-id="a2768-104">The **Win32\_ProgramGroupContents** association [WMI class](../wmisdk/retrieving-a-class.md) relates a program group order and an individual program group or item contained in it.</span></span>

<span data-ttu-id="a2768-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a2768-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a2768-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a2768-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2768-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2768-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{86E30E83-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupContents : CIM_Component
{
  Win32_LogicalProgramGroup REF GroupComponent;
  Win32_ProgramGroupOrItem  REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="a2768-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a2768-108">Members</span></span>

<span data-ttu-id="a2768-109">La **clase \_ ProgramGroupContents de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a2768-109">The **Win32\_ProgramGroupContents** class has these types of members:</span></span>

-   [<span data-ttu-id="a2768-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a2768-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2768-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a2768-111">Properties</span></span>

<span data-ttu-id="a2768-112">La **clase \_ ProgramGroupContents de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a2768-112">The **Win32\_ProgramGroupContents** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2768-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="a2768-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2768-114">Tipo de datos: **Win32 \_ LogicalProgramGroup**</span><span class="sxs-lookup"><span data-stu-id="a2768-114">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="a2768-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a2768-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2768-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LogicalProgramGroup")</span><span class="sxs-lookup"><span data-stu-id="a2768-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="a2768-117">Referencia a la instancia de que representa el grupo de programas lógicos para esta asociación.</span><span class="sxs-lookup"><span data-stu-id="a2768-117">Reference to the instance representing the logical program group for this association.</span></span>

</dd> <dt>

<span data-ttu-id="a2768-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a2768-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2768-119">Tipo de datos: **Win32 \_ ProgramGroupOrItem**</span><span class="sxs-lookup"><span data-stu-id="a2768-119">Data type: **Win32\_ProgramGroupOrItem**</span></span>
</dt> <dt>

<span data-ttu-id="a2768-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a2768-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2768-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ProgramGroupOrItem")</span><span class="sxs-lookup"><span data-stu-id="a2768-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ProgramGroupOrItem")</span></span>
</dt> </dl>

<span data-ttu-id="a2768-122">Referencia a la instancia de que representa el grupo o el elemento del menú **Inicio** para esta asociación.</span><span class="sxs-lookup"><span data-stu-id="a2768-122">Reference to the instance representing the **Start** menu group or item for this association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2768-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2768-123">Remarks</span></span>

<span data-ttu-id="a2768-124">La **clase \_ ProgramGroupContents de Win32** se deriva [**del \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="a2768-124">The **Win32\_ProgramGroupContents** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a2768-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2768-125">Requirements</span></span>



| <span data-ttu-id="a2768-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2768-126">Requirement</span></span> | <span data-ttu-id="a2768-127">Value</span><span class="sxs-lookup"><span data-stu-id="a2768-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2768-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2768-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a2768-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2768-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a2768-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2768-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a2768-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2768-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a2768-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a2768-132">Namespace</span></span><br/>                | <span data-ttu-id="a2768-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a2768-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a2768-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a2768-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2768-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2768-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2768-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a2768-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2768-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2768-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2768-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2768-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2768-139">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="a2768-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="a2768-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a2768-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
