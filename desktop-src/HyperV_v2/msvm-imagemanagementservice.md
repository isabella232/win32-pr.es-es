---
description: Administra los medios virtuales (archivos. vhd,. vhdx,. ISO o. VFD) para una máquina virtual.
ms.assetid: 7caa720e-37cf-454e-8634-f2bd82bcf83d
title: Msvm_ImageManagementService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService
- Msvm_ImageManagementService.InstanceID
- Msvm_ImageManagementService.Caption
- Msvm_ImageManagementService.Description
- Msvm_ImageManagementService.ElementName
- Msvm_ImageManagementService.InstallDate
- Msvm_ImageManagementService.OperationalStatus
- Msvm_ImageManagementService.StatusDescriptions
- Msvm_ImageManagementService.Status
- Msvm_ImageManagementService.HealthState
- Msvm_ImageManagementService.CommunicationStatus
- Msvm_ImageManagementService.DetailedStatus
- Msvm_ImageManagementService.OperatingStatus
- Msvm_ImageManagementService.PrimaryStatus
- Msvm_ImageManagementService.EnabledState
- Msvm_ImageManagementService.OtherEnabledState
- Msvm_ImageManagementService.RequestedState
- Msvm_ImageManagementService.EnabledDefault
- Msvm_ImageManagementService.TimeOfLastStateChange
- Msvm_ImageManagementService.AvailableRequestedStates
- Msvm_ImageManagementService.TransitioningToState
- Msvm_ImageManagementService.SystemCreationClassName
- Msvm_ImageManagementService.SystemName
- Msvm_ImageManagementService.CreationClassName
- Msvm_ImageManagementService.Name
- Msvm_ImageManagementService.PrimaryOwnerName
- Msvm_ImageManagementService.PrimaryOwnerContact
- Msvm_ImageManagementService.StartMode
- Msvm_ImageManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36a45041ec41b8fbd87801a65fa2b28ac99da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810429"
---
# <a name="msvm_imagemanagementservice-class"></a><span data-ttu-id="39061-103">MSVM \_ ImageManagementService (clase)</span><span class="sxs-lookup"><span data-stu-id="39061-103">Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="39061-104">Administra los medios virtuales (archivos. vhd,. vhdx,. ISO o. VFD) para una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="39061-104">Manages the virtual media (.vhd, .vhdx, .iso, or .vfd files) for a virtual machine.</span></span>

<span data-ttu-id="39061-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="39061-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="39061-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39061-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ImageManagementService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Image Management Service";
  string   Description = "Provides Image Management servicing for Hyper-V";
  string   ElementName = "Hyper-V Image Management Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_ImageManagementService";
  string   Name = "vhdsvc";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="39061-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="39061-107">Members</span></span>

<span data-ttu-id="39061-108">La clase **MSVM \_ ImageManagementService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="39061-108">The **Msvm\_ImageManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="39061-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="39061-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="39061-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="39061-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="39061-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="39061-111">Methods</span></span>

<span data-ttu-id="39061-112">La clase **MSVM \_ ImageManagementService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="39061-112">The **Msvm\_ImageManagementService** class has these methods.</span></span>



