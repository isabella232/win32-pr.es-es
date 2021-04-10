---
description: La \_ clase WMI OnBoardDevice de Win32 representa los dispositivos de adaptador comunes integrados en la placa base (placa de sistema).
ms.assetid: 6fac38b4-7c04-4f64-997d-40bcbf767959
ms.tgt_platform: multiple
title: Win32_OnBoardDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OnBoardDevice
- Win32_OnBoardDevice.Caption
- Win32_OnBoardDevice.CreationClassName
- Win32_OnBoardDevice.Description
- Win32_OnBoardDevice.DeviceType
- Win32_OnBoardDevice.Enabled
- Win32_OnBoardDevice.HotSwappable
- Win32_OnBoardDevice.InstallDate
- Win32_OnBoardDevice.Manufacturer
- Win32_OnBoardDevice.Model
- Win32_OnBoardDevice.Name
- Win32_OnBoardDevice.OtherIdentifyingInfo
- Win32_OnBoardDevice.PartNumber
- Win32_OnBoardDevice.PoweredOn
- Win32_OnBoardDevice.Removable
- Win32_OnBoardDevice.Replaceable
- Win32_OnBoardDevice.SerialNumber
- Win32_OnBoardDevice.SKU
- Win32_OnBoardDevice.Status
- Win32_OnBoardDevice.Tag
- Win32_OnBoardDevice.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5fae5416a4b3cbeda0d8c63f6834c0406e628013
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275077"
---
# <a name="win32_onboarddevice-class"></a><span data-ttu-id="3cf2b-103">\_Clase Win32 OnBoardDevice</span><span class="sxs-lookup"><span data-stu-id="3cf2b-103">Win32\_OnBoardDevice class</span></span>

<span data-ttu-id="3cf2b-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ OnBoardDevice de Win32** representa los dispositivos de adaptador comunes integrados en la placa base (placa de sistema).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-104">The **Win32\_OnBoardDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents common adapter devices built into the motherboard (system board).</span></span>

<span data-ttu-id="3cf2b-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3cf2b-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cf2b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3cf2b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{AEECF151-D0EA-11d2-ABFC-00805F538618}"), AMENDMENT]
class Win32_OnBoardDevice : CIM_PhysicalComponent
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  uint16   DeviceType;
  boolean  Enabled;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="3cf2b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3cf2b-108">Members</span></span>

<span data-ttu-id="3cf2b-109">La **clase \_ OnBoardDevice de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3cf2b-109">The **Win32\_OnBoardDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="3cf2b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3cf2b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3cf2b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3cf2b-111">Properties</span></span>

<span data-ttu-id="3cf2b-112">La **clase \_ OnBoardDevice de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-112">The **Win32\_OnBoardDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3cf2b-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-116">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-117">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-117">Short description of the object.</span></span>

<span data-ttu-id="3cf2b-118">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-122">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="3cf2b-122">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-123">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-123">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="3cf2b-124">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-124">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="3cf2b-125">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-125">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-129">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 10 \| Description")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-129">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Description")</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-130">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-130">Description of the object.</span></span>

<span data-ttu-id="3cf2b-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-132">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-132">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-133">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-135">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (tipo de \| dispositivo 10 de tipo SMBIOS \| n)</span><span class="sxs-lookup"><span data-stu-id="3cf2b-135">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Device Type n")</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-136">Tipo de dispositivo que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-136">Type of device being represented.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3cf2b-137">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="3cf2b-137">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3cf2b-138">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="3cf2b-138">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

<span data-ttu-id="3cf2b-139">**Vídeo** (3)</span><span class="sxs-lookup"><span data-stu-id="3cf2b-139">**Video** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Controller"></span><span id="scsi_controller"></span><span id="SCSI_CONTROLLER"></span>

