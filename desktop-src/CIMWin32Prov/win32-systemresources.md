---
description: La \_ clase WMI SystemResources Association de Win32 relaciona un recurso del sistema y el sistema del equipo en el que reside.
ms.assetid: 90bff0b0-7c1d-44bf-b67e-aefeaa4b4a83
ms.tgt_platform: multiple
title: Win32_SystemResources (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemResources
- Win32_SystemResources.GroupComponent
- Win32_SystemResources.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe96467e4bc609fa9426edd3c977b5596ea95fe7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000590"
---
# <a name="win32_systemresources-class"></a><span data-ttu-id="cd449-103">\_Clase Win32 SystemResources</span><span class="sxs-lookup"><span data-stu-id="cd449-103">Win32\_SystemResources class</span></span>

<span data-ttu-id="cd449-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemResources** Association de Win32 relaciona un recurso del sistema y el sistema del equipo en el que reside.</span><span class="sxs-lookup"><span data-stu-id="cd449-104">The **Win32\_SystemResources** association [WMI class](../wmisdk/retrieving-a-class.md) relates a system resource and the computer system it resides on.</span></span>

<span data-ttu-id="cd449-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cd449-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="cd449-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="cd449-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd449-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd449-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemResources : CIM_ComputerSystemResource
{
  Win32_ComputerSystem REF GroupComponent;
  CIM_SystemResource   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="cd449-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="cd449-108">Members</span></span>

<span data-ttu-id="cd449-109">La **clase \_ SystemResources de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cd449-109">The **Win32\_SystemResources** class has these types of members:</span></span>

-   [<span data-ttu-id="cd449-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd449-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd449-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd449-111">Properties</span></span>

<span data-ttu-id="cd449-112">La **clase \_ SystemResources de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cd449-112">The **Win32\_SystemResources** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd449-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="cd449-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd449-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="cd449-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="cd449-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd449-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd449-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="cd449-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="cd449-117">Referencia a la instancia de que representa el sistema del equipo en el que se encuentra el recurso.</span><span class="sxs-lookup"><span data-stu-id="cd449-117">Reference to the instance representing the computer system where the resource is located.</span></span>

</dd> <dt>

<span data-ttu-id="cd449-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="cd449-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd449-119">Tipo de datos: **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="cd449-119">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="cd449-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd449-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd449-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ SystemResource")</span><span class="sxs-lookup"><span data-stu-id="cd449-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="cd449-122">Referencia a la instancia de que representa el recurso (por ejemplo, servicios de e/s y recursos de memoria) disponible en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="cd449-122">Reference to the instance representing the resource (such as I/O services and memory resources) available on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd449-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd449-123">Remarks</span></span>

<span data-ttu-id="cd449-124">La **clase \_ SystemResources de Win32** se deriva de [**\_ ComputerSystemResource de CIM**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="cd449-124">The **Win32\_SystemResources** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd449-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd449-125">Requirements</span></span>



| <span data-ttu-id="cd449-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd449-126">Requirement</span></span> | <span data-ttu-id="cd449-127">Value</span><span class="sxs-lookup"><span data-stu-id="cd449-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd449-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd449-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cd449-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd449-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cd449-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd449-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cd449-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd449-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cd449-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cd449-132">Namespace</span></span><br/>                | <span data-ttu-id="cd449-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cd449-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cd449-134">MOF</span><span class="sxs-lookup"><span data-stu-id="cd449-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd449-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd449-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd449-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cd449-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd449-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd449-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd449-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd449-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd449-139">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="cd449-139">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> <dt>

[<span data-ttu-id="cd449-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="cd449-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