| <span data-ttu-id="39061-113">Método</span><span class="sxs-lookup"><span data-stu-id="39061-113">Method</span></span>                                                                                                           | <span data-ttu-id="39061-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="39061-114">Description</span></span>                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39061-115">**AttachVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="39061-115">**AttachVirtualHardDisk**</span></span>](attachvirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="39061-116">Conecta un archivo de imagen de disco virtual en modo de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="39061-116">Attaches a virtual disk image file in loopback mode.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="39061-117">**CompactVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="39061-117">**CompactVirtualHardDisk**</span></span>](compactvirtualharddisk-msvm-imagemanagementservice.md)                             | <span data-ttu-id="39061-118">Compacta un archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="39061-118">Compacts a virtual hard disk file.</span></span><br/>                                                                                                                                                                                               |
| [<span data-ttu-id="39061-119">**ConvertVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="39061-119">**ConvertVirtualHardDisk**</span></span>](convertvirtualharddisk-msvm-imagemanagementservice.md)                             | <span data-ttu-id="39061-120">Convierte un disco duro virtual existente en un tipo o formato diferente.</span><span class="sxs-lookup"><span data-stu-id="39061-120">Converts an existing virtual hard disk to a different type or format.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="39061-121">**ConvertVirtualHardDiskToVHDSet**</span><span class="sxs-lookup"><span data-stu-id="39061-121">**ConvertVirtualHardDiskToVHDSet**</span></span>](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md)             | <span data-ttu-id="39061-122">Convierte un archivo de disco duro virtual mediante la creación de un nuevo archivo del conjunto de VHD junto con el disco duro virtual existente.</span><span class="sxs-lookup"><span data-stu-id="39061-122">Converts a virtual hard disk file by creating a new VHD Set file alongside the existing virtual hard disk.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="39061-123">**CreateVirtualFloppyDisk**</span><span class="sxs-lookup"><span data-stu-id="39061-123">**CreateVirtualFloppyDisk**</span></span>](createvirtualfloppydisk-msvm-imagemanagementservice.md)                           | <span data-ttu-id="39061-124">Crea un archivo de disquete virtual.</span><span class="sxs-lookup"><span data-stu-id="39061-124">Creates a virtual floppy disk file.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="39061-125">**CreateVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="39061-125">**CreateVirtualHardDisk**</span></span>](createvirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="39061-126">Crea un archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="39061-126">Creates a virtual hard disk file.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="39061-127">**DeleteVHDSnapshot**</span><span class="sxs-lookup"><span data-stu-id="39061-127">**DeleteVHDSnapshot**</span></span>](msvm-imagemanagementservice-deletevhdsnapshot.md)                                       | <span data-ttu-id="39061-128">Elimina una entrada de instantánea de VHD dentro de un archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="39061-128">Deletes a VHD Snapshot entry within a VHD Set file.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="39061-129">**FindMountedStorageImageInstance**</span><span class="sxs-lookup"><span data-stu-id="39061-129">**FindMountedStorageImageInstance**</span></span>](msvm-imagemanagementservice-findmountedstorageimageinstance.md)           | <span data-ttu-id="39061-130">Busca un \_ objeto MSVM MountedStorageImage para una ruta de acceso de imagen de disco determinada.</span><span class="sxs-lookup"><span data-stu-id="39061-130">Finds a Msvm\_MountedStorageImage object for a given disk image path.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="39061-131">**GetVHDSetInformation**</span><span class="sxs-lookup"><span data-stu-id="39061-131">**GetVHDSetInformation**</span></span>](msvm-imagemanagementservice-getvhdsetinformation.md)                                 | <span data-ttu-id="39061-132">Recupera información acerca de un archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="39061-132">Retrieves information about a VHD Set file.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="39061-133">**GetVHDSnapshotInformation**</span><span class="sxs-lookup"><span data-stu-id="39061-133">**GetVHDSnapshotInformation**</span></span>](msvm-imagemanagementservice-getvhdsnapshotinformation.md)                       | <span data-ttu-id="39061-134">Recupera información sobre una instantánea de VHD dentro de un archivo de VHD set.</span><span class="sxs-lookup"><span data-stu-id="39061-134">Retrieves information about a VHD Snapshot within a VHD Set file.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="39061-135">**GetVirtualDiskChanges**</span><span class="sxs-lookup"><span data-stu-id="39061-135">**GetVirtualDiskChanges**</span></span>](msvm-imagemanagementservice-getvirtualdiskchanges.md)                               | <span data-ttu-id="39061-136">Recupera una lista de cambios en la región especificada de un disco virtual desde el identificador de Change Tracking resistente o el identificador de la instantánea de VHDSet proporcionado.</span><span class="sxs-lookup"><span data-stu-id="39061-136">Retrieves a list of changes in the specified region of a virtual disk since the provided Resilient Change Tracking Id or VHDSet Snapshot Id.</span></span><br/>                                                                                     |
| [<span data-ttu-id="39061-137">**GetVirtualHardDiskSettingData**</span><span class="sxs-lookup"><span data-stu-id="39061-137">**GetVirtualHardDiskSettingData**</span></span>](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | <span data-ttu-id="39061-138">Recupera los datos de configuración asociados a los archivos de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="39061-138">Retrieves setting data associated with virtual hard disk files.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="39061-139">**GetVirtualHardDiskState**</span><span class="sxs-lookup"><span data-stu-id="39061-139">**GetVirtualHardDiskState**</span></span>](getvirtualharddiskstate-msvm-imagemanagementservice.md)                           | <span data-ttu-id="39061-140">Recupera el estado de los archivos de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="39061-140">Retrieves state of virtual hard disk files.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="39061-141">**MergeVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="39061-141">**MergeVirtualHardDisk**</span></span>](mergevirtualharddisk-msvm-imagemanagementservice.md)                                 | <span data-ttu-id="39061-142">Combina un disco duro virtual secundario en una cadena de diferenciación con uno o varios discos duros virtuales principales de la cadena.</span><span class="sxs-lookup"><span data-stu-id="39061-142">Merges a child virtual hard disk in a differencing chain with one or more parent virtual hard disks in the chain.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="39061-143">**OptimizeVHDSet**</span><span class="sxs-lookup"><span data-stu-id="39061-143">**OptimizeVHDSet**</span></span>](msvm-imagemanagementservice-optimizevhdset.md)                                             | <span data-ttu-id="39061-144">Optimiza un archivo de VHD set para que use menos espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="39061-144">Optimizes a VHD Set file to use less disk space.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="39061-145">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="39061-145">**RequestStateChange**</span></span>](msvm-imagemanagementservice-requeststatechange.md)                                     | <span data-ttu-id="39061-146">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="39061-146">Requests a state change.</span></span><br/>                                                                                                                                                                                                         |
| [<span data-ttu-id="39061-147">**ResizeVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="39061-147">**ResizeVirtualHardDisk**</span></span>](resizevirtualharddisk-msvm-imagemanagementservice.md)                               | <span data-ttu-id="39061-148">Cambia el tamaño de un disco duro virtual existente.</span><span class="sxs-lookup"><span data-stu-id="39061-148">Resizes an existing virtual hard disk.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="39061-149">**SetParentVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="39061-149">**SetParentVirtualHardDisk**</span></span>](setparentvirtualharddisk-msvm-imagemanagementservice.md)                         | <span data-ttu-id="39061-150">Actualiza el elemento primario de los archivos de disco duro virtual de hoja y secundario especificados.</span><span class="sxs-lookup"><span data-stu-id="39061-150">Updates the parent for the specified leaf and child virtual hard disk files.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="39061-151">**SetVHDSnapshotInformation**</span><span class="sxs-lookup"><span data-stu-id="39061-151">**SetVHDSnapshotInformation**</span></span>](msvm-imagemanagementservice-setvhdsnapshotinformation.md)                       | <span data-ttu-id="39061-152">Edita una entrada de instantánea de VHD dentro de un archivo de conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="39061-152">Edits a VHD Snapshot entry within a VHD Set file.</span></span> <span data-ttu-id="39061-153">Si el ID. de instantánea en cuestión ya existe, la entrada de instantánea existente se sobrescribirá con la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="39061-153">If the Snapshot Id in question already exists, the existing Snapshot entry will be overwritten with the new entry.</span></span> <span data-ttu-id="39061-154">De lo contrario, la nueva entrada se agregará al archivo del conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="39061-154">Otherwise, the new entry will be added to the VHD Set file.</span></span><br/> |
| [<span data-ttu-id="39061-155">**SetVirtualHardDiskSettingData**</span><span class="sxs-lookup"><span data-stu-id="39061-155">**SetVirtualHardDiskSettingData**</span></span>](setvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | <span data-ttu-id="39061-156">Establece un archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="39061-156">Sets a virtual hard disk file.</span></span><br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="39061-157">**StartService**</span><span class="sxs-lookup"><span data-stu-id="39061-157">**StartService**</span></span>](msvm-imagemanagementservice-startservice.md)                                                 | <span data-ttu-id="39061-158">inicia el servicio.</span><span class="sxs-lookup"><span data-stu-id="39061-158">Starts the service.</span></span><br/>                                                                                                                                                                                                              |
| [<span data-ttu-id="39061-159">**StopService**</span><span class="sxs-lookup"><span data-stu-id="39061-159">**StopService**</span></span>](msvm-imagemanagementservice-stopservice.md)                                                   | <span data-ttu-id="39061-160">detiene el servicio.</span><span class="sxs-lookup"><span data-stu-id="39061-160">Stops the service.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="39061-161">**ValidatePersistentReservationSupport**</span><span class="sxs-lookup"><span data-stu-id="39061-161">**ValidatePersistentReservationSupport**</span></span>](msvm-imagemanagementservice-validatepersistentreservationsupport.md) | <span data-ttu-id="39061-162">Valida si un sistema de archivos puede admitir un disco duro virtual con reservas persistentes habilitadas.</span><span class="sxs-lookup"><span data-stu-id="39061-162">Validates whether a file system can support a virtual hard disk with persistent reservations enabled.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="39061-163">**ValidateVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="39061-163">**ValidateVirtualHardDisk**</span></span>](validatevirtualharddisk-msvm-imagemanagementservice.md)                           | <span data-ttu-id="39061-164">Valida si una imagen de disco virtual se puede abrir en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="39061-164">Validates whether a virtual disk image can be opened in read-only mode.</span></span><br/>                                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="39061-165">Propiedades</span><span class="sxs-lookup"><span data-stu-id="39061-165">Properties</span></span>

