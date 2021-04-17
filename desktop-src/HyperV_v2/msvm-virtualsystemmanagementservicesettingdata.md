---
description: Representa la configuración para el servicio de virtualización presente en un sistema host único.
ms.assetid: E3265AFE-0117-4F59-9A6B-34CEA7A61EDD
title: Msvm_VirtualSystemManagementServiceSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementServiceSettingData
- Msvm_VirtualSystemManagementServiceSettingData.InstanceID
- Msvm_VirtualSystemManagementServiceSettingData.Caption
- Msvm_VirtualSystemManagementServiceSettingData.Description
- Msvm_VirtualSystemManagementServiceSettingData.ElementName
- Msvm_VirtualSystemManagementServiceSettingData.BiosLockString
- Msvm_VirtualSystemManagementServiceSettingData.DefaultExternalDataRoot
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskPath
- Msvm_VirtualSystemManagementServiceSettingData.MaximumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumMacAddress
- Msvm_VirtualSystemManagementServiceSettingData.NumaSpanningEnabled
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerContact
- Msvm_VirtualSystemManagementServiceSettingData.PrimaryOwnerName
- Msvm_VirtualSystemManagementServiceSettingData.HbaLunTimeout
- Msvm_VirtualSystemManagementServiceSettingData.MaximumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.MinimumWWPNAddress
- Msvm_VirtualSystemManagementServiceSettingData.CurrentWWNNAddress
- Msvm_VirtualSystemManagementServiceSettingData.DefaultVirtualHardDiskCachingMode
- Msvm_VirtualSystemManagementServiceSettingData.HypervisorRootSchedulerEnabled
- Msvm_VirtualSystemManagementServiceSettingData.EnhancedSessionModeEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 782f196fdbd3a09126a7b4d14be6789bb633f043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686579"
---
# <a name="msvm_virtualsystemmanagementservicesettingdata-class"></a><span data-ttu-id="3ec99-103">MSVM \_ VirtualSystemManagementServiceSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="3ec99-103">Msvm\_VirtualSystemManagementServiceSettingData class</span></span>

<span data-ttu-id="3ec99-104">Representa la configuración para el servicio de virtualización presente en un sistema host único.</span><span class="sxs-lookup"><span data-stu-id="3ec99-104">Represents the settings for the virtualization service present on a single host system.</span></span> <span data-ttu-id="3ec99-105">Las propiedades de esta clase no se pueden modificar directamente.</span><span class="sxs-lookup"><span data-stu-id="3ec99-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="3ec99-106">El cliente debe llamar al método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para modificar cualquiera de estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3ec99-106">The client must call the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify any of these properties.</span></span>

