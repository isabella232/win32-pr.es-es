---
description: La \_ clase WMI PnPAllocatedResource Association de Win32 representa una asociación entre dispositivos lógicos y recursos del sistema.
ms.assetid: e3cef457-cf88-4df5-8db8-b0495f636904
ms.tgt_platform: multiple
title: Win32_PnPAllocatedResource (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPAllocatedResource
- Win32_PnPAllocatedResource.Antecedent
- Win32_PnPAllocatedResource.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353009016c8d4d54cdc92fb8f0ed062567dded6f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907521"
---
# <a name="win32_pnpallocatedresource-class"></a><span data-ttu-id="0fd10-103">\_Clase Win32 PnPAllocatedResource</span><span class="sxs-lookup"><span data-stu-id="0fd10-103">Win32\_PnPAllocatedResource class</span></span>

<span data-ttu-id="0fd10-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PnPAllocatedResource** Association de Win32 representa una asociación entre dispositivos lógicos y recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="0fd10-104">The **Win32\_PnPAllocatedResource** association [WMI class](../wmisdk/retrieving-a-class.md) represents an association between logical devices and system resources.</span></span> <span data-ttu-id="0fd10-105">Esta clase se usa para detectar los recursos que están en uso por un dispositivo específico, como una solicitud de interrupción (IRQ) o un canal de acceso directo a memoria (DMA).</span><span class="sxs-lookup"><span data-stu-id="0fd10-105">This class is used to discover the resources that are in-use by a specific device, such as an Interrupt ReQuest (IRQ) or a Direct Memory Access (DMA) channel.</span></span>

<span data-ttu-id="0fd10-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0fd10-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0fd10-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="0fd10-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd10-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0fd10-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("970C0998-41FE-4275-B7D9-7DABAD3FBC4D"), AMENDMENT]
class Win32_PnPAllocatedResource : CIM_AllocatedResource
{
  CIM_SystemResource REF Antecedent;
  Win32_PnPEntity    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="0fd10-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0fd10-109">Members</span></span>

<span data-ttu-id="0fd10-110">La **clase \_ PnPAllocatedResource de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0fd10-110">The **Win32\_PnPAllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="0fd10-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0fd10-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0fd10-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0fd10-112">Properties</span></span>

<span data-ttu-id="0fd10-113">La **clase \_ PnPAllocatedResource de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0fd10-113">The **Win32\_PnPAllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0fd10-114">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="0fd10-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fd10-115">Tipo de datos: **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="0fd10-115">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="0fd10-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0fd10-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fd10-117">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ SystemResource")</span><span class="sxs-lookup"><span data-stu-id="0fd10-117">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="0fd10-118">Referencia a la instancia de [**\_ SystemResource de CIM**](cim-systemresource.md) que representa las propiedades de un recurso del sistema disponible para el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="0fd10-118">Reference to the [**CIM\_SystemResource**](cim-systemresource.md) instance that represents the properties of a system resource available to the logical device.</span></span> <span data-ttu-id="0fd10-119">Esta propiedad se hereda de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="0fd10-119">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fd10-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="0fd10-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fd10-121">Tipo de datos: **Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="0fd10-121">Data type: **Win32\_PnPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="0fd10-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0fd10-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fd10-123">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("dependiente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| lógico CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="0fd10-123">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="0fd10-124">Referencia a la instancia de [**Win32 \_ PnPEntity**](win32-pnpentity.md) que representa las propiedades del dispositivo lógico usando los recursos del sistema asignados a él.</span><span class="sxs-lookup"><span data-stu-id="0fd10-124">Reference to the [**Win32\_PnPEntity**](win32-pnpentity.md) instance that represents the properties of the logical device using the system resources assigned to it.</span></span> <span data-ttu-id="0fd10-125">Esta propiedad se hereda de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="0fd10-125">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fd10-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0fd10-126">Remarks</span></span>

<span data-ttu-id="0fd10-127">La **clase \_ PnPAllocatedResource de Win32** se deriva de [**\_ AllocatedResource de CIM**](cim-allocatedresource.md).</span><span class="sxs-lookup"><span data-stu-id="0fd10-127">The **Win32\_PnPAllocatedResource** class is derived from [**CIM\_AllocatedResource**](cim-allocatedresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fd10-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fd10-128">Requirements</span></span>



| <span data-ttu-id="0fd10-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fd10-129">Requirement</span></span> | <span data-ttu-id="0fd10-130">Value</span><span class="sxs-lookup"><span data-stu-id="0fd10-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd10-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fd10-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0fd10-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0fd10-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0fd10-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fd10-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0fd10-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fd10-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0fd10-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0fd10-135">Namespace</span></span><br/>                | <span data-ttu-id="0fd10-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0fd10-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0fd10-137">MOF</span><span class="sxs-lookup"><span data-stu-id="0fd10-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0fd10-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0fd10-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0fd10-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0fd10-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fd10-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fd10-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fd10-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fd10-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd10-142">**\_ALLOCATEDRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="0fd10-142">**CIM\_AllocatedResource**</span></span>](cim-allocatedresource.md)
</dt> <dt>

[<span data-ttu-id="0fd10-143">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="0fd10-143">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
