---
description: La \_ clase CIM TapeDrive representa una unidad de cinta en el sistema. Las unidades de cinta se distinguen principalmente en que solo se puede tener acceso a ellas de forma secuencial.
ms.assetid: 8b7f2277-e37d-4597-81bb-d3c8d4966a81
ms.tgt_platform: multiple
title: CIM_TapeDrive (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive
- CIM_TapeDrive.Availability
- CIM_TapeDrive.Capabilities
- CIM_TapeDrive.CapabilityDescriptions
- CIM_TapeDrive.Caption
- CIM_TapeDrive.CompressionMethod
- CIM_TapeDrive.ConfigManagerErrorCode
- CIM_TapeDrive.ConfigManagerUserConfig
- CIM_TapeDrive.CreationClassName
- CIM_TapeDrive.DefaultBlockSize
- CIM_TapeDrive.Description
- CIM_TapeDrive.DeviceID
- CIM_TapeDrive.EOTWarningZoneSize
- CIM_TapeDrive.ErrorCleared
- CIM_TapeDrive.ErrorDescription
- CIM_TapeDrive.ErrorMethodology
- CIM_TapeDrive.InstallDate
- CIM_TapeDrive.LastErrorCode
- CIM_TapeDrive.MaxBlockSize
- CIM_TapeDrive.MaxMediaSize
- CIM_TapeDrive.MaxPartitionCount
- CIM_TapeDrive.MinBlockSize
- CIM_TapeDrive.Name
- CIM_TapeDrive.NeedsCleaning
- CIM_TapeDrive.NumberOfMediaSupported
- CIM_TapeDrive.Padding
- CIM_TapeDrive.PNPDeviceID
- CIM_TapeDrive.PowerManagementCapabilities
- CIM_TapeDrive.PowerManagementSupported
- CIM_TapeDrive.Status
- CIM_TapeDrive.StatusInfo
- CIM_TapeDrive.SystemCreationClassName
- CIM_TapeDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 184b855d5989c77292e51e8b477c5392893deccb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907547"
---
# <a name="cim_tapedrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="dd09b-104">CIM_TapeDrive (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="dd09b-104">CIM_TapeDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="dd09b-105">La clase **CIM \_ TapeDrive** representa una unidad de cinta en el sistema.</span><span class="sxs-lookup"><span data-stu-id="dd09b-105">The **CIM\_TapeDrive** class represents a tape drive on the system.</span></span> <span data-ttu-id="dd09b-106">Las unidades de cinta se distinguen principalmente en que solo se puede tener acceso a ellas de forma secuencial.</span><span class="sxs-lookup"><span data-stu-id="dd09b-106">Tape drives are primarily distinguished in that they can only be accessed sequentially.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd09b-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="dd09b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dd09b-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dd09b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dd09b-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="dd09b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dd09b-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="dd09b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd09b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd09b-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_TapeDrive : CIM_MediaAccessDevice
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  uint32   EOTWarningZoneSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint32   MaxPartitionCount;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Padding;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="dd09b-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="dd09b-112">Members</span></span>

<span data-ttu-id="dd09b-113">La clase **CIM \_ TapeDrive** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dd09b-113">The **CIM\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="dd09b-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="dd09b-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="dd09b-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd09b-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dd09b-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="dd09b-116">Methods</span></span>

<span data-ttu-id="dd09b-117">La clase **CIM \_ TapeDrive** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dd09b-117">The **CIM\_TapeDrive** class has these methods.</span></span>



| <span data-ttu-id="dd09b-118">Método</span><span class="sxs-lookup"><span data-stu-id="dd09b-118">Method</span></span>                                                               | <span data-ttu-id="dd09b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd09b-119">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd09b-120">**Reset**</span><span class="sxs-lookup"><span data-stu-id="dd09b-120">**Reset**</span></span>](reset-method-in-class-cim-tapedrive.md)                 | <span data-ttu-id="dd09b-121">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dd09b-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="dd09b-122">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="dd09b-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="dd09b-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="dd09b-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-tapedrive.md) | <span data-ttu-id="dd09b-124">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="dd09b-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="dd09b-125">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="dd09b-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dd09b-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd09b-126">Properties</span></span>

<span data-ttu-id="dd09b-127">La clase **CIM \_ TapeDrive** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dd09b-127">The **CIM\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd09b-128">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="dd09b-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd09b-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-131">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="dd09b-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-132">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-132">Availability and status of the device.</span></span>

