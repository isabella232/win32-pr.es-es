---
description: La \_ clase del chasis CIM representa los elementos físicos que contienen otros elementos y proporcionan funcionalidad definible, como un escritorio, un nodo de procesamiento, un SAI, un almacenamiento en disco o en cinta, o una combinación de estos.
ms.assetid: 4c55dbff-bc4a-4cc9-8f34-29636defaa56
ms.tgt_platform: multiple
title: CIM_Chassis (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis
- CIM_Chassis.Caption
- CIM_Chassis.Description
- CIM_Chassis.InstallDate
- CIM_Chassis.Name
- CIM_Chassis.Status
- CIM_Chassis.CreationClassName
- CIM_Chassis.Manufacturer
- CIM_Chassis.Model
- CIM_Chassis.OtherIdentifyingInfo
- CIM_Chassis.PartNumber
- CIM_Chassis.PoweredOn
- CIM_Chassis.SerialNumber
- CIM_Chassis.SKU
- CIM_Chassis.Tag
- CIM_Chassis.Version
- CIM_Chassis.Depth
- CIM_Chassis.Height
- CIM_Chassis.HotSwappable
- CIM_Chassis.Removable
- CIM_Chassis.Replaceable
- CIM_Chassis.Weight
- CIM_Chassis.Width
- CIM_Chassis.AudibleAlarm
- CIM_Chassis.BreachDescription
- CIM_Chassis.CableManagementStrategy
- CIM_Chassis.LockPresent
- CIM_Chassis.SecurityBreach
- CIM_Chassis.ServiceDescriptions
- CIM_Chassis.ServicePhilosophy
- CIM_Chassis.VisibleAlarm
- CIM_Chassis.ChassisTypes
- CIM_Chassis.CurrentRequiredOrProduced
- CIM_Chassis.HeatGeneration
- CIM_Chassis.NumberOfPowerCords
- CIM_Chassis.TypeDescriptions
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b1eb7f5e2733056cf48c1c9333453613ace699c6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153245"
---
# <a name="cim_chassis-class"></a><span data-ttu-id="4e406-103">\_Clase de chasis CIM</span><span class="sxs-lookup"><span data-stu-id="4e406-103">CIM\_Chassis class</span></span>

<span data-ttu-id="4e406-104">La clase del **\_ chasis CIM** representa los elementos físicos que contienen otros elementos y proporcionan funcionalidad definible, como un escritorio, un nodo de procesamiento, un SAI, un almacenamiento en disco o en cinta, o una combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="4e406-104">The **CIM\_Chassis** class represents the physical elements that enclose other elements and provide definable functionality, such as a desktop, processing node, UPS, disk or tape storage, or a combination of these.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e406-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="4e406-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4e406-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4e406-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4e406-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4e406-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4e406-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="4e406-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e406-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e406-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B72-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chassis : CIM_PhysicalFrame
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  real32   Depth;
  real32   Height;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  real32   Weight;
  real32   Width;
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  boolean  LockPresent;
  uint16   SecurityBreach;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  boolean  VisibleAlarm;
  uint16   ChassisTypes[];
  sint16   CurrentRequiredOrProduced;
  uint16   HeatGeneration;
  uint16   NumberOfPowerCords;
  string   TypeDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="4e406-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="4e406-110">Members</span></span>

<span data-ttu-id="4e406-111">La clase del **\_ chasis CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4e406-111">The **CIM\_Chassis** class has these types of members:</span></span>

-   [<span data-ttu-id="4e406-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4e406-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="4e406-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4e406-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4e406-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="4e406-114">Methods</span></span>

<span data-ttu-id="4e406-115">La clase del **\_ chasis CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4e406-115">The **CIM\_Chassis** class has these methods.</span></span>



| <span data-ttu-id="4e406-116">Método</span><span class="sxs-lookup"><span data-stu-id="4e406-116">Method</span></span>                                                           | <span data-ttu-id="4e406-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e406-117">Description</span></span>                                                                                                                                      |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e406-118">**IsCompatible**</span><span class="sxs-lookup"><span data-stu-id="4e406-118">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-chassis.md) | <span data-ttu-id="4e406-119">Comprueba si el elemento físico al que se hace referencia puede estar contenido o insertado en el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="4e406-119">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="4e406-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="4e406-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4e406-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4e406-121">Properties</span></span>

<span data-ttu-id="4e406-122">La clase del **\_ chasis CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4e406-122">The **CIM\_Chassis** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e406-123">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="4e406-123">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-124">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4e406-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e406-126">Si es **true**, el marco está equipado con una alarma audible.</span><span class="sxs-lookup"><span data-stu-id="4e406-126">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="4e406-127">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-127">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-128">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="4e406-128">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e406-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-131">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span><span class="sxs-lookup"><span data-stu-id="4e406-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-132">Cadena de forma libre que proporciona más información si la propiedad **SecurityBreach** indica que se ha producido una infracción o algún otro evento relacionado con la seguridad.</span><span class="sxs-lookup"><span data-stu-id="4e406-132">Free-form string that provides more information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

<span data-ttu-id="4e406-133">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-133">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-134">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="4e406-134">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e406-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e406-137">Cadena de forma libre que contiene información sobre cómo se conectan los distintos cables y se empaquetan para el marco.</span><span class="sxs-lookup"><span data-stu-id="4e406-137">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="4e406-138">Con muchos cables de red, relacionados con el almacenamiento y de alimentación, la administración de cables puede ser un esfuerzo complejo y desafiante.</span><span class="sxs-lookup"><span data-stu-id="4e406-138">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="4e406-139">Esta propiedad de cadena contiene información para ayudar en el ensamblado y el servicio del marco.</span><span class="sxs-lookup"><span data-stu-id="4e406-139">This string property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="4e406-140">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-140">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-141">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4e406-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e406-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-144">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="4e406-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-145">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="4e406-145">A short textual description of the object.</span></span>

<span data-ttu-id="4e406-146">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-147">**ChassisTypes**</span><span class="sxs-lookup"><span data-stu-id="4e406-147">**ChassisTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-148">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e406-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4e406-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-150">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Tabla global de contenedor físico DMTF \| 002,1 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ chasis CIM**.**TypeDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="4e406-150">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.1"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Chassis**.**TypeDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-151">Matriz de valores enteros enumerados que indica el tipo de chasis.</span><span class="sxs-lookup"><span data-stu-id="4e406-151">Enumerated, integer-valued array that indicates the type of chassis.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4e406-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="4e406-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-153">Otros.</span><span class="sxs-lookup"><span data-stu-id="4e406-153">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e406-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="4e406-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-155">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="4e406-155">Unknown.</span></span>

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="4e406-156"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Escritorio** (3)</span><span class="sxs-lookup"><span data-stu-id="4e406-156"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-157">Escritorio.</span><span class="sxs-lookup"><span data-stu-id="4e406-157">Desktop.</span></span>

</dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span data-ttu-id="4e406-158"><span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**Escritorio de bajo perfil** (4)</span><span class="sxs-lookup"><span data-stu-id="4e406-158"><span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**Low Profile Desktop** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-159">Escritorio de bajo perfil.</span><span class="sxs-lookup"><span data-stu-id="4e406-159">Low-profile desktop.</span></span>

</dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span data-ttu-id="4e406-160"><span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**Cuadro de pizza** (5)</span><span class="sxs-lookup"><span data-stu-id="4e406-160"><span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**Pizza Box** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-161">Cuadro pizza.</span><span class="sxs-lookup"><span data-stu-id="4e406-161">Pizza box.</span></span>

</dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span data-ttu-id="4e406-162"><span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**Minitorre (6** )</span><span class="sxs-lookup"><span data-stu-id="4e406-162"><span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**Mini Tower** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-163">Minitorre.</span><span class="sxs-lookup"><span data-stu-id="4e406-163">Mini tower.</span></span>

</dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span data-ttu-id="4e406-164"><span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**Torre** (7)</span><span class="sxs-lookup"><span data-stu-id="4e406-164"><span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**Tower** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-165">Torre.</span><span class="sxs-lookup"><span data-stu-id="4e406-165">Tower.</span></span>

</dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span data-ttu-id="4e406-166"><span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**Portable** (8)</span><span class="sxs-lookup"><span data-stu-id="4e406-166"><span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**Portable** (8)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-167">Portable.</span><span class="sxs-lookup"><span data-stu-id="4e406-167">Portable.</span></span>

</dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="4e406-168"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Portátil** (9)</span><span class="sxs-lookup"><span data-stu-id="4e406-168"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (9)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-169">Equipo portátil.</span><span class="sxs-lookup"><span data-stu-id="4e406-169">Laptop.</span></span>

</dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span data-ttu-id="4e406-170"><span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**Cuaderno** (10)</span><span class="sxs-lookup"><span data-stu-id="4e406-170"><span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**Notebook** (10)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-171">Inspiron.</span><span class="sxs-lookup"><span data-stu-id="4e406-171">Notebook.</span></span>

</dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span data-ttu-id="4e406-172"><span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**Mano** (11)</span><span class="sxs-lookup"><span data-stu-id="4e406-172"><span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**Hand Held** (11)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-173">Disponible.</span><span class="sxs-lookup"><span data-stu-id="4e406-173">Hand-held.</span></span>

</dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span data-ttu-id="4e406-174"><span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**Estación de acoplamiento** (12)</span><span class="sxs-lookup"><span data-stu-id="4e406-174"><span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**Docking Station** (12)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-175">Estación de acoplamiento.</span><span class="sxs-lookup"><span data-stu-id="4e406-175">Docking station.</span></span>

</dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span data-ttu-id="4e406-176"><span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**Todo en uno** (13)</span><span class="sxs-lookup"><span data-stu-id="4e406-176"><span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**All in One** (13)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-177">Todo en uno.</span><span class="sxs-lookup"><span data-stu-id="4e406-177">All-in-one.</span></span>

</dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span data-ttu-id="4e406-178"><span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**Sub Notebook** (14)</span><span class="sxs-lookup"><span data-stu-id="4e406-178"><span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**Sub Notebook** (14)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-179">Subcuaderno.</span><span class="sxs-lookup"><span data-stu-id="4e406-179">Subnotebook.</span></span>

</dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span data-ttu-id="4e406-180"><span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**Ahorrar espacio** (15)</span><span class="sxs-lookup"><span data-stu-id="4e406-180"><span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**Space-Saving** (15)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-181">Ahorrar espacio.</span><span class="sxs-lookup"><span data-stu-id="4e406-181">Space-saving.</span></span>

</dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span data-ttu-id="4e406-182"><span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>**Caja del almuerzo** (16)</span><span class="sxs-lookup"><span data-stu-id="4e406-182"><span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>**Lunch Box** (16)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-183">Caja del almuerzo.</span><span class="sxs-lookup"><span data-stu-id="4e406-183">Lunch box.</span></span>

</dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span data-ttu-id="4e406-184"><span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**Chasis del sistema principal** (17)</span><span class="sxs-lookup"><span data-stu-id="4e406-184"><span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**Main System Chassis** (17)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-185">Chasis del sistema principal.</span><span class="sxs-lookup"><span data-stu-id="4e406-185">Main system chassis.</span></span>

</dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span data-ttu-id="4e406-186"><span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**Chasis de expansión** (18)</span><span class="sxs-lookup"><span data-stu-id="4e406-186"><span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**Expansion Chassis** (18)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-187">Chasis de expansión.</span><span class="sxs-lookup"><span data-stu-id="4e406-187">Expansion chassis.</span></span>

</dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span data-ttu-id="4e406-188"><span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>**Subchasis** (19)</span><span class="sxs-lookup"><span data-stu-id="4e406-188"><span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>**SubChassis** (19)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-189">Subchasis.</span><span class="sxs-lookup"><span data-stu-id="4e406-189">Subchassis.</span></span>

</dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span data-ttu-id="4e406-190"><span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**Chasis de expansión de bus** (20)</span><span class="sxs-lookup"><span data-stu-id="4e406-190"><span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**Bus Expansion Chassis** (20)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-191">Chasis de expansión de bus.</span><span class="sxs-lookup"><span data-stu-id="4e406-191">Bus-expansion chassis.</span></span>

</dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span data-ttu-id="4e406-192"><span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**Chasis de periféricos** (21)</span><span class="sxs-lookup"><span data-stu-id="4e406-192"><span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**Peripheral Chassis** (21)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-193">Chasis de periféricos.</span><span class="sxs-lookup"><span data-stu-id="4e406-193">Peripheral chassis.</span></span>

</dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span data-ttu-id="4e406-194"><span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**Chasis de almacenamiento** (22)</span><span class="sxs-lookup"><span data-stu-id="4e406-194"><span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**Storage Chassis** (22)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-195">Chasis de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="4e406-195">Storage chassis.</span></span>

</dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span data-ttu-id="4e406-196"><span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**Chasis de montaje en bastidor** (23)</span><span class="sxs-lookup"><span data-stu-id="4e406-196"><span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**Rack Mount Chassis** (23)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-197">Chasis montado en bastidor.</span><span class="sxs-lookup"><span data-stu-id="4e406-197">Rack-mount chassis.</span></span>

</dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span data-ttu-id="4e406-198"><span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**Equipos sellados** (24)</span><span class="sxs-lookup"><span data-stu-id="4e406-198"><span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**Sealed-Case PC** (24)</span></span>


</dt> <dd>

<span data-ttu-id="4e406-199">Equipo sellado.</span><span class="sxs-lookup"><span data-stu-id="4e406-199">Sealed-case computer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4e406-200">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4e406-200">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e406-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-203">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4e406-203">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4e406-204">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="4e406-204">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4e406-205">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="4e406-205">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4e406-206">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-206">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-207">**CurrentRequiredOrProduced**</span><span class="sxs-lookup"><span data-stu-id="4e406-207">**CurrentRequiredOrProduced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-208">Tipo de datos: **sint16**</span><span class="sxs-lookup"><span data-stu-id="4e406-208">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-210">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("amperios at 120 voltios")</span><span class="sxs-lookup"><span data-stu-id="4e406-210">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("amps at 120 volts")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-211">Lo requiere actualmente el chasis en 120 voltios.</span><span class="sxs-lookup"><span data-stu-id="4e406-211">Currently required by the chassis at 120 volts.</span></span> <span data-ttu-id="4e406-212">Si el chasis proporciona alimentación (como en el caso de un SAI), esta propiedad puede indicar el amperaje producido, como un número negativo.</span><span class="sxs-lookup"><span data-stu-id="4e406-212">If power is provided by the chassis (as in the case of a UPS), this property can indicate the amperage produced, as a negative number.</span></span>

</dd> <dt>

<span data-ttu-id="4e406-213">**Profundidad**</span><span class="sxs-lookup"><span data-stu-id="4e406-213">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-214">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="4e406-214">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-216">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="4e406-216">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-217">Profundidad del paquete físico, en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="4e406-217">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="4e406-218">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-218">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-219">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4e406-219">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-220">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e406-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-222">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="4e406-222">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-223">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="4e406-223">A textual description of the object.</span></span>

<span data-ttu-id="4e406-224">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-225">**HeatGeneration**</span><span class="sxs-lookup"><span data-stu-id="4e406-225">**HeatGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-226">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e406-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-227">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-228">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("BTU por hora")</span><span class="sxs-lookup"><span data-stu-id="4e406-228">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BTU per hour")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-229">Cantidad de calor generada por el chasis en BTU/hora.</span><span class="sxs-lookup"><span data-stu-id="4e406-229">Amount of heat generated by the chassis in Btu/hour.</span></span>

</dd> <dt>

<span data-ttu-id="4e406-230">**Height**</span><span class="sxs-lookup"><span data-stu-id="4e406-230">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-231">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="4e406-231">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-233">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="4e406-233">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-234">Alto del paquete físico, en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="4e406-234">Height of the physical package, in inches.</span></span>

<span data-ttu-id="4e406-235">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-235">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-236">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="4e406-236">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-237">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4e406-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e406-239">Si **es true**, el paquete puede intercambiarse en caliente.</span><span class="sxs-lookup"><span data-stu-id="4e406-239">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="4e406-240">Un paquete físico puede intercambiarse en caliente si el elemento se puede reemplazar por uno físicamente diferente (pero equivalente) mientras se activa el paquete contenedor.</span><span class="sxs-lookup"><span data-stu-id="4e406-240">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="4e406-241">Por ejemplo, un componente de ventilador se puede diseñar para que se intercambie en caliente.</span><span class="sxs-lookup"><span data-stu-id="4e406-241">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="4e406-242">Todos los componentes que se pueden intercambiar en caliente son intrínsecamente extraíbles y reemplazables.</span><span class="sxs-lookup"><span data-stu-id="4e406-242">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="4e406-243">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-243">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-244">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4e406-244">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-245">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4e406-245">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-246">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-247">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="4e406-247">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-248">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="4e406-248">Indicates when the object was installed.</span></span> <span data-ttu-id="4e406-249">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="4e406-249">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="4e406-250">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-250">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-251">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="4e406-251">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-252">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4e406-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e406-254">Si es **true**, el marco está protegido con un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="4e406-254">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="4e406-255">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-255">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-256">**Le**</span><span class="sxs-lookup"><span data-stu-id="4e406-256">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e406-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-259">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4e406-259">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4e406-260">Nombre de la organización responsable de producir el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="4e406-260">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="4e406-261">Para obtener más información, consulte la propiedad **Vendor** de [**CIM \_ Product**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-261">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="4e406-262">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-263">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="4e406-263">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e406-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-266">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="4e406-266">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4e406-267">Nombre por el que se suele conocer el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="4e406-267">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="4e406-268">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-268">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-269">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="4e406-269">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-270">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e406-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-271">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-272">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="4e406-272">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-273">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="4e406-273">Label by which the object is known.</span></span> <span data-ttu-id="4e406-274">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="4e406-274">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4e406-275">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-275">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-276">**NumberOfPowerCords**</span><span class="sxs-lookup"><span data-stu-id="4e406-276">**NumberOfPowerCords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-277">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e406-277">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e406-279">Número de cables de alimentación que deben estar conectados al chasis para que todos los componentes puedan funcionar.</span><span class="sxs-lookup"><span data-stu-id="4e406-279">Number of power cords that must be connected to the chassis so that all of the components can operate.</span></span>

</dd> <dt>

<span data-ttu-id="4e406-280">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="4e406-280">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-281">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e406-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e406-283">Datos adicionales, más allá de la información de etiquetas de recursos, que se pueden usar para identificar un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="4e406-283">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="4e406-284">Un ejemplo son los datos de código de barras que están asociados a un elemento, que también tiene una etiqueta de recurso.</span><span class="sxs-lookup"><span data-stu-id="4e406-284">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="4e406-285">Tenga en cuenta que si solo están disponibles los datos de código de barras y es único y se puede usar como una clave de elemento, esta propiedad sería NULL y los datos de código de barras se utilizarían como clave de clase en la propiedad de **etiqueta** .</span><span class="sxs-lookup"><span data-stu-id="4e406-285">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="4e406-286">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-286">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-287">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="4e406-287">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-288">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e406-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-290">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4e406-290">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4e406-291">Número de pieza asignado por la organización responsable de producir o fabricar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="4e406-291">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="4e406-292">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-292">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-293">**Poweredon**</span><span class="sxs-lookup"><span data-stu-id="4e406-293">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-294">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4e406-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e406-296">Si es **true**, el elemento físico está encendido.</span><span class="sxs-lookup"><span data-stu-id="4e406-296">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="4e406-297">De lo contrario, está actualmente desactivado.</span><span class="sxs-lookup"><span data-stu-id="4e406-297">Otherwise, it is currently off.</span></span>

<span data-ttu-id="4e406-298">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-298">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-299">**Quitar**</span><span class="sxs-lookup"><span data-stu-id="4e406-299">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-300">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4e406-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e406-302">Si es **true**, el paquete está diseñado para tomarse dentro y fuera del contenedor físico en el que se encuentra normalmente, sin perjudicar la función del empaquetado global.</span><span class="sxs-lookup"><span data-stu-id="4e406-302">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="4e406-303">Un paquete se considera extraíble incluso si la alimentación debe estar desactivada para realizar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="4e406-303">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="4e406-304">Si la potencia puede estar activada y se ha quitado el paquete, el elemento es extraíble y se puede intercambiar en caliente.</span><span class="sxs-lookup"><span data-stu-id="4e406-304">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="4e406-305">Por ejemplo, un chip de Procesador actualizable es extraíble.</span><span class="sxs-lookup"><span data-stu-id="4e406-305">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="4e406-306">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-306">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-307">**Reemplazables**</span><span class="sxs-lookup"><span data-stu-id="4e406-307">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-308">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4e406-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e406-310">Si es **true**, es posible reemplazar el elemento por uno físicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="4e406-310">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="4e406-311">Por ejemplo, algunos sistemas informáticos permiten que el chip del procesador principal se actualice a una clasificación de reloj más alta.</span><span class="sxs-lookup"><span data-stu-id="4e406-311">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="4e406-312">En este caso, se dice que el procesador es reemplazable.</span><span class="sxs-lookup"><span data-stu-id="4e406-312">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="4e406-313">Todos los componentes extraíbles se pueden reemplazar de forma inherente.</span><span class="sxs-lookup"><span data-stu-id="4e406-313">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="4e406-314">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-314">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-315">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="4e406-315">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-316">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e406-316">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-318">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Tabla global de contenedor físico DMTF \| 002,12 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="4e406-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-319">Indica si se intentó una infracción física del fotograma pero no se ha realizado correctamente, o si se ha intentado y se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="4e406-319">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span>

<span data-ttu-id="4e406-320">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-320">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4e406-321">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="4e406-321">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e406-322">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="4e406-322">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="4e406-323">**Sin brecha** (3)</span><span class="sxs-lookup"><span data-stu-id="4e406-323">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="4e406-324">**Intento de infracción** (4)</span><span class="sxs-lookup"><span data-stu-id="4e406-324">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="4e406-325">**Infracción correcta** (5)</span><span class="sxs-lookup"><span data-stu-id="4e406-325">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4e406-326">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="4e406-326">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-327">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e406-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-329">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="4e406-329">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4e406-330">Número asignado por el fabricante que se usa para identificar el elemento físico.</span><span class="sxs-lookup"><span data-stu-id="4e406-330">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="4e406-331">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-331">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-332">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4e406-332">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-333">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="4e406-333">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4e406-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-335">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span><span class="sxs-lookup"><span data-stu-id="4e406-335">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-336">Cadenas de forma libre que proporcionan explicaciones detalladas para las entradas de la matriz **ServicePhilosophy** .</span><span class="sxs-lookup"><span data-stu-id="4e406-336">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span>

> [!Note]  
> <span data-ttu-id="4e406-337">Cada entrada de esta matriz está relacionada con la entrada de la matriz de **ServicePhilosophy** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="4e406-337">Each entry of this array is related to the entry in **ServicePhilosophy** array that is located at the same index.</span></span>

 

<span data-ttu-id="4e406-338">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-338">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-339">**ServicePhilosophy**</span><span class="sxs-lookup"><span data-stu-id="4e406-339">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-340">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4e406-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4e406-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-342">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="4e406-342">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-343">Indica si el marco se va a atender desde la parte superior, delantera, posterior o lateral; y si tienen bandejas deslizantes o laterales extraíbles, y si el fotograma se va a mover (por ejemplo, con rodillos).</span><span class="sxs-lookup"><span data-stu-id="4e406-343">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<span data-ttu-id="4e406-344">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-344">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e406-345">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="4e406-345">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4e406-346">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="4e406-346">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="4e406-347">**Servicio desde arriba** (2)</span><span class="sxs-lookup"><span data-stu-id="4e406-347">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="4e406-348">**Servicio desde delante** (3)</span><span class="sxs-lookup"><span data-stu-id="4e406-348">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="4e406-349">**Servicio de atrás** (4)</span><span class="sxs-lookup"><span data-stu-id="4e406-349">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="4e406-350">**Servicio desde el lado** (5)</span><span class="sxs-lookup"><span data-stu-id="4e406-350">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="4e406-351">**Bandejas deslizantes** (6)</span><span class="sxs-lookup"><span data-stu-id="4e406-351">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="4e406-352">**Lados extraíbles** (7)</span><span class="sxs-lookup"><span data-stu-id="4e406-352">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="4e406-353">**Móvil** (8)</span><span class="sxs-lookup"><span data-stu-id="4e406-353">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4e406-354">**SKU**</span><span class="sxs-lookup"><span data-stu-id="4e406-354">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-355">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e406-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-357">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="4e406-357">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4e406-358">Número de unidad de almacén para este elemento físico.</span><span class="sxs-lookup"><span data-stu-id="4e406-358">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="4e406-359">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-359">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-360">**Estado**</span><span class="sxs-lookup"><span data-stu-id="4e406-360">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-361">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e406-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-363">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="4e406-363">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-364">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="4e406-364">String that indicates the current status of the object.</span></span> <span data-ttu-id="4e406-365">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="4e406-365">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="4e406-366">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="4e406-366">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="4e406-367">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="4e406-367">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="4e406-368">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="4e406-368">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4e406-369">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="4e406-369">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4e406-370">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="4e406-370">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4e406-371">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-371">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4e406-372">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="4e406-372">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4e406-373">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="4e406-373">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4e406-374">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="4e406-374">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4e406-375">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="4e406-375">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e406-376">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="4e406-376">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4e406-377">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="4e406-377">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4e406-378">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="4e406-378">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4e406-379">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="4e406-379">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4e406-380">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="4e406-380">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4e406-381">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="4e406-381">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4e406-382">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="4e406-382">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4e406-383">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="4e406-383">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4e406-384">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="4e406-384">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4e406-385">**Tag**</span><span class="sxs-lookup"><span data-stu-id="4e406-385">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-386">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e406-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-388">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4e406-388">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4e406-389">Identifica de forma única el elemento físico y actúa como la clave del elemento.</span><span class="sxs-lookup"><span data-stu-id="4e406-389">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="4e406-390">Esta propiedad puede contener información, como la etiqueta de activo o los datos de número de serie.</span><span class="sxs-lookup"><span data-stu-id="4e406-390">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="4e406-391">La clave de [**\_ PhysicalElement de CIM**](cim-physicalelement.md) se coloca muy alta en la jerarquía de objetos para identificar de forma independiente el hardware o la entidad, independientemente de la ubicación física en (o en) archivadores, adaptadores, etc.</span><span class="sxs-lookup"><span data-stu-id="4e406-391">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="4e406-392">Por ejemplo, un componente extraíble que puede intercambiarse en caliente puede tomarse de su paquete contenedor (ámbito) y estar temporalmente sin usar.</span><span class="sxs-lookup"><span data-stu-id="4e406-392">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="4e406-393">El objeto sigue existiendo y se puede insertar incluso en otro contenedor de ámbito.</span><span class="sxs-lookup"><span data-stu-id="4e406-393">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="4e406-394">La clave de un elemento físico es una cadena arbitraria que se define independientemente de la ubicación o la jerarquía orientada a ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="4e406-394">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="4e406-395">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-395">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-396">**TypeDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4e406-396">**TypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-397">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="4e406-397">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4e406-398">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-399">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ chasis CIM**.**ChassisTypes**")</span><span class="sxs-lookup"><span data-stu-id="4e406-399">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Chassis**.**ChassisTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-400">Matriz de cadenas de formato libre que proporciona información sobre las entradas de la matriz **ChassisTypes** .</span><span class="sxs-lookup"><span data-stu-id="4e406-400">Array of free-form strings that provides information about the **ChassisTypes** array entries.</span></span>

> [!Note]  
> <span data-ttu-id="4e406-401">Cada entrada de la matriz está relacionada con la entrada de la propiedad **ChassisTypes** , que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="4e406-401">Each array entry is related to the entry in the **ChassisTypes** property, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="4e406-402">**Versión**</span><span class="sxs-lookup"><span data-stu-id="4e406-402">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-403">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4e406-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-405">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="4e406-405">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4e406-406">Indica la versión del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="4e406-406">Indicates the version of the physical element.</span></span>

<span data-ttu-id="4e406-407">Esta propiedad se hereda de [**\_ PhysicalElement CIM**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-407">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-408">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="4e406-408">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-409">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4e406-409">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e406-411">Si **es true**, el equipo incluye una alarma visible.</span><span class="sxs-lookup"><span data-stu-id="4e406-411">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="4e406-412">Esta propiedad se hereda de [**\_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-412">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-413">**Peso**</span><span class="sxs-lookup"><span data-stu-id="4e406-413">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-414">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="4e406-414">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-415">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-416">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("libras")</span><span class="sxs-lookup"><span data-stu-id="4e406-416">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-417">Peso del paquete físico, en libras.</span><span class="sxs-lookup"><span data-stu-id="4e406-417">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="4e406-418">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-418">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e406-419">**Width**</span><span class="sxs-lookup"><span data-stu-id="4e406-419">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e406-420">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="4e406-420">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="4e406-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e406-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e406-422">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="4e406-422">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="4e406-423">Ancho del paquete físico, en pulgadas.</span><span class="sxs-lookup"><span data-stu-id="4e406-423">Width of the physical package, in inches.</span></span>

<span data-ttu-id="4e406-424">Esta propiedad se hereda de [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-424">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e406-425">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e406-425">Remarks</span></span>

<span data-ttu-id="4e406-426">La clase del **\_ chasis CIM** se deriva [**de \_ PhysicalFrame CIM**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-426">The **CIM\_Chassis** class is derived from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<span data-ttu-id="4e406-427">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="4e406-427">WMI does not implement this class.</span></span> <span data-ttu-id="4e406-428">Para obtener más información sobre las clases derivadas del **\_ chasis CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4e406-428">For more information about classes derived from **CIM\_Chassis**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4e406-429">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="4e406-429">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4e406-430">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="4e406-430">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e406-431">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e406-431">Requirements</span></span>



| <span data-ttu-id="4e406-432">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e406-432">Requirement</span></span> | <span data-ttu-id="4e406-433">Value</span><span class="sxs-lookup"><span data-stu-id="4e406-433">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e406-434">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e406-434">Minimum supported client</span></span><br/> | <span data-ttu-id="4e406-435">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e406-435">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e406-436">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e406-436">Minimum supported server</span></span><br/> | <span data-ttu-id="4e406-437">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e406-437">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e406-438">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4e406-438">Namespace</span></span><br/>                | <span data-ttu-id="4e406-439">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4e406-439">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e406-440">MOF</span><span class="sxs-lookup"><span data-stu-id="4e406-440">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e406-441"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e406-441"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e406-442">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e406-442">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e406-443"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e406-443"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e406-444">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e406-444">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e406-445">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="4e406-445">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 

