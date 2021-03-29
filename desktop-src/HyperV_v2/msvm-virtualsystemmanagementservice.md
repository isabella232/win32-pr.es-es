---
description: Representa el servicio de virtualización presente en un sistema host único.
ms.assetid: 7f4bd9e0-b034-4882-ad01-f7df740939ae
title: Msvm_VirtualSystemManagementService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService
- Msvm_VirtualSystemManagementService.InstanceID
- Msvm_VirtualSystemManagementService.Caption
- Msvm_VirtualSystemManagementService.Description
- Msvm_VirtualSystemManagementService.ElementName
- Msvm_VirtualSystemManagementService.InstallDate
- Msvm_VirtualSystemManagementService.Name
- Msvm_VirtualSystemManagementService.OperationalStatus
- Msvm_VirtualSystemManagementService.StatusDescriptions
- Msvm_VirtualSystemManagementService.Status
- Msvm_VirtualSystemManagementService.HealthState
- Msvm_VirtualSystemManagementService.CommunicationStatus
- Msvm_VirtualSystemManagementService.DetailedStatus
- Msvm_VirtualSystemManagementService.OperatingStatus
- Msvm_VirtualSystemManagementService.PrimaryStatus
- Msvm_VirtualSystemManagementService.EnabledState
- Msvm_VirtualSystemManagementService.OtherEnabledState
- Msvm_VirtualSystemManagementService.RequestedState
- Msvm_VirtualSystemManagementService.EnabledDefault
- Msvm_VirtualSystemManagementService.TimeOfLastStateChange
- Msvm_VirtualSystemManagementService.AvailableRequestedStates
- Msvm_VirtualSystemManagementService.TransitioningToState
- Msvm_VirtualSystemManagementService.SystemCreationClassName
- Msvm_VirtualSystemManagementService.SystemName
- Msvm_VirtualSystemManagementService.CreationClassName
- Msvm_VirtualSystemManagementService.PrimaryOwnerName
- Msvm_VirtualSystemManagementService.PrimaryOwnerContact
- Msvm_VirtualSystemManagementService.StartMode
- Msvm_VirtualSystemManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ee79b9690f1eacdf7dc57a2ebfc2133091a1d55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808779"
---
# <a name="msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="5c5fe-103">MSVM \_ VirtualSystemManagementService (clase)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-103">Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="5c5fe-104">Representa el servicio de virtualización presente en un sistema host único.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-104">Represents the virtualization service present on a single host system.</span></span> <span data-ttu-id="5c5fe-105">**MSVM \_ VirtualSystemManagementService** se usa para controlar la definición, la modificación y la eliminación de máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-105">**Msvm\_VirtualSystemManagementService** is used to control the definition, modification, and deletion of virtual machines.</span></span> <span data-ttu-id="5c5fe-106">También tiene métodos para realizar operaciones en máquinas virtuales, como la clonación, la instantánea y la importación o exportación de máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-106">It also has methods for performing operations on virtual machines, such as cloning, snapshotting, and the importing or exporting of virtual machines.</span></span> <span data-ttu-id="5c5fe-107">Para recuperar la información de la máquina virtual, use [**MSVM \_ ComputerSystem**](msvm-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-107">To retrieve per-virtual machine information, use [**Msvm\_ComputerSystem**](msvm-computersystem.md).</span></span>

<span data-ttu-id="5c5fe-108">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c5fe-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c5fe-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual System Management Service";
  string   Description = "Service for creating, manipulating, and managing virtual machines";
  string   ElementName = "Hyper-V Virtual System Management Service";
  datetime InstallDate;
  string   Name = "vmms";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
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
  string   CreationClassName = "Msvm_VirtualSystemManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="5c5fe-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="5c5fe-110">Members</span></span>

<span data-ttu-id="5c5fe-111">La clase **MSVM \_ VirtualSystemManagementService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5c5fe-111">The **Msvm\_VirtualSystemManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="5c5fe-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c5fe-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="5c5fe-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c5fe-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5c5fe-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c5fe-114">Methods</span></span>