<span data-ttu-id="39061-166">La clase **MSVM \_ ImageManagementService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="39061-166">The **Msvm\_ImageManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39061-167">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="39061-167">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-168">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39061-168">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="39061-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-170">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="39061-170">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="39061-171">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="39061-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="39061-172">**Caption**</span><span class="sxs-lookup"><span data-stu-id="39061-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39061-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39061-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-175">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="39061-175">A short description of the object.</span></span> <span data-ttu-id="39061-176">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "servicio de administración de imágenes de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="39061-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Image Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="39061-177">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="39061-177">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-178">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39061-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39061-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-180">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="39061-180">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="39061-181">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="39061-181">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="39061-182">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="39061-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="39061-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="39061-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="39061-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="39061-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="39061-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="39061-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="39061-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="39061-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="39061-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="39061-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="39061-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="39061-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="39061-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="39061-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="39061-190">)</span><span class="sxs-lookup"><span data-stu-id="39061-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="39061-191">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="39061-191">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39061-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39061-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-194">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="39061-194">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="39061-195">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ ImageManagementService".</span><span class="sxs-lookup"><span data-stu-id="39061-195">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ImageManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="39061-196">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="39061-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39061-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39061-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-199">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="39061-199">A description of the object.</span></span> <span data-ttu-id="39061-200">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "proporciona servicio de administración de imágenes para Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="39061-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Image Management servicing for Hyper-V".</span></span>

