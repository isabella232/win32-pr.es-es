---
description: La \_ clase CIM MagnetoOpticalDrive representa las capacidades y la administración de una unidad magneto-óptica, un subtipo del dispositivo de acceso a medios.
ms.assetid: 82a4604d-3bef-4378-812b-550849e30b8c
ms.tgt_platform: multiple
title: CIM_MagnetoOpticalDrive (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MagnetoOpticalDrive
- CIM_MagnetoOpticalDrive.Availability
- CIM_MagnetoOpticalDrive.Capabilities
- CIM_MagnetoOpticalDrive.CapabilityDescriptions
- CIM_MagnetoOpticalDrive.Caption
- CIM_MagnetoOpticalDrive.CompressionMethod
- CIM_MagnetoOpticalDrive.ConfigManagerErrorCode
- CIM_MagnetoOpticalDrive.ConfigManagerUserConfig
- CIM_MagnetoOpticalDrive.CreationClassName
- CIM_MagnetoOpticalDrive.DefaultBlockSize
- CIM_MagnetoOpticalDrive.Description
- CIM_MagnetoOpticalDrive.DeviceID
- CIM_MagnetoOpticalDrive.ErrorCleared
- CIM_MagnetoOpticalDrive.ErrorDescription
- CIM_MagnetoOpticalDrive.ErrorMethodology
- CIM_MagnetoOpticalDrive.InstallDate
- CIM_MagnetoOpticalDrive.LastErrorCode
- CIM_MagnetoOpticalDrive.MaxBlockSize
- CIM_MagnetoOpticalDrive.MaxMediaSize
- CIM_MagnetoOpticalDrive.MinBlockSize
- CIM_MagnetoOpticalDrive.Name
- CIM_MagnetoOpticalDrive.NeedsCleaning
- CIM_MagnetoOpticalDrive.NumberOfMediaSupported
- CIM_MagnetoOpticalDrive.PNPDeviceID
- CIM_MagnetoOpticalDrive.PowerManagementCapabilities
- CIM_MagnetoOpticalDrive.PowerManagementSupported
- CIM_MagnetoOpticalDrive.Status
- CIM_MagnetoOpticalDrive.StatusInfo
- CIM_MagnetoOpticalDrive.SystemCreationClassName
- CIM_MagnetoOpticalDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: abc5acdf25a2920fa53c6315109264180b6e7c23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496277"
---
# <a name="cim_magnetoopticaldrive-class"></a><span data-ttu-id="036d9-103">\_Clase MagnetoOpticalDrive de CIM</span><span class="sxs-lookup"><span data-stu-id="036d9-103">CIM\_MagnetoOpticalDrive class</span></span>

<span data-ttu-id="036d9-104">La clase **CIM \_ MagnetoOpticalDrive** representa las capacidades y la administración de una unidad magneto-óptica, un subtipo del dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="036d9-104">The **CIM\_MagnetoOpticalDrive** class represents the capabilities and management of a magneto-optical drive, a subtype of the media access device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="036d9-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="036d9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="036d9-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="036d9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="036d9-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="036d9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="036d9-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="036d9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="036d9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="036d9-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{F62037D8-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_MagnetoOpticalDrive : CIM_MediaAccessDevice
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
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="036d9-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="036d9-110">Members</span></span>

<span data-ttu-id="036d9-111">La clase **CIM \_ MagnetoOpticalDrive** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="036d9-111">The **CIM\_MagnetoOpticalDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="036d9-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="036d9-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="036d9-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="036d9-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="036d9-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="036d9-114">Methods</span></span>

<span data-ttu-id="036d9-115">La clase **CIM \_ MagnetoOpticalDrive** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="036d9-115">The **CIM\_MagnetoOpticalDrive** class has these methods.</span></span>



| <span data-ttu-id="036d9-116">Método</span><span class="sxs-lookup"><span data-stu-id="036d9-116">Method</span></span>                                                                         | <span data-ttu-id="036d9-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="036d9-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="036d9-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="036d9-118">**Reset**</span></span>](reset-method-in-class-cim-magnetoopticaldrive.md)                 | <span data-ttu-id="036d9-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="036d9-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="036d9-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="036d9-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="036d9-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="036d9-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-magnetoopticaldrive.md) | <span data-ttu-id="036d9-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="036d9-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="036d9-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="036d9-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="036d9-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="036d9-124">Properties</span></span>

<span data-ttu-id="036d9-125">La clase **CIM \_ MagnetoOpticalDrive** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="036d9-125">The **CIM\_MagnetoOpticalDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="036d9-126">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="036d9-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="036d9-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-129">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="036d9-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="036d9-130">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="036d9-130">Availability and status of the device.</span></span>

<span data-ttu-id="036d9-131">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="036d9-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="036d9-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="036d9-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="036d9-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="036d9-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="036d9-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="036d9-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="036d9-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="036d9-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="036d9-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="036d9-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="036d9-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="036d9-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="036d9-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="036d9-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="036d9-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="036d9-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="036d9-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="036d9-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="036d9-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="036d9-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="036d9-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="036d9-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="036d9-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="036d9-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="036d9-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-145">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="036d9-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="036d9-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="036d9-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-147">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="036d9-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="036d9-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="036d9-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-149">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="036d9-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="036d9-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="036d9-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="036d9-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="036d9-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-152">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="036d9-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="036d9-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="036d9-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-154">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="036d9-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="036d9-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="036d9-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-156">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="036d9-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="036d9-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="036d9-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-158">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="036d9-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="036d9-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="036d9-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-160">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="036d9-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="036d9-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="036d9-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-162">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="036d9-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="036d9-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-164">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de almacenamiento DMTF \| 001,9 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,11 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,12 "," MIF. \|Discos DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="036d9-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="036d9-165">Capacidades del dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="036d9-165">Capabilities of the media access device.</span></span>

<span data-ttu-id="036d9-166">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-166">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="036d9-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="036d9-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-168">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="036d9-168">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="036d9-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="036d9-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-170">Otros.</span><span class="sxs-lookup"><span data-stu-id="036d9-170">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="036d9-171"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acceso secuencial** (2)</span><span class="sxs-lookup"><span data-stu-id="036d9-171"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-172">Acceso secuencial.</span><span class="sxs-lookup"><span data-stu-id="036d9-172">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="036d9-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acceso aleatorio** (3)</span><span class="sxs-lookup"><span data-stu-id="036d9-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-174">Acceso aleatorio.</span><span class="sxs-lookup"><span data-stu-id="036d9-174">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="036d9-175"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Admite escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="036d9-175"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-176">Escritura.</span><span class="sxs-lookup"><span data-stu-id="036d9-176">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="036d9-177"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Cifrado** (5)</span><span class="sxs-lookup"><span data-stu-id="036d9-177"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-178">Cifrado.</span><span class="sxs-lookup"><span data-stu-id="036d9-178">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="036d9-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compresión** (6)</span><span class="sxs-lookup"><span data-stu-id="036d9-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-180">Compression.</span><span class="sxs-lookup"><span data-stu-id="036d9-180">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="036d9-181"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Admite medios** extraíbles (7)</span><span class="sxs-lookup"><span data-stu-id="036d9-181"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-182">Medios extraíbles.</span><span class="sxs-lookup"><span data-stu-id="036d9-182">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="036d9-183"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpieza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="036d9-183"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-184">Limpieza manual.</span><span class="sxs-lookup"><span data-stu-id="036d9-184">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="036d9-185"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpieza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="036d9-185"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-186">Limpieza automática.</span><span class="sxs-lookup"><span data-stu-id="036d9-186">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="036d9-187"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificación inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="036d9-187"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-188">Notificación inteligente.</span><span class="sxs-lookup"><span data-stu-id="036d9-188">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="036d9-189"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Admite medios de doble cara** (11)</span><span class="sxs-lookup"><span data-stu-id="036d9-189"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-190">Distingue un dispositivo que puede tener acceso a ambos lados de un medio de dos caras desde un dispositivo que lee solo un lado y requiere que el medio se desactive.</span><span class="sxs-lookup"><span data-stu-id="036d9-190">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="036d9-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT no requerido** (12)</span><span class="sxs-lookup"><span data-stu-id="036d9-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-192">Indica que el medio no tiene que extraerse explícitamente del dispositivo antes de que un elemento selector tenga acceso a él.</span><span class="sxs-lookup"><span data-stu-id="036d9-192">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="036d9-193">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="036d9-193">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-194">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="036d9-194">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="036d9-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-196">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="036d9-196">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="036d9-197">Matriz de cadenas de formato libre que proporciona explicaciones detalladas para las características del dispositivo de acceso indicadas en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="036d9-197">Array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="036d9-198">Cada entrada de la matriz está relacionada con la entrada de la matriz de **funciones** , que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="036d9-198">Each array entry is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

<span data-ttu-id="036d9-199">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-199">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-200">**Caption**</span><span class="sxs-lookup"><span data-stu-id="036d9-200">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="036d9-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-203">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="036d9-203">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="036d9-204">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="036d9-204">Short textual description of the object.</span></span>

<span data-ttu-id="036d9-205">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-205">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-206">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="036d9-206">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="036d9-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="036d9-209">Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="036d9-209">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="036d9-210">Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="036d9-210">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="036d9-211">Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido".</span><span class="sxs-lookup"><span data-stu-id="036d9-211">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="036d9-212">Si el archivo lógico no está comprimido, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="036d9-212">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="036d9-213">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-213">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="036d9-214">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="036d9-214">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="036d9-215">El esquema de compresión es desconocido o no se ha descrito.</span><span class="sxs-lookup"><span data-stu-id="036d9-215">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="036d9-216">("Comprimido")</span><span class="sxs-lookup"><span data-stu-id="036d9-216">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="036d9-217">El archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito</span><span class="sxs-lookup"><span data-stu-id="036d9-217">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="036d9-218">("No comprimido")</span><span class="sxs-lookup"><span data-stu-id="036d9-218">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="036d9-219">Si el archivo lógico no está comprimido</span><span class="sxs-lookup"><span data-stu-id="036d9-219">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="036d9-220">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="036d9-220">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-221">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="036d9-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-223">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="036d9-223">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="036d9-224">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="036d9-224">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="036d9-225">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-225">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="036d9-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="036d9-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="036d9-227"> (0)</span><span class="sxs-lookup"><span data-stu-id="036d9-227">(0)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-228">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="036d9-228">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="036d9-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="036d9-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="036d9-230">(1)</span><span class="sxs-lookup"><span data-stu-id="036d9-230">(1)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-231">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="036d9-231">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="036d9-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="036d9-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="036d9-233">(2)</span><span class="sxs-lookup"><span data-stu-id="036d9-233">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="036d9-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="036d9-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="036d9-235">(3)</span><span class="sxs-lookup"><span data-stu-id="036d9-235">(3)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-236">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="036d9-236">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="036d9-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="036d9-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="036d9-238">(4)</span><span class="sxs-lookup"><span data-stu-id="036d9-238">(4)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-239">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="036d9-239">Device is not working properly.</span></span> <span data-ttu-id="036d9-240">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="036d9-240">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="036d9-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="036d9-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="036d9-242">(5)</span><span class="sxs-lookup"><span data-stu-id="036d9-242">(5)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-243">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="036d9-243">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="036d9-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="036d9-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="036d9-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="036d9-245">(6)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-246">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="036d9-246">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="036d9-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="036d9-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="036d9-248">(7)</span><span class="sxs-lookup"><span data-stu-id="036d9-248">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="036d9-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="036d9-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="036d9-250">(8)</span><span class="sxs-lookup"><span data-stu-id="036d9-250">(8)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-251">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="036d9-251">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="036d9-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="036d9-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="036d9-253">(9)</span><span class="sxs-lookup"><span data-stu-id="036d9-253">(9)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-254">El dispositivo no funciona correctamente. el firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="036d9-254">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="036d9-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="036d9-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="036d9-256">(10)</span><span class="sxs-lookup"><span data-stu-id="036d9-256">(10)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-257">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="036d9-257">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="036d9-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="036d9-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="036d9-259">(11)</span><span class="sxs-lookup"><span data-stu-id="036d9-259">(11)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-260">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="036d9-260">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="036d9-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="036d9-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="036d9-262">(12)</span><span class="sxs-lookup"><span data-stu-id="036d9-262">(12)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-263">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="036d9-263">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="036d9-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="036d9-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="036d9-265">(13)</span><span class="sxs-lookup"><span data-stu-id="036d9-265">(13)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-266">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="036d9-266">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="036d9-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="036d9-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="036d9-268">(14)</span><span class="sxs-lookup"><span data-stu-id="036d9-268">(14)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-269">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="036d9-269">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="036d9-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="036d9-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="036d9-271">(15)</span><span class="sxs-lookup"><span data-stu-id="036d9-271">(15)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-272">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="036d9-272">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="036d9-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="036d9-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="036d9-274">(16)</span><span class="sxs-lookup"><span data-stu-id="036d9-274">(16)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-275">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="036d9-275">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="036d9-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="036d9-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="036d9-277">(17)</span><span class="sxs-lookup"><span data-stu-id="036d9-277">(17)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-278">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="036d9-278">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="036d9-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="036d9-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="036d9-280">(18)</span><span class="sxs-lookup"><span data-stu-id="036d9-280">(18)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-281">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="036d9-281">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="036d9-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="036d9-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="036d9-283">(19)</span><span class="sxs-lookup"><span data-stu-id="036d9-283">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="036d9-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="036d9-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="036d9-285">(20)</span><span class="sxs-lookup"><span data-stu-id="036d9-285">(20)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-286">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="036d9-286">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="036d9-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="036d9-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="036d9-288">(21)</span><span class="sxs-lookup"><span data-stu-id="036d9-288">(21)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-289">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="036d9-289">System failure.</span></span> <span data-ttu-id="036d9-290">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="036d9-290">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="036d9-291">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="036d9-291">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="036d9-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="036d9-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="036d9-293">(22)</span><span class="sxs-lookup"><span data-stu-id="036d9-293">(22)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-294">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="036d9-294">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="036d9-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="036d9-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="036d9-296">(23)</span><span class="sxs-lookup"><span data-stu-id="036d9-296">(23)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-297">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="036d9-297">System failure.</span></span> <span data-ttu-id="036d9-298">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="036d9-298">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="036d9-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="036d9-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="036d9-300">(24)</span><span class="sxs-lookup"><span data-stu-id="036d9-300">(24)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-301">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="036d9-301">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="036d9-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="036d9-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="036d9-303">(25)</span><span class="sxs-lookup"><span data-stu-id="036d9-303">(25)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-304">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="036d9-304">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="036d9-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="036d9-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="036d9-306">(26)</span><span class="sxs-lookup"><span data-stu-id="036d9-306">(26)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-307">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="036d9-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="036d9-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="036d9-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="036d9-309">(27)</span><span class="sxs-lookup"><span data-stu-id="036d9-309">(27)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-310">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="036d9-310">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="036d9-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="036d9-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="036d9-312">(28)</span><span class="sxs-lookup"><span data-stu-id="036d9-312">(28)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-313">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="036d9-313">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="036d9-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="036d9-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="036d9-315">(29)</span><span class="sxs-lookup"><span data-stu-id="036d9-315">(29)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-316">El dispositivo está deshabilitado; el firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="036d9-316">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="036d9-317"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="036d9-317"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="036d9-318">(30)</span><span class="sxs-lookup"><span data-stu-id="036d9-318">(30)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-319">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="036d9-319">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="036d9-320"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="036d9-320"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="036d9-321">31</span><span class="sxs-lookup"><span data-stu-id="036d9-321">(31)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-322">El dispositivo no funciona correctamente. Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="036d9-322">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="036d9-323">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="036d9-323">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-324">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="036d9-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-326">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="036d9-326">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="036d9-327">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="036d9-327">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="036d9-328">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-329">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="036d9-329">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-330">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="036d9-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-332">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="036d9-332">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="036d9-333">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="036d9-333">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="036d9-334">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="036d9-334">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="036d9-335">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-336">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="036d9-336">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-337">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="036d9-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-339">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="036d9-339">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="036d9-340">Tamaño de bloque predeterminado, en bytes, para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="036d9-340">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="036d9-341">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-341">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="036d9-342">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="036d9-342">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-343">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="036d9-343">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-344">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="036d9-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-346">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="036d9-346">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="036d9-347">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="036d9-347">Textual description of the object.</span></span>

<span data-ttu-id="036d9-348">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-349">**ID**</span><span class="sxs-lookup"><span data-stu-id="036d9-349">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-350">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="036d9-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-352">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="036d9-352">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="036d9-353">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="036d9-353">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="036d9-354">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-355">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="036d9-355">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-356">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="036d9-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="036d9-358">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="036d9-358">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="036d9-359">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-360">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="036d9-360">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-361">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="036d9-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="036d9-363">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="036d9-363">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="036d9-364">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-365">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="036d9-365">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-366">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="036d9-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="036d9-368">Cadena de forma libre que describe los tipos de detección y corrección de errores admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="036d9-368">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="036d9-369">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-369">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-370">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="036d9-370">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-371">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="036d9-371">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-373">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="036d9-373">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="036d9-374">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="036d9-374">Date and time the object was installed.</span></span> <span data-ttu-id="036d9-375">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="036d9-375">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="036d9-376">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-376">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-377">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="036d9-377">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-378">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="036d9-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-379">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="036d9-380">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="036d9-380">Last error code reported by the logical device.</span></span>

<span data-ttu-id="036d9-381">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-382">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="036d9-382">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-383">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="036d9-383">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-384">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-385">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="036d9-385">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="036d9-386">Tamaño máximo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="036d9-386">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="036d9-387">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-387">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="036d9-388">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="036d9-388">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-389">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="036d9-389">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-390">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="036d9-390">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-391">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-392">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acceso secuencial DMTF \| 001,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="036d9-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="036d9-393">Tamaño máximo, en kilobytes, de los medios admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="036d9-393">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="036d9-394">Los kilobytes se interpretan como el número de bytes multiplicado por 1000 (no por el número de bytes multiplicado por 1024).</span><span class="sxs-lookup"><span data-stu-id="036d9-394">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="036d9-395">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-395">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="036d9-396">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="036d9-396">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-397">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="036d9-397">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-398">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="036d9-398">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-400">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="036d9-400">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="036d9-401">Tamaño mínimo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="036d9-401">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="036d9-402">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-402">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="036d9-403">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="036d9-403">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-404">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="036d9-404">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-405">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="036d9-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-406">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-407">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="036d9-407">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="036d9-408">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="036d9-408">Label by which the object is known.</span></span> <span data-ttu-id="036d9-409">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="036d9-409">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="036d9-410">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-410">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-411">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="036d9-411">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-412">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="036d9-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="036d9-414">Si **es true**, el dispositivo de acceso a medios necesita limpieza.</span><span class="sxs-lookup"><span data-stu-id="036d9-414">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="036d9-415">Si la limpieza manual o automática es posible, se indica en la propiedad array de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="036d9-415">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="036d9-416">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-416">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-417">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="036d9-417">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-418">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="036d9-418">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-419">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="036d9-420">Si el dispositivo de acceso a medios admite varios medios individuales, esta propiedad define el número máximo que se puede admitir o insertar.</span><span class="sxs-lookup"><span data-stu-id="036d9-420">If the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="036d9-421">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-421">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-422">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="036d9-422">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-423">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="036d9-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-424">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-425">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="036d9-425">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="036d9-426">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="036d9-426">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="036d9-427">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="036d9-428">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="036d9-428">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="036d9-429">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="036d9-429">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-430">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="036d9-430">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="036d9-431">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="036d9-432">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="036d9-432">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="036d9-433">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="036d9-433">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="036d9-434"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="036d9-434"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="036d9-435"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="036d9-435"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-436">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="036d9-436">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="036d9-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="036d9-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="036d9-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="036d9-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-439">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="036d9-439">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="036d9-440"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="036d9-440"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-441">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="036d9-441">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="036d9-442"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="036d9-442"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-443">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="036d9-443">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="036d9-444">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="036d9-444">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="036d9-445">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="036d9-445">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="036d9-446"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="036d9-446"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-447">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="036d9-447">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="036d9-448"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="036d9-448"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="036d9-449">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="036d9-449">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="036d9-450">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="036d9-450">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-451">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="036d9-451">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-452">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="036d9-453">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="036d9-453">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="036d9-454">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="036d9-454">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="036d9-455">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="036d9-455">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="036d9-456">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="036d9-456">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="036d9-457">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-457">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-458">**Estado**</span><span class="sxs-lookup"><span data-stu-id="036d9-458">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-459">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="036d9-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-460">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-461">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="036d9-461">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="036d9-462">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="036d9-462">Current status of the object.</span></span>

<span data-ttu-id="036d9-463">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-463">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="036d9-464">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="036d9-464">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="036d9-465">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="036d9-465">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="036d9-466">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="036d9-466">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="036d9-467">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="036d9-467">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="036d9-468">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="036d9-468">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="036d9-469">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="036d9-469">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="036d9-470">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="036d9-470">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="036d9-471">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="036d9-471">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="036d9-472">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="036d9-472">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="036d9-473">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="036d9-473">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="036d9-474">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="036d9-474">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="036d9-475">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="036d9-475">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="036d9-476">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="036d9-476">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="036d9-477">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="036d9-477">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-478">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="036d9-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-479">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-479">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-480">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="036d9-480">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="036d9-481">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="036d9-481">State of the logical device.</span></span> <span data-ttu-id="036d9-482">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="036d9-482">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="036d9-483">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-483">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="036d9-484">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="036d9-484">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="036d9-485">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="036d9-485">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="036d9-486">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="036d9-486">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="036d9-487">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="036d9-487">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="036d9-488">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="036d9-488">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="036d9-489">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="036d9-489">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-490">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="036d9-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-491">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-492">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="036d9-492">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="036d9-493">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="036d9-493">Scoping system's creation class name.</span></span>

<span data-ttu-id="036d9-494">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-494">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="036d9-495">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="036d9-495">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="036d9-496">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="036d9-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="036d9-497">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="036d9-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="036d9-498">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="036d9-498">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="036d9-499">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="036d9-499">Scoping system's name.</span></span>

<span data-ttu-id="036d9-500">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-500">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="036d9-501">Observaciones</span><span class="sxs-lookup"><span data-stu-id="036d9-501">Remarks</span></span>

<span data-ttu-id="036d9-502">La clase **CIM \_ MagnetoOpticalDrive** se deriva de [**\_ MediaAccessDevice de CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="036d9-502">The **CIM\_MagnetoOpticalDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="036d9-503">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="036d9-503">WMI does not implement this class.</span></span>

<span data-ttu-id="036d9-504">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="036d9-504">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="036d9-505">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="036d9-505">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="036d9-506">Requisitos</span><span class="sxs-lookup"><span data-stu-id="036d9-506">Requirements</span></span>



| <span data-ttu-id="036d9-507">Requisito</span><span class="sxs-lookup"><span data-stu-id="036d9-507">Requirement</span></span> | <span data-ttu-id="036d9-508">Value</span><span class="sxs-lookup"><span data-stu-id="036d9-508">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="036d9-509">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="036d9-509">Minimum supported client</span></span><br/> | <span data-ttu-id="036d9-510">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="036d9-510">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="036d9-511">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="036d9-511">Minimum supported server</span></span><br/> | <span data-ttu-id="036d9-512">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="036d9-512">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="036d9-513">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="036d9-513">Namespace</span></span><br/>                | <span data-ttu-id="036d9-514">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="036d9-514">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="036d9-515">MOF</span><span class="sxs-lookup"><span data-stu-id="036d9-515">MOF</span></span><br/>                      | <dl> <span data-ttu-id="036d9-516"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="036d9-516"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="036d9-517">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="036d9-517">DLL</span></span><br/>                      | <dl> <span data-ttu-id="036d9-518"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="036d9-518"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="036d9-519">Vea también</span><span class="sxs-lookup"><span data-stu-id="036d9-519">See also</span></span>

<dl> <dt>

[<span data-ttu-id="036d9-520">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="036d9-520">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

