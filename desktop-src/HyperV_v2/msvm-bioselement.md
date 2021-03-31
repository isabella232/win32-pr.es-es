---
description: Representa el software de bajo nivel que se carga en la RAM para configurar e iniciar el sistema.
ms.assetid: D123601A-DEE6-43EA-BD95-1F7F0F2C2B43
title: Msvm_BIOSElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BIOSElement
- Msvm_BIOSElement.InstanceID
- Msvm_BIOSElement.Caption
- Msvm_BIOSElement.Description
- Msvm_BIOSElement.ElementName
- Msvm_BIOSElement.InstallDate
- Msvm_BIOSElement.OperationalStatus
- Msvm_BIOSElement.StatusDescriptions
- Msvm_BIOSElement.Status
- Msvm_BIOSElement.HealthState
- Msvm_BIOSElement.CommunicationStatus
- Msvm_BIOSElement.DetailedStatus
- Msvm_BIOSElement.OperatingStatus
- Msvm_BIOSElement.PrimaryStatus
- Msvm_BIOSElement.Name
- Msvm_BIOSElement.SoftwareElementState
- Msvm_BIOSElement.SoftwareElementID
- Msvm_BIOSElement.TargetOperatingSystem
- Msvm_BIOSElement.OtherTargetOS
- Msvm_BIOSElement.BuildNumber
- Msvm_BIOSElement.SerialNumber
- Msvm_BIOSElement.CodeSet
- Msvm_BIOSElement.IdentificationCode
- Msvm_BIOSElement.LanguageEdition
- Msvm_BIOSElement.Version
- Msvm_BIOSElement.Manufacturer
- Msvm_BIOSElement.PrimaryBIOS
- Msvm_BIOSElement.ListOfLanguages
- Msvm_BIOSElement.CurrentLanguage
- Msvm_BIOSElement.LoadedStartingAddress
- Msvm_BIOSElement.LoadedEndingAddress
- Msvm_BIOSElement.LoadUtilityInformation
- Msvm_BIOSElement.ReleaseDate
- Msvm_BIOSElement.RegistryURIs
- Msvm_BIOSElement.BIOSGUID
- Msvm_BIOSElement.BIOSSerialNumber
- Msvm_BIOSElement.BaseBoardSerialNumber
- Msvm_BIOSElement.ChassisSerialNumber
- Msvm_BIOSElement.ChassisAssetTag
- Msvm_BIOSElement.BIOSNumLock
- Msvm_BIOSElement.BootOrder
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8d36ea50791bf6f1413815583fe1168f564d50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908223"
---
# <a name="msvm_bioselement-class"></a><span data-ttu-id="4112e-103">MSVM \_ BIOSElement (clase)</span><span class="sxs-lookup"><span data-stu-id="4112e-103">Msvm\_BIOSElement class</span></span>

<span data-ttu-id="4112e-104">Representa el software de bajo nivel que se carga en la RAM para configurar e iniciar el sistema.</span><span class="sxs-lookup"><span data-stu-id="4112e-104">Represents the low-level software that is loaded into RAM to configure and start the system.</span></span> <span data-ttu-id="4112e-105">El BIOS no es un dispositivo lógico, por lo tanto, el BIOS virtual no debe considerarse como un dispositivo de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4112e-105">The BIOS is not a logical device, hence the virtual BIOS should not be thought of as a virtual machine device.</span></span> <span data-ttu-id="4112e-106">Dado que no es un dispositivo, no tiene un grupo de recursos de equipo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4112e-106">As it is not a device, it does not have a corresponding resource pool.</span></span> <span data-ttu-id="4112e-107">El objeto BIOS está asociado a la máquina virtual a través de la Asociación [**MSVM \_ SystemBIOS**](msvm-systembios.md) .</span><span class="sxs-lookup"><span data-stu-id="4112e-107">The BIOS object is associated with the virtual machine through the [**Msvm\_SystemBIOS**](msvm-systembios.md) association.</span></span>

