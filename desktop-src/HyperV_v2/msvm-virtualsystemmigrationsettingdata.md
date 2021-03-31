---
description: Representa la configuración de migración para migrar un sistema virtual y el almacenamiento conectado a un sistema virtual.
ms.assetid: 2d632fe2-31ee-4e4d-b2a6-c1d1f3b4d624
title: Msvm_VirtualSystemMigrationSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationSettingData
- Msvm_VirtualSystemMigrationSettingData.InstanceID
- Msvm_VirtualSystemMigrationSettingData.Caption
- Msvm_VirtualSystemMigrationSettingData.Description
- Msvm_VirtualSystemMigrationSettingData.ElementName
- Msvm_VirtualSystemMigrationSettingData.MigrationType
- Msvm_VirtualSystemMigrationSettingData.Priority
- Msvm_VirtualSystemMigrationSettingData.Bandwidth
- Msvm_VirtualSystemMigrationSettingData.BandwidthUnit
- Msvm_VirtualSystemMigrationSettingData.OtherTransportType
- Msvm_VirtualSystemMigrationSettingData.TransportType
- Msvm_VirtualSystemMigrationSettingData.RemoveSourceUnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.AvoidRemovingVHDs
- Msvm_VirtualSystemMigrationSettingData.CPUCappingMagnitude
- Msvm_VirtualSystemMigrationSettingData.CancelIfBlackoutThresholdExceeded
- Msvm_VirtualSystemMigrationSettingData.AllowOverwriteExistingFile
- Msvm_VirtualSystemMigrationSettingData.UnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.DestinationPlannedVirtualSystemId
- Msvm_VirtualSystemMigrationSettingData.DestinationIPAddressList
- Msvm_VirtualSystemMigrationSettingData.RetainVhdCopiesOnSource
- Msvm_VirtualSystemMigrationSettingData.EnableCompression
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 254884153b3f733691b1103a6eb57f204b5d1764
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907693"
---
# <a name="msvm_virtualsystemmigrationsettingdata-class"></a><span data-ttu-id="590a5-103">MSVM \_ VirtualSystemMigrationSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="590a5-103">Msvm\_VirtualSystemMigrationSettingData class</span></span>

<span data-ttu-id="590a5-104">Representa la configuración de migración para migrar un sistema virtual y el almacenamiento conectado a un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="590a5-104">Represents the migration settings for migrating a virtual system and the storage attached to a virtual system.</span></span>