<span data-ttu-id="3ec99-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3ec99-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ec99-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ec99-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementServiceSettingData : CIM_SettingData
{
  string  InstanceID = "Microsoft:host";
  string  Caption = "Hyper-V Virtual System Management Service";
  string  Description = "Settings for the Virtual System Management Service";
  string  ElementName = "Hyper-V Virtual System Management Service";
  string  BiosLockString;
  string  DefaultExternalDataRoot = "root\ProgramData\Microsoft\Windows\Virtualization";
  string  DefaultVirtualHardDiskPath = "root\Users\Public\Documents\Virtual Hard Disks";
  string  MaximumMacAddress;
  string  MinimumMacAddress;
  boolean NumaSpanningEnabled;
  string  PrimaryOwnerContact = "";
  string  PrimaryOwnerName = "Administrators";
  uint32  HbaLunTimeout;
  string  MaximumWWPNAddress;
  string  MinimumWWPNAddress;
  string  CurrentWWNNAddress;
  uint16  DefaultVirtualHardDiskCachingMode;
  boolean HypervisorRootSchedulerEnabled;
  boolean EnhancedSessionModeEnabled;
};
```

## <a name="members"></a><span data-ttu-id="3ec99-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="3ec99-109">Members</span></span>

<span data-ttu-id="3ec99-110">La clase **MSVM \_ VirtualSystemManagementServiceSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3ec99-110">The **Msvm\_VirtualSystemManagementServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3ec99-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ec99-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ec99-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ec99-112">Properties</span></span>

<span data-ttu-id="3ec99-113">La clase **MSVM \_ VirtualSystemManagementServiceSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3ec99-113">The **Msvm\_VirtualSystemManagementServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ec99-114">**BiosLockString**</span><span class="sxs-lookup"><span data-stu-id="3ec99-114">**BiosLockString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ec99-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-117">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)</span><span class="sxs-lookup"><span data-stu-id="3ec99-117">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32)</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-118">Lo usan los OEM para permitir que los sistemas operativos Windows bloqueados por BIOS se ejecuten en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3ec99-118">Used by OEMs to allow BIOS-locked Windows operating systems to run in the virtual machine.</span></span> <span data-ttu-id="3ec99-119">Esta cadena debe tener exactamente 32 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="3ec99-119">This string must be exactly 32 characters in length.</span></span>

<span data-ttu-id="3ec99-120">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec99-120">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3ec99-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3ec99-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ec99-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-124">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ec99-124">A short description of the object.</span></span> <span data-ttu-id="3ec99-125">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de administración del sistema virtual de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="3ec99-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="3ec99-126">**CurrentWWNNAddress**</span><span class="sxs-lookup"><span data-stu-id="3ec99-126">**CurrentWWNNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ec99-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-129">La dirección del nombre de nodo World Wide node Name (WWNN) para direcciones de World Wide Name generadas dinámicamente usadas para adaptadores de bus host sintéticos.</span><span class="sxs-lookup"><span data-stu-id="3ec99-129">The world wide node name (WWNN) address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="3ec99-130">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec99-130">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3ec99-131">**DefaultExternalDataRoot**</span><span class="sxs-lookup"><span data-stu-id="3ec99-131">**DefaultExternalDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ec99-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-134">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).**ConfigurationDataRoot**")</span><span class="sxs-lookup"><span data-stu-id="3ec99-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).**ConfigurationDataRoot**")</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-135">Raíz de datos externos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3ec99-135">The default external data root.</span></span> <span data-ttu-id="3ec99-136">De forma predeterminada, "*raíz* \\ ProgramData \\ Microsoft \\ Windows \\ Virtualization".</span><span class="sxs-lookup"><span data-stu-id="3ec99-136">By default, "*root*\\ProgramData\\Microsoft\\Windows\\Virtualization".</span></span>

<span data-ttu-id="3ec99-137">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec99-137">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3ec99-138">**DefaultVirtualHardDiskCachingMode**</span><span class="sxs-lookup"><span data-stu-id="3ec99-138">**DefaultVirtualHardDiskCachingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-139">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ec99-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-141">Indica si se debe usar el almacenamiento en caché de archivos en memoria de forma predeterminada para los discos.</span><span class="sxs-lookup"><span data-stu-id="3ec99-141">Indicates whether in-memory file caching should be used for disks by default.</span></span> <span data-ttu-id="3ec99-142">Este valor se puede invalidar en cada disco en el campo **CachingMode** de la clase StorageAllocationSettingData de [**MSVM \_**](msvm-storageallocationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec99-142">This value can be overridden on a per-disk basis in the **CachingMode** field of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="3ec99-143">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="3ec99-143">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3ec99-144">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3ec99-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

<span data-ttu-id="3ec99-145">**Sin almacenamiento en caché** (3)</span><span class="sxs-lookup"><span data-stu-id="3ec99-145">**No Caching** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

<span data-ttu-id="3ec99-146">**Elementos primarios que se pueda compartir en caché** (4)</span><span class="sxs-lookup"><span data-stu-id="3ec99-146">**Cache Sharable Parents** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3ec99-147">**DefaultVirtualHardDiskPath**</span><span class="sxs-lookup"><span data-stu-id="3ec99-147">**DefaultVirtualHardDiskPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ec99-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-150">La ruta de acceso del disco duro virtual predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3ec99-150">The default virtual hard disk path.</span></span> <span data-ttu-id="3ec99-151">De forma predeterminada, "*raíz* \\ usuarios \\ públicos \\ documentos \\ discos duros virtuales".</span><span class="sxs-lookup"><span data-stu-id="3ec99-151">By default, "*root*\\Users\\Public\\Documents\\Virtual Hard Disks".</span></span>

<span data-ttu-id="3ec99-152">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec99-152">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3ec99-153">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3ec99-153">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ec99-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-156">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ec99-156">A description of the object.</span></span> <span data-ttu-id="3ec99-157">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del servicio de administración del sistema virtual".</span><span class="sxs-lookup"><span data-stu-id="3ec99-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Settings for the Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="3ec99-158">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3ec99-158">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ec99-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-161">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ec99-161">A display name for the object.</span></span> <span data-ttu-id="3ec99-162">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de administración del sistema virtual de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="3ec99-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span> <span data-ttu-id="3ec99-163">Al cambiar esta propiedad, se cambiará la propiedad **ElementName** del derivado de [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) asociado.</span><span class="sxs-lookup"><span data-stu-id="3ec99-163">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

</dd> <dt>

<span data-ttu-id="3ec99-164">**EnhancedSessionModeEnabled**</span><span class="sxs-lookup"><span data-stu-id="3ec99-164">**EnhancedSessionModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-165">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3ec99-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-167">Indica si se permite el modo de sesión mejorada en el servidor.</span><span class="sxs-lookup"><span data-stu-id="3ec99-167">Indicates whether enhanced session mode is permitted on the server.</span></span> <span data-ttu-id="3ec99-168">**True** indica permitido; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="3ec99-168">**True** indicates permitted, otherwise **False**.</span></span>

<span data-ttu-id="3ec99-169">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="3ec99-169">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="3ec99-170">**HbaLunTimeout**</span><span class="sxs-lookup"><span data-stu-id="3ec99-170">**HbaLunTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-171">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ec99-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-173">Especifica la cantidad de tiempo que el dispositivo virtual sintético Canal de fibra esperará a que aparezca un número de unidad lógica (LUN) antes de iniciar una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3ec99-173">Specifies the amount of time that the synthetic Fibre Channel virtual device will wait for a logical unit number (LUN) to appear before starting a virtual machine.</span></span>

<span data-ttu-id="3ec99-174">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec99-174">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3ec99-175">**HypervisorRootSchedulerEnabled**</span><span class="sxs-lookup"><span data-stu-id="3ec99-175">**HypervisorRootSchedulerEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-176">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3ec99-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-178">Si el programador raíz del hipervisor está habilitado o no.</span><span class="sxs-lookup"><span data-stu-id="3ec99-178">Whether or not the hypervisor root scheduler is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="3ec99-179">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="3ec99-179">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="3ec99-180">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3ec99-180">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ec99-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-183">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="3ec99-183">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-184">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="3ec99-184">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3ec99-185">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85))y siempre se establece en "Microsoft:*host*", donde *host* es el nombre NetBIOS del sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="3ec99-185">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*host*", where *host* is the NetBIOS name of the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="3ec99-186">**MaximumMacAddress**</span><span class="sxs-lookup"><span data-stu-id="3ec99-186">**MaximumMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ec99-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-189">La dirección MAC máxima para direcciones MAC generadas dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="3ec99-189">The maximum MAC address for dynamically generated MAC addresses.</span></span>

<span data-ttu-id="3ec99-190">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec99-190">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3ec99-191">**MaximumWWPNAddress**</span><span class="sxs-lookup"><span data-stu-id="3ec99-191">**MaximumWWPNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ec99-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-194">La dirección de nombre de Puerto WWPN (WWPN) máxima para direcciones de World Wide Name generadas dinámicamente usadas para adaptadores de bus host sintéticos.</span><span class="sxs-lookup"><span data-stu-id="3ec99-194">The maximum world wide port name (WWPN) address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="3ec99-195">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec99-195">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3ec99-196">**MinimumMacAddress**</span><span class="sxs-lookup"><span data-stu-id="3ec99-196">**MinimumMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ec99-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-199">La dirección MAC mínima para direcciones MAC generadas dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="3ec99-199">The minimum MAC address for dynamically generated MAC addresses.</span></span>

<span data-ttu-id="3ec99-200">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec99-200">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3ec99-201">**MinimumWWPNAddress**</span><span class="sxs-lookup"><span data-stu-id="3ec99-201">**MinimumWWPNAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ec99-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-204">La dirección de nombre de Puerto WWPN mínima para direcciones de World Wide Name generadas dinámicamente que se usan para adaptadores de bus host sintéticos.</span><span class="sxs-lookup"><span data-stu-id="3ec99-204">The minimum world wide port name address for dynamically generated world wide name addresses used for synthetic host bus adapters.</span></span>

<span data-ttu-id="3ec99-205">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec99-205">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3ec99-206">**NumaSpanningEnabled**</span><span class="sxs-lookup"><span data-stu-id="3ec99-206">**NumaSpanningEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-207">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3ec99-207">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-209">Especifica si se puede asignar memoria desde nodos de acceso a memoria no uniforme (NUMA) remotos al iniciar una máquina virtual o al asignar memoria a una máquina virtual mediante la memoria dinámica.</span><span class="sxs-lookup"><span data-stu-id="3ec99-209">Specifies whether memory can be allocated from remote nonuniform memory access (NUMA) nodes when starting a virtual machine or when assigning memory to a virtual machine by dynamic memory.</span></span> <span data-ttu-id="3ec99-210">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3ec99-210">This can be one of the following values.</span></span>



| <span data-ttu-id="3ec99-211">Value</span><span class="sxs-lookup"><span data-stu-id="3ec99-211">Value</span></span>                                                                                | <span data-ttu-id="3ec99-212">Significado</span><span class="sxs-lookup"><span data-stu-id="3ec99-212">Meaning</span></span>                                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3ec99-213"><dt>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="3ec99-213"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="3ec99-214">La memoria se puede asignar desde los nodos NUMA locales y remotos.</span><span class="sxs-lookup"><span data-stu-id="3ec99-214">Memory can be allocated from both local and remote NUMA nodes.</span></span><br/>                   |
| <dl> <span data-ttu-id="3ec99-215"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="3ec99-215"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="3ec99-216">La memoria solo se puede asignar desde el nodo NUMA asignado a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3ec99-216">Memory can be allocated only from the NUMA node assigned to the virtual machine.</span></span><br/> |



 

<span data-ttu-id="3ec99-217">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec99-217">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3ec99-218">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="3ec99-218">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ec99-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-221">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información general de DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="3ec99-221">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-222">Describe cómo se puede alcanzar el propietario del sistema principal (por ejemplo, el número de teléfono o la dirección de correo electrónico).</span><span class="sxs-lookup"><span data-stu-id="3ec99-222">Describes how the primary system owner can be reached (for example, phone number or email address).</span></span> <span data-ttu-id="3ec99-223">De forma predeterminada, está vacío.</span><span class="sxs-lookup"><span data-stu-id="3ec99-223">By default, empty.</span></span> <span data-ttu-id="3ec99-224">Este nombre no puede superar los 256 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="3ec99-224">This name may not exceed 256 characters in length.</span></span>

<span data-ttu-id="3ec99-225">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec99-225">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3ec99-226">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="3ec99-226">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ec99-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ec99-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ec99-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ec99-229">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información general de DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="3ec99-229">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="3ec99-230">Nombre del propietario del sistema principal.</span><span class="sxs-lookup"><span data-stu-id="3ec99-230">The name of the primary system owner.</span></span> <span data-ttu-id="3ec99-231">De forma predeterminada, los "administradores".</span><span class="sxs-lookup"><span data-stu-id="3ec99-231">By default, "Administrators".</span></span> <span data-ttu-id="3ec99-232">Este valor no puede superar los 64 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="3ec99-232">This value may not exceed 64 characters in length.</span></span>

<span data-ttu-id="3ec99-233">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3ec99-233">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ec99-234">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ec99-234">Remarks</span></span>

<span data-ttu-id="3ec99-235">El acceso a la clase **MSVM \_ VirtualSystemManagementServiceSettingData** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="3ec99-235">Access to the **Msvm\_VirtualSystemManagementServiceSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3ec99-236">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3ec99-236">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ec99-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ec99-237">Requirements</span></span>



| <span data-ttu-id="3ec99-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ec99-238">Requirement</span></span> | <span data-ttu-id="3ec99-239">Value</span><span class="sxs-lookup"><span data-stu-id="3ec99-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec99-240">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ec99-240">Minimum supported client</span></span><br/> | <span data-ttu-id="3ec99-241">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ec99-241">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3ec99-242">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ec99-242">Minimum supported server</span></span><br/> | <span data-ttu-id="3ec99-243">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ec99-243">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3ec99-244">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3ec99-244">Namespace</span></span><br/>                | <span data-ttu-id="3ec99-245">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3ec99-245">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3ec99-246">MOF</span><span class="sxs-lookup"><span data-stu-id="3ec99-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ec99-247"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ec99-247"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ec99-248">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ec99-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ec99-249"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ec99-249"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3ec99-250">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ec99-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ec99-251">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="3ec99-251">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="3ec99-252">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="3ec99-252">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="3ec99-253">[**SettingData de CIM \_**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3ec99-253">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3ec99-254">Clases de administración de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="3ec99-254">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

