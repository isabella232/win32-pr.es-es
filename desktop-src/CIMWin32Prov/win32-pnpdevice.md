---
description: La \_ clase WMI PnPDevice Association de Win32 relaciona un dispositivo (conocido para Configuration Manager como PNPEntity) y la función que realiza.
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Win32_PnPDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevice
- Win32_PnPDevice.SameElement
- Win32_PnPDevice.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c17dc6d4169854469d630e2a622eacc85e8a587c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659745"
---
# <a name="win32_pnpdevice-class"></a><span data-ttu-id="d93e1-103">\_Clase Win32 PnPDevice</span><span class="sxs-lookup"><span data-stu-id="d93e1-103">Win32\_PnPDevice class</span></span>

<span data-ttu-id="d93e1-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PnPDevice** Association de Win32 relaciona un dispositivo (conocido para Configuration Manager como PNPEntity) y la función que realiza.</span><span class="sxs-lookup"><span data-stu-id="d93e1-104">The **Win32\_PnPDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a device (known to Configuration Manager as a PNPEntity) and the function it performs.</span></span> <span data-ttu-id="d93e1-105">Su función está representada por una subclase del dispositivo lógico que describe su uso.</span><span class="sxs-lookup"><span data-stu-id="d93e1-105">Its function is represented by a subclass of the logical device that describes its use.</span></span> <span data-ttu-id="d93e1-106">Por ejemplo, una instancia de Win32 [**\_ Keyboard**](win32-keyboard.md) o [**Win32 \_ DiskDrive**](win32-diskdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="d93e1-106">For example, a [**Win32\_Keyboard**](win32-keyboard.md) or [**Win32\_DiskDrive**](win32-diskdrive.md) instance.</span></span> <span data-ttu-id="d93e1-107">Ambos objetos a los que se hace referencia representan el mismo dispositivo del sistema subyacente; los cambios en la asignación de recursos en el lado de PNPEntity afectarán al dispositivo asociado.</span><span class="sxs-lookup"><span data-stu-id="d93e1-107">Both referenced objects represent the same underlying system device; changes to resource allocation on the PNPEntity side will effect the associated device.</span></span>

<span data-ttu-id="d93e1-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d93e1-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d93e1-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d93e1-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d93e1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d93e1-110">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{FE28FD96-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPDevice
{
  CIM_LogicalDevice REF SameElement;
  Win32_PnPEntity   REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="d93e1-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="d93e1-111">Members</span></span>

<span data-ttu-id="d93e1-112">La **clase \_ PnPDevice de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d93e1-112">The **Win32\_PnPDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="d93e1-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d93e1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d93e1-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d93e1-114">Properties</span></span>

<span data-ttu-id="d93e1-115">La **clase \_ PnPDevice de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d93e1-115">The **Win32\_PnPDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d93e1-116">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="d93e1-116">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d93e1-117">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="d93e1-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="d93e1-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d93e1-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d93e1-119">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="d93e1-119">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="d93e1-120">Referencia a la instancia de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que representa las propiedades del dispositivo lógico asociadas al plug and Play dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d93e1-120">Reference to the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance representing the logical device properties associated with the Plug and Play device.</span></span>

</dd> <dt>

<span data-ttu-id="d93e1-121">**SystemElement**</span><span class="sxs-lookup"><span data-stu-id="d93e1-121">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d93e1-122">Tipo de datos: **Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="d93e1-122">Data type: **Win32\_PnPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="d93e1-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d93e1-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d93e1-124">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PnPEntity")</span><span class="sxs-lookup"><span data-stu-id="d93e1-124">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PnPEntity")</span></span>
</dt> </dl>

<span data-ttu-id="d93e1-125">Referencia a la instancia de [**Win32 \_ PnPEntity**](win32-pnpentity.md) que representa el dispositivo Plug and Play asociado con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d93e1-125">Reference to the [**Win32\_PnPEntity**](win32-pnpentity.md) instance representing the Plug and Play device associated with the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d93e1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d93e1-126">Requirements</span></span>



| <span data-ttu-id="d93e1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d93e1-127">Requirement</span></span> | <span data-ttu-id="d93e1-128">Value</span><span class="sxs-lookup"><span data-stu-id="d93e1-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d93e1-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d93e1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d93e1-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d93e1-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d93e1-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d93e1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d93e1-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d93e1-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d93e1-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d93e1-133">Namespace</span></span><br/>                | <span data-ttu-id="d93e1-134">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d93e1-134">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d93e1-135">MOF</span><span class="sxs-lookup"><span data-stu-id="d93e1-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d93e1-136"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d93e1-136"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d93e1-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d93e1-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d93e1-138"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d93e1-138"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d93e1-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d93e1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d93e1-140">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="d93e1-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
