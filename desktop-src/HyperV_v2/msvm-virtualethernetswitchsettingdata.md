---
description: Representa la configuración actual de un conmutador Ethernet virtual.
ms.assetid: a7c03517-332d-47ce-8e04-c2187bcb2977
title: Msvm_VirtualEthernetSwitchSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingData
- Msvm_VirtualEthernetSwitchSettingData.InstanceID
- Msvm_VirtualEthernetSwitchSettingData.Caption
- Msvm_VirtualEthernetSwitchSettingData.Description
- Msvm_VirtualEthernetSwitchSettingData.ElementName
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemType
- Msvm_VirtualEthernetSwitchSettingData.Notes
- Msvm_VirtualEthernetSwitchSettingData.CreationTime
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationID
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationFile
- Msvm_VirtualEthernetSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SuspendDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualEthernetSwitchSettingData.LogDataRoot
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualEthernetSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualEthernetSwitchSettingData.RecoveryFile
- Msvm_VirtualEthernetSwitchSettingData.VLANConnection
- Msvm_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- Msvm_VirtualEthernetSwitchSettingData.MaxNumMACAddress
- Msvm_VirtualEthernetSwitchSettingData.IOVPreferred
- Msvm_VirtualEthernetSwitchSettingData.ExtensionOrder
- Msvm_VirtualEthernetSwitchSettingData.BandwidthReservationMode
- Msvm_VirtualEthernetSwitchSettingData.TeamingEnabled
- Msvm_VirtualEthernetSwitchSettingData.PacketDirectEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3eccbd9dabe853f01c54c78ca651d590afc49f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687260"
---
# <a name="msvm_virtualethernetswitchsettingdata-class"></a><span data-ttu-id="42eb3-103">MSVM \_ VirtualEthernetSwitchSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="42eb3-103">Msvm\_VirtualEthernetSwitchSettingData class</span></span>

<span data-ttu-id="42eb3-104">Representa la configuración actual de un conmutador Ethernet virtual.</span><span class="sxs-lookup"><span data-stu-id="42eb3-104">Represents the current configuration of a virtual Ethernet switch.</span></span>

