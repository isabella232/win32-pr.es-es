---
description: Representa una placa base, que también se conoce como placa base o de sistema.
ms.assetid: 04ac7522-8b99-4ffc-9f7d-d1225f55a862
ms.tgt_platform: multiple
title: Win32_BaseBoard (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseBoard
- Win32_BaseBoard.IsCompatible
- Win32_BaseBoard.Caption
- Win32_BaseBoard.ConfigOptions
- Win32_BaseBoard.CreationClassName
- Win32_BaseBoard.Depth
- Win32_BaseBoard.Description
- Win32_BaseBoard.Height
- Win32_BaseBoard.HostingBoard
- Win32_BaseBoard.HotSwappable
- Win32_BaseBoard.InstallDate
- Win32_BaseBoard.Manufacturer
- Win32_BaseBoard.Model
- Win32_BaseBoard.Name
- Win32_BaseBoard.OtherIdentifyingInfo
- Win32_BaseBoard.PartNumber
- Win32_BaseBoard.PoweredOn
- Win32_BaseBoard.Product
- Win32_BaseBoard.Removable
- Win32_BaseBoard.Replaceable
- Win32_BaseBoard.RequirementsDescription
- Win32_BaseBoard.RequiresDaughterBoard
- Win32_BaseBoard.SerialNumber
- Win32_BaseBoard.SKU
- Win32_BaseBoard.SlotLayout
- Win32_BaseBoard.SpecialRequirements
- Win32_BaseBoard.Status
- Win32_BaseBoard.Tag
- Win32_BaseBoard.Version
- Win32_BaseBoard.Weight
- Win32_BaseBoard.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4287076a550e25bf74a160b191c777c25d9ab3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080280"
---
# <a name="win32_baseboard-class"></a><span data-ttu-id="b8036-103">\_Clase de placa base Win32</span><span class="sxs-lookup"><span data-stu-id="b8036-103">Win32\_BaseBoard class</span></span>

<span data-ttu-id="b8036-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) de la **\_ placa base de Win32** representa una placa base, que también se conoce como placa base o de sistema.</span><span class="sxs-lookup"><span data-stu-id="b8036-104">The **Win32\_BaseBoard** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a baseboard, which is also known as a motherboard or system board.</span></span>

<span data-ttu-id="b8036-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b8036-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8036-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8036-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B95-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_BaseBoard : CIM_Card
{
  string   Caption;
  string   ConfigOptions[];
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HostingBoard;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   Product;
  boolean  Removable;
  boolean  Replaceable;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SerialNumber;
  string   SKU;
  string   SlotLayout;
  boolean  SpecialRequirements;
  string   Status;
  string   Tag;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="b8036-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b8036-107">Members</span></span>

<span data-ttu-id="b8036-108">La clase de **\_ placa base de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b8036-108">The **Win32\_BaseBoard** class has these types of members:</span></span>

-   [<span data-ttu-id="b8036-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="b8036-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="b8036-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b8036-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b8036-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b8036-111">Methods</span></span>

<span data-ttu-id="b8036-112">La clase de **\_ placa base de Win32** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b8036-112">The **Win32\_BaseBoard** class has these methods.</span></span>



| <span data-ttu-id="b8036-113">Método</span><span class="sxs-lookup"><span data-stu-id="b8036-113">Method</span></span>           | <span data-ttu-id="b8036-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8036-114">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="b8036-115">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="b8036-115">**IsCompatible**</span></span> | <span data-ttu-id="b8036-116">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="b8036-116">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b8036-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b8036-117">Properties</span></span>

<span data-ttu-id="b8036-118">La clase de **\_ placa base de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b8036-118">The **Win32\_BaseBoard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8036-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b8036-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8036-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-122">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b8036-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b8036-123">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="b8036-123">Short description of the object a one-line string.</span></span>

<span data-ttu-id="b8036-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-125">**ConfigOptions**</span><span class="sxs-lookup"><span data-stu-id="b8036-125">**ConfigOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-126">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="b8036-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b8036-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-128">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("cadenas de opciones de configuración de tipo de SMBIOS \| 12 \| ")</span><span class="sxs-lookup"><span data-stu-id="b8036-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 12\|Configuration Options Strings")</span></span>
</dt> </dl>

<span data-ttu-id="b8036-129">Matriz que representa la configuración de los puentes y modificadores ubicados en la placa base.</span><span class="sxs-lookup"><span data-stu-id="b8036-129">Array that represents the configuration of the jumpers and switches located on the baseboard.</span></span>

<span data-ttu-id="b8036-130">Ejemplo: "JP2: el tamaño de caché de 1-2 es 256 k, el tamaño de caché de 2-3 es 512 k, SW1-1: Close to Disable in Board video"</span><span class="sxs-lookup"><span data-stu-id="b8036-130">Example: "JP2: 1-2 Cache Size is 256K, 2-3 Cache Size is 512K, SW1-1: Close to Disable On Board Video"</span></span>

</dd> <dt>

<span data-ttu-id="b8036-131">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b8036-131">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8036-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-134">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b8036-134">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b8036-135">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="b8036-135">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b8036-136">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="b8036-136">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="b8036-137">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-137">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-138">**Profundidad**</span><span class="sxs-lookup"><span data-stu-id="b8036-138">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-139">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="b8036-139">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-141">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="b8036-141">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="b8036-142">Profundidad del paquete físico en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="b8036-142">Depth of the physical package in inches.</span></span>

<span data-ttu-id="b8036-143">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-143">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8036-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8036-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-147">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="b8036-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b8036-148">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8036-148">Description of the object.</span></span>

<span data-ttu-id="b8036-149">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-149">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-150">**Height**</span><span class="sxs-lookup"><span data-stu-id="b8036-150">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-151">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="b8036-151">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-153">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="b8036-153">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="b8036-154">Alto del paquete físico en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="b8036-154">Height of the physical package in inches.</span></span>

<span data-ttu-id="b8036-155">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-155">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-156">**HostingBoard**</span><span class="sxs-lookup"><span data-stu-id="b8036-156">**HostingBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-157">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8036-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8036-159">Si es **true**, la tarjeta es una placa base o una placa base en un chasis.</span><span class="sxs-lookup"><span data-stu-id="b8036-159">If **TRUE**, the card is a motherboard, or a baseboard in a chassis.</span></span>

<span data-ttu-id="b8036-160">Esta propiedad se hereda de [**la \_ tarjeta CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-160">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-161">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="b8036-161">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-162">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8036-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8036-164">Si **es true**, el paquete puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="b8036-164">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="b8036-165">Un paquete físico puede intercambiarse en caliente si es posible reemplazar el elemento con un elemento físicamente diferente pero equivalente mientras el paquete contenedor tiene energía aplicada, es decir, mientras está activado.</span><span class="sxs-lookup"><span data-stu-id="b8036-165">A physical package can be hot-swapped if it is possible to replace the element with a physically different but equivalent element while the containing package has power applied to it that is, while it is ON.</span></span> <span data-ttu-id="b8036-166">Por ejemplo, un paquete de unidad de disco insertado mediante conectores SCA es extraíble y puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="b8036-166">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="b8036-167">Todos los paquetes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.</span><span class="sxs-lookup"><span data-stu-id="b8036-167">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="b8036-168">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-168">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-169">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b8036-169">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-170">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8036-170">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-172">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="b8036-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b8036-173">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="b8036-173">Date and time the object was installed.</span></span> <span data-ttu-id="b8036-174">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="b8036-174">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b8036-175">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-175">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-176">**Le**</span><span class="sxs-lookup"><span data-stu-id="b8036-176">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8036-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-179">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b8036-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b8036-180">Nombre de la organización responsable de producir el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b8036-180">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="b8036-181">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-181">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-182">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="b8036-182">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8036-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-185">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b8036-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b8036-186">Nombre por el que se conoce el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b8036-186">Name by which the physical element is known.</span></span>

<span data-ttu-id="b8036-187">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-187">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-188">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b8036-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8036-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-191">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b8036-191">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b8036-192">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="b8036-192">Label by which the object is known.</span></span> <span data-ttu-id="b8036-193">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="b8036-193">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b8036-194">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-195">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="b8036-195">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-196">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8036-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8036-198">Captura datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b8036-198">Captures additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="b8036-199">Un ejemplo son los datos de código de barras que están asociados a un elemento que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="b8036-199">One example is bar code data that is associated with an element that also has an asset tag.</span></span> <span data-ttu-id="b8036-200">Tenga en cuenta que si solo los datos de código de barras están disponibles y son únicos o se pueden usar como una clave de elemento, el valor de la propiedad sería **null** y los datos de código de barras se utilizarían como la clave de clase en la propiedad de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="b8036-200">Note that if only bar code data is available and unique or able to be used as an element key, the property value would be **NULL** and the bar code data would be used as the class key, in the tag property.</span></span>

<span data-ttu-id="b8036-201">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-201">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-202">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="b8036-202">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8036-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-205">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b8036-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b8036-206">Número de pieza asignado por la organización responsable de producir o fabricar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b8036-206">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="b8036-207">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-207">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-208">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="b8036-208">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-209">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8036-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8036-211">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="b8036-211">If **TRUE**, the physical element is powered ON.</span></span>

<span data-ttu-id="b8036-212">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-212">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-213">**Producto**</span><span class="sxs-lookup"><span data-stu-id="b8036-213">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-214">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8036-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-216">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 2 \| producto")</span><span class="sxs-lookup"><span data-stu-id="b8036-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 2\|Product")</span></span>
</dt> </dl>

<span data-ttu-id="b8036-217">Número de pieza de la placa base definida por el fabricante.</span><span class="sxs-lookup"><span data-stu-id="b8036-217">Baseboard part number defined by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="b8036-218">**Quitar**</span><span class="sxs-lookup"><span data-stu-id="b8036-218">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-219">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8036-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8036-221">Si es **true**, un paquete es extraíble.</span><span class="sxs-lookup"><span data-stu-id="b8036-221">If **TRUE**, a package is removable.</span></span> <span data-ttu-id="b8036-222">Un paquete físico es extraíble si está diseñado para tomarse dentro y fuera del contenedor físico en el que se encuentra normalmente sin perjudicar a la función del empaquetado global.</span><span class="sxs-lookup"><span data-stu-id="b8036-222">A physical package is removable if it is designed to be taken in and out of the physical container in which it is normally found without impairing the function of the overall packaging.</span></span> <span data-ttu-id="b8036-223">Un paquete todavía puede ser extraíble si la alimentación debe estar desactivada para realizar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="b8036-223">A package can still be removable if the power must be OFF to perform the removal.</span></span> <span data-ttu-id="b8036-224">Si la potencia puede estar activada y se ha quitado el paquete, el elemento es extraíble y se puede intercambiar en caliente.</span><span class="sxs-lookup"><span data-stu-id="b8036-224">If the power can be ON and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="b8036-225">Por ejemplo, una batería adicional en un equipo portátil es extraíble, como un paquete de unidad de disco insertado mediante conectores SCA.</span><span class="sxs-lookup"><span data-stu-id="b8036-225">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="b8036-226">Sin embargo, el último también puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="b8036-226">However, the latter can also be hot-swapped.</span></span> <span data-ttu-id="b8036-227">La pantalla de un portátil no es extraíble, ni tampoco es una fuente de alimentación que no sea redundante.</span><span class="sxs-lookup"><span data-stu-id="b8036-227">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="b8036-228">La eliminación de estos componentes afectaría a la función del empaquetado global o es imposible debido a la estrecha integración del paquete.</span><span class="sxs-lookup"><span data-stu-id="b8036-228">Removing these components would impact the function of the overall packaging, or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="b8036-229">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-229">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-230">**Reemplazables**</span><span class="sxs-lookup"><span data-stu-id="b8036-230">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-231">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8036-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8036-233">Si es **true**, un paquete es reemplazable.</span><span class="sxs-lookup"><span data-stu-id="b8036-233">If **TRUE**, a package is replaceable.</span></span> <span data-ttu-id="b8036-234">Un paquete físico es reemplazable si es posible reemplazar (FRU o actualizar) el elemento con uno físicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="b8036-234">A physical package is replaceable if it is possible to replace (FRU or upgrade) the element with a physically different one.</span></span> <span data-ttu-id="b8036-235">Por ejemplo, algunos sistemas informáticos permiten que el chip del procesador principal se actualice a una clasificación de reloj más alta.</span><span class="sxs-lookup"><span data-stu-id="b8036-235">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="b8036-236">En este caso, se dice que el procesador es reemplazable.</span><span class="sxs-lookup"><span data-stu-id="b8036-236">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="b8036-237">Otro ejemplo es un paquete de fuente de alimentación montado en raíles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="b8036-237">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="b8036-238">Todos los paquetes extraíbles se pueden reemplazar de forma inherente.</span><span class="sxs-lookup"><span data-stu-id="b8036-238">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="b8036-239">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-239">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-240">**RequirementsDescription**</span><span class="sxs-lookup"><span data-stu-id="b8036-240">**RequirementsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-241">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8036-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-243">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ tarjeta CIM**](cim-card.md).**SpecialRequirements**")</span><span class="sxs-lookup"><span data-stu-id="b8036-243">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Card**](cim-card.md).**SpecialRequirements**")</span></span>
</dt> </dl>

<span data-ttu-id="b8036-244">Cadena de forma libre que describe la forma en que esta tarjeta es única físicamente desde otras tarjetas.</span><span class="sxs-lookup"><span data-stu-id="b8036-244">Free-form string that describes the way in which this card is physically unique from other cards.</span></span> <span data-ttu-id="b8036-245">La propiedad solo tiene significado cuando la propiedad booleana correspondiente **SpecialRequirements** se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="b8036-245">The property only has meaning when the corresponding Boolean property **SpecialRequirements** is set to **TRUE**.</span></span>

<span data-ttu-id="b8036-246">Esta propiedad se hereda de [**la \_ tarjeta CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-246">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-247">**RequiresDaughterBoard**</span><span class="sxs-lookup"><span data-stu-id="b8036-247">**RequiresDaughterBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-248">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8036-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8036-250">Si es **true**, se requiere al menos una tarjeta daughterboard o auxiliar para funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="b8036-250">If **TRUE**, at least one daughterboard or auxiliary card is required to function properly.</span></span>

<span data-ttu-id="b8036-251">Esta propiedad se hereda de [**la \_ tarjeta CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-251">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-252">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="b8036-252">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-253">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8036-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-255">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b8036-255">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b8036-256">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b8036-256">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="b8036-257">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-258">**SKU**</span><span class="sxs-lookup"><span data-stu-id="b8036-258">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-259">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8036-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-260">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-261">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b8036-261">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b8036-262">Número de unidad de almacén para el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b8036-262">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="b8036-263">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-263">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-264">**SlotLayout**</span><span class="sxs-lookup"><span data-stu-id="b8036-264">**SlotLayout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-265">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8036-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-266">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8036-267">Cadena de forma libre que describe la posición de la ranura, el uso típico, las restricciones, el espaciado de ranura individual o cualquier otra información pertinente para las ranuras de una tarjeta.</span><span class="sxs-lookup"><span data-stu-id="b8036-267">Free-form string that describes the slot position, typical usage, restrictions, individual slot spacing or any other pertinent information for the slots on a card.</span></span>

<span data-ttu-id="b8036-268">Esta propiedad se hereda de [**la \_ tarjeta CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-268">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-269">**SpecialRequirements**</span><span class="sxs-lookup"><span data-stu-id="b8036-269">**SpecialRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-270">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8036-270">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-271">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-272">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ tarjeta CIM**](cim-card.md).**RequirementsDescription**")</span><span class="sxs-lookup"><span data-stu-id="b8036-272">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Card**](cim-card.md).**RequirementsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="b8036-273">Si es **true**, esta tarjeta es única físicamente desde otras tarjetas del mismo tipo y, por tanto, requiere una ranura especial.</span><span class="sxs-lookup"><span data-stu-id="b8036-273">If **TRUE**, this card is physically unique from other cards of the same type and therefore requires a special slot.</span></span> <span data-ttu-id="b8036-274">Por ejemplo, una tarjeta de doble ancho requiere dos ranuras.</span><span class="sxs-lookup"><span data-stu-id="b8036-274">For example, a double-wide card requires two slots.</span></span> <span data-ttu-id="b8036-275">Otro ejemplo es el lugar en el que se puede usar una tarjeta determinada para la misma función general que otras tarjetas, pero requiere una ranura especial (por ejemplo, extra larga), mientras que las otras tarjetas pueden colocarse en cualquier ranura disponible.</span><span class="sxs-lookup"><span data-stu-id="b8036-275">Another example is where a certain card may be used for the same general function as other cards but requires a special slot (for example, extra long), whereas the other cards can be placed in any available slot.</span></span> <span data-ttu-id="b8036-276">Si se establece en **true**, la propiedad correspondiente, **RequirementsDescription**, debe especificar la naturaleza de la unicidad o el propósito de la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="b8036-276">If set to **TRUE**, then the corresponding property, **RequirementsDescription**, should specify the nature of the uniqueness or purpose of the card.</span></span>

<span data-ttu-id="b8036-277">Esta propiedad se hereda de [**la \_ tarjeta CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-277">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-278">**Estado**</span><span class="sxs-lookup"><span data-stu-id="b8036-278">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-279">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8036-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-281">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b8036-281">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b8036-282">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8036-282">Current status of the object.</span></span> <span data-ttu-id="b8036-283">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="b8036-283">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b8036-284">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="b8036-284">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b8036-285">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="b8036-285">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b8036-286">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="b8036-286">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b8036-287">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="b8036-287">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b8036-288">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b8036-289">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b8036-289">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b8036-290">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="b8036-290">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b8036-291">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="b8036-291">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b8036-292">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b8036-292">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8036-293">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="b8036-293">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b8036-294">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="b8036-294">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b8036-295">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="b8036-295">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b8036-296">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="b8036-296">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b8036-297">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="b8036-297">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b8036-298">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="b8036-298">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b8036-299">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b8036-299">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b8036-300">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="b8036-300">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b8036-301">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="b8036-301">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b8036-302">**Tag**</span><span class="sxs-lookup"><span data-stu-id="b8036-302">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8036-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-305">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("etiqueta"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b8036-305">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b8036-306">Identificador único de la placa base del sistema.</span><span class="sxs-lookup"><span data-stu-id="b8036-306">Unique identifier of the baseboard of the system.</span></span>

<span data-ttu-id="b8036-307">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-307">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="b8036-308">Ejemplo: "placa base"</span><span class="sxs-lookup"><span data-stu-id="b8036-308">Example: "Base Board"</span></span>

</dd> <dt>

<span data-ttu-id="b8036-309">**Versión**</span><span class="sxs-lookup"><span data-stu-id="b8036-309">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-310">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8036-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-312">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b8036-312">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b8036-313">Versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="b8036-313">Version of the physical element.</span></span>

<span data-ttu-id="b8036-314">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-315">**Peso**</span><span class="sxs-lookup"><span data-stu-id="b8036-315">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-316">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="b8036-316">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-318">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("libras")</span><span class="sxs-lookup"><span data-stu-id="b8036-318">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="b8036-319">Peso del paquete físico en libras.</span><span class="sxs-lookup"><span data-stu-id="b8036-319">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="b8036-320">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-320">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8036-321">**Width**</span><span class="sxs-lookup"><span data-stu-id="b8036-321">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8036-322">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="b8036-322">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b8036-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8036-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8036-324">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="b8036-324">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="b8036-325">Ancho del paquete físico en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="b8036-325">Width of the physical package in inches.</span></span>

<span data-ttu-id="b8036-326">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-326">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8036-327">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8036-327">Remarks</span></span>

<span data-ttu-id="b8036-328">La clase de **\_ placa base de Win32** se deriva de la [**\_ tarjeta CIM**](cim-card.md) , que deriva de [**CIM \_ PhysicalPackage**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8036-328">The **Win32\_BaseBoard** class is derived from [**CIM\_Card**](cim-card.md) which derives from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b8036-329">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b8036-329">Examples</span></span>

<span data-ttu-id="b8036-330">En el ejemplo Perl del equipo de lista de propiedades de la [placa base](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8) se devuelve información acerca de la placa base del equipo.</span><span class="sxs-lookup"><span data-stu-id="b8036-330">The [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8) Perl sample returns information about the computer baseboard.</span></span>

<span data-ttu-id="b8036-331">En el ejemplo de PowerShell de [propiedades de placa base del equipo](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9) se devuelve información acerca de la placa base del equipo.</span><span class="sxs-lookup"><span data-stu-id="b8036-331">The [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9) PowerShell sample returns information about the computer baseboard.</span></span>

<span data-ttu-id="b8036-332">El siguiente ejemplo de VBScript también devuelve información acerca de la placa base del equipo.</span><span class="sxs-lookup"><span data-stu-id="b8036-332">The following VBScript sample also returns information about the computer baseboard.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BaseBoard") 
 
For Each objItem in colItems 
    For Each strOption in objItem.ConfigOptions 
        Wscript.Echo "Configuration Option: " & strOption 
    Next 
    Wscript.Echo "Depth: " & objItem.Depth 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Height: " & objItem.Height 
    Wscript.Echo "Hosting Board: " & objItem.HostingBoard 
    Wscript.Echo "Hot Swappable: " & objItem.HotSwappable 
    Wscript.Echo "Manufacturer: " & objItem.Manufacturer 
    Wscript.Echo "Model: " & objItem.Model 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Other Identifying Information: " & _ 
        objItem.OtherIdentifyingInfo 
    Wscript.Echo "Part Number: " & objItem.PartNumber 
    Wscript.Echo "Powered-On: " & objItem.PoweredOn 
    Wscript.Echo "Product: " & objItem.Product 
    Wscript.Echo "Removable: " & objItem.Removable 
    Wscript.Echo "Replaceable: " & objItem.Replaceable 
    Wscript.Echo "Requirements Description: " & objItem.RequirementsDescription 
    Wscript.Echo "Requires Daughterboard: " & objItem.RequiresDaughterBoard 
    Wscript.Echo "Serial Number: " & objItem.SerialNumber 
    Wscript.Echo "SKU: " & objItem.SKU 
    Wscript.Echo "Slot Layout: " & objItem.SlotLayout 
    Wscript.Echo "Special Requirements: " & objItem.SpecialRequirements 
    Wscript.Echo "Tag: " & objItem.Tag 
    Wscript.Echo "Version: " & objItem.Version 
    Wscript.Echo "Weight: " & objItem.Weight 
    Wscript.Echo "Width: " & objItem.Width 
Next 
```



## <a name="requirements"></a><span data-ttu-id="b8036-333">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8036-333">Requirements</span></span>



| <span data-ttu-id="b8036-334">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8036-334">Requirement</span></span> | <span data-ttu-id="b8036-335">Value</span><span class="sxs-lookup"><span data-stu-id="b8036-335">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8036-336">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8036-336">Minimum supported client</span></span><br/> | <span data-ttu-id="b8036-337">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8036-337">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8036-338">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8036-338">Minimum supported server</span></span><br/> | <span data-ttu-id="b8036-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8036-339">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8036-340">MOF</span><span class="sxs-lookup"><span data-stu-id="b8036-340">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8036-341"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8036-341"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8036-342">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8036-342">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8036-343"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8036-343"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8036-344">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8036-344">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8036-345">**\_Tarjeta CIM**</span><span class="sxs-lookup"><span data-stu-id="b8036-345">**CIM\_Card**</span></span>](cim-card.md)
</dt> <dt>

[<span data-ttu-id="b8036-346">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="b8036-346">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