</dd> <dt>

<span data-ttu-id="39061-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="39061-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-202">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39061-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39061-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-204">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="39061-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="39061-205">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="39061-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="39061-206">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="39061-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="39061-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="39061-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="39061-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="39061-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="39061-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="39061-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="39061-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="39061-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="39061-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="39061-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="39061-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="39061-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="39061-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="39061-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="39061-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="39061-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="39061-215">)</span><span class="sxs-lookup"><span data-stu-id="39061-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="39061-216">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="39061-216">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39061-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39061-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-219">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="39061-219">A display name for the object.</span></span> <span data-ttu-id="39061-220">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "servicio de administración de imágenes de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="39061-220">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Image Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="39061-221">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="39061-221">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-222">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39061-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39061-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-224">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="39061-224">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="39061-225">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="39061-225">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="39061-226">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="39061-226">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-227">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39061-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39061-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-229">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="39061-229">The enabled and disabled states of an element.</span></span> <span data-ttu-id="39061-230">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="39061-230">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="39061-231">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="39061-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="39061-232">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="39061-232">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-233">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39061-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39061-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-235">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="39061-235">The current health of the element.</span></span> <span data-ttu-id="39061-236">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="39061-236">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="39061-237">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="39061-237">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="39061-238">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5.</span><span class="sxs-lookup"><span data-stu-id="39061-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="39061-239">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="39061-239">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-240">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="39061-240">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="39061-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-242">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="39061-242">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="39061-243">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="39061-243">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="39061-244">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="39061-244">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-245">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39061-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39061-246">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39061-247">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="39061-247">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="39061-248">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="39061-248">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="39061-249">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="39061-249">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="39061-250">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="39061-250">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-251">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39061-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39061-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39061-253">Calificadores: **clave**, **invalidación** ("nombre"), **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="39061-253">Qualifiers: **Key**, **Override** ("Name"), **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="39061-254">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="39061-254">The label by which the object is known.</span></span> <span data-ttu-id="39061-255">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "vhdsvc".</span><span class="sxs-lookup"><span data-stu-id="39061-255">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "vhdsvc".</span></span>