<span data-ttu-id="dd09b-133">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dd09b-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="dd09b-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd09b-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="dd09b-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="dd09b-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="dd09b-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="dd09b-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="dd09b-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="dd09b-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="dd09b-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dd09b-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="dd09b-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="dd09b-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="dd09b-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="dd09b-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="dd09b-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="dd09b-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="dd09b-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dd09b-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="dd09b-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="dd09b-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="dd09b-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="dd09b-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="dd09b-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="dd09b-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="dd09b-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-147">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="dd09b-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="dd09b-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="dd09b-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-149">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="dd09b-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="dd09b-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="dd09b-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-151">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="dd09b-151">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="dd09b-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="dd09b-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="dd09b-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="dd09b-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-154">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="dd09b-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="dd09b-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="dd09b-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-156">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="dd09b-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="dd09b-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="dd09b-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-158">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="dd09b-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="dd09b-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-160">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="dd09b-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="dd09b-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="dd09b-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-162">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="dd09b-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dd09b-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="dd09b-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-164">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd09b-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-166">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de almacenamiento DMTF \| 001,9 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,11 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,12 "," MIF. \|Discos DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="dd09b-166">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-167">Capacidades del dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="dd09b-167">Capabilities of the media access device.</span></span> <span data-ttu-id="dd09b-168">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-168">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd09b-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="dd09b-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-170">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="dd09b-170">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dd09b-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="dd09b-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-172">Otros.</span><span class="sxs-lookup"><span data-stu-id="dd09b-172">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="dd09b-173"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acceso secuencial** (2)</span><span class="sxs-lookup"><span data-stu-id="dd09b-173"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-174">Acceso secuencial.</span><span class="sxs-lookup"><span data-stu-id="dd09b-174">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="dd09b-175"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acceso aleatorio** (3)</span><span class="sxs-lookup"><span data-stu-id="dd09b-175"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-176">Acceso aleatorio.</span><span class="sxs-lookup"><span data-stu-id="dd09b-176">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="dd09b-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Admite escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="dd09b-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-178">Escritura.</span><span class="sxs-lookup"><span data-stu-id="dd09b-178">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="dd09b-179"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Cifrado** (5)</span><span class="sxs-lookup"><span data-stu-id="dd09b-179"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-180">Cifrado.</span><span class="sxs-lookup"><span data-stu-id="dd09b-180">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="dd09b-181"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compresión** (6)</span><span class="sxs-lookup"><span data-stu-id="dd09b-181"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-182">Compression.</span><span class="sxs-lookup"><span data-stu-id="dd09b-182">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="dd09b-183"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Admite medios** extraíbles (7)</span><span class="sxs-lookup"><span data-stu-id="dd09b-183"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-184">Medios extraíbles.</span><span class="sxs-lookup"><span data-stu-id="dd09b-184">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="dd09b-185"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpieza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="dd09b-185"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-186">Limpieza manual.</span><span class="sxs-lookup"><span data-stu-id="dd09b-186">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="dd09b-187"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpieza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="dd09b-187"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-188">Limpieza automática.</span><span class="sxs-lookup"><span data-stu-id="dd09b-188">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="dd09b-189"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificación inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="dd09b-189"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-190">Notificación inteligente.</span><span class="sxs-lookup"><span data-stu-id="dd09b-190">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="dd09b-191"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Admite medios de doble cara** (11)</span><span class="sxs-lookup"><span data-stu-id="dd09b-191"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-192">Distingue un dispositivo que puede tener acceso a ambos lados de un medio de dos caras desde un dispositivo que lee solo un lado y requiere que el medio se desactive.</span><span class="sxs-lookup"><span data-stu-id="dd09b-192">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="dd09b-193"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT no requerido** (12)</span><span class="sxs-lookup"><span data-stu-id="dd09b-193"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-194">Indica que el medio no tiene que extraerse explícitamente del dispositivo antes de que un elemento selector tenga acceso a él.</span><span class="sxs-lookup"><span data-stu-id="dd09b-194">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dd09b-195">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="dd09b-195">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-196">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="dd09b-196">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-198">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="dd09b-198">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-199">Cadenas de forma libre que proporcionan explicaciones detalladas para las características del dispositivo de acceso indicadas en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="dd09b-199">Free-form strings that provide detailed explanations for the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="dd09b-200">Tenga en cuenta que cada entrada de esta matriz está relacionada con la entrada de la matriz de **capacidades** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="dd09b-200">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="dd09b-201">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-201">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-202">**Caption**</span><span class="sxs-lookup"><span data-stu-id="dd09b-202">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd09b-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-205">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="dd09b-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-206">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="dd09b-206">Short textual description of the object.</span></span>