<span data-ttu-id="590a5-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="590a5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="590a5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="590a5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationSettingData : CIM_VirtualSystemMigrationSettingData
{
  string  InstanceID;
  string  Caption = "Migration Setting Data";
  string  Description = "Virtual System Migration Setting Data";
  string  ElementName;
  uint16  MigrationType;
  uint16  Priority;
  uint16  Bandwidth;
  string  BandwidthUnit;
  string  OtherTransportType;
  uint16  TransportType;
  boolean RemoveSourceUnmanagedVhds;
  boolean AvoidRemovingVHDs;
  uint16  CPUCappingMagnitude;
  boolean CancelIfBlackoutThresholdExceeded;
  boolean AllowOverwriteExistingFile;
  string  UnmanagedVhds[];
  string  DestinationPlannedVirtualSystemId;
  string  DestinationIPAddressList[];
  boolean RetainVhdCopiesOnSource;
  boolean EnableCompression;
};
```

## <a name="members"></a><span data-ttu-id="590a5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="590a5-107">Members</span></span>

<span data-ttu-id="590a5-108">La clase **MSVM \_ VirtualSystemMigrationSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="590a5-108">The **Msvm\_VirtualSystemMigrationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="590a5-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="590a5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="590a5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="590a5-110">Properties</span></span>

<span data-ttu-id="590a5-111">La clase **MSVM \_ VirtualSystemMigrationSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="590a5-111">The **Msvm\_VirtualSystemMigrationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="590a5-112">**AllowOverwriteExistingFile**</span><span class="sxs-lookup"><span data-stu-id="590a5-112">**AllowOverwriteExistingFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="590a5-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="590a5-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="590a5-115">Permita que la operación de migración de almacenamiento sobrescriba los archivos. vhdx existentes.</span><span class="sxs-lookup"><span data-stu-id="590a5-115">Allow the storage migration operation to overwrite existing .vhdx files.</span></span>

> [!Note]  
> <span data-ttu-id="590a5-116">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="590a5-116">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="590a5-117">**AvoidRemovingVHDs**</span><span class="sxs-lookup"><span data-stu-id="590a5-117">**AvoidRemovingVHDs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-118">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="590a5-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="590a5-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="590a5-120">No quite los discos duros virtuales durante la migración, es decir, los VHD del origen en los VHD de successand en el destino en caso de error.</span><span class="sxs-lookup"><span data-stu-id="590a5-120">Do not remove any VHDs during the migration, i.e. VHDs on the source in successand VHDs on the destination in failure.</span></span>

> [!Note]  
> <span data-ttu-id="590a5-121">Agregado en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="590a5-121">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="590a5-122">**Ancho de banda**</span><span class="sxs-lookup"><span data-stu-id="590a5-122">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-123">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="590a5-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="590a5-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="590a5-125">Especifica el ancho de banda asignado a o solicitado para una operación de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="590a5-125">Specifies the bandwidth assigned to or requested for a virtual system migration operation.</span></span> <span data-ttu-id="590a5-126">Las unidades de ancho de banda se especifican mediante la propiedad **BandwidthUnit** .</span><span class="sxs-lookup"><span data-stu-id="590a5-126">The bandwidth units are specified by the **BandwidthUnit** property.</span></span> <span data-ttu-id="590a5-127">En una migración, el valor 0 indica el ancho de banda predeterminado.</span><span class="sxs-lookup"><span data-stu-id="590a5-127">Within a migration, a value of 0 indicates the default bandwidth.</span></span> <span data-ttu-id="590a5-128">De lo contrario, un valor de 0 indica que no se admiten anchos de banda.</span><span class="sxs-lookup"><span data-stu-id="590a5-128">Otherwise, a value of 0 indicates that bandwidths are not supported.</span></span>

<span data-ttu-id="590a5-129">El **ancho de banda** y la **prioridad** se pueden usar conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="590a5-129">**Bandwidth** and **Priority** can be used in conjunction.</span></span> <span data-ttu-id="590a5-130">Los procesos de migración que tienen el valor de prioridad más alto comparten el ancho de banda disponible según el ancho de banda solicitado.</span><span class="sxs-lookup"><span data-stu-id="590a5-130">Migration processes that have the highest equal priority value share the available bandwidth based on their requested bandwidth.</span></span> <span data-ttu-id="590a5-131">Si este conjunto de procesos no consume todo el ancho de banda, los procesos de migración con la siguiente prioridad inferior menor comparten el ancho de banda restante.</span><span class="sxs-lookup"><span data-stu-id="590a5-131">If not all bandwidth is consumed by this set of processes, migration processes with the next lower equal priority share the remaining bandwidth.</span></span> <span data-ttu-id="590a5-132">Si todavía queda más ancho de banda, se tienen en cuenta los procesos de migración con la siguiente prioridad más baja y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="590a5-132">If still more bandwidth remains, migration processes with the next lower equal priority are considered, and so forth.</span></span>

<span data-ttu-id="590a5-133">Esta propiedad se hereda de **\_ VirtualSystemMigrationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="590a5-133">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="590a5-134">**BandwidthUnit**</span><span class="sxs-lookup"><span data-stu-id="590a5-134">**BandwidthUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="590a5-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="590a5-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="590a5-137">Especifica las unidades utilizadas por la propiedad de **ancho de banda** .</span><span class="sxs-lookup"><span data-stu-id="590a5-137">Specifies the units used by the **Bandwidth** property.</span></span> <span data-ttu-id="590a5-138">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el Apéndice C. 1 de DSP0004 V 2.4 o posterior.</span><span class="sxs-lookup"><span data-stu-id="590a5-138">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

<span data-ttu-id="590a5-139">Si el valor de esta propiedad es "Percent", el valor de la propiedad de **ancho de banda** debe estar entre 0 y 100, con valores más altos que indican un ancho de banda mayor.</span><span class="sxs-lookup"><span data-stu-id="590a5-139">If the value of this property is "percent", the value of the **Bandwidth** property must be between 0 and 100, with higher values indicating a higher bandwidth.</span></span> <span data-ttu-id="590a5-140">Un valor de 100 indica el ancho de banda total disponible para realizar operaciones de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="590a5-140">A value of 100 indicates the total available bandwidth for performing virtual system migration operations.</span></span> <span data-ttu-id="590a5-141">Los valores entre 1 y 100 deben correlacionarse linealmente con el intervalo de ancho de banda disponible.</span><span class="sxs-lookup"><span data-stu-id="590a5-141">Values between 1 and 100 should linearly correlate with the available bandwidth range.</span></span> <span data-ttu-id="590a5-142">Por ejemplo, un valor de 50 debe solicitar la mitad del ancho de banda disponible.</span><span class="sxs-lookup"><span data-stu-id="590a5-142">For example, a value of 50 should request half of the available bandwidth.</span></span>

<span data-ttu-id="590a5-143">Esta propiedad se hereda de **\_ VirtualSystemMigrationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="590a5-143">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="590a5-144">**CancelIfBlackoutThresholdExceeded**</span><span class="sxs-lookup"><span data-stu-id="590a5-144">**CancelIfBlackoutThresholdExceeded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-145">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="590a5-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-146">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="590a5-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="590a5-147">Cancela la migración si se supera el tiempo de umbral de apagón.</span><span class="sxs-lookup"><span data-stu-id="590a5-147">Cancels migration if the blackout threshold time is exceeded.</span></span>

> [!Note]  
> <span data-ttu-id="590a5-148">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="590a5-148">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="590a5-149">**Caption**</span><span class="sxs-lookup"><span data-stu-id="590a5-149">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="590a5-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="590a5-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="590a5-152">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="590a5-152">A short description of the object.</span></span> <span data-ttu-id="590a5-153">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="590a5-153">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="590a5-154">**CPUCappingMagnitude**</span><span class="sxs-lookup"><span data-stu-id="590a5-154">**CPUCappingMagnitude**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-155">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="590a5-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-156">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="590a5-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="590a5-157">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CPUCappingMagnitude")</span><span class="sxs-lookup"><span data-stu-id="590a5-157">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CPUCappingMagnitude")</span></span>
</dt> </dl>

<span data-ttu-id="590a5-158">Grado de límite de CPU durante la migración.</span><span class="sxs-lookup"><span data-stu-id="590a5-158">Degree of CPU capping during migration.</span></span>

> [!Note]  
> <span data-ttu-id="590a5-159">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="590a5-159">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="590a5-160">**Normal** (0)</span><span class="sxs-lookup"><span data-stu-id="590a5-160">**Normal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="590a5-161">**Bajo** (1)</span><span class="sxs-lookup"><span data-stu-id="590a5-161">**Low** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="590a5-162">**Alto** (2)</span><span class="sxs-lookup"><span data-stu-id="590a5-162">**High** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="590a5-163">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="590a5-163">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="590a5-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="590a5-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="590a5-166">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="590a5-166">A description of the object.</span></span> <span data-ttu-id="590a5-167">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="590a5-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="590a5-168">**DestinationIPAddressList**</span><span class="sxs-lookup"><span data-stu-id="590a5-168">**DestinationIPAddressList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-169">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="590a5-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="590a5-170">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="590a5-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="590a5-171">Será **null** para la migración de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="590a5-171">This will be **Null** for storage migration.</span></span> <span data-ttu-id="590a5-172">En el caso de la migración del sistema virtual, esta puede contener una lista de direcciones IP del host de destino.</span><span class="sxs-lookup"><span data-stu-id="590a5-172">For virtual system migration, this can contain a list of IP addresses of the destination host.</span></span>

</dd> <dt>

<span data-ttu-id="590a5-173">**DestinationPlannedVirtualSystemId**</span><span class="sxs-lookup"><span data-stu-id="590a5-173">**DestinationPlannedVirtualSystemId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="590a5-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="590a5-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="590a5-176">Si existe una máquina virtual planeada en el destino de la migración, esta propiedad se establecerá en el GUID de la máquina virtual planeada de destino en la que se debe migrar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="590a5-176">If a planned virtual machine exists at the migration destination, this property will be set to the GUID of the destination planned virtual machine where the virtual machine needs to migrate.</span></span> <span data-ttu-id="590a5-177">Esto resulta útil para los casos en los que un usuario ha creado una máquina virtual planeada en el destino, junto con la configuración de recursos, y desea que una máquina virtual del origen migre a esta máquina virtual planeada.</span><span class="sxs-lookup"><span data-stu-id="590a5-177">This is useful for cases where a user has created a planned virtual machine at the destination, along with resource setup, and wants a virtual machine from the source to migrate into this planned virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="590a5-178">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="590a5-178">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="590a5-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="590a5-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="590a5-181">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="590a5-181">A display name for the object.</span></span> <span data-ttu-id="590a5-182">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="590a5-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="590a5-183">**EnableCompression**</span><span class="sxs-lookup"><span data-stu-id="590a5-183">**EnableCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-184">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="590a5-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-185">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="590a5-185">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="590a5-186">Indica si se debe comprimir el tráfico de migración en vivo.</span><span class="sxs-lookup"><span data-stu-id="590a5-186">Indicates whether to compress the live migration traffic.</span></span> <span data-ttu-id="590a5-187">**True** indica que se va a comprimir; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="590a5-187">**True** indicates to compress; otherwise **False**.</span></span>

<span data-ttu-id="590a5-188">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="590a5-188">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="590a5-189">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="590a5-189">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="590a5-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="590a5-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="590a5-192">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="590a5-192">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="590a5-193">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="590a5-193">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="590a5-194">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="590a5-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="590a5-195">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="590a5-195">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-196">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="590a5-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-197">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="590a5-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="590a5-198">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MigrationType")</span><span class="sxs-lookup"><span data-stu-id="590a5-198">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MigrationType")</span></span>
</dt> </dl>

<span data-ttu-id="590a5-199">Especifica el tipo de operación de migración que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="590a5-199">Specifies the type of migration operation to be performed.</span></span> <span data-ttu-id="590a5-200">Esta propiedad se hereda de **\_ VirtualSystemMigrationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="590a5-200">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="590a5-201"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="590a5-201"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>

<span data-ttu-id="590a5-202"><span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768)</span><span class="sxs-lookup"><span data-stu-id="590a5-202"><span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="590a5-203">Migra el sistema virtual al host de destino.</span><span class="sxs-lookup"><span data-stu-id="590a5-203">Migrates the virtual system to the destination host.</span></span>

</dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span data-ttu-id="590a5-204"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Almacenamiento** (32769)</span><span class="sxs-lookup"><span data-stu-id="590a5-204"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Storage** (32769)</span></span>


</dt> <dd>

<span data-ttu-id="590a5-205">Migra solo los recursos de almacenamiento del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="590a5-205">Migrates only the storage resources of the virtual system.</span></span>

</dd> <dt>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>

<span data-ttu-id="590a5-206"><span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Almacenado provisionalmente** (32770)</span><span class="sxs-lookup"><span data-stu-id="590a5-206"><span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Staged** (32770)</span></span>


</dt> <dd>

<span data-ttu-id="590a5-207">Mediante la configuración del sistema virtual, crea un sistema virtual planeado en el host de destino.</span><span class="sxs-lookup"><span data-stu-id="590a5-207">Using the virtual system configuration, creates a planned virtual system at the destination host.</span></span>

</dd> <dt>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>

<span data-ttu-id="590a5-208"><span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771)</span><span class="sxs-lookup"><span data-stu-id="590a5-208"><span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771)</span></span>


</dt> <dd>

<span data-ttu-id="590a5-209">Migra el sistema virtual y su almacenamiento al host de destino.</span><span class="sxs-lookup"><span data-stu-id="590a5-209">Migrates the virtual system and its storage to the destination host.</span></span>

</dd> <dt>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>

<span data-ttu-id="590a5-210"><span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772)</span><span class="sxs-lookup"><span data-stu-id="590a5-210"><span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772)</span></span>


</dt> <dd>

<span data-ttu-id="590a5-211">Realiza una comprobación de la capacidad de migración de recursos de almacenamiento del sistema virtual en el host de destino.</span><span class="sxs-lookup"><span data-stu-id="590a5-211">Performs a virtual system storage resource migration ability check at the destination host.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="590a5-212">**OtherTransportType**</span><span class="sxs-lookup"><span data-stu-id="590a5-212">**OtherTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="590a5-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="590a5-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="590a5-215">Especifica el tipo de transporte que se va a aplicar si el valor de **TransportType** es 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="590a5-215">Specifies the type of transport to be applied if the value of **TransportType** is 1 (Other).</span></span> <span data-ttu-id="590a5-216">Esta propiedad se hereda de **\_ VirtualSystemMigrationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="590a5-216">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="590a5-217">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="590a5-217">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-218">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="590a5-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="590a5-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="590a5-220">Especifica una importancia relativa de la migración, que el sistema de migración puede usar para ordenar o dar preferencia entre varias solicitudes de migración pendientes.</span><span class="sxs-lookup"><span data-stu-id="590a5-220">Specifies a relative migration importance, which the migration system may use to order or otherwise give preference among multiple pending migration requests.</span></span> <span data-ttu-id="590a5-221">Cuanto menor sea el valor, mayor será la prioridad.</span><span class="sxs-lookup"><span data-stu-id="590a5-221">The lower the value, the higher the priority.</span></span> <span data-ttu-id="590a5-222">En una migración, un valor de 0 indica la prioridad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="590a5-222">Within a migration, a value of 0 indicates the default priority.</span></span> <span data-ttu-id="590a5-223">De lo contrario, un valor de 0 indica que no se admiten las prioridades.</span><span class="sxs-lookup"><span data-stu-id="590a5-223">Otherwise, a value of 0 indicates that priorities are not supported.</span></span>

<span data-ttu-id="590a5-224">Esta propiedad se hereda de **\_ VirtualSystemMigrationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="590a5-224">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="590a5-225">**RemoveSourceUnmanagedVhds**</span><span class="sxs-lookup"><span data-stu-id="590a5-225">**RemoveSourceUnmanagedVhds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-226">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="590a5-226">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-227">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="590a5-227">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="590a5-228">Quite los VHD no administrados de origen.</span><span class="sxs-lookup"><span data-stu-id="590a5-228">Remove source unmanaged VHDs.</span></span>

> [!Note]  
> <span data-ttu-id="590a5-229">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="590a5-229">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="590a5-230">**RetainVhdCopiesOnSource**</span><span class="sxs-lookup"><span data-stu-id="590a5-230">**RetainVhdCopiesOnSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-231">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="590a5-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-232">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="590a5-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="590a5-233">En el caso de una migración de almacenamiento, especifica si se deben quitar los VHD de solo lectura del host de origen una vez completada la migración.</span><span class="sxs-lookup"><span data-stu-id="590a5-233">For a storage migration, this specifies whether the read-only VHDs on the source host should be removed after the migration is completed.</span></span>

</dd> <dt>

<span data-ttu-id="590a5-234">**TransportType**</span><span class="sxs-lookup"><span data-stu-id="590a5-234">**TransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-235">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="590a5-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="590a5-236">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="590a5-236">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="590a5-237">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")</span><span class="sxs-lookup"><span data-stu-id="590a5-237">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")</span></span>
</dt> </dl>

<span data-ttu-id="590a5-238">Especifica el tipo de transporte que se va a aplicar a una operación de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="590a5-238">Specifies the type of transport to be applied for a virtual system migration operation.</span></span> <span data-ttu-id="590a5-239">Esta propiedad se hereda de **\_ VirtualSystemMigrationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="590a5-239">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="590a5-240">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="590a5-240">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="590a5-241">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="590a5-241">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

<span data-ttu-id="590a5-242">**Ssh** (2)</span><span class="sxs-lookup"><span data-stu-id="590a5-242">**SSH** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

<span data-ttu-id="590a5-243">**TLS** (3)</span><span class="sxs-lookup"><span data-stu-id="590a5-243">**TLS** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

<span data-ttu-id="590a5-244">**TLS STRICT** (4)</span><span class="sxs-lookup"><span data-stu-id="590a5-244">**TLS Strict** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="590a5-245">**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="590a5-245">**TCP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="590a5-246">**IPC** (6)</span><span class="sxs-lookup"><span data-stu-id="590a5-246">**IPC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="590a5-247">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="590a5-247">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="590a5-248">**Proveedor reservado** (32768...)</span><span class="sxs-lookup"><span data-stu-id="590a5-248">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="590a5-249"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="590a5-249"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="590a5-250">Para la migración en vivo, esta propiedad especifica el tipo de transporte que se va a usar para transferir el estado del sistema virtual al host de destino.</span><span class="sxs-lookup"><span data-stu-id="590a5-250">For live migration, this property specifies the transport type to be used for transferring virtual system state to the destination host.</span></span> <span data-ttu-id="590a5-251">Los valores admitidos son:</span><span class="sxs-lookup"><span data-stu-id="590a5-251">The supported values are:</span></span>

<dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="590a5-252"><span id="TCP"></span><span id="tcp"></span>**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="590a5-252"><span id="TCP"></span><span id="tcp"></span>**TCP** (5)</span></span>


</dt> <dd>

<span data-ttu-id="590a5-253">Indica el tipo de transporte TCP.</span><span class="sxs-lookup"><span data-stu-id="590a5-253">Indicates the TCP transport type.</span></span>

</dd> <dt>

<span id="SMB"></span><span id="smb"></span>

<span data-ttu-id="590a5-254"><span id="SMB"></span><span id="smb"></span>**SMB** (32768)</span><span class="sxs-lookup"><span data-stu-id="590a5-254"><span id="SMB"></span><span id="smb"></span>**SMB** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="590a5-255">Indica que el tipo de transporte para transferir el estado de la máquina virtual es SMB.</span><span class="sxs-lookup"><span data-stu-id="590a5-255">Indicates the transport type for transferring the virtual machine state is SMB.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="590a5-256">**UnmanagedVhds**</span><span class="sxs-lookup"><span data-stu-id="590a5-256">**UnmanagedVhds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="590a5-257">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="590a5-257">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="590a5-258">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="590a5-258">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="590a5-259">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), **HyperVEmbeddedInstance** ("MSVM \_ MoveUnmanagedVhd")</span><span class="sxs-lookup"><span data-stu-id="590a5-259">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_MoveUnmanagedVhd")</span></span>
</dt> </dl>

<span data-ttu-id="590a5-260">Una matriz de instancias de [**MSVM \_ MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md) insertadas que contienen información de VHD no administrados.</span><span class="sxs-lookup"><span data-stu-id="590a5-260">An array of embedded [**Msvm\_MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md) instances which contain unmanaged VHDs information.</span></span>

> [!Note]  
> <span data-ttu-id="590a5-261">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="590a5-261">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="590a5-262">Requisitos</span><span class="sxs-lookup"><span data-stu-id="590a5-262">Requirements</span></span>



| <span data-ttu-id="590a5-263">Requisito</span><span class="sxs-lookup"><span data-stu-id="590a5-263">Requirement</span></span> | <span data-ttu-id="590a5-264">Value</span><span class="sxs-lookup"><span data-stu-id="590a5-264">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="590a5-265">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="590a5-265">Minimum supported client</span></span><br/> | <span data-ttu-id="590a5-266">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="590a5-266">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="590a5-267">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="590a5-267">Minimum supported server</span></span><br/> | <span data-ttu-id="590a5-268">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="590a5-268">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="590a5-269">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="590a5-269">Namespace</span></span><br/>                | <span data-ttu-id="590a5-270">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="590a5-270">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="590a5-271">MOF</span><span class="sxs-lookup"><span data-stu-id="590a5-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="590a5-272"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="590a5-272"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="590a5-273">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="590a5-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="590a5-274"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="590a5-274"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="590a5-275">Vea también</span><span class="sxs-lookup"><span data-stu-id="590a5-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="590a5-276">**\_VIRTUALSYSTEMMIGRATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="590a5-276">**CIM\_VirtualSystemMigrationSettingData**</span></span>](cim-virtualsystemmigrationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="590a5-277">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="590a5-277">**MigrateVirtualSystemToHost**</span></span>](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