</dd> <dt>

<span data-ttu-id="39061-256">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="39061-256">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-257">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39061-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39061-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-259">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="39061-259">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="39061-260">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="39061-260">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="39061-261">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="39061-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="39061-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="39061-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="39061-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="39061-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="39061-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="39061-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="39061-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="39061-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="39061-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="39061-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="39061-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="39061-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="39061-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="39061-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="39061-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="39061-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="39061-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="39061-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="39061-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="39061-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="39061-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="39061-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="39061-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="39061-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="39061-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="39061-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="39061-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="39061-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="39061-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="39061-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="39061-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="39061-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="39061-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="39061-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="39061-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="39061-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="39061-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="39061-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="39061-281">)</span><span class="sxs-lookup"><span data-stu-id="39061-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="39061-282">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="39061-282">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-283">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39061-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="39061-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-285">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="39061-285">The current status of the object.</span></span> <span data-ttu-id="39061-286">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="39061-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="39061-287">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="39061-287">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-288">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39061-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39061-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-290">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="39061-290">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="39061-291">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="39061-291">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="39061-292">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="39061-292">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="39061-293">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="39061-293">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-294">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39061-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39061-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-296">Una cadena que proporciona información sobre cómo se puede alcanzar el propietario principal del servicio (por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.).</span><span class="sxs-lookup"><span data-stu-id="39061-296">A string that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="39061-297">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="39061-297">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="39061-298">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="39061-298">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-299">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39061-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39061-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-301">Nombre del propietario principal del servicio, si se ha definido uno.</span><span class="sxs-lookup"><span data-stu-id="39061-301">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="39061-302">El propietario principal es el contacto de soporte inicial para el servicio.</span><span class="sxs-lookup"><span data-stu-id="39061-302">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="39061-303">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="39061-303">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="39061-304">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="39061-304">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-305">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39061-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39061-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-307">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="39061-307">Provides high level status information.</span></span> <span data-ttu-id="39061-308">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="39061-308">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="39061-309">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="39061-309">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="39061-310">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="39061-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="39061-311"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="39061-311"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="39061-312"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="39061-312"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="39061-313"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="39061-313"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="39061-314"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="39061-314"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="39061-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="39061-315"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="39061-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="39061-316"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="39061-317">)</span><span class="sxs-lookup"><span data-stu-id="39061-317">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="39061-318">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="39061-318">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-319">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39061-319">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39061-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-321">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="39061-321">The last requested or desired state for the element.</span></span> <span data-ttu-id="39061-322">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="39061-322">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="39061-323">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="39061-323">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="39061-324">Una instancia concreta de **EnabledLogicalElement** podría no ser compatible con **RequestedStateChange**.</span><span class="sxs-lookup"><span data-stu-id="39061-324">A particular instance of **EnabledLogicalElement** might not support **RequestedStateChange**.</span></span> <span data-ttu-id="39061-325">Si esto ocurre, se usa el valor 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="39061-325">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="39061-326">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="39061-326">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="39061-327">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="39061-327">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-328">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="39061-328">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="39061-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-330">Indica si se ha iniciado el servicio.</span><span class="sxs-lookup"><span data-stu-id="39061-330">Indicates whether the service has been started.</span></span> <span data-ttu-id="39061-331">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="39061-331">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="39061-332">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="39061-332">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-333">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39061-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39061-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-335">Un valor de cadena que indica si el servicio se inicia automáticamente por un sistema, un sistema operativo o se inicia solo después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="39061-335">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="39061-336">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="39061-336">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="39061-337">**Estado**</span><span class="sxs-lookup"><span data-stu-id="39061-337">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-338">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39061-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39061-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-340">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="39061-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="39061-341">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="39061-341">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-342">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="39061-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="39061-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-344">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="39061-344">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="39061-345">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="39061-345">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="39061-346">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="39061-346">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-347">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39061-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39061-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-349">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="39061-349">The scoping system's creation class name.</span></span> <span data-ttu-id="39061-350">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="39061-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="39061-351">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="39061-351">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="39061-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39061-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-354">Nombre del sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="39061-354">The name of the hosting computer system.</span></span> <span data-ttu-id="39061-355">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="39061-355">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="39061-356">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="39061-356">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-357">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="39061-357">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="39061-358">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-359">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="39061-359">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="39061-360">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="39061-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="39061-361">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="39061-361">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39061-362">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="39061-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39061-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39061-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39061-364">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="39061-364">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="39061-365">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="39061-365">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39061-366">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39061-366">Remarks</span></span>