<span data-ttu-id="dd09b-207">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-207">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-208">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="dd09b-208">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-209">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd09b-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-211">Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dd09b-211">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="dd09b-212">Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="dd09b-212">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="dd09b-213">Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido".</span><span class="sxs-lookup"><span data-stu-id="dd09b-213">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="dd09b-214">Si el archivo lógico no está comprimido, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="dd09b-214">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="dd09b-215">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-215">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="dd09b-216">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="dd09b-216">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-217">El esquema de compresión es desconocido o no se ha descrito.</span><span class="sxs-lookup"><span data-stu-id="dd09b-217">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="dd09b-218">("Comprimido")</span><span class="sxs-lookup"><span data-stu-id="dd09b-218">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-219">El archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito</span><span class="sxs-lookup"><span data-stu-id="dd09b-219">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="dd09b-220">("No comprimido")</span><span class="sxs-lookup"><span data-stu-id="dd09b-220">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-221">Si el archivo lógico no está comprimido</span><span class="sxs-lookup"><span data-stu-id="dd09b-221">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dd09b-222">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="dd09b-222">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-223">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd09b-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-225">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dd09b-225">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-226">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="dd09b-226">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="dd09b-227">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-227">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="dd09b-228"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-228"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="dd09b-229"> (0)</span><span class="sxs-lookup"><span data-stu-id="dd09b-229">(0)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-230">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="dd09b-230">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="dd09b-231"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-231"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="dd09b-232">(1)</span><span class="sxs-lookup"><span data-stu-id="dd09b-232">(1)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-233">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="dd09b-233">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dd09b-234"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-234"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="dd09b-235">(2)</span><span class="sxs-lookup"><span data-stu-id="dd09b-235">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="dd09b-236"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-236"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="dd09b-237">(3)</span><span class="sxs-lookup"><span data-stu-id="dd09b-237">(3)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-238">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="dd09b-238">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dd09b-239"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-239"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="dd09b-240">(4)</span><span class="sxs-lookup"><span data-stu-id="dd09b-240">(4)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-241">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="dd09b-241">Device is not working properly.</span></span> <span data-ttu-id="dd09b-242">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="dd09b-242">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="dd09b-243"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-243"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="dd09b-244">(5)</span><span class="sxs-lookup"><span data-stu-id="dd09b-244">(5)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-245">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="dd09b-245">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="dd09b-246"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-246"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="dd09b-247"> (6)</span><span class="sxs-lookup"><span data-stu-id="dd09b-247">(6)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-248">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="dd09b-248">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="dd09b-249"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-249"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="dd09b-250">(7)</span><span class="sxs-lookup"><span data-stu-id="dd09b-250">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="dd09b-251"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-251"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="dd09b-252">(8)</span><span class="sxs-lookup"><span data-stu-id="dd09b-252">(8)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-253">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-253">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="dd09b-254"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-254"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="dd09b-255">(9)</span><span class="sxs-lookup"><span data-stu-id="dd09b-255">(9)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-256">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="dd09b-256">Device is not working properly.</span></span> <span data-ttu-id="dd09b-257">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-257">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="dd09b-258"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-258"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="dd09b-259">(10)</span><span class="sxs-lookup"><span data-stu-id="dd09b-259">(10)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-260">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="dd09b-260">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="dd09b-261"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-261"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="dd09b-262">(11)</span><span class="sxs-lookup"><span data-stu-id="dd09b-262">(11)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-263">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-263">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="dd09b-264"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-264"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="dd09b-265">(12)</span><span class="sxs-lookup"><span data-stu-id="dd09b-265">(12)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-266">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="dd09b-266">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="dd09b-267"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-267"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="dd09b-268">(13)</span><span class="sxs-lookup"><span data-stu-id="dd09b-268">(13)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-269">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-269">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="dd09b-270"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-270"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="dd09b-271">(14)</span><span class="sxs-lookup"><span data-stu-id="dd09b-271">(14)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-272">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-272">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="dd09b-273"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-273"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="dd09b-274">(15)</span><span class="sxs-lookup"><span data-stu-id="dd09b-274">(15)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-275">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="dd09b-275">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="dd09b-276"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-276"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="dd09b-277">(16)</span><span class="sxs-lookup"><span data-stu-id="dd09b-277">(16)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-278">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-278">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="dd09b-279"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-279"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="dd09b-280">(17)</span><span class="sxs-lookup"><span data-stu-id="dd09b-280">(17)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-281">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="dd09b-281">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dd09b-282"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-282"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="dd09b-283">(18)</span><span class="sxs-lookup"><span data-stu-id="dd09b-283">(18)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-284">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="dd09b-284">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="dd09b-285"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-285"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="dd09b-286">(19)</span><span class="sxs-lookup"><span data-stu-id="dd09b-286">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dd09b-287"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-287"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="dd09b-288">(20)</span><span class="sxs-lookup"><span data-stu-id="dd09b-288">(20)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-289">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="dd09b-289">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="dd09b-290"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-290"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="dd09b-291">(21)</span><span class="sxs-lookup"><span data-stu-id="dd09b-291">(21)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-292">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="dd09b-292">System failure.</span></span> <span data-ttu-id="dd09b-293">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="dd09b-293">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="dd09b-294">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-294">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="dd09b-295"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-295"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="dd09b-296">(22)</span><span class="sxs-lookup"><span data-stu-id="dd09b-296">(22)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-297">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="dd09b-297">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="dd09b-298"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-298"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="dd09b-299">(23)</span><span class="sxs-lookup"><span data-stu-id="dd09b-299">(23)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-300">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="dd09b-300">System failure.</span></span> <span data-ttu-id="dd09b-301">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="dd09b-301">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="dd09b-302"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-302"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="dd09b-303">(24)</span><span class="sxs-lookup"><span data-stu-id="dd09b-303">(24)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-304">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="dd09b-304">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dd09b-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dd09b-306">(25)</span><span class="sxs-lookup"><span data-stu-id="dd09b-306">(25)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-307">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dd09b-308"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-308"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dd09b-309">(26)</span><span class="sxs-lookup"><span data-stu-id="dd09b-309">(26)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-310">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-310">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="dd09b-311"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-311"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="dd09b-312">(27)</span><span class="sxs-lookup"><span data-stu-id="dd09b-312">(27)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-313">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="dd09b-313">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="dd09b-314"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-314"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="dd09b-315">(28)</span><span class="sxs-lookup"><span data-stu-id="dd09b-315">(28)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-316">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="dd09b-316">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="dd09b-317"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-317"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="dd09b-318">(29)</span><span class="sxs-lookup"><span data-stu-id="dd09b-318">(29)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-319">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="dd09b-319">Device is disabled.</span></span> <span data-ttu-id="dd09b-320">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="dd09b-320">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="dd09b-321"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-321"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="dd09b-322">(30)</span><span class="sxs-lookup"><span data-stu-id="dd09b-322">(30)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-323">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="dd09b-323">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dd09b-324"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="dd09b-324"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="dd09b-325">31</span><span class="sxs-lookup"><span data-stu-id="dd09b-325">(31)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-326">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="dd09b-326">Device is not working properly.</span></span> <span data-ttu-id="dd09b-327">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="dd09b-327">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dd09b-328">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="dd09b-328">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-329">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dd09b-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-331">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dd09b-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-332">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="dd09b-332">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="dd09b-333">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-333">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-334">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dd09b-334">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-335">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd09b-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-337">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dd09b-337">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-338">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="dd09b-338">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="dd09b-339">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="dd09b-339">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="dd09b-340">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-341">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="dd09b-341">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-342">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dd09b-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-344">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="dd09b-344">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-345">Tamaño de bloque predeterminado, en bytes, para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-345">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="dd09b-346">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-346">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="dd09b-347">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dd09b-347">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-348">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd09b-348">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-349">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd09b-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-351">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="dd09b-351">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-352">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="dd09b-352">Textual description of the object.</span></span>