<span data-ttu-id="3cf2b-140">**Controladora SCSI** (4)</span><span class="sxs-lookup"><span data-stu-id="3cf2b-140">**SCSI Controller** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="3cf2b-141">**Ethernet** (5)</span><span class="sxs-lookup"><span data-stu-id="3cf2b-141">**Ethernet** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="3cf2b-142">**Token ring** (6)</span><span class="sxs-lookup"><span data-stu-id="3cf2b-142">**Token Ring** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Sound"></span><span id="sound"></span><span id="SOUND"></span>

<span data-ttu-id="3cf2b-143">**Sonido** (7)</span><span class="sxs-lookup"><span data-stu-id="3cf2b-143">**Sound** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3cf2b-144">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-144">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-145">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-147">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 10 \| Estado del dispositivo n")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 10\|Device Status n")</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-148">Si es **true**, el dispositivo incorporado está disponible para su uso.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-148">If **TRUE**, the on-board device is available for use.</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-149">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-149">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-150">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-152">Si es **true**, un paquete físico puede intercambiarse en caliente (si es posible reemplazarlo por uno físicamente diferente pero equivalente mientras el paquete contenedor tiene energía aplicada a él).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-152">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it).</span></span> <span data-ttu-id="3cf2b-153">Por ejemplo, un paquete de unidad de disco insertado mediante conectores SCA es extraíble y puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-153">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="3cf2b-154">Todos los paquetes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-154">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="3cf2b-155">Esta propiedad se hereda de [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-155">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-156">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-156">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-157">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-159">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-160">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-160">Date and time the object was installed.</span></span> <span data-ttu-id="3cf2b-161">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-161">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3cf2b-162">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-163">**Le**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-163">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-166">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="3cf2b-166">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-167">Nombre de la organización responsable de producir el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-167">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="3cf2b-168">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-168">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-169">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-169">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-172">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="3cf2b-172">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-173">Nombre por el que se suele conocer el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-173">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="3cf2b-174">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-174">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-175">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-175">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-178">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-178">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-179">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-179">Label by which the object is known.</span></span> <span data-ttu-id="3cf2b-180">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-180">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="3cf2b-181">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-182">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-182">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-185">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-185">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="3cf2b-186">Un ejemplo son los datos de código de barras asociados a un elemento que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-186">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="3cf2b-187">Tenga en cuenta que si solo están disponibles los datos de código de barras y es único o se puede usar como una clave de elemento, esta propiedad sería **null** y los datos de código de barras se usan como clave de clase en la propiedad de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-187">Note that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="3cf2b-188">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-188">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-189">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-189">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-192">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="3cf2b-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-193">Número de pieza asignado por la organización responsable de producir o fabricar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-193">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="3cf2b-194">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-194">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-195">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-195">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-196">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-198">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-198">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="3cf2b-199">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-199">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-200">**Quitar**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-200">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-201">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-203">Si es **true**, un paquete físico es extraíble (si está diseñado para tomarse dentro y fuera del contenedor físico en el que se encuentra normalmente, sin perjudicar la función del empaquetado general).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-203">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="3cf2b-204">Un paquete todavía puede ser extraíble si la alimentación debe estar "desactivada" para realizar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-204">A package can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="3cf2b-205">Si la potencia puede ser "ON" y se ha quitado el paquete, el elemento es extraíble y puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-205">If power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="3cf2b-206">Por ejemplo, una batería adicional en un equipo portátil es extraíble, como un paquete de unidad de disco insertado mediante conectores SCA.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-206">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="3cf2b-207">Sin embargo, el último puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-207">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="3cf2b-208">La pantalla de un portátil no es extraíble, ni tampoco es una fuente de alimentación que no sea redundante.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-208">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="3cf2b-209">La eliminación de estos componentes afectaría a la función del empaquetado general o no es posible debido a la estrecha integración del paquete.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-209">Removing these components would affect the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="3cf2b-210">Esta propiedad se hereda de [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-210">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-211">**Reemplazables**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-211">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-212">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-214">Si es **true**, un paquete físico es reemplazable (si es posible reemplazar, FRU o actualizar, el elemento con uno físicamente diferente).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-214">If **TRUE**, a physical package is replaceable (if it is possible to replace, FRU or upgrade, the element with a physically different one).</span></span> <span data-ttu-id="3cf2b-215">Por ejemplo, algunos sistemas informáticos permiten que el chip del procesador principal se actualice a una clasificación de reloj más alta.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-215">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="3cf2b-216">En este caso, se dice que el procesador es reemplazable.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-216">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="3cf2b-217">Otro ejemplo es un paquete de fuente de alimentación montado en raíles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-217">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="3cf2b-218">Todos los paquetes extraíbles se pueden reemplazar de forma inherente.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-218">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="3cf2b-219">Esta propiedad se hereda de [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-219">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-220">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-220">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-221">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-223">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="3cf2b-223">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-224">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-224">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="3cf2b-225">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-225">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-226">**SKU**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-226">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-229">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="3cf2b-229">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-230">Número de unidad de almacén para el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-230">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="3cf2b-231">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-231">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-232">**Estado**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-232">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-233">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-235">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-235">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-236">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-236">Current status of the object.</span></span> <span data-ttu-id="3cf2b-237">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-237">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="3cf2b-238">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-238">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="3cf2b-239">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="3cf2b-239">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3cf2b-240">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-240">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3cf2b-241">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-241">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3cf2b-242">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3cf2b-243">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="3cf2b-243">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3cf2b-244">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-244">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3cf2b-245">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-245">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3cf2b-246">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-246">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3cf2b-247">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-247">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3cf2b-248">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-248">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3cf2b-249">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-249">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3cf2b-250">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-250">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3cf2b-251">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-251">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3cf2b-252">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-252">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3cf2b-253">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-253">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3cf2b-254">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-254">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3cf2b-255">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-255">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3cf2b-256">**Tag**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-256">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-259">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**invalidación**](../wmisdk/standard-qualifiers.md) ("etiqueta"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="3cf2b-259">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-260">Identificador único del dispositivo incorporado conectado al sistema.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-260">Unique identifier of the on-board device connected to the system.</span></span>

<span data-ttu-id="3cf2b-261">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-261">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="3cf2b-262">Ejemplo: "dispositivo de placa 1"</span><span class="sxs-lookup"><span data-stu-id="3cf2b-262">Example: "On Board Device 1"</span></span>

</dd> <dt>

<span data-ttu-id="3cf2b-263">**Versión**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-263">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf2b-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cf2b-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cf2b-266">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="3cf2b-266">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3cf2b-267">Versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-267">Version of the physical element.</span></span>

<span data-ttu-id="3cf2b-268">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-268">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3cf2b-269">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3cf2b-269">Remarks</span></span>

<span data-ttu-id="3cf2b-270">La **clase \_ OnBoardDevice de Win32** se deriva de [**\_ PhysicalComponent de CIM**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-270">The **Win32\_OnBoardDevice** class is derived from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3cf2b-271">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cf2b-271">Requirements</span></span>



| <span data-ttu-id="3cf2b-272">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cf2b-272">Requirement</span></span> | <span data-ttu-id="3cf2b-273">Value</span><span class="sxs-lookup"><span data-stu-id="3cf2b-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf2b-274">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cf2b-274">Minimum supported client</span></span><br/> | <span data-ttu-id="3cf2b-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3cf2b-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3cf2b-276">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cf2b-276">Minimum supported server</span></span><br/> | <span data-ttu-id="3cf2b-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3cf2b-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3cf2b-278">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3cf2b-278">Namespace</span></span><br/>                | <span data-ttu-id="3cf2b-279">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3cf2b-279">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3cf2b-280">MOF</span><span class="sxs-lookup"><span data-stu-id="3cf2b-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cf2b-281"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3cf2b-281"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cf2b-282">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3cf2b-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cf2b-283"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cf2b-283"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cf2b-284">Vea también</span><span class="sxs-lookup"><span data-stu-id="3cf2b-284">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf2b-285">**\_PHYSICALCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3cf2b-285">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> <dt>

[<span data-ttu-id="3cf2b-286">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="3cf2b-286">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
