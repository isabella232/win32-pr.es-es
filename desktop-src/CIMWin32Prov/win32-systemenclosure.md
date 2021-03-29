---
description: Representa las propiedades que están asociadas a un gabinete del sistema físico.
ms.assetid: a8244dc0-a95e-4940-9b92-7820bdf14916
ms.tgt_platform: multiple
title: Win32_SystemEnclosure (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemEnclosure
- Win32_SystemEnclosure.IsCompatible
- Win32_SystemEnclosure.AudibleAlarm
- Win32_SystemEnclosure.BreachDescription
- Win32_SystemEnclosure.CableManagementStrategy
- Win32_SystemEnclosure.Caption
- Win32_SystemEnclosure.ChassisTypes
- Win32_SystemEnclosure.CreationClassName
- Win32_SystemEnclosure.CurrentRequiredOrProduced
- Win32_SystemEnclosure.Depth
- Win32_SystemEnclosure.Description
- Win32_SystemEnclosure.HeatGeneration
- Win32_SystemEnclosure.Height
- Win32_SystemEnclosure.HotSwappable
- Win32_SystemEnclosure.InstallDate
- Win32_SystemEnclosure.LockPresent
- Win32_SystemEnclosure.Manufacturer
- Win32_SystemEnclosure.Model
- Win32_SystemEnclosure.Name
- Win32_SystemEnclosure.NumberOfPowerCords
- Win32_SystemEnclosure.OtherIdentifyingInfo
- Win32_SystemEnclosure.PartNumber
- Win32_SystemEnclosure.PoweredOn
- Win32_SystemEnclosure.Removable
- Win32_SystemEnclosure.Replaceable
- Win32_SystemEnclosure.SecurityBreach
- Win32_SystemEnclosure.SecurityStatus
- Win32_SystemEnclosure.SerialNumber
- Win32_SystemEnclosure.ServiceDescriptions
- Win32_SystemEnclosure.ServicePhilosophy
- Win32_SystemEnclosure.SKU
- Win32_SystemEnclosure.SMBIOSAssetTag
- Win32_SystemEnclosure.Status
- Win32_SystemEnclosure.Tag
- Win32_SystemEnclosure.TypeDescriptions
- Win32_SystemEnclosure.Version
- Win32_SystemEnclosure.VisibleAlarm
- Win32_SystemEnclosure.Weight
- Win32_SystemEnclosure.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c7f3b65f6435d8ff828aebf5310f9b21a2ea7f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000788"
---
# <a name="win32_systemenclosure-class"></a><span data-ttu-id="8e8a8-103">\_Clase Win32 SystemEnclosure</span><span class="sxs-lookup"><span data-stu-id="8e8a8-103">Win32\_SystemEnclosure class</span></span>

<span data-ttu-id="8e8a8-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemEnclosure de Win32** representa las propiedades asociadas a un gabinete del sistema físico.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-104">The **Win32\_SystemEnclosure** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties that are associated with a physical system enclosure.</span></span>

<span data-ttu-id="8e8a8-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8e8a8-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e8a8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e8a8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B94-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemEnclosure : CIM_Chassis
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  uint16   ChassisTypes[];
  string   CreationClassName;
  sint16   CurrentRequiredOrProduced;
  real32   Depth;
  string   Description;
  uint16   HeatGeneration;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  uint16   NumberOfPowerCords;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  uint16   SecurityStatus;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   SMBIOSAssetTag;
  string   Status;
  string   Tag;
  string   TypeDescriptions[];
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="8e8a8-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8e8a8-108">Members</span></span>

<span data-ttu-id="8e8a8-109">La **clase \_ SystemEnclosure de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8e8a8-109">The **Win32\_SystemEnclosure** class has these types of members:</span></span>

-   [<span data-ttu-id="8e8a8-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="8e8a8-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8e8a8-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8e8a8-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8e8a8-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8e8a8-112">Methods</span></span>

<span data-ttu-id="8e8a8-113">La clase **Win32 \_ SystemEnclosure** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-113">The **Win32\_SystemEnclosure** class has these methods.</span></span>



| <span data-ttu-id="8e8a8-114">Método</span><span class="sxs-lookup"><span data-stu-id="8e8a8-114">Method</span></span>           | <span data-ttu-id="8e8a8-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e8a8-115">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="8e8a8-116">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-116">**IsCompatible**</span></span> | <span data-ttu-id="8e8a8-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-117">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8e8a8-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8e8a8-118">Properties</span></span>

<span data-ttu-id="8e8a8-119">La **clase \_ SystemEnclosure de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-119">The **Win32\_SystemEnclosure** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e8a8-120">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-120">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-121">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-123">Si es **true**, el marco está equipado con una alarma audible.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-123">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="8e8a8-124">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-124">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-125">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-125">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-128">Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-128">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-129">Cadena de forma libre que proporciona más información si la propiedad **SecurityBreach** indica que se ha producido un evento relacionado con la seguridad.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-129">Free-form string that provides more information if the **SecurityBreach** property indicates that a security-related event occurred.</span></span>

<span data-ttu-id="8e8a8-130">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-130">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-131">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-131">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-134">Cadena de forma libre que contiene información sobre cómo se conectan y empaquetan los distintos cables del marco.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-134">Free-form string that contains information about how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="8e8a8-135">Con muchos cables de red, relacionados con el almacenamiento y de alimentación, la administración de cables puede ser un esfuerzo complejo y desafiante.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-135">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="8e8a8-136">Esta propiedad contiene información para ayudar en el ensamblado y el servicio del marco.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-136">This property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="8e8a8-137">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-137">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-141">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-141">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-142">Breve descripción del objeto: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-142">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="8e8a8-143">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-144">**ChassisTypes**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-144">**ChassisTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-145">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-145">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-147">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Tabla global de contenedor físico DMTF \| 002,1 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ chasis CIM**](cim-chassis.md).**TypeDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-147">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Physical Container Global Table\|002.1"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Chassis**](cim-chassis.md).**TypeDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-148">Matriz de tipos de chasis.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-148">Array of chassis types.</span></span>

<span data-ttu-id="8e8a8-149">Este valor procede del miembro de **tipo** del **alojamiento del sistema o** de la estructura del chasis en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-149">This value comes from the **Type** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="8e8a8-150">Esta propiedad se hereda del [**\_ chasis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-150">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8e8a8-151">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-151">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e8a8-152">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-152">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="8e8a8-153">**Escritorio** (3)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-153">**Desktop** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span data-ttu-id="8e8a8-154">**Escritorio de bajo perfil** (4)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-154">**Low Profile Desktop** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span data-ttu-id="8e8a8-155">**Cuadro de pizza** (5)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-155">**Pizza Box** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span data-ttu-id="8e8a8-156">**Minitorre (6** )</span><span class="sxs-lookup"><span data-stu-id="8e8a8-156">**Mini Tower** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span data-ttu-id="8e8a8-157">**Torre** (7)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-157">**Tower** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span data-ttu-id="8e8a8-158">**Portable** (8)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-158">**Portable** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="8e8a8-159">**Portátil** (9)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-159">**Laptop** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span data-ttu-id="8e8a8-160">**Cuaderno** (10)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-160">**Notebook** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span data-ttu-id="8e8a8-161">**Mano** (11)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-161">**Hand Held** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span data-ttu-id="8e8a8-162">**Estación de acoplamiento** (12)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-162">**Docking Station** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span data-ttu-id="8e8a8-163">**Todo en uno** (13)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-163">**All in One** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span data-ttu-id="8e8a8-164">**Sub Notebook** (14)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-164">**Sub Notebook** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span data-ttu-id="8e8a8-165">**Ahorrar espacio** (15)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-165">**Space-Saving** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span data-ttu-id="8e8a8-166">**Caja del almuerzo** (16)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-166">**Lunch Box** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span data-ttu-id="8e8a8-167">**Chasis del sistema principal** (17)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-167">**Main System Chassis** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span data-ttu-id="8e8a8-168">**Chasis de expansión** (18)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-168">**Expansion Chassis** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span data-ttu-id="8e8a8-169">**Subchasis** (19)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-169">**SubChassis** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span data-ttu-id="8e8a8-170">**Chasis de expansión de bus** (20)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-170">**Bus Expansion Chassis** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span data-ttu-id="8e8a8-171">**Chasis de periféricos** (21)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-171">**Peripheral Chassis** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span data-ttu-id="8e8a8-172">**Chasis de almacenamiento** (22)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-172">**Storage Chassis** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span data-ttu-id="8e8a8-173">**Chasis de montaje en bastidor** (23)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-173">**Rack Mount Chassis** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span data-ttu-id="8e8a8-174">**Equipos sellados** (24)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-174">**Sealed-Case PC** (24)</span></span>

</dt> <dd></dd> <dt>

<span id="Tablet"></span><span id="tablet"></span><span id="TABLET"></span>

<span data-ttu-id="8e8a8-175">**Tableta** (30)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-175">**Tablet** (30)</span></span>

</dt> <dd></dd> <dt>

<span id="Convertible"></span><span id="Convertible"></span><span id="Convertible"></span>

<span data-ttu-id="8e8a8-176">**Convertible** (31)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-176">**Convertible** (31)</span></span>

</dt> <dd></dd> <dt>

<span id="Detachable"></span><span id="Detachable "></span><span id="Detachable "></span>

<span data-ttu-id="8e8a8-177">**Desasociable** (32)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-177">**Detachable** (32)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e8a8-178">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-178">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-181">Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-181">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-182">Nombre de la primera clase concreta que aparece en la cadena de herencia que se utiliza en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-182">Name of the first concrete class that appears in the inheritance chain that is used in the creation of an instance.</span></span> <span data-ttu-id="8e8a8-183">Cuando se usa con las otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-183">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="8e8a8-184">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-184">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-185">**CurrentRequiredOrProduced**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-185">**CurrentRequiredOrProduced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-186">Tipo de datos: **sint16**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-186">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-188">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("amperios at 120 voltios")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-188">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("amps at 120 volts")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-189">Actual que requiere el chasis a 120 v.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-189">Current that is required by the chassis at 120V.</span></span> <span data-ttu-id="8e8a8-190">Si el chasis proporciona alimentación, como en el caso de una fuente de alimentación ininterrumpida (SAI), esta propiedad puede indicar el amperaje producido (como un número negativo).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-190">If power is provided by the chassis—as in the case of an uninterruptible power supply (UPS)—this property may indicate the amperage produced (as a negative number).</span></span>

<span data-ttu-id="8e8a8-191">Esta propiedad se hereda del [**\_ chasis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-191">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-192">**Profundidad**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-192">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-193">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-193">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-195">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-195">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-196">Profundidad del paquete físico: en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-196">Depth of the physical package—in inches.</span></span>

<span data-ttu-id="8e8a8-197">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-197">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-198">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-201">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-201">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-202">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-202">Description of the object.</span></span>

<span data-ttu-id="8e8a8-203">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-204">**HeatGeneration**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-204">**HeatGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-205">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-207">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("BTU por hora")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-207">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("BTU per hour")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-208">Cantidad de calor generada por el chasis en BTU/hora.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-208">Amount of heat that is generated by the chassis in BTU/hour.</span></span>

<span data-ttu-id="8e8a8-209">Esta propiedad se hereda del [**\_ chasis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-209">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-210">**Height**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-210">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-211">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-211">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-213">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-213">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-214">Alto del paquete físico: en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-214">Height of the physical package—in inches.</span></span>

<span data-ttu-id="8e8a8-215">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-215">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-216">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-216">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-217">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-219">Si es **true**, un paquete físico puede intercambiarse en caliente (si es posible reemplazarlo por uno físicamente diferente pero equivalente mientras el paquete contenedor tiene energía aplicada a él).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-219">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it).</span></span> <span data-ttu-id="8e8a8-220">Por ejemplo, un paquete de unidad de disco que se inserta mediante conectores SCA es extraíble y puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-220">For example, a disk drive package that is inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="8e8a8-221">Todos los paquetes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-221">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="8e8a8-222">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-222">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-223">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-223">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-224">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-224">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-226">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-226">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-227">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-227">Date and time the object was installed.</span></span> <span data-ttu-id="8e8a8-228">Esta propiedad no requiere un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-228">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8e8a8-229">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-229">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-230">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-230">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-231">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-233">Si es **true**, el marco está protegido con un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-233">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="8e8a8-234">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-234">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-235">**Le**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-235">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-236">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-238">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-238">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-239">Nombre de la organización que produce el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-239">Name of the organization that produces the physical element.</span></span>

<span data-ttu-id="8e8a8-240">Este valor procede del miembro **manufacturer** del alojamiento del **sistema o** de la estructura del chasis en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-240">This value comes from the **Manufacturer** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="8e8a8-241">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-241">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-242">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-242">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-243">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-245">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-245">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-246">Nombre por el que se conoce el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-246">Name by which the physical element is known.</span></span>

<span data-ttu-id="8e8a8-247">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-247">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-248">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-248">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-251">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-251">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-252">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-252">Label by which the object is known.</span></span> <span data-ttu-id="8e8a8-253">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-253">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="8e8a8-254">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-254">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-255">**NumberOfPowerCords**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-255">**NumberOfPowerCords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-256">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-256">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-258">Número de cables de alimentación que deben estar conectados al chasis para que funcionen todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-258">Number of power cords that must be connected to the chassis for all of the components to operate.</span></span>

<span data-ttu-id="8e8a8-259">Esta propiedad se hereda del [**\_ chasis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-259">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-260">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-260">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-263">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-263">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="8e8a8-264">Un ejemplo son los datos de código de barras que están asociados a un elemento que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-264">One example is bar code data that is associated with an element that also has an asset tag.</span></span> <span data-ttu-id="8e8a8-265">Tenga en cuenta que si solo están disponibles los datos de código de barras y es único o se puede usar como una clave de elemento, esta propiedad sería **null** y los datos de código de barras usados como clave de clase en la propiedad de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-265">Be aware that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data used as the class key, in the tag property.</span></span>

<span data-ttu-id="8e8a8-266">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-266">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-267">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-267">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-268">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-270">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-270">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-271">Número de pieza asignado por la organización que produce o fabrica el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-271">Part number that is assigned by the organization that produces or manufacturing the physical element.</span></span>

<span data-ttu-id="8e8a8-272">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-272">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-273">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-273">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-274">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-276">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-276">If **TRUE**, the physical element is powered ON.</span></span>

<span data-ttu-id="8e8a8-277">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-277">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-278">**Quitar**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-278">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-279">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-281">Si es **true**, un paquete físico es extraíble (si está diseñado para tomarse dentro y fuera del contenedor físico en el que se encuentra normalmente, sin perjudicar la función del empaquetado general).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-281">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="8e8a8-282">Un paquete todavía puede ser extraíble si la alimentación debe estar "desactivada" para realizar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-282">A package can still be removable if the power must be "OFF" to perform the removal.</span></span> <span data-ttu-id="8e8a8-283">Si se puede quitar el paquete mientras la alimentación está activada, el elemento es extraíble y puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-283">If the package can be removed while the power is ON, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="8e8a8-284">Por ejemplo, una batería adicional en un equipo portátil es extraíble, como un paquete de unidad de disco que se inserta mediante conectores de la aplicación de configuración del servidor (SCA).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-284">For example, an extra battery in a laptop is removable, as is a disk drive package that is inserted using Server Configuration Application (SCA) connectors.</span></span> <span data-ttu-id="8e8a8-285">Sin embargo, el último puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-285">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="8e8a8-286">Una pantalla de equipo portátil no es extraíble, ni es una fuente de alimentación no redundante.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-286">A laptop display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="8e8a8-287">La eliminación de estos componentes afectaría a la función del empaquetado general o no es posible debido a la estrecha integración del paquete.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-287">Removing these components would affect the function of the overall packaging or is impossible because of the tight integration of the package.</span></span>

<span data-ttu-id="8e8a8-288">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-288">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-289">**Reemplazables**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-289">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-290">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-292">Si **es true**, este componente de medio físico se puede reemplazar por uno físicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-292">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="8e8a8-293">Por ejemplo, algunos sistemas informáticos permiten que el chip del procesador principal se actualice a una clasificación de reloj más alta.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-293">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="8e8a8-294">En este caso, se dice que el procesador es reemplazable.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-294">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="8e8a8-295">Otro ejemplo es un paquete de fuente de alimentación montado en raíles deslizantes.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-295">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="8e8a8-296">Todos los paquetes extraíbles se pueden reemplazar de forma inherente.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-296">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="8e8a8-297">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-297">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-298">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-298">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-299">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-301">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Tabla global de contenedor físico DMTF \| 002,12 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-302">Estado de una infracción física del marco.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-302">Status of a physical breach of the frame.</span></span>

<span data-ttu-id="8e8a8-303">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-303">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8e8a8-304">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-304">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e8a8-305">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-305">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="8e8a8-306">**Sin brecha** (3)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-306">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="8e8a8-307">**Intento de infracción** (4)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-307">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="8e8a8-308">**Infracción correcta** (5)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-308">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e8a8-309">**SecurityStatus**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-309">**SecurityStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-310">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-312">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("estado de seguridad de SMBIOS \| tipo 3 \| ")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-312">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 3\|Security Status")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-313">Configuración de seguridad para la entrada externa, por ejemplo, un teclado, a un equipo.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-313">Security setting for external input, for example, a keyboard, to a computer.</span></span>

<span data-ttu-id="8e8a8-314">Este valor procede del miembro de **Estado de seguridad** de la estructura **del chasis o del chasis del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-314">This value comes from the **Security Status** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8e8a8-315">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-315">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e8a8-316">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-316">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="8e8a8-317">**Ninguno** (3)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-317">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="External_interface_locked_out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

<span data-ttu-id="8e8a8-318">**Interfaz externa bloqueada** (4)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-318">**External interface locked out** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="External_interface_enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

<span data-ttu-id="8e8a8-319">**Interfaz externa habilitada** (5)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-319">**External interface enabled** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e8a8-320">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-320">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-321">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-323">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-323">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-324">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-324">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="8e8a8-325">Este valor procede del miembro del **número de serie** del **alojamiento del sistema o** de la estructura del chasis en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-325">This value comes from the **Serial Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="8e8a8-326">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-326">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-327">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-327">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-328">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-328">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-330">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-330">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-331">Matriz de explicaciones más detalladas para cualquiera de las entradas de la matriz **ServicePhilosophy** .</span><span class="sxs-lookup"><span data-stu-id="8e8a8-331">Array of more detailed explanations for any of the entries in the **ServicePhilosophy** array.</span></span> <span data-ttu-id="8e8a8-332">Tenga en cuenta que cada entrada de esta matriz está relacionada con la entrada de **ServicePhilosophy** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-332">Be aware that each entry of this array is related to the entry in **ServicePhilosophy** that is located at the same index.</span></span>

<span data-ttu-id="8e8a8-333">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-333">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-334">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-334">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-335">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-335">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-337">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-337">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-338">Matriz que incluye si el marco se va a mantener desde la parte superior, delantera, posterior o lateral, si el marco tiene bandejas deslizantes o lados extraíbles, y si el fotograma se va a mover, por ejemplo, con rodillos.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-338">Array that includes whether the frame is serviced from the top, front, back, or side, whether the frame has sliding trays or removable sides, and whether the frame is moveable—for example, having rollers.</span></span>

<span data-ttu-id="8e8a8-339">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-339">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e8a8-340">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-340">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8e8a8-341">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-341">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="8e8a8-342">**Servicio desde arriba** (2)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-342">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="8e8a8-343">**Servicio desde delante** (3)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-343">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="8e8a8-344">**Servicio de atrás** (4)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-344">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="8e8a8-345">**Servicio desde el lado** (5)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-345">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="8e8a8-346">**Bandejas deslizantes** (6)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-346">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="8e8a8-347">**Lados extraíbles** (7)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-347">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="8e8a8-348">**Móvil** (8)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-348">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e8a8-349">**SKU**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-349">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-350">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-352">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-352">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-353">Número de referencia de almacén para el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-353">Stock keeping unit number for the physical element.</span></span>

<span data-ttu-id="8e8a8-354">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-355">**SMBIOSAssetTag**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-355">**SMBIOSAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-356">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-358">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| etiqueta de recurso de tipo SMBIOS 3 \| ")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-358">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 3\|Asset Tag")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-359">Número de etiqueta de activo del alojamiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-359">Asset tag number of the system enclosure.</span></span>

<span data-ttu-id="8e8a8-360">Este valor procede del miembro **número de etiqueta de activo** del **alojamiento del sistema o** de la estructura del chasis en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-360">This value comes from the **Asset Tag Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-361">**Estado**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-361">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-362">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-364">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-364">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-365">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-365">Current status of the object.</span></span> <span data-ttu-id="8e8a8-366">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-366">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8e8a8-367">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-367">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8e8a8-368">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="8e8a8-368">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8e8a8-369">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-369">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8e8a8-370">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-370">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8e8a8-371">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-371">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8e8a8-372">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8e8a8-372">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8e8a8-373">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-373">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8e8a8-374">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-374">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8e8a8-375">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-375">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e8a8-376">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-376">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8e8a8-377">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-377">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8e8a8-378">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-378">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8e8a8-379">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-379">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8e8a8-380">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-380">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8e8a8-381">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-381">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8e8a8-382">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-382">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8e8a8-383">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-383">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8e8a8-384">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-384">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8e8a8-385">**Tag**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-385">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-386">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-388">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**invalidación**](../wmisdk/standard-qualifiers.md) ("etiqueta"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-388">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-389">Identificador único del alojamiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-389">Unique identifier of the system enclosure.</span></span>

<span data-ttu-id="8e8a8-390">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-390">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="8e8a8-391">Ejemplo: "gabinete del sistema 1"</span><span class="sxs-lookup"><span data-stu-id="8e8a8-391">Example: "System Enclosure 1"</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-392">**TypeDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-392">**TypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-393">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-393">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-395">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ chasis CIM**](cim-chassis.md).**ChassisTypes**")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-395">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Chassis**](cim-chassis.md).**ChassisTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-396">Matriz de más información sobre las entradas de la matriz **ChassisTypes** .</span><span class="sxs-lookup"><span data-stu-id="8e8a8-396">Array of more information about the **ChassisTypes** array entries.</span></span> <span data-ttu-id="8e8a8-397">Tenga en cuenta que cada entrada de esta matriz está relacionada con la entrada de **ChassisTypes** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-397">Be aware that each entry of this array is related to the entry in **ChassisTypes** that is located at the same index.</span></span>

<span data-ttu-id="8e8a8-398">Esta propiedad se hereda del [**\_ chasis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-398">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-399">**Versión**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-399">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-400">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-401">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-402">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="8e8a8-402">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-403">Versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-403">Version of the physical element.</span></span>

<span data-ttu-id="8e8a8-404">Este valor procede del miembro de la **versión** del **alojamiento del sistema o** de la estructura del chasis en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-404">This value comes from the **Version** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="8e8a8-405">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-405">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-406">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-406">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-407">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-407">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-408">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-409">Si **es true**, el equipo incluye una alarma visible.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-409">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="8e8a8-410">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-410">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-411">**Peso**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-411">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-412">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-412">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-414">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("libras")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-414">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-415">Peso del paquete físico en libras.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-415">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="8e8a8-416">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-416">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e8a8-417">**Width**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-417">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e8a8-418">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-418">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-419">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e8a8-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e8a8-420">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="8e8a8-420">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="8e8a8-421">Ancho del paquete físico en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-421">Width of the physical package in inches.</span></span>

<span data-ttu-id="8e8a8-422">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-422">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e8a8-423">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e8a8-423">Remarks</span></span>

<span data-ttu-id="8e8a8-424">La **clase \_ SystemEnclosure de Win32** se deriva [**del \_ chasis CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="8e8a8-424">The **Win32\_SystemEnclosure** class is derived from [**CIM\_Chassis**](cim-chassis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8e8a8-425">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8e8a8-425">Examples</span></span>

<span data-ttu-id="8e8a8-426">El ejemplo de [recopilación de recursos del sistema multiproceso con](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell de PowerShell en la galería de TechNet usa una serie de clases, incluido **Win32 \_ SystemEnclosure**, para recuperar datos de un sistema.</span><span class="sxs-lookup"><span data-stu-id="8e8a8-426">The [Multithreaded System Asset Gathering with Powershell](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell example on TechNet gallery uses a number of classes, including **Win32\_SystemEnclosure**, to retrieve data from a system.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e8a8-427">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e8a8-427">Requirements</span></span>



| <span data-ttu-id="8e8a8-428">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e8a8-428">Requirement</span></span> | <span data-ttu-id="8e8a8-429">Value</span><span class="sxs-lookup"><span data-stu-id="8e8a8-429">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e8a8-430">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e8a8-430">Minimum supported client</span></span><br/> | <span data-ttu-id="8e8a8-431">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e8a8-431">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e8a8-432">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e8a8-432">Minimum supported server</span></span><br/> | <span data-ttu-id="8e8a8-433">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e8a8-433">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e8a8-434">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8e8a8-434">Namespace</span></span><br/>                | <span data-ttu-id="8e8a8-435">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8e8a8-435">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e8a8-436">MOF</span><span class="sxs-lookup"><span data-stu-id="8e8a8-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e8a8-437"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e8a8-437"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e8a8-438">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8e8a8-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e8a8-439"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e8a8-439"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e8a8-440">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e8a8-440">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e8a8-441">**\_Chasis CIM**</span><span class="sxs-lookup"><span data-stu-id="8e8a8-441">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> <dt>

[<span data-ttu-id="8e8a8-442">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="8e8a8-442">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8e8a8-443">Tareas WMI: hardware del equipo</span><span class="sxs-lookup"><span data-stu-id="8e8a8-443">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 