<span data-ttu-id="dd09b-353">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-353">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-354">**ID**</span><span class="sxs-lookup"><span data-stu-id="dd09b-354">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-355">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd09b-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-357">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dd09b-357">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-358">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dd09b-358">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="dd09b-359">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-360">**EOTWarningZoneSize**</span><span class="sxs-lookup"><span data-stu-id="dd09b-360">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-361">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd09b-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-363">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="dd09b-363">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-364">Tamaño, en bytes, del área designada como final de la cinta.</span><span class="sxs-lookup"><span data-stu-id="dd09b-364">Size, in bytes, of the area designated as end-of-tape.</span></span> <span data-ttu-id="dd09b-365">El acceso en esta área genera una advertencia de final de cinta.</span><span class="sxs-lookup"><span data-stu-id="dd09b-365">Access in this area generates an end-of-tape warning.</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-366">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="dd09b-366">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-367">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dd09b-367">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-369">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="dd09b-369">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="dd09b-370">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-371">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="dd09b-371">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-372">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd09b-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-373">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-374">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="dd09b-374">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="dd09b-375">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-376">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="dd09b-376">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-377">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd09b-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-378">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-379">Cadena de forma libre que describe los tipos de detección y corrección de errores admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-379">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="dd09b-380">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-380">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-381">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dd09b-381">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-382">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dd09b-382">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-384">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="dd09b-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-385">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="dd09b-385">Date and time the object was installed.</span></span> <span data-ttu-id="dd09b-386">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="dd09b-386">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dd09b-387">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-387">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-388">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="dd09b-388">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-389">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd09b-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-391">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dd09b-391">Last error code reported by the logical device.</span></span>