<span data-ttu-id="4112e-108">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4112e-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4112e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4112e-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BIOSElement : CIM_BIOSElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   Name = "BIOS";
  uint16   SoftwareElementState = 2;
  string   SoftwareElementID = "Microsoft:GUID\device-specific data";
  uint16   TargetOperatingSystem = 0;
  string   OtherTargetOS;
  string   BuildNumber = 14;
  string   SerialNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   Version = "8.02.00";
  string   Manufacturer = "Microsoft Corporation";
  boolean  PrimaryBIOS = True;
  string   ListOfLanguages[] = "en|US|iso8859-1";
  string   CurrentLanguage = "en|US|iso8859-1";
  unit64   LoadedStartingAddress = 0xE0000;
  unit64   LoadedEndingAddress = 0xFFFFF;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
};
```

## <a name="members"></a><span data-ttu-id="4112e-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="4112e-110">Members</span></span>

<span data-ttu-id="4112e-111">La clase **MSVM \_ BIOSElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4112e-111">The **Msvm\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="4112e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4112e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4112e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4112e-113">Properties</span></span>

<span data-ttu-id="4112e-114">La clase **MSVM \_ BIOSElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4112e-114">The **Msvm\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4112e-115">**BaseBoardSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="4112e-115">**BaseBoardSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-118">Número de serie del panel base de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4112e-118">The serial number for the base board on the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-119">**BIOSGUID**</span><span class="sxs-lookup"><span data-stu-id="4112e-119">**BIOSGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-122">Identificador único del BIOS.</span><span class="sxs-lookup"><span data-stu-id="4112e-122">The unique identifier for the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-123">**BIOSNumLock**</span><span class="sxs-lookup"><span data-stu-id="4112e-123">**BIOSNumLock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-124">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4112e-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-126">El estado habilitado del Bloq Num en el BIOS.</span><span class="sxs-lookup"><span data-stu-id="4112e-126">The enabled state of the Num Lock in the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-127">**BIOSSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="4112e-127">**BIOSSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-130">Número de serie del BIOS.</span><span class="sxs-lookup"><span data-stu-id="4112e-130">The serial number for the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-131">**BootOrder**</span><span class="sxs-lookup"><span data-stu-id="4112e-131">**BootOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-132">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4112e-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4112e-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4112e-134">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span><span class="sxs-lookup"><span data-stu-id="4112e-134">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span></span>
</dt> </dl>

<span data-ttu-id="4112e-135">El orden en el que se buscará en los dispositivos un sector de arranque en el inicio.</span><span class="sxs-lookup"><span data-stu-id="4112e-135">The order in which devices will be searched for a boot sector at startup.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-136">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="4112e-136">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4112e-139">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="4112e-139">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="4112e-140">Identificador interno de esta compilación de elemento de software.</span><span class="sxs-lookup"><span data-stu-id="4112e-140">The internal identifier for this compilation of software element.</span></span> <span data-ttu-id="4112e-141">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre está establecida en 14.</span><span class="sxs-lookup"><span data-stu-id="4112e-141">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 14.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-142">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4112e-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4112e-145">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="4112e-145">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="4112e-146">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="4112e-146">A short description of the object.</span></span> <span data-ttu-id="4112e-147">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4112e-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4112e-148">**ChassisAssetTag**</span><span class="sxs-lookup"><span data-stu-id="4112e-148">**ChassisAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-151">El BIOS lo rellena automáticamente cuando se crea la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4112e-151">Automatically populated by the BIOS when the virtual machine is created.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-152">**ChassisSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="4112e-152">**ChassisSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-155">El BIOS lo rellena automáticamente cuando se crea la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4112e-155">Automatically populated by the BIOS when the virtual machine is created.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-156">**Dese**</span><span class="sxs-lookup"><span data-stu-id="4112e-156">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4112e-159">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="4112e-159">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="4112e-160">Conjunto de código utilizado por el elemento de software.</span><span class="sxs-lookup"><span data-stu-id="4112e-160">The code set used by the software element.</span></span> <span data-ttu-id="4112e-161">Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="4112e-161">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="4112e-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-163">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4112e-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-165">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="4112e-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="4112e-166">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="4112e-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4112e-167">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4112e-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4112e-168">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="4112e-168">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-171">Idioma seleccionado actualmente para el BIOS.</span><span class="sxs-lookup"><span data-stu-id="4112e-171">The currently selected language for the BIOS.</span></span> <span data-ttu-id="4112e-172">Esta propiedad se hereda de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre se establece en "en \| US \| ISO8859-1".</span><span class="sxs-lookup"><span data-stu-id="4112e-172">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "en\|US\|iso8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="4112e-173">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4112e-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-176">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="4112e-176">A description of the object.</span></span> <span data-ttu-id="4112e-177">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4112e-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4112e-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="4112e-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-179">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4112e-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-181">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="4112e-181">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="4112e-182">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="4112e-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4112e-183">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4112e-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4112e-184">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4112e-184">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-187">Nombre para mostrar del elemento.</span><span class="sxs-lookup"><span data-stu-id="4112e-187">A display name for the element.</span></span> <span data-ttu-id="4112e-188">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4112e-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4112e-189">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="4112e-189">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-190">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4112e-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-192">Especifica el estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="4112e-192">Specifies the current health of the element.</span></span> <span data-ttu-id="4112e-193">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="4112e-193">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="4112e-194">Cuando se produzca un error crítico, compruebe el registro de eventos para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4112e-194">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="4112e-195">La propiedad **EnabledState** también puede contener más información.</span><span class="sxs-lookup"><span data-stu-id="4112e-195">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="4112e-196">Por ejemplo, si el espacio en disco es muy bajo, **HealthState** se establece en 25, la máquina virtual se pausa y **EnabledState** se establece en 32768 (en pausa).</span><span class="sxs-lookup"><span data-stu-id="4112e-196">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="4112e-197">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4112e-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="4112e-198">Value</span><span class="sxs-lookup"><span data-stu-id="4112e-198">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="4112e-199">Significado</span><span class="sxs-lookup"><span data-stu-id="4112e-199">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="4112e-200"><dt>**Aceptar**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-200"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="4112e-201">La máquina virtual es totalmente funcional y funciona en parámetros operativos normales y sin errores.</span><span class="sxs-lookup"><span data-stu-id="4112e-201">The virtual machine is fully functional and is operating within normal operational parameters and without error.</span></span><br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="4112e-202"><dt>**Error principal**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-202"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="4112e-203">Se produjo un error importante en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4112e-203">The virtual machine has suffered a major failure.</span></span> <span data-ttu-id="4112e-204">Este valor se usa cuando uno o varios discos que contienen los VHD de la máquina virtual tienen poco espacio en disco y la máquina virtual se ha puesto en pausa.</span><span class="sxs-lookup"><span data-stu-id="4112e-204">This value is used when one or more disks that contain the virtual machine's VHDs is low on disk space and the virtual machine has been paused.</span></span><br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="4112e-205"><dt>**Error crítico**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-205"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="4112e-206">El elemento no es funcional y es posible que la recuperación no sea posible.</span><span class="sxs-lookup"><span data-stu-id="4112e-206">The element is nonfunctional, and recovery might not be possible.</span></span> <span data-ttu-id="4112e-207">Esto puede indicar que el proceso de trabajo de la máquina virtual (Vmwp.exe) no responde a las solicitudes de control o información, o que uno o varios discos que contienen los discos duros virtuales de la máquina virtual tienen poco espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="4112e-207">This can indicate that the worker process for the virtual machine (Vmwp.exe) is not responding to control or information requests, or that one or more disks that contain the VHDs for the virtual machine are low on disk space.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4112e-208">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="4112e-208">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-209">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4112e-211">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="4112e-211">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="4112e-212">Identificador del fabricante para este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="4112e-212">The manufacturer's identifier for this software element.</span></span> <span data-ttu-id="4112e-213">A menudo, se trata de una referencia de almacén (SKU) o un número de pieza.</span><span class="sxs-lookup"><span data-stu-id="4112e-213">Often this will be a stock keeping unit (SKU) or a part number.</span></span> <span data-ttu-id="4112e-214">Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="4112e-214">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4112e-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-216">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4112e-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-218">El BIOS lo rellena automáticamente cuando se crea la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4112e-218">Automatically populated by the BIOS when the virtual machine is created.</span></span> <span data-ttu-id="4112e-219">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4112e-219">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4112e-220">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4112e-220">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-221">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4112e-223">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="4112e-223">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4112e-224">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="4112e-224">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4112e-225">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4112e-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4112e-226">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="4112e-226">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4112e-229">Calificadores: **MaxLen** (32)</span><span class="sxs-lookup"><span data-stu-id="4112e-229">Qualifiers: **MaxLen** (32)</span></span>
</dt> </dl>

<span data-ttu-id="4112e-230">Edición de idioma de este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="4112e-230">The language edition of this software element.</span></span> <span data-ttu-id="4112e-231">Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="4112e-231">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-232">**ListOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="4112e-232">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-233">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="4112e-233">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4112e-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-235">Una lista de idiomas instalables para el BIOS.</span><span class="sxs-lookup"><span data-stu-id="4112e-235">A list of installable languages for the BIOS.</span></span> <span data-ttu-id="4112e-236">Esta propiedad se hereda de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre se establece en "en \| US \| ISO8859-1".</span><span class="sxs-lookup"><span data-stu-id="4112e-236">THIS property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "en\|US\|iso8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="4112e-237">**LoadedEndingAddress**</span><span class="sxs-lookup"><span data-stu-id="4112e-237">**LoadedEndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-238">Tipo de datos: **unit64**</span><span class="sxs-lookup"><span data-stu-id="4112e-238">Data type: **unit64**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-240">Dirección final de la memoria que ocupa este BIOS.</span><span class="sxs-lookup"><span data-stu-id="4112e-240">The ending address of the memory which this BIOS occupies.</span></span> <span data-ttu-id="4112e-241">Esta propiedad se hereda de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre está establecida en 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="4112e-241">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to 0xFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-242">**LoadedStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="4112e-242">**LoadedStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-243">Tipo de datos: **unit64**</span><span class="sxs-lookup"><span data-stu-id="4112e-243">Data type: **unit64**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-245">Dirección inicial de la memoria que ocupa este BIOS.</span><span class="sxs-lookup"><span data-stu-id="4112e-245">The starting address of the memory which this BIOS occupies.</span></span> <span data-ttu-id="4112e-246">Esta propiedad se hereda de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre está establecida en 0xE0000.</span><span class="sxs-lookup"><span data-stu-id="4112e-246">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to 0xE0000.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-247">**LoadUtilityInformation**</span><span class="sxs-lookup"><span data-stu-id="4112e-247">**LoadUtilityInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-248">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-250">Cadena que describe la utilidad Flash/Load de BIOS necesaria para actualizar el elemento BIOS.</span><span class="sxs-lookup"><span data-stu-id="4112e-250">A string that describes the BIOS flash/load utility that is required to update the BIOS element.</span></span> <span data-ttu-id="4112e-251">En esta propiedad se puede indicar la versión y otra información.</span><span class="sxs-lookup"><span data-stu-id="4112e-251">Version and other information may be indicated in this property.</span></span> <span data-ttu-id="4112e-252">Esta propiedad se hereda de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="4112e-252">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-253">**Le**</span><span class="sxs-lookup"><span data-stu-id="4112e-253">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-254">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-255">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4112e-256">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="4112e-256">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4112e-257">Fabricante de este BIOS.</span><span class="sxs-lookup"><span data-stu-id="4112e-257">The manufacturer of this BIOS.</span></span> <span data-ttu-id="4112e-258">Esta propiedad se hereda de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre está establecida en "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="4112e-258">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "Microsoft Corporation".</span></span>

</dd> <dt>

<span data-ttu-id="4112e-259">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="4112e-259">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-260">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-261">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4112e-262">Calificadores: **MaxLen** (1024)</span><span class="sxs-lookup"><span data-stu-id="4112e-262">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="4112e-263">Nombre usado para identificar este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="4112e-263">The name used to identify this software element.</span></span> <span data-ttu-id="4112e-264">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="4112e-264">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="4112e-265">Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre se establece en "BIOS".</span><span class="sxs-lookup"><span data-stu-id="4112e-265">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to "BIOS".</span></span>

</dd> <dt>

<span data-ttu-id="4112e-266">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="4112e-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-267">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4112e-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-269">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="4112e-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="4112e-270">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="4112e-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4112e-271">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4112e-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4112e-272">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="4112e-272">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-273">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4112e-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4112e-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-275">Una matriz que contiene los Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="4112e-275">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="4112e-276">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4112e-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="4112e-277">El valor en el índice cero (0) es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4112e-277">The value at index zero (0) is one of the following values.</span></span>



| <span data-ttu-id="4112e-278">Value</span><span class="sxs-lookup"><span data-stu-id="4112e-278">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="4112e-279">Significado</span><span class="sxs-lookup"><span data-stu-id="4112e-279">Meaning</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="4112e-280"><dt>**Aceptar**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-280"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                      | <span data-ttu-id="4112e-281">La máquina virtual es funcional y funciona con normalidad.</span><span class="sxs-lookup"><span data-stu-id="4112e-281">The virtual machine is functional and operating normally.</span></span><br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="4112e-282"><dt>**Degradado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-282"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                         | <span data-ttu-id="4112e-283">La máquina virtual solo es parcialmente funcional.</span><span class="sxs-lookup"><span data-stu-id="4112e-283">The virtual machine is only partially functional.</span></span> <span data-ttu-id="4112e-284">Esto indica que no se puede tener acceso al almacenamiento que contiene la configuración.</span><span class="sxs-lookup"><span data-stu-id="4112e-284">This indicates that the storage that contains the configuration is not accessible.</span></span> <span data-ttu-id="4112e-285">Una máquina virtual en este estado solo se puede desactivar o eliminar.</span><span class="sxs-lookup"><span data-stu-id="4112e-285">A virtual machine in this state may only be turned off or deleted.</span></span> <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <span data-ttu-id="4112e-286"><dt>**Error predictivo**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-286"><dt>**Predictive Failure**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="4112e-287">La máquina virtual es funcional, pero puede producir un error en el futuro.</span><span class="sxs-lookup"><span data-stu-id="4112e-287">The virtual machine is functional but may fail in the future.</span></span> <span data-ttu-id="4112e-288">Esto indica que el almacenamiento que contiene el disco duro virtual de la máquina virtual tiene poco espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="4112e-288">This indicates that the storage that contains the virtual machine's virtual hard disk is low on free space.</span></span> <span data-ttu-id="4112e-289">La máquina virtual se pausará si no hay más espacio disponible en disco.</span><span class="sxs-lookup"><span data-stu-id="4112e-289">The virtual machine will be paused if more disk space is not made available.</span></span><br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <span data-ttu-id="4112e-290"><dt>**Detenido**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-290"><dt>**Stopped**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="4112e-291">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="4112e-291">This value is not supported.</span></span> <span data-ttu-id="4112e-292">Si se detiene la máquina virtual, la propiedad **EnabledState** tendrá un valor de 3 (deshabilitado).</span><span class="sxs-lookup"><span data-stu-id="4112e-292">If the virtual machine is stopped, the **EnabledState** property will have a value of 3 (Disabled).</span></span><br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <span data-ttu-id="4112e-293"><dt>**En el servicio**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-293"><dt>**In Service**</dt> <dt>11</dt></span></span> </dl>                                | <span data-ttu-id="4112e-294">La máquina virtual está procesando una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4112e-294">The virtual machine is processing a request.</span></span><br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <span data-ttu-id="4112e-295"><dt>**Inactivo**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-295"><dt>**Dormant**</dt> <dt>15</dt></span></span> </dl>                                            | <span data-ttu-id="4112e-296">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="4112e-296">This value is not supported.</span></span> <span data-ttu-id="4112e-297">Si la máquina virtual está suspendida o en pausa, la propiedad **EnabledState** tendrá un valor de 32769 (suspendido) o 32768 (en pausa).</span><span class="sxs-lookup"><span data-stu-id="4112e-297">If the virtual machine is suspended or paused, the **EnabledState** property will have a value of 32769 (Suspended) or 32768 (Paused).</span></span><br/>                                                                                    |



 

<span data-ttu-id="4112e-298">El valor en el índice uno (1) es opcional y contiene información de estado secundaria.</span><span class="sxs-lookup"><span data-stu-id="4112e-298">The value at index one (1) is optional and contains secondary status information.</span></span> <span data-ttu-id="4112e-299">Un cliente debe usar el estado principal del índice cero (0) para determinar si se puede emitir una nueva solicitud a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4112e-299">A client should use the primary status from index zero (0) to determine whether a new request can be issued to the virtual machine.</span></span> <span data-ttu-id="4112e-300">Si **OperationalStatus** \[ 0 \] es 2 (OK),  \[ \] se puede interrumpir la operación indicada por OperationalStatus 1.</span><span class="sxs-lookup"><span data-stu-id="4112e-300">If **OperationalStatus**\[0\] is 2 (OK), then the operation indicated by **OperationalStatus**\[1\] can be interrupted.</span></span>

<span data-ttu-id="4112e-301">El valor de **OperationalStatus** \[ 1 \] es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4112e-301">The value at **OperationalStatus**\[1\] is one of the following values.</span></span>



| <span data-ttu-id="4112e-302">Value</span><span class="sxs-lookup"><span data-stu-id="4112e-302">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="4112e-303">Significado</span><span class="sxs-lookup"><span data-stu-id="4112e-303">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <span data-ttu-id="4112e-304"><dt>**Creando instantánea**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-304"><dt>**Creating Snapshot**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="4112e-305">Se está creando una instantánea en el proceso de creación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4112e-305">A snapshot is in the process of being created for the virtual machine.</span></span><br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <span data-ttu-id="4112e-306"><dt>**Aplicando la instantánea**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-306"><dt>**Applying Snapshot**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="4112e-307">Una instantánea está en proceso de aplicarse a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4112e-307">A snapshot is in the process of being applied to the virtual machine.</span></span><br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <span data-ttu-id="4112e-308"><dt>**Eliminando instantánea**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-308"><dt>**Deleting Snapshot**</dt> <dt>32770</dt></span></span> </dl>                                 | <span data-ttu-id="4112e-309">Se está eliminando una instantánea de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4112e-309">A snapshot is in the process of being deleted from the virtual machine.</span></span><br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <span data-ttu-id="4112e-310"><dt>**Esperando a iniciar**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-310"><dt>**Waiting to Start**</dt> <dt>32771</dt></span></span> </dl>                                     | <span data-ttu-id="4112e-311">La máquina virtual se iniciará después de que haya transcurrido el retraso de inicio automático.</span><span class="sxs-lookup"><span data-stu-id="4112e-311">The virtual machine will be started after the automatic startup delay has elapsed.</span></span><br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <span data-ttu-id="4112e-312"><dt>**Combinación de discos**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-312"><dt>**Merging Disks**</dt> <dt>32772</dt></span></span> </dl>                                                 | <span data-ttu-id="4112e-313">Se están combinando los discos duros virtuales de las instantáneas eliminadas previamente.</span><span class="sxs-lookup"><span data-stu-id="4112e-313">Virtual hard disks from previously deleted snapshots are being merged.</span></span><br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="4112e-314"><dt>**Exportando Máquina Virtual**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-314"><dt>**Exporting Virtual Machine**</dt> <dt>32773</dt></span></span> </dl> | <span data-ttu-id="4112e-315">La máquina virtual se está exportando.</span><span class="sxs-lookup"><span data-stu-id="4112e-315">The virtual machine is being exported.</span></span><br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="4112e-316"><dt>**Migrando la máquina Virtual**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-316"><dt>**Migrating Virtual Machine**</dt> <dt>32774</dt></span></span> </dl> | <span data-ttu-id="4112e-317">La máquina virtual se está migrando en directo desde un equipo físico a otro.</span><span class="sxs-lookup"><span data-stu-id="4112e-317">The virtual machine is being migrated live from one physical computer to another.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="4112e-318">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="4112e-318">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-319">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4112e-321">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="4112e-321">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="4112e-322">El fabricante y el sistema operativo de un elemento de software cuando la propiedad **TargetOperatingSystem** tiene un valor de 1 (otro), que requiere que la propiedad **OtherTargetOS** tenga un valor distinto de **null** .</span><span class="sxs-lookup"><span data-stu-id="4112e-322">The manufacturer and operating system for a software element when the **TargetOperatingSystem** property has a value of 1 (Other), which requires the **OtherTargetOS** property to have a non-**Null** value.</span></span> <span data-ttu-id="4112e-323">Para el resto de los valores de **TargetOperatingSystem**, la propiedad **OtherTargetOS** debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="4112e-323">For all other values of **TargetOperatingSystem**, the **OtherTargetOS** property must be **Null**.</span></span> <span data-ttu-id="4112e-324">Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="4112e-324">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-325">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="4112e-325">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-326">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4112e-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-328">Si es true, se trata del BIOS principal del equipo.</span><span class="sxs-lookup"><span data-stu-id="4112e-328">If True, this is the primary BIOS of the computer system.</span></span> <span data-ttu-id="4112e-329">Esta propiedad se hereda de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="4112e-329">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-330">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="4112e-330">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-331">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4112e-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-333">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="4112e-333">Provides high level status information.</span></span> <span data-ttu-id="4112e-334">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="4112e-334">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="4112e-335">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="4112e-335">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="4112e-336">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4112e-336">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4112e-337">**RegistryURIs**</span><span class="sxs-lookup"><span data-stu-id="4112e-337">**RegistryURIs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-338">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="4112e-338">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4112e-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-340">Matriz de cadenas que representa la ubicación de publicación del registro de atributos del BIOS o de los registros a los que se ajusta la implementación.</span><span class="sxs-lookup"><span data-stu-id="4112e-340">An array of strings representing the publication location of the BIOS attribute registry or registries the implementation complies to.</span></span> <span data-ttu-id="4112e-341">Esta propiedad se hereda de [**\_ BIOSElement CIM**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span><span class="sxs-lookup"><span data-stu-id="4112e-341">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span></span>

</dd> <dt>

<span data-ttu-id="4112e-342">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="4112e-342">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-343">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4112e-343">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-345">La fecha en la que se liberó el BIOS.</span><span class="sxs-lookup"><span data-stu-id="4112e-345">The date that the BIOS was released.</span></span> <span data-ttu-id="4112e-346">Esta propiedad se hereda de [**\_ BIOSElement CIM**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span><span class="sxs-lookup"><span data-stu-id="4112e-346">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span></span>

</dd> <dt>

<span data-ttu-id="4112e-347">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="4112e-347">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-348">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4112e-350">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="4112e-350">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="4112e-351">Número de serie asignado del BIOS.</span><span class="sxs-lookup"><span data-stu-id="4112e-351">The assigned serial number of the BIOS.</span></span> <span data-ttu-id="4112e-352">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](/windows/desktop/CIMWin32Prov/cim-softwareelement).</span><span class="sxs-lookup"><span data-stu-id="4112e-352">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement).</span></span>

</dd> <dt>

<span data-ttu-id="4112e-353">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="4112e-353">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-354">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4112e-356">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="4112e-356">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4112e-357">Identificador del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="4112e-357">An identifier for the software element.</span></span> <span data-ttu-id="4112e-358">Esta propiedad se hereda de [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre se establece en "Microsoft:*GUID* \\ *specific Device-specific Data*".</span><span class="sxs-lookup"><span data-stu-id="4112e-358">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="4112e-359">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="4112e-359">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-360">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4112e-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-362">El estado del ciclo de vida de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="4112e-362">The state of a software element's life cycle.</span></span> <span data-ttu-id="4112e-363">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre está establecida en 2 (ejecutable).</span><span class="sxs-lookup"><span data-stu-id="4112e-363">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 2 (Executable).</span></span>

</dd> <dt>

<span data-ttu-id="4112e-364">**Estado**</span><span class="sxs-lookup"><span data-stu-id="4112e-364">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-365">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-367">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="4112e-367">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4112e-368">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4112e-368">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-369">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="4112e-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4112e-370">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4112e-371">Calificadores: **ArrayType** ("indexado")</span><span class="sxs-lookup"><span data-stu-id="4112e-371">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="4112e-372">Una matriz que contiene cadenas que describen los valores correspondientes de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="4112e-372">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="4112e-373">Por ejemplo, si 11 (en servicio) es el valor asignado a **OperationalStatus** \[ 0 \] , **StatusDescriptions** \[ 0 \] puede incluir una explicación sobre el motivo por el que la máquina virtual está procesando una solicitud.</span><span class="sxs-lookup"><span data-stu-id="4112e-373">For example, if 11 (In Service) is the value assigned to **OperationalStatus**\[0\], then **StatusDescriptions**\[0\] may contain an explanation as to why the virtual machine is processing a request.</span></span> <span data-ttu-id="4112e-374">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="4112e-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="4112e-375">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="4112e-375">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-376">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4112e-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4112e-378">Entorno del sistema operativo del elemento.</span><span class="sxs-lookup"><span data-stu-id="4112e-378">The element's operating system environment.</span></span> <span data-ttu-id="4112e-379">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](/windows/desktop/CIMWin32Prov/cim-softwareelement)y siempre está establecida en 0 (desconocido).</span><span class="sxs-lookup"><span data-stu-id="4112e-379">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 0 (Unknown).</span></span>

</dd> <dt>

<span data-ttu-id="4112e-380">**Versión**</span><span class="sxs-lookup"><span data-stu-id="4112e-380">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4112e-381">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4112e-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4112e-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4112e-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4112e-383">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="4112e-383">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="4112e-384">Versión del BIOS.</span><span class="sxs-lookup"><span data-stu-id="4112e-384">The version of the BIOS.</span></span> <span data-ttu-id="4112e-385">Esta propiedad se hereda de [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)y siempre se establece en "8.02.00".</span><span class="sxs-lookup"><span data-stu-id="4112e-385">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "8.02.00".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4112e-386">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4112e-386">Remarks</span></span>

<span data-ttu-id="4112e-387">El acceso a la clase **MSVM \_ BIOSElement** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="4112e-387">Access to the **Msvm\_BIOSElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4112e-388">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4112e-388">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="4112e-389">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4112e-389">Requirements</span></span>



| <span data-ttu-id="4112e-390">Requisito</span><span class="sxs-lookup"><span data-stu-id="4112e-390">Requirement</span></span> | <span data-ttu-id="4112e-391">Value</span><span class="sxs-lookup"><span data-stu-id="4112e-391">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4112e-392">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4112e-392">Minimum supported client</span></span><br/> | <span data-ttu-id="4112e-393">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4112e-393">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4112e-394">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4112e-394">Minimum supported server</span></span><br/> | <span data-ttu-id="4112e-395">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4112e-395">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4112e-396">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4112e-396">Namespace</span></span><br/>                | <span data-ttu-id="4112e-397">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4112e-397">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4112e-398">MOF</span><span class="sxs-lookup"><span data-stu-id="4112e-398">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4112e-399"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-399"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4112e-400">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4112e-400">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4112e-401"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4112e-401"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4112e-402">Vea también</span><span class="sxs-lookup"><span data-stu-id="4112e-402">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4112e-403">**\_BIOSELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="4112e-403">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dt>

[<span data-ttu-id="4112e-404">Clases de BIOS</span><span class="sxs-lookup"><span data-stu-id="4112e-404">BIOS Classes</span></span>](bios-classes.md)
</dt> <dt>

[<span data-ttu-id="4112e-405">**\_BIOSELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="4112e-405">**CIM\_BIOSElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-bioselement)
</dt> </dl>

 