<span data-ttu-id="42eb3-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="42eb3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="42eb3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42eb3-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingData : CIM_VirtualEthernetSwitchSettingData
{
  string   InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string   Caption = "Virtual Ethernet Switch Settings";
  string   Description = "Active settings for the virtual Ethernet switch";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   VLANConnection[];
  string   AssociatedResourcePool[];
  uint32   MaxNumMACAddress;
  boolean  IOVPreferred = FALSE;
  string   ExtensionOrder[];
  uint32   BandwidthReservationMode = 0;
  boolean  TeamingEnabled = FALSE;
  boolean  PacketDirectEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="42eb3-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="42eb3-107">Members</span></span>

<span data-ttu-id="42eb3-108">La clase **MSVM \_ VirtualEthernetSwitchSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="42eb3-108">The **Msvm\_VirtualEthernetSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="42eb3-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42eb3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42eb3-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42eb3-110">Properties</span></span>

<span data-ttu-id="42eb3-111">La clase **MSVM \_ VirtualEthernetSwitchSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="42eb3-111">The **Msvm\_VirtualEthernetSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42eb3-112">**AssociatedResourcePool**</span><span class="sxs-lookup"><span data-stu-id="42eb3-112">**AssociatedResourcePool**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-113">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="42eb3-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-115">Una lista de grupos de recursos de host que se van a asociar o que están asociados actualmente con el conmutador Ethernet con el fin de asignar conexiones Ethernet entre una máquina virtual y un conmutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="42eb3-115">A list of host resource pools to be associated or that are currently associated with the Ethernet switch for the purpose of the allocation of Ethernet connections between a virtual machine and an Ethernet switch.</span></span> <span data-ttu-id="42eb3-116">Cada valor debe ajustarse al URI de WBEM de producción \_ \_ UntypedInstancePath, tal y como se define en DSP0207.</span><span class="sxs-lookup"><span data-stu-id="42eb3-116">Each value must conform to the production WBEM\_URI\_UntypedInstancePath as defined in DSP0207.</span></span> <span data-ttu-id="42eb3-117">Esta propiedad se hereda de **\_ VirtualEthernetSwitchSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="42eb3-117">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-118">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="42eb3-118">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-119">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42eb3-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-121">Acción que se debe realizar para la máquina virtual cuando se produce un error en el software ejecutado por la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="42eb3-121">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="42eb3-122">Los errores en este caso significan un error que es detectado por la plataforma del host, como una condición de estado de espera no interrumpida.</span><span class="sxs-lookup"><span data-stu-id="42eb3-122">Failures in this case means a failure that is detectable by the host platform, such as a non-interruptible wait state condition.</span></span> <span data-ttu-id="42eb3-123">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="42eb3-123">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-124">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="42eb3-124">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42eb3-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-127">Acción que se realizará para la máquina virtual cuando se apague el host.</span><span class="sxs-lookup"><span data-stu-id="42eb3-127">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="42eb3-128">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="42eb3-128">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-129">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="42eb3-129">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-130">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42eb3-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-132">Acción que se realizará para la máquina virtual cuando se inicie el host.</span><span class="sxs-lookup"><span data-stu-id="42eb3-132">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="42eb3-133">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="42eb3-133">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-134">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="42eb3-134">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-135">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="42eb3-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-137">El tiempo de retardo antes de que la máquina virtual se inicie automáticamente.</span><span class="sxs-lookup"><span data-stu-id="42eb3-137">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="42eb3-138">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="42eb3-138">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-139">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="42eb3-139">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-140">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="42eb3-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-142">Número que indica la secuencia relativa de activación de la máquina virtual cuando se inicia el sistema host.</span><span class="sxs-lookup"><span data-stu-id="42eb3-142">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="42eb3-143">Un número menor indica la activación anterior.</span><span class="sxs-lookup"><span data-stu-id="42eb3-143">A lower number indicates earlier activation.</span></span> <span data-ttu-id="42eb3-144">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="42eb3-144">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-145">**BandwidthReservationMode**</span><span class="sxs-lookup"><span data-stu-id="42eb3-145">**BandwidthReservationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42eb3-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-147">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="42eb3-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-148">Modo de reserva de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="42eb3-148">The bandwidth reservation mode.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="42eb3-149">**Valor predeterminado** (0)</span><span class="sxs-lookup"><span data-stu-id="42eb3-149">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

<span data-ttu-id="42eb3-150">**Peso** (1)</span><span class="sxs-lookup"><span data-stu-id="42eb3-150">**Weight** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

<span data-ttu-id="42eb3-151">**Absolute** (2)</span><span class="sxs-lookup"><span data-stu-id="42eb3-151">**Absolute** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="42eb3-152">**Ninguno** (3)</span><span class="sxs-lookup"><span data-stu-id="42eb3-152">**None** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="42eb3-153">**Caption**</span><span class="sxs-lookup"><span data-stu-id="42eb3-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42eb3-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-156">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="42eb3-156">A short description of the object.</span></span> <span data-ttu-id="42eb3-157">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del conmutador Ethernet virtual".</span><span class="sxs-lookup"><span data-stu-id="42eb3-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Ethernet Switch Settings".</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-158">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="42eb3-158">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42eb3-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-161">La ruta de acceso de un directorio donde se almacena la información sobre la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="42eb3-161">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="42eb3-162">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="42eb3-162">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-163">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="42eb3-163">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42eb3-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-166">La ruta de acceso relativa y el nombre de un archivo donde se almacena la información sobre la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="42eb3-166">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="42eb3-167">Esta ruta de acceso es relativa a la propiedad **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="42eb3-167">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="42eb3-168">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="42eb3-168">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-169">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="42eb3-169">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42eb3-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-172">Identificador único de la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="42eb3-172">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="42eb3-173">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="42eb3-173">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-174">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="42eb3-174">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-175">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="42eb3-175">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-177">Fecha y hora en que se creó la configuración.</span><span class="sxs-lookup"><span data-stu-id="42eb3-177">The date and time at which the settings were created.</span></span> <span data-ttu-id="42eb3-178">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="42eb3-178">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-179">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="42eb3-179">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42eb3-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-182">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="42eb3-182">A description of the object.</span></span> <span data-ttu-id="42eb3-183">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "configuración activa del conmutador Ethernet virtual".</span><span class="sxs-lookup"><span data-stu-id="42eb3-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Active settings for the virtual Ethernet switch".</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-184">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="42eb3-184">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42eb3-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-187">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="42eb3-187">A display name for the object.</span></span> <span data-ttu-id="42eb3-188">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="42eb3-188">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-189">**ExtensionOrder**</span><span class="sxs-lookup"><span data-stu-id="42eb3-189">**ExtensionOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-190">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="42eb3-190">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-191">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="42eb3-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-192">Matriz de instancias incrustadas de la clase [**MSVM \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) que representan las extensiones de conmutador enlazadas a este modificador en el orden en que se aplican.</span><span class="sxs-lookup"><span data-stu-id="42eb3-192">An array of embedded instances of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represent the switch extensions bound to this switch, in the order in which they are applied.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-193">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="42eb3-193">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42eb3-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-196">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="42eb3-196">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-197">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="42eb3-197">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="42eb3-198">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)) y siempre se establece en "Microsoft:*GUID* \\ *DeviceSpecificData*".</span><span class="sxs-lookup"><span data-stu-id="42eb3-198">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-199">**IOVPreferred**</span><span class="sxs-lookup"><span data-stu-id="42eb3-199">**IOVPreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-200">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="42eb3-200">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-201">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="42eb3-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-202">Especifica si la virtualización de e/s de raíz única (SR-IOV) es preferida o no, si está disponible, en el adaptador subyacente.</span><span class="sxs-lookup"><span data-stu-id="42eb3-202">Specifies whether single root IO virtualization (SR-IOV) is preferred or not, if available, on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-203">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="42eb3-203">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-204">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42eb3-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-206">La ruta de acceso de un directorio en el que se almacena la información de registro de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="42eb3-206">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="42eb3-207">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="42eb3-207">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-208">**MaxNumMACAddress**</span><span class="sxs-lookup"><span data-stu-id="42eb3-208">**MaxNumMACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-209">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="42eb3-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-211">Especifica el número máximo de direcciones MAC únicas que puede obtener el conmutador para admitir el aprendizaje de direcciones MAC, tal como se define en el estándar IEEE 802,1.</span><span class="sxs-lookup"><span data-stu-id="42eb3-211">Specifies the maximum number of unique MAC addresses that can be learned by the switch to support MAC Address Learning, as defined in the IEEE 802.1 standard.</span></span> <span data-ttu-id="42eb3-212">Esta propiedad se hereda de **\_ VirtualEthernetSwitchSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="42eb3-212">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-213">**Notas**</span><span class="sxs-lookup"><span data-stu-id="42eb3-213">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-214">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="42eb3-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-216">Notas proporcionadas por el usuario que están relacionadas con la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="42eb3-216">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="42eb3-217">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="42eb3-217">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-218">**PacketDirectEnabled**</span><span class="sxs-lookup"><span data-stu-id="42eb3-218">**PacketDirectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-219">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="42eb3-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-220">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="42eb3-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-221">Especifica si se debe usar PacketDirect, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="42eb3-221">Specifies whether PacketDirect should be used, if available.</span></span> <span data-ttu-id="42eb3-222">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="42eb3-222">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="42eb3-223">Esta propiedad se agregó en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="42eb3-223">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="42eb3-224">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="42eb3-224">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42eb3-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-227">La ruta de acceso completa de un archivo donde se almacena información relacionada con la recuperación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="42eb3-227">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="42eb3-228">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="42eb3-228">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-229">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="42eb3-229">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-230">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42eb3-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-232">La ruta de acceso de un directorio donde se almacena información sobre las instantáneas de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="42eb3-232">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="42eb3-233">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="42eb3-233">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-234">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="42eb3-234">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-235">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42eb3-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-237">La ruta de acceso de un directorio donde se almacena información relacionada con la suspensión de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="42eb3-237">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="42eb3-238">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="42eb3-238">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-239">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="42eb3-239">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-240">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42eb3-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-242">La ruta de acceso de un directorio donde se almacenan los archivos de intercambio de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="42eb3-242">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="42eb3-243">Esta propiedad se hereda de [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85))y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="42eb3-243">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-244">**TeamingEnabled**</span><span class="sxs-lookup"><span data-stu-id="42eb3-244">**TeamingEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-245">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="42eb3-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-246">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="42eb3-246">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-247">Especifica si se debe usar la formación de equipos NIC.</span><span class="sxs-lookup"><span data-stu-id="42eb3-247">Specifies whether NIC Teaming should be used.</span></span> <span data-ttu-id="42eb3-248">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="42eb3-248">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="42eb3-249">Esta propiedad se agregó en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="42eb3-249">This property was added inWindows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="42eb3-250">**Virtualsystemidentifer**</span><span class="sxs-lookup"><span data-stu-id="42eb3-250">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-251">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42eb3-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-253">Nombre del objeto [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) al que pertenecen estos datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="42eb3-253">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="42eb3-254">Esta propiedad es una invalidación de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="42eb3-254">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-255">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="42eb3-255">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-256">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="42eb3-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-258">Especifica el tipo de máquina virtual que representan los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="42eb3-258">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="42eb3-259">Esta propiedad se hereda de la [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="42eb3-259">This property is inherited from the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="42eb3-260">**VLANConnection**</span><span class="sxs-lookup"><span data-stu-id="42eb3-260">**VLANConnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42eb3-261">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="42eb3-261">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="42eb3-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42eb3-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="42eb3-263">Una lista de identificadores de VLAN a los que puede tener acceso este conmutador.</span><span class="sxs-lookup"><span data-stu-id="42eb3-263">A list of VLAN identifiers that this switch can access.</span></span> <span data-ttu-id="42eb3-264">Esta propiedad se hereda de **\_ VirtualEthernetSwitchSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="42eb3-264">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42eb3-265">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42eb3-265">Requirements</span></span>



| <span data-ttu-id="42eb3-266">Requisito</span><span class="sxs-lookup"><span data-stu-id="42eb3-266">Requirement</span></span> | <span data-ttu-id="42eb3-267">Value</span><span class="sxs-lookup"><span data-stu-id="42eb3-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42eb3-268">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42eb3-268">Minimum supported client</span></span><br/> | <span data-ttu-id="42eb3-269">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="42eb3-269">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="42eb3-270">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42eb3-270">Minimum supported server</span></span><br/> | <span data-ttu-id="42eb3-271">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="42eb3-271">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="42eb3-272">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="42eb3-272">Namespace</span></span><br/>                | <span data-ttu-id="42eb3-273">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="42eb3-273">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="42eb3-274">MOF</span><span class="sxs-lookup"><span data-stu-id="42eb3-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42eb3-275"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42eb3-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="42eb3-276">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42eb3-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42eb3-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42eb3-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