<span data-ttu-id="dd09b-392">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-393">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="dd09b-393">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-394">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dd09b-394">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-395">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-396">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="dd09b-396">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-397">Tamaño máximo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-397">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="dd09b-398">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-398">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="dd09b-399">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dd09b-399">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-400">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="dd09b-400">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-401">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dd09b-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-403">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acceso secuencial DMTF \| 001,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="dd09b-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-404">Tamaño máximo, en kilobytes, de los medios admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-404">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="dd09b-405">Los kilobytes se interpretan como el número de bytes multiplicado por 1000 (no por el número de bytes multiplicado por 1024).</span><span class="sxs-lookup"><span data-stu-id="dd09b-405">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="dd09b-406">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-406">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="dd09b-407">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dd09b-407">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-408">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="dd09b-408">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-409">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd09b-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-411">Recuento máximo de particiones para la unidad de cinta.</span><span class="sxs-lookup"><span data-stu-id="dd09b-411">Maximum partition count for the tape drive.</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-412">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="dd09b-412">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-413">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dd09b-413">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-414">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-415">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="dd09b-415">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-416">Tamaño mínimo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-416">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="dd09b-417">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-417">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="dd09b-418">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dd09b-418">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-419">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="dd09b-419">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-420">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd09b-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-422">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="dd09b-422">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-423">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="dd09b-423">Label by which the object is known.</span></span> <span data-ttu-id="dd09b-424">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="dd09b-424">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="dd09b-425">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-425">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-426">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="dd09b-426">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-427">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dd09b-427">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-428">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-429">Si **es true**, el dispositivo de acceso a medios necesita limpieza.</span><span class="sxs-lookup"><span data-stu-id="dd09b-429">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="dd09b-430">Si la limpieza manual o automática es posible, se indica en la propiedad array de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="dd09b-430">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="dd09b-431">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-431">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-432">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="dd09b-432">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-433">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd09b-433">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-434">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-435">Cuando el dispositivo de acceso a medios admite varios medios individuales, esta propiedad define el número máximo que se puede admitir o insertar.</span><span class="sxs-lookup"><span data-stu-id="dd09b-435">When the media access device supports multiple individual media, this property defines the maximum number which can be supported or inserted.</span></span>