<span data-ttu-id="39061-367">El acceso a la clase **MSVM \_ ImageManagementService** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="39061-367">Access to the **Msvm\_ImageManagementService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="39061-368">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="39061-368">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="39061-369">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39061-369">Requirements</span></span>



| <span data-ttu-id="39061-370">Requisito</span><span class="sxs-lookup"><span data-stu-id="39061-370">Requirement</span></span> | <span data-ttu-id="39061-371">Value</span><span class="sxs-lookup"><span data-stu-id="39061-371">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39061-372">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39061-372">Minimum supported client</span></span><br/> | <span data-ttu-id="39061-373">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="39061-373">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="39061-374">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39061-374">Minimum supported server</span></span><br/> | <span data-ttu-id="39061-375">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="39061-375">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39061-376">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="39061-376">Namespace</span></span><br/>                | <span data-ttu-id="39061-377">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="39061-377">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="39061-378">MOF</span><span class="sxs-lookup"><span data-stu-id="39061-378">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39061-379"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39061-379"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="39061-380">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="39061-380">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39061-381"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="39061-381"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="39061-382">Vea también</span><span class="sxs-lookup"><span data-stu-id="39061-382">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39061-383">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="39061-383">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

[<span data-ttu-id="39061-384">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="39061-384">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> <dt>

[<span data-ttu-id="39061-385">Clases de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="39061-385">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