<span data-ttu-id="5c5fe-115">La clase **MSVM \_ VirtualSystemManagementService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-115">The **Msvm\_VirtualSystemManagementService** class has these methods.</span></span>



| <span data-ttu-id="5c5fe-116">Método</span><span class="sxs-lookup"><span data-stu-id="5c5fe-116">Method</span></span>                                                                                                                 | <span data-ttu-id="5c5fe-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c5fe-117">Description</span></span>                                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c5fe-118">**AddBootSourceSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-118">**AddBootSourceSettings**</span></span>](msvm-virtualsystemmanagementservice-addbootsourcesettings.md)                             | <span data-ttu-id="5c5fe-119">Agrega orígenes de arranque a una configuración de sistema virtual cuando se aplica a una configuración de sistema virtual "State".</span><span class="sxs-lookup"><span data-stu-id="5c5fe-119">Adds boot sources to a virtual system configuration when applied to a "state" virtual system configuration.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="5c5fe-120">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-120">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualsystemmanagementservice.md)                                   | <span data-ttu-id="5c5fe-121">Agrega la configuración de características Ethernet a la configuración de una conexión Ethernet de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-121">Adds Ethernet feature settings to the configuration of a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="5c5fe-122">**AddFibreChannelChap**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-122">**AddFibreChannelChap**</span></span>](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)                                 | <span data-ttu-id="5c5fe-123">Agrega parámetros DH-CHAP a un puerto de Canal de fibra sintético en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-123">Adds DH-CHAP parameters to a synthetic Fibre Channel port in a virtual machine.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="5c5fe-124">**AddGuestServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-124">**AddGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-addguestservicesettings.md)                         | <span data-ttu-id="5c5fe-125">Agrega la configuración del servicio de invitado a una configuración de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-125">Adds guest service settings to a virtual system configuration.</span></span><br/> <span data-ttu-id="5c5fe-126">Cuando se aplica a partes de una configuración de sistema virtual "actual", se puede modificar como un efecto secundario en los servicios invitados del sistema virtual activo.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-126">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>              |
| [<span data-ttu-id="5c5fe-127">**AddKvpItems**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-127">**AddKvpItems**</span></span>](addkvpitems-msvm-virtualsystemmanagementservice.md)                                                 | <span data-ttu-id="5c5fe-128">Agrega pares clave-valor a una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-128">Adds key-value pairs to a virtual machine.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="5c5fe-129">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-129">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualsystemmanagementservice.md)                                 | <span data-ttu-id="5c5fe-130">Agrega recursos a una configuración de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-130">Adds resources to a virtual machine configuration.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="5c5fe-131">**AddSystemComponentSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-131">**AddSystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md)                   | <span data-ttu-id="5c5fe-132">Agrega la configuración genérica a una configuración de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-132">Adds generic settings to a virtual system configuration.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="5c5fe-133">**DefinePlannedSystem**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-133">**DefinePlannedSystem**</span></span>](msvm-virtualsystemmanagementservice-defineplannedsystem.md)                                 | <span data-ttu-id="5c5fe-134">Define un sistema virtual planeado.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-134">Defines a planned virtual system.</span></span><br/> <span data-ttu-id="5c5fe-135">La entrada que no se ha especificado completamente puede rellenarse con valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-135">Input that is not completely specified may be filled out with default values.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="5c5fe-136">**DefineSystem**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-136">**DefineSystem**</span></span>](definesystem-msvm-virtualsystemmanagementservice.md)                                               | <span data-ttu-id="5c5fe-137">Crea una nueva definición de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-137">Creates a new virtual machine definition.</span></span><br/>                                                                                                                                                                                               |
| [<span data-ttu-id="5c5fe-138">**DestroySystem**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-138">**DestroySystem**</span></span>](destroysystem-msvm-virtualsystemmanagementservice.md)                                             | <span data-ttu-id="5c5fe-139">Elimina una definición de máquina virtual existente.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-139">Deletes an existing virtual machine definition.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="5c5fe-140">**DiagnoseNetworkConnection**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-140">**DiagnoseNetworkConnection**</span></span>](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md)                     | <span data-ttu-id="5c5fe-141">Diagnostica la conectividad de red de una máquina virtual en un entorno de virtualización de red de Windows.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-141">Diagnoses the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="5c5fe-142">**ExportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-142">**ExportSystemDefinition**</span></span>](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="5c5fe-143">Exporta una máquina virtual, o una instantánea de una máquina virtual, a un archivo.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-143">Exports a virtual machine, or a snapshot of a virtual machine, to a file.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="5c5fe-144">**FormatError**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-144">**FormatError**</span></span>](formaterror-msvm-virtualsystemmanagementservice.md)                                                 | <span data-ttu-id="5c5fe-145">Devuelve una cadena de mensaje de error con formato para la matriz especificada de instancias de [**\_ error**](msvm-error.md) incrustadas MSVM.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-145">Returns a formatted error message string for the specified array of embedded [**Msvm\_Error**](msvm-error.md) instances.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="5c5fe-146">**GenerateWwpn**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-146">**GenerateWwpn**</span></span>](generatewwpn-msvm-virtualsystemmanagementservice.md)                                               | <span data-ttu-id="5c5fe-147">Genera un conjunto de nombres de Puerto WWPN (WWPN).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-147">Generates a set of World Wide Port Names (WWPNs).</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="5c5fe-148">**GetCurrentWwpnFromGenerator**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-148">**GetCurrentWwpnFromGenerator**</span></span>](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)                 | <span data-ttu-id="5c5fe-149">Proporciona la capacidad de obtener una vista previa del nombre de Puerto WWPN (WWPN) actual sin reservar el WWPN.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-149">Provides the ability to preview the current World Wide Port Name (WWPN) without the WWPN being reserved.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="5c5fe-150">**GetDefinitionFileSummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-150">**GetDefinitionFileSummaryInformation**</span></span>](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) | <span data-ttu-id="5c5fe-151">Devuelve información de Resumen de la máquina virtual para los archivos de definición de máquina virtual especificados.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-151">Returns virtual machine summary information for the specified virtual machine definition files.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="5c5fe-152">**GetSizeOfSystemFiles**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-152">**GetSizeOfSystemFiles**</span></span>](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="5c5fe-153">Recupera el tamaño total de los archivos del sistema de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-153">Retrieves the total size of the system files of virtual machine.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="5c5fe-154">**GetSummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-154">**GetSummaryInformation**</span></span>](getsummaryinformation-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="5c5fe-155">Devuelve información de Resumen de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-155">Returns virtual machine summary information.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="5c5fe-156">**GetVirtualSystemThumbnailImage**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-156">**GetVirtualSystemThumbnailImage**</span></span>](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)           | <span data-ttu-id="5c5fe-157">Recupera una imagen en miniatura de una máquina virtual existente.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-157">Retrieves a thumbnail image of an existing virtual machine.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="5c5fe-158">**ImportSnapshotDefinitions**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-158">**ImportSnapshotDefinitions**</span></span>](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)                     | <span data-ttu-id="5c5fe-159">Busca en la carpeta especificada cualquier archivo de definición de instantánea asociado al sistema de equipo planeado especificado y crea una nueva instantánea en el sistema del equipo planeado para cada archivo de definición asociado en esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-159">Searches the specified folder for any snapshot definition files associated with the specified planned computer system, and creates a new snapshot on the planned computer system for every associated definition file in this location.</span></span><br/> |
| [<span data-ttu-id="5c5fe-160">**ImportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-160">**ImportSystemDefinition**</span></span>](importsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="5c5fe-161">Crea un nuevo sistema de equipo planeado basado en la definición de máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-161">Creates a new planned computer system based on the specified virtual machine definition.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="5c5fe-162">**ModifyDiskMergeSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-162">**ModifyDiskMergeSettings**</span></span>](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)                         | <span data-ttu-id="5c5fe-163">Modifica los datos de configuración de combinación de discos.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-163">Modifies the disk merge setting data.</span></span><br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="5c5fe-164">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-164">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="5c5fe-165">Modifica la configuración actual de las características de una conexión Ethernet de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-165">Modifies the current feature settings of a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="5c5fe-166">**ModifyGuestServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-166">**ModifyGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md)                   | <span data-ttu-id="5c5fe-167">Modifica la configuración del servicio de invitado.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-167">Modifies guest service settings.</span></span><br/> <span data-ttu-id="5c5fe-168">Cuando se aplica a partes de una configuración de sistema virtual "actual", se puede modificar como un efecto secundario en los servicios invitados del sistema virtual activo.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-168">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>                                            |
| [<span data-ttu-id="5c5fe-169">**ModifyKvpItems**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-169">**ModifyKvpItems**</span></span>](modifykvpitems-msvm-virtualsystemmanagementservice.md)                                           | <span data-ttu-id="5c5fe-170">Modifica los pares de clave y valor existentes en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-170">Modifies existing key-value pairs on a virtual machine.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="5c5fe-171">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-171">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="5c5fe-172">Modifica la configuración de recursos virtuales.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-172">Modifies virtual resource settings.</span></span><br/>                                                                                                                                                                                                     |
| [<span data-ttu-id="5c5fe-173">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-173">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="5c5fe-174">Modifica los datos de configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-174">Modifies the service's setting data.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="5c5fe-175">**ModifySystemComponentSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-175">**ModifySystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)             | <span data-ttu-id="5c5fe-176">Modifica la configuración genérica del componente del sistema.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-176">Modifies generic system component settings.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="5c5fe-177">**ModifySystemSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-177">**ModifySystemSettings**</span></span>](modifysystemsettings-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="5c5fe-178">Modifica la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-178">Modifies virtual machine settings.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="5c5fe-179">**RealizePlannedSystem**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-179">**RealizePlannedSystem**</span></span>](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="5c5fe-180">Valida la configuración de una máquina virtual planeada y la convierte en una máquina virtual realizada.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-180">Validates the configuration of a planned virtual machine and converts it to a realized virtual machine.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="5c5fe-181">**RemoveBootSourceSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-181">**RemoveBootSourceSettings**</span></span>](msvm-virtualsystemmanagementservice-removebootsourcesettings.md)                       | <span data-ttu-id="5c5fe-182">Quita la configuración de recursos virtuales de una configuración de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-182">Removes virtual resource settings from a virtual system configuration.</span></span><br/> <span data-ttu-id="5c5fe-183">Cuando se aplica a partes de una configuración de sistema virtual "actual", es posible que se eliminen los recursos secundarios del sistema virtual activo.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-183">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span><br/>            |
| [<span data-ttu-id="5c5fe-184">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-184">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="5c5fe-185">Quita la configuración de características de una conexión Ethernet de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-185">Removes feature settings from a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="5c5fe-186">**RemoveFibreChannelChap**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-186">**RemoveFibreChannelChap**</span></span>](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="5c5fe-187">Quita los parámetros DH-CHAP de un puerto de Canal de fibra sintético en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-187">Removes DH-CHAP parameters from a synthetic Fibre Channel port in a virtual machine.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="5c5fe-188">**RemoveGuestServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-188">**RemoveGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-removeguestservicesettings.md)                   | <span data-ttu-id="5c5fe-189">Quita la configuración del servicio de invitado de una configuración de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-189">Removes guest service settings from a virtual system configuration.</span></span><br/> <span data-ttu-id="5c5fe-190">Cuando se aplica a partes de una configuración de sistema virtual "actual", se puede modificar como un efecto secundario en los servicios invitados del sistema virtual activo.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-190">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>         |
| [<span data-ttu-id="5c5fe-191">**RemoveKvpItems**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-191">**RemoveKvpItems**</span></span>](removekvpitems-msvm-virtualsystemmanagementservice.md)                                           | <span data-ttu-id="5c5fe-192">Quita los pares de clave y valor existentes de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-192">Removes existing key-value pairs from a virtual machine.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="5c5fe-193">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-193">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="5c5fe-194">Quita la configuración de recursos virtuales de una configuración de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-194">Removes virtual resource settings from a virtual machine configuration.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="5c5fe-195">**RemoveSystemComponentSettings**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-195">**RemoveSystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)             | <span data-ttu-id="5c5fe-196">Quita la configuración de componentes genéricos de una configuración de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-196">Removes generic component settings from a virtual system configuration.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="5c5fe-197">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-197">**RequestStateChange**</span></span>](msvm-virtualsystemmanagementservice-requeststatechange.md)                                   | <span data-ttu-id="5c5fe-198">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-198">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="5c5fe-199">**SetGuestNetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-199">**SetGuestNetworkAdapterConfiguration**</span></span>](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md) | <span data-ttu-id="5c5fe-200">Configura los adaptadores de red en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-200">Configures the network adapters within the guest operating system.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="5c5fe-201">**SetInitialMachineConfigurationData**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-201">**SetInitialMachineConfigurationData**</span></span>](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)   | <span data-ttu-id="5c5fe-202">Establece los datos de configuración de la máquina inicial de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-202">Sets a VM's initial machine configuration data.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="5c5fe-203">**StartService**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-203">**StartService**</span></span>](msvm-virtualsystemmanagementservice-startservice.md)                                               | <span data-ttu-id="5c5fe-204">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-204">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="5c5fe-205">**StopService**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-205">**StopService**</span></span>](msvm-virtualsystemmanagementservice-stopservice.md)                                                 | <span data-ttu-id="5c5fe-206">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-206">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="5c5fe-207">**TestNetworkConnection**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-207">**TestNetworkConnection**</span></span>](msvm-virtualsystemmanagementservice-testnetworkconnection.md)                             | <span data-ttu-id="5c5fe-208">Prueba la conectividad de red de una máquina virtual en un entorno de virtualización de red de Windows.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-208">Tests the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="5c5fe-209">**UpgradeSystemVersion**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-209">**UpgradeSystemVersion**</span></span>](msvm-virtualsystemmanagementservice-upgradesystemversion.md)                               | <span data-ttu-id="5c5fe-210">Actualiza el sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-210">Upgrades the virtual system.</span></span><br/> <span data-ttu-id="5c5fe-211">Cuando se aplica a la configuración del sistema de una configuración de sistema virtual "actual"</span><span class="sxs-lookup"><span data-stu-id="5c5fe-211">When applied to the system settings of a "current" virtual system configuration</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="5c5fe-212">**ValidatePlannedSystem**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-212">**ValidatePlannedSystem**</span></span>](validateplannedsystem-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="5c5fe-213">Valida el sistema planeado especificado.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-213">Validates the specified planned system.</span></span><br/>                                                                                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="5c5fe-214">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c5fe-214">Properties</span></span>

<span data-ttu-id="5c5fe-215">La clase **MSVM \_ VirtualSystemManagementService** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-215">The **Msvm\_VirtualSystemManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c5fe-216">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-216">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-217">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-217">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-219">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="5c5fe-219">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="5c5fe-220">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-220">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-221">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-221">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-224">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-224">A short description of the object.</span></span> <span data-ttu-id="5c5fe-225">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de administración del sistema virtual de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="5c5fe-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-226">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-226">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-227">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-229">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-229">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="5c5fe-230">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-230">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5c5fe-231">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-231">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5c5fe-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-233"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-233"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-234"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-234"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-235"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-235"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-236"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-236"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="5c5fe-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5c5fe-239">)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-239">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5c5fe-240">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-241">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-243">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-243">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-244">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-244">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5c5fe-245">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ VirtualSystemManagementService".</span><span class="sxs-lookup"><span data-stu-id="5c5fe-245">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-246">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-247">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-249">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-249">A description of the object.</span></span> <span data-ttu-id="5c5fe-250">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio para crear, manipular y administrar máquinas virtuales".</span><span class="sxs-lookup"><span data-stu-id="5c5fe-250">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Service for creating, manipulating, and managing virtual machines".</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-251">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-251">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-252">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-254">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-254">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="5c5fe-255">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-255">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5c5fe-256">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5c5fe-257"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-257"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-258"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-258"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-259"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-259"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-260"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-260"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-261"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-261"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-262"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-262"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="5c5fe-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5c5fe-265">)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-265">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5c5fe-266">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-266">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-267">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-269">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-269">A display name for the object.</span></span> <span data-ttu-id="5c5fe-270">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de administración del sistema virtual de Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="5c5fe-270">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-271">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-271">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-272">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-272">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-273">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-274">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-274">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="5c5fe-275">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-275">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="5c5fe-276">Value</span><span class="sxs-lookup"><span data-stu-id="5c5fe-276">Value</span></span>                                                                        | <span data-ttu-id="5c5fe-277">Significado</span><span class="sxs-lookup"><span data-stu-id="5c5fe-277">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="5c5fe-278"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5c5fe-278"><dt>2</dt></span></span> </dl> | <span data-ttu-id="5c5fe-279">habilitado</span><span class="sxs-lookup"><span data-stu-id="5c5fe-279">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5c5fe-280">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-280">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-281">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-283">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-283">The enabled and disabled states of an element.</span></span> <span data-ttu-id="5c5fe-284">Esta propiedad también puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-284">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="5c5fe-285">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-285">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="5c5fe-286">Value</span><span class="sxs-lookup"><span data-stu-id="5c5fe-286">Value</span></span>                                                                        | <span data-ttu-id="5c5fe-287">Significado</span><span class="sxs-lookup"><span data-stu-id="5c5fe-287">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="5c5fe-288"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5c5fe-288"><dt>2</dt></span></span> </dl> | <span data-ttu-id="5c5fe-289">habilitado</span><span class="sxs-lookup"><span data-stu-id="5c5fe-289">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5c5fe-290">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-290">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-291">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-293">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-293">The current health of the element.</span></span> <span data-ttu-id="5c5fe-294">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-294">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="5c5fe-295">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-295">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="5c5fe-296">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-296">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="5c5fe-297">Value</span><span class="sxs-lookup"><span data-stu-id="5c5fe-297">Value</span></span>                                                                        | <span data-ttu-id="5c5fe-298">Significado</span><span class="sxs-lookup"><span data-stu-id="5c5fe-298">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="5c5fe-299"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="5c5fe-299"><dt>5</dt></span></span> </dl> | <span data-ttu-id="5c5fe-300">El estado de mantenimiento es normal.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-300">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5c5fe-301">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-301">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-302">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-302">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-304">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-304">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="5c5fe-305">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-306">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-306">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-309">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-309">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-310">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-310">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5c5fe-311">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-311">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-312">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-312">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-313">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-315">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-315">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-316">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-316">The label by which the object is known.</span></span> <span data-ttu-id="5c5fe-317">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre se establece en "vMMS".</span><span class="sxs-lookup"><span data-stu-id="5c5fe-317">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vmms".</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-318">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-318">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-319">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-319">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-321">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="5c5fe-321">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="5c5fe-322">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-322">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5c5fe-323">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5c5fe-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-325"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-325"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-326"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-326"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-327"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-327"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-328"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-328"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-329"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-329"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-330"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-330"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-331"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-331"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-332"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-332"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-333"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-333"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-334"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-334"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-335"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-335"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-336"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-336"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-337"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-337"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-338"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-338"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-339"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-339"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-340"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-340"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-341"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-341"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-342"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="5c5fe-342"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5c5fe-343">)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-343">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5c5fe-344">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-344">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-345">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-347">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-347">The current statuses of the object.</span></span> <span data-ttu-id="5c5fe-348">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-349">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-349">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-350">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-352">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 ("otro").</span><span class="sxs-lookup"><span data-stu-id="5c5fe-352">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="5c5fe-353">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-353">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="5c5fe-354">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-354">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-355">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-355">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-356">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-358">Calificadores: **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-358">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-359">Cualquier información sobre cómo se puede alcanzar el propietario principal del servicio (por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-359">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="5c5fe-360">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-360">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-361">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-361">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-362">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-364">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-364">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-365">Nombre del propietario principal del servicio, si se ha definido uno.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-365">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="5c5fe-366">El propietario principal es el contacto de soporte inicial para el servicio.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-366">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="5c5fe-367">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-367">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-368">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-368">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-369">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-370">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-371">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-371">Provides high level status information.</span></span> <span data-ttu-id="5c5fe-372">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-372">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="5c5fe-373">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-373">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5c5fe-374">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5c5fe-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-376"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-376"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-377"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-377"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-378"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-378"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-379"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-379"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-380"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="5c5fe-380"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5c5fe-381">)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-381">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5c5fe-382">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-382">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-383">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-383">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-384">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-385">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-385">The last requested or desired state for the element.</span></span> <span data-ttu-id="5c5fe-386">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-386">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="5c5fe-387">Esta propiedad se proporciona para comparar el último estado solicitado y el actual para un elemento.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-387">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="5c5fe-388">Una instancia concreta de la [**clase \_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir la propiedad **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="5c5fe-388">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="5c5fe-389">Si esto ocurre, se usa el valor 12 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="5c5fe-389">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="5c5fe-390">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM** y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-390">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="5c5fe-391">Value</span><span class="sxs-lookup"><span data-stu-id="5c5fe-391">Value</span></span>                                                                         | <span data-ttu-id="5c5fe-392">Significado</span><span class="sxs-lookup"><span data-stu-id="5c5fe-392">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="5c5fe-393"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="5c5fe-393"><dt>12</dt></span></span> </dl> | <span data-ttu-id="5c5fe-394">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-394">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5c5fe-395">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-395">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-396">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-398">Indica si el servicio se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-398">Indicates whether the service is currently running.</span></span> <span data-ttu-id="5c5fe-399">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-399">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-400">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-400">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-401">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-403">Calificadores: **MaxLen** (10)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-403">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-404">Un valor de cadena que indica si el servicio se inicia automáticamente por un sistema, un sistema operativo o se inicia solo después de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-404">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="5c5fe-405">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-405">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-406">**Estado**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-406">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-407">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-408">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-409">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-409">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-410">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-410">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-411">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-411">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-412">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-413">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="5c5fe-413">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="5c5fe-414">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "el servicio se está ejecutando normalmente".</span><span class="sxs-lookup"><span data-stu-id="5c5fe-414">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-415">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-415">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-416">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-417">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-418">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-418">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-419">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-419">The scoping system's creation class name.</span></span> <span data-ttu-id="5c5fe-420">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="5c5fe-420">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-421">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-421">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-422">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-422">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-423">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-424">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="5c5fe-424">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-425">Nombre NetBIOS del sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-425">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="5c5fe-426">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-426">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-427">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-427">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-428">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-428">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-429">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-430">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-430">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="5c5fe-431">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-431">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5c5fe-432">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-432">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c5fe-433">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-433">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-434">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c5fe-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c5fe-435">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-435">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="5c5fe-436">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-436">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c5fe-437">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c5fe-437">Remarks</span></span>

<span data-ttu-id="5c5fe-438">El acceso a la clase **MSVM \_ VirtualSystemManagementService** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="5c5fe-438">Access to the **Msvm\_VirtualSystemManagementService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5c5fe-439">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5c5fe-439">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c5fe-440">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c5fe-440">Requirements</span></span>



| <span data-ttu-id="5c5fe-441">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c5fe-441">Requirement</span></span> | <span data-ttu-id="5c5fe-442">Value</span><span class="sxs-lookup"><span data-stu-id="5c5fe-442">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c5fe-443">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c5fe-443">Minimum supported client</span></span><br/> | <span data-ttu-id="5c5fe-444">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c5fe-444">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5c5fe-445">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c5fe-445">Minimum supported server</span></span><br/> | <span data-ttu-id="5c5fe-446">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c5fe-446">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5c5fe-447">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5c5fe-447">Namespace</span></span><br/>                | <span data-ttu-id="5c5fe-448">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="5c5fe-448">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5c5fe-449">MOF</span><span class="sxs-lookup"><span data-stu-id="5c5fe-449">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c5fe-450"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c5fe-450"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c5fe-451">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5c5fe-451">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c5fe-452"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5c5fe-452"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5c5fe-453">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c5fe-453">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c5fe-454">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="5c5fe-454">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="5c5fe-455">[**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**](/previous-versions//cc136952(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5c5fe-455">[**CIM\_VirtualSystemManagementService**](/previous-versions//cc136952(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="5c5fe-456">[**MSVM \_ VirtualSystemManagementService (V1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5c5fe-456">[**Msvm\_VirtualSystemManagementService (V1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5c5fe-457">Clases de administración de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="5c5fe-457">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

