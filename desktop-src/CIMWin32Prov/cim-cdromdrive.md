---
description: La \_ clase CIM CDROMDrive representa una unidad de CD-ROM del equipo.
ms.assetid: 044c9687-fc25-4a8c-b2ef-bd7ea332af7b
ms.tgt_platform: multiple
title: CIM_CDROMDrive (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CDROMDrive
- CIM_CDROMDrive.Caption
- CIM_CDROMDrive.Description
- CIM_CDROMDrive.InstallDate
- CIM_CDROMDrive.Name
- CIM_CDROMDrive.Status
- CIM_CDROMDrive.Availability
- CIM_CDROMDrive.ConfigManagerErrorCode
- CIM_CDROMDrive.ConfigManagerUserConfig
- CIM_CDROMDrive.CreationClassName
- CIM_CDROMDrive.DeviceID
- CIM_CDROMDrive.PowerManagementCapabilities
- CIM_CDROMDrive.ErrorCleared
- CIM_CDROMDrive.ErrorDescription
- CIM_CDROMDrive.LastErrorCode
- CIM_CDROMDrive.PNPDeviceID
- CIM_CDROMDrive.PowerManagementSupported
- CIM_CDROMDrive.StatusInfo
- CIM_CDROMDrive.SystemCreationClassName
- CIM_CDROMDrive.SystemName
- CIM_CDROMDrive.Capabilities
- CIM_CDROMDrive.CapabilityDescriptions
- CIM_CDROMDrive.CompressionMethod
- CIM_CDROMDrive.DefaultBlockSize
- CIM_CDROMDrive.ErrorMethodology
- CIM_CDROMDrive.MaxBlockSize
- CIM_CDROMDrive.MaxMediaSize
- CIM_CDROMDrive.MinBlockSize
- CIM_CDROMDrive.NeedsCleaning
- CIM_CDROMDrive.NumberOfMediaSupported
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 499607e050124533465a40da9e73d433142e6515
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907342"
---
# <a name="cim_cdromdrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="68300-103">CIM_CDROMDrive (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="68300-103">CIM_CDROMDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="68300-104">La clase **CIM \_ CDROMDrive** representa una unidad de CD-ROM del equipo.</span><span class="sxs-lookup"><span data-stu-id="68300-104">The **CIM\_CDROMDrive** class represents a CD-ROM drive on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="68300-105">El nombre de la unidad no se corresponde con la letra de unidad lógica asignada al dispositivo, que es el nombre del dispositivo de almacenamiento lógico que depende de la unidad.</span><span class="sxs-lookup"><span data-stu-id="68300-105">The name of the drive does not correspond to the logical drive letter assigned to the device, which is the name of the logical storage device that is dependent on the drive.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="68300-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="68300-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="68300-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="68300-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="68300-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="68300-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="68300-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="68300-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68300-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68300-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_CDROMDrive : CIM_MediaAccessDevice
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   CompressionMethod;
  uint64   DefaultBlockSize;
  string   ErrorMethodology;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
};
```

## <a name="members"></a><span data-ttu-id="68300-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="68300-111">Members</span></span>

<span data-ttu-id="68300-112">La clase **CIM \_ CDROMDrive** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="68300-112">The **CIM\_CDROMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="68300-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="68300-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="68300-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="68300-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="68300-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="68300-115">Methods</span></span>

<span data-ttu-id="68300-116">La clase **CIM \_ CDROMDrive** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="68300-116">The **CIM\_CDROMDrive** class has these methods.</span></span>



| <span data-ttu-id="68300-117">Método</span><span class="sxs-lookup"><span data-stu-id="68300-117">Method</span></span>                                                                | <span data-ttu-id="68300-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="68300-118">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68300-119">**Reset**</span><span class="sxs-lookup"><span data-stu-id="68300-119">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="68300-120">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="68300-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="68300-121">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="68300-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="68300-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="68300-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="68300-123">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="68300-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="68300-124">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="68300-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="68300-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="68300-125">Properties</span></span>

<span data-ttu-id="68300-126">La clase **CIM \_ CDROMDrive** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="68300-126">The **CIM\_CDROMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68300-127">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="68300-127">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-128">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68300-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68300-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-130">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="68300-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="68300-131">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68300-131">Availability and status of the device.</span></span>

<span data-ttu-id="68300-132">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-132">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="68300-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="68300-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68300-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="68300-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="68300-135"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="68300-135"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="68300-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="68300-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="68300-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="68300-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="68300-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="68300-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="68300-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="68300-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="68300-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="68300-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="68300-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="68300-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="68300-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="68300-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="68300-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="68300-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="68300-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="68300-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="68300-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="68300-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="68300-146">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="68300-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="68300-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="68300-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="68300-148">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="68300-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="68300-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="68300-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="68300-150">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="68300-150">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="68300-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="68300-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="68300-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="68300-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="68300-153">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="68300-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="68300-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="68300-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="68300-155">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="68300-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="68300-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="68300-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="68300-157">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="68300-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="68300-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="68300-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="68300-159">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="68300-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="68300-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="68300-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="68300-161">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="68300-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="68300-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="68300-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-163">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68300-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="68300-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-165">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de almacenamiento DMTF \| 001,9 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,11 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,12 "," MIF. \|Discos DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="68300-165">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="68300-166">Capacidades del dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="68300-166">Capabilities of the media access device.</span></span>

<span data-ttu-id="68300-167">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68300-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="68300-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="68300-169">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="68300-169">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="68300-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="68300-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="68300-171">Otros.</span><span class="sxs-lookup"><span data-stu-id="68300-171">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="68300-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acceso secuencial** (2)</span><span class="sxs-lookup"><span data-stu-id="68300-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="68300-173">Acceso secuencial.</span><span class="sxs-lookup"><span data-stu-id="68300-173">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="68300-174"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acceso aleatorio** (3)</span><span class="sxs-lookup"><span data-stu-id="68300-174"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="68300-175">Acceso aleatorio.</span><span class="sxs-lookup"><span data-stu-id="68300-175">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="68300-176"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Admite escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="68300-176"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="68300-177">Escritura.</span><span class="sxs-lookup"><span data-stu-id="68300-177">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="68300-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Cifrado** (5)</span><span class="sxs-lookup"><span data-stu-id="68300-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="68300-179">Cifrado.</span><span class="sxs-lookup"><span data-stu-id="68300-179">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="68300-180"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compresión** (6)</span><span class="sxs-lookup"><span data-stu-id="68300-180"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="68300-181">Compression.</span><span class="sxs-lookup"><span data-stu-id="68300-181">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="68300-182"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Admite medios** extraíbles (7)</span><span class="sxs-lookup"><span data-stu-id="68300-182"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="68300-183">Medios extraíbles.</span><span class="sxs-lookup"><span data-stu-id="68300-183">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="68300-184"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpieza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="68300-184"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="68300-185">Limpieza manual.</span><span class="sxs-lookup"><span data-stu-id="68300-185">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="68300-186"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpieza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="68300-186"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="68300-187">Limpieza automática.</span><span class="sxs-lookup"><span data-stu-id="68300-187">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="68300-188"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificación inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="68300-188"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="68300-189">Notificación inteligente.</span><span class="sxs-lookup"><span data-stu-id="68300-189">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="68300-190"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Admite medios de doble cara** (11)</span><span class="sxs-lookup"><span data-stu-id="68300-190"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="68300-191">Distingue un dispositivo que puede tener acceso a ambos lados de un medio de dos caras desde un dispositivo que lee solo un lado y requiere que el medio se desactive.</span><span class="sxs-lookup"><span data-stu-id="68300-191">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="68300-192"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT no requerido** (12)</span><span class="sxs-lookup"><span data-stu-id="68300-192"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="68300-193">Indica que el medio no tiene que extraerse explícitamente del dispositivo antes de que un elemento selector tenga acceso a él.</span><span class="sxs-lookup"><span data-stu-id="68300-193">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="68300-194">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="68300-194">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-195">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="68300-195">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="68300-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-197">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="68300-197">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="68300-198">Matriz de cadenas de formato libre que proporciona explicaciones detalladas para las características del dispositivo de acceso indicadas en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="68300-198">Array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="68300-199">Cada entrada de esta matriz está relacionada con la entrada de la matriz de **funciones** , que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="68300-199">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

<span data-ttu-id="68300-200">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-200">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-201">**Caption**</span><span class="sxs-lookup"><span data-stu-id="68300-201">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68300-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68300-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-204">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="68300-204">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="68300-205">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="68300-205">A short textual description of the object.</span></span>

<span data-ttu-id="68300-206">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68300-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-207">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="68300-207">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68300-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68300-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68300-210">Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="68300-210">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="68300-211">Si no es posible describir el esquema de compresión (porque es desconocido), use lo siguiente: si es, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="68300-211">If it is not possible to describe the compression scheme (because it is unknown), use the following:If , use "Unknown".</span></span> <span data-ttu-id="68300-212">Si es, use "Compressed".</span><span class="sxs-lookup"><span data-stu-id="68300-212">If , use "Compressed".</span></span> <span data-ttu-id="68300-213">, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="68300-213">, use "Not Compressed".</span></span>

<span data-ttu-id="68300-214">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-214">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="68300-215">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="68300-215">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="68300-216">El esquema de compresión es desconocido o no se ha descrito.</span><span class="sxs-lookup"><span data-stu-id="68300-216">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="68300-217">("Comprimido")</span><span class="sxs-lookup"><span data-stu-id="68300-217">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="68300-218">El archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito</span><span class="sxs-lookup"><span data-stu-id="68300-218">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="68300-219">("No comprimido")</span><span class="sxs-lookup"><span data-stu-id="68300-219">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="68300-220">Si el archivo lógico no está comprimido</span><span class="sxs-lookup"><span data-stu-id="68300-220">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="68300-221">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="68300-221">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-222">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68300-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68300-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-224">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="68300-224">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="68300-225">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="68300-225">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="68300-226">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-226">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="68300-227">**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="68300-227">**This device is working properly.**</span></span> <span data-ttu-id="68300-228"> (0)</span><span class="sxs-lookup"><span data-stu-id="68300-228">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="68300-229">**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="68300-229">**This device is not configured correctly.**</span></span> <span data-ttu-id="68300-230">(1)</span><span class="sxs-lookup"><span data-stu-id="68300-230">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="68300-231">**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="68300-231">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="68300-232">(2)</span><span class="sxs-lookup"><span data-stu-id="68300-232">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="68300-233">**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="68300-233">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="68300-234">(3)</span><span class="sxs-lookup"><span data-stu-id="68300-234">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="68300-235">**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="68300-235">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="68300-236">(4)</span><span class="sxs-lookup"><span data-stu-id="68300-236">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="68300-237">**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="68300-237">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="68300-238">(5)</span><span class="sxs-lookup"><span data-stu-id="68300-238">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="68300-239">**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="68300-239">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="68300-240"> (6)</span><span class="sxs-lookup"><span data-stu-id="68300-240">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="68300-241">**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="68300-241">**Cannot filter.**</span></span> <span data-ttu-id="68300-242">(7)</span><span class="sxs-lookup"><span data-stu-id="68300-242">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="68300-243">**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="68300-243">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="68300-244">(8)</span><span class="sxs-lookup"><span data-stu-id="68300-244">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="68300-245">**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="68300-245">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="68300-246">(9)</span><span class="sxs-lookup"><span data-stu-id="68300-246">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="68300-247">**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="68300-247">**This device cannot start.**</span></span> <span data-ttu-id="68300-248">(10)</span><span class="sxs-lookup"><span data-stu-id="68300-248">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="68300-249">**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="68300-249">**This device failed.**</span></span> <span data-ttu-id="68300-250">(11)</span><span class="sxs-lookup"><span data-stu-id="68300-250">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="68300-251">**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="68300-251">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="68300-252">(12)</span><span class="sxs-lookup"><span data-stu-id="68300-252">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="68300-253">**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="68300-253">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="68300-254">(13)</span><span class="sxs-lookup"><span data-stu-id="68300-254">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="68300-255">**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="68300-255">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="68300-256">(14)</span><span class="sxs-lookup"><span data-stu-id="68300-256">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="68300-257">**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="68300-257">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="68300-258">(15)</span><span class="sxs-lookup"><span data-stu-id="68300-258">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="68300-259">**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="68300-259">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="68300-260">(16)</span><span class="sxs-lookup"><span data-stu-id="68300-260">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="68300-261">**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="68300-261">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="68300-262">(17)</span><span class="sxs-lookup"><span data-stu-id="68300-262">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="68300-263">**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="68300-263">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="68300-264">(18)</span><span class="sxs-lookup"><span data-stu-id="68300-264">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="68300-265">**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="68300-265">**Failure using the VxD loader.**</span></span> <span data-ttu-id="68300-266">(19)</span><span class="sxs-lookup"><span data-stu-id="68300-266">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="68300-267">**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="68300-267">**Your registry might be corrupted.**</span></span> <span data-ttu-id="68300-268">(20)</span><span class="sxs-lookup"><span data-stu-id="68300-268">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="68300-269">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="68300-269">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="68300-270">(21)</span><span class="sxs-lookup"><span data-stu-id="68300-270">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="68300-271">**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="68300-271">**This device is disabled.**</span></span> <span data-ttu-id="68300-272">(22)</span><span class="sxs-lookup"><span data-stu-id="68300-272">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="68300-273">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="68300-273">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="68300-274">(23)</span><span class="sxs-lookup"><span data-stu-id="68300-274">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="68300-275">**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="68300-275">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="68300-276">(24)</span><span class="sxs-lookup"><span data-stu-id="68300-276">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="68300-277">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="68300-277">**Windows is still setting up this device.**</span></span> <span data-ttu-id="68300-278">(25)</span><span class="sxs-lookup"><span data-stu-id="68300-278">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="68300-279">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="68300-279">**Windows is still setting up this device.**</span></span> <span data-ttu-id="68300-280">(26)</span><span class="sxs-lookup"><span data-stu-id="68300-280">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="68300-281">**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="68300-281">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="68300-282">(27)</span><span class="sxs-lookup"><span data-stu-id="68300-282">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="68300-283">**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="68300-283">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="68300-284">(28)</span><span class="sxs-lookup"><span data-stu-id="68300-284">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="68300-285">**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="68300-285">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="68300-286">(29)</span><span class="sxs-lookup"><span data-stu-id="68300-286">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="68300-287">**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="68300-287">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="68300-288">(30)</span><span class="sxs-lookup"><span data-stu-id="68300-288">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="68300-289">**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="68300-289">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="68300-290">31</span><span class="sxs-lookup"><span data-stu-id="68300-290">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="68300-291">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="68300-291">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-292">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="68300-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68300-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-294">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="68300-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="68300-295">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="68300-295">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="68300-296">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-297">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="68300-297">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-298">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68300-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68300-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-300">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="68300-300">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="68300-301">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="68300-301">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="68300-302">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="68300-302">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="68300-303">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-304">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="68300-304">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-305">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68300-305">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68300-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-307">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="68300-307">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="68300-308">Tamaño de bloque predeterminado, en bytes, para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68300-308">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="68300-309">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="68300-309">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="68300-310">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-310">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-311">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="68300-311">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-312">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68300-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68300-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-314">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="68300-314">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="68300-315">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="68300-315">A textual description of the object.</span></span>

<span data-ttu-id="68300-316">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68300-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-317">**ID**</span><span class="sxs-lookup"><span data-stu-id="68300-317">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-318">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68300-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68300-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-320">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="68300-320">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="68300-321">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="68300-321">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="68300-322">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-323">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="68300-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-324">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="68300-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68300-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68300-326">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="68300-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="68300-327">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-328">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="68300-328">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-329">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68300-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68300-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68300-331">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="68300-331">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="68300-332">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-333">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="68300-333">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-334">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68300-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68300-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68300-336">Cadena de forma libre que describe los tipos de detección y corrección de errores admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68300-336">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="68300-337">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-337">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-338">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="68300-338">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-339">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="68300-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="68300-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-341">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="68300-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="68300-342">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="68300-342">Indicates when the object was installed.</span></span> <span data-ttu-id="68300-343">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="68300-343">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="68300-344">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68300-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-345">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="68300-345">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-346">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68300-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68300-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68300-348">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="68300-348">Last error code reported by the logical device.</span></span>

<span data-ttu-id="68300-349">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-350">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="68300-350">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-351">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68300-351">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68300-352">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-353">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="68300-353">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="68300-354">Tamaño máximo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68300-354">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="68300-355">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="68300-355">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="68300-356">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-356">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-357">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="68300-357">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-358">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68300-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68300-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-360">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acceso secuencial DMTF \| 001,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="68300-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="68300-361">Tamaño máximo, en kilobytes, de los medios admitidos por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68300-361">Maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="68300-362">Los kilobytes se interpretan como el número de bytes multiplicado por 1000 (no por el número de bytes multiplicado por 1024).</span><span class="sxs-lookup"><span data-stu-id="68300-362">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="68300-363">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="68300-363">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="68300-364">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-364">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-365">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="68300-365">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-366">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68300-366">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68300-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-368">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="68300-368">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="68300-369">Tamaño mínimo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68300-369">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="68300-370">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="68300-370">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="68300-371">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-371">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-372">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="68300-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-373">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68300-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68300-374">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-375">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="68300-375">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="68300-376">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="68300-376">Label by which the object is known.</span></span> <span data-ttu-id="68300-377">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="68300-377">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="68300-378">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68300-378">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-379">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="68300-379">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-380">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="68300-380">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68300-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68300-382">Si **es true**, el dispositivo de acceso a medios necesita limpieza.</span><span class="sxs-lookup"><span data-stu-id="68300-382">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="68300-383">Si la limpieza manual o automática es posible, se indica en la propiedad array de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="68300-383">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="68300-384">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-384">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-385">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="68300-385">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-386">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68300-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68300-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68300-388">Número máximo de medios individuales que se pueden admitir o insertar.</span><span class="sxs-lookup"><span data-stu-id="68300-388">Maximum number of multiple individual media that can be supported or inserted.</span></span>

<span data-ttu-id="68300-389">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-390">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="68300-390">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-391">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68300-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68300-392">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-393">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="68300-393">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="68300-394">Indica el identificador de dispositivo Plug and Play Win32 del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="68300-394">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="68300-395">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="68300-395">Example: "\*PNP030b"</span></span>

<span data-ttu-id="68300-396">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-397">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="68300-397">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-398">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68300-398">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="68300-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68300-400">Indica las capacidades de energía específicas relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="68300-400">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="68300-401">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-401">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68300-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="68300-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="68300-403">Las capacidades relacionadas con la energía son desconocidas.</span><span class="sxs-lookup"><span data-stu-id="68300-403">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="68300-404"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="68300-404"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="68300-405">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68300-405">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="68300-406"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="68300-406"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="68300-407">Se han deshabilitado las capacidades relacionadas con la energía.</span><span class="sxs-lookup"><span data-stu-id="68300-407">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="68300-408"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="68300-408"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="68300-409">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="68300-409">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="68300-410"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="68300-410"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="68300-411">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="68300-411">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="68300-412"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="68300-412"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="68300-413">Se admite el método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="68300-413">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="68300-414">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="68300-414">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="68300-415">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="68300-415">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="68300-416"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="68300-416"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="68300-417">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="68300-417">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="68300-418"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="68300-418"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="68300-419">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o Interval, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="68300-419">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="68300-420">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="68300-420">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-421">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="68300-421">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68300-422">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68300-423">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="68300-423">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="68300-424">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="68300-424">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="68300-425">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="68300-425">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="68300-426">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="68300-426">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="68300-427">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-428">**Estado**</span><span class="sxs-lookup"><span data-stu-id="68300-428">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-429">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68300-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68300-430">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-431">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="68300-431">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="68300-432">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="68300-432">String that indicates the current status of the object.</span></span> <span data-ttu-id="68300-433">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="68300-433">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="68300-434">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="68300-434">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="68300-435">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="68300-435">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="68300-436">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="68300-436">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="68300-437">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="68300-437">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="68300-438">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="68300-438">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="68300-439">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68300-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="68300-440">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="68300-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="68300-441">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="68300-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="68300-442">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="68300-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="68300-443">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="68300-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68300-444">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="68300-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="68300-445">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="68300-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="68300-446">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="68300-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="68300-447">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="68300-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="68300-448">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="68300-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="68300-449">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="68300-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="68300-450">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="68300-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="68300-451">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="68300-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="68300-452">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="68300-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="68300-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="68300-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-454">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68300-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68300-455">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-456">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="68300-456">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="68300-457">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="68300-457">State of the logical device.</span></span> <span data-ttu-id="68300-458">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="68300-458">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="68300-459">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="68300-460">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="68300-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68300-461">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="68300-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="68300-462">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="68300-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="68300-463">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="68300-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="68300-464">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="68300-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="68300-465">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="68300-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-466">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68300-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68300-467">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-468">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="68300-468">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="68300-469">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="68300-469">The scoping system's creation class name.</span></span>

<span data-ttu-id="68300-470">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="68300-471">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="68300-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68300-472">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68300-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68300-473">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="68300-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68300-474">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="68300-474">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="68300-475">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="68300-475">The scoping system's name.</span></span>

<span data-ttu-id="68300-476">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68300-477">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68300-477">Remarks</span></span>

<span data-ttu-id="68300-478">La clase **CIM \_ CDROMDrive** se deriva de [**\_ MediaAccessDevice de CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="68300-478">The **CIM\_CDROMDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="68300-479">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="68300-479">WMI does not implement this class.</span></span> <span data-ttu-id="68300-480">Para obtener más información sobre las clases derivadas de **CIM \_ CDROMDrive**, vea [Win32 classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="68300-480">For more information about classes derived from **CIM\_CDROMDrive**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="68300-481">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="68300-481">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="68300-482">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="68300-482">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="68300-483">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68300-483">Requirements</span></span>



| <span data-ttu-id="68300-484">Requisito</span><span class="sxs-lookup"><span data-stu-id="68300-484">Requirement</span></span> | <span data-ttu-id="68300-485">Value</span><span class="sxs-lookup"><span data-stu-id="68300-485">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68300-486">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68300-486">Minimum supported client</span></span><br/> | <span data-ttu-id="68300-487">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68300-487">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68300-488">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68300-488">Minimum supported server</span></span><br/> | <span data-ttu-id="68300-489">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68300-489">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68300-490">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="68300-490">Namespace</span></span><br/>                | <span data-ttu-id="68300-491">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="68300-491">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68300-492">MOF</span><span class="sxs-lookup"><span data-stu-id="68300-492">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68300-493"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68300-493"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68300-494">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68300-494">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68300-495"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68300-495"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68300-496">Vea también</span><span class="sxs-lookup"><span data-stu-id="68300-496">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68300-497">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="68300-497">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