<span data-ttu-id="dd09b-436">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-436">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-437">**Relleno**</span><span class="sxs-lookup"><span data-stu-id="dd09b-437">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-438">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd09b-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-439">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-440">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="dd09b-440">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-441">Número de bytes insertados entre bloques en un medio de cinta.</span><span class="sxs-lookup"><span data-stu-id="dd09b-441">Number of bytes inserted between blocks on a tape media.</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-442">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="dd09b-442">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-443">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd09b-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-444">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-445">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dd09b-445">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-446">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dd09b-446">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="dd09b-447">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="dd09b-448">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="dd09b-448">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-449">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="dd09b-449">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-450">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd09b-450">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-451">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-452">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dd09b-452">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="dd09b-453">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="dd09b-453">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd09b-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="dd09b-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="dd09b-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="dd09b-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-456">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd09b-456">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dd09b-457"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="dd09b-457"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dd09b-458"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="dd09b-458"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-459">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="dd09b-459">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="dd09b-460"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="dd09b-460"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-461">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="dd09b-461">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="dd09b-462"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="dd09b-462"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-463">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="dd09b-463">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="dd09b-464">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="dd09b-464">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="dd09b-465">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="dd09b-465">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="dd09b-466"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="dd09b-466"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-467">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="dd09b-467">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="dd09b-468"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="dd09b-468"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="dd09b-469">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="dd09b-469">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dd09b-470">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="dd09b-470">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-471">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dd09b-471">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-472">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-473">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="dd09b-473">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="dd09b-474">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="dd09b-474">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="dd09b-475">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="dd09b-475">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="dd09b-476">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="dd09b-476">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="dd09b-477">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-478">**Estado**</span><span class="sxs-lookup"><span data-stu-id="dd09b-478">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-479">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd09b-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-480">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-481">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="dd09b-481">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-482">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="dd09b-482">Current status of the object.</span></span> <span data-ttu-id="dd09b-483">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-483">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dd09b-484">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="dd09b-484">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dd09b-485">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="dd09b-485">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dd09b-486">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="dd09b-486">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dd09b-487">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="dd09b-487">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd09b-488">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="dd09b-488">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dd09b-489">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="dd09b-489">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dd09b-490">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="dd09b-490">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dd09b-491">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="dd09b-491">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dd09b-492">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="dd09b-492">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dd09b-493">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="dd09b-493">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dd09b-494">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="dd09b-494">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dd09b-495">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="dd09b-495">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dd09b-496">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="dd09b-496">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd09b-497">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="dd09b-497">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-498">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd09b-498">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-499">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-500">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="dd09b-500">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-501">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="dd09b-501">State of the logical device.</span></span> <span data-ttu-id="dd09b-502">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="dd09b-502">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="dd09b-503">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dd09b-504">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="dd09b-504">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd09b-505">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="dd09b-505">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dd09b-506">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="dd09b-506">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dd09b-507">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="dd09b-507">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dd09b-508">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="dd09b-508">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd09b-509">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dd09b-509">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-510">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd09b-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-511">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-512">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dd09b-512">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-513">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="dd09b-513">Scoping system's creation class name.</span></span>

<span data-ttu-id="dd09b-514">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-514">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd09b-515">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dd09b-515">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd09b-516">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd09b-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-517">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd09b-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd09b-518">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dd09b-518">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dd09b-519">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="dd09b-519">Scoping system's name.</span></span>

<span data-ttu-id="dd09b-520">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-520">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd09b-521">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd09b-521">Remarks</span></span>

<span data-ttu-id="dd09b-522">La clase **CIM \_ TapeDrive** se deriva de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-522">The **CIM\_TapeDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="dd09b-523">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="dd09b-523">WMI does not implement this class.</span></span> <span data-ttu-id="dd09b-524">Para las clases WMI derivadas de **CIM \_ TapeDrive**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="dd09b-524">For WMI classes derived from **CIM\_TapeDrive**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="dd09b-525">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="dd09b-525">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dd09b-526">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="dd09b-526">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd09b-527">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd09b-527">Requirements</span></span>



| <span data-ttu-id="dd09b-528">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd09b-528">Requirement</span></span> | <span data-ttu-id="dd09b-529">Value</span><span class="sxs-lookup"><span data-stu-id="dd09b-529">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd09b-530">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd09b-530">Minimum supported client</span></span><br/> | <span data-ttu-id="dd09b-531">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd09b-531">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd09b-532">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd09b-532">Minimum supported server</span></span><br/> | <span data-ttu-id="dd09b-533">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd09b-533">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd09b-534">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dd09b-534">Namespace</span></span><br/>                | <span data-ttu-id="dd09b-535">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dd09b-535">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dd09b-536">MOF</span><span class="sxs-lookup"><span data-stu-id="dd09b-536">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd09b-537"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd09b-537"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd09b-538">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dd09b-538">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd09b-539"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd09b-539"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd09b-540">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd09b-540">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd09b-541">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="dd09b-541">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

