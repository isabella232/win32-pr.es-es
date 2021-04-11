---
description: La \_ clase CIM DiskDrive representa una unidad de disco física tal como la muestra el sistema operativo.
ms.assetid: 3a63506e-455e-4108-b0c7-03b2af249d61
ms.tgt_platform: multiple
title: CIM_DiskDrive (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskDrive
- CIM_DiskDrive.Availability
- CIM_DiskDrive.Capabilities
- CIM_DiskDrive.CapabilityDescriptions
- CIM_DiskDrive.Caption
- CIM_DiskDrive.CompressionMethod
- CIM_DiskDrive.ConfigManagerErrorCode
- CIM_DiskDrive.ConfigManagerUserConfig
- CIM_DiskDrive.CreationClassName
- CIM_DiskDrive.DefaultBlockSize
- CIM_DiskDrive.Description
- CIM_DiskDrive.DeviceID
- CIM_DiskDrive.ErrorCleared
- CIM_DiskDrive.ErrorDescription
- CIM_DiskDrive.ErrorMethodology
- CIM_DiskDrive.InstallDate
- CIM_DiskDrive.LastErrorCode
- CIM_DiskDrive.MaxBlockSize
- CIM_DiskDrive.MaxMediaSize
- CIM_DiskDrive.MinBlockSize
- CIM_DiskDrive.Name
- CIM_DiskDrive.NeedsCleaning
- CIM_DiskDrive.NumberOfMediaSupported
- CIM_DiskDrive.PNPDeviceID
- CIM_DiskDrive.PowerManagementCapabilities
- CIM_DiskDrive.PowerManagementSupported
- CIM_DiskDrive.Status
- CIM_DiskDrive.StatusInfo
- CIM_DiskDrive.SystemCreationClassName
- CIM_DiskDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c68e8fc53898220737f473cc0c13f43d7ad471b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275034"
---
# <a name="cim_diskdrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="03fb0-103">CIM_DiskDrive (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="03fb0-103">CIM_DiskDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="03fb0-104">La clase **CIM \_ DiskDrive** representa una unidad de disco física tal como la muestra el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-104">The **CIM\_DiskDrive** class represents a physical disk drive as seen by the operating system.</span></span> <span data-ttu-id="03fb0-105">Las características de la unidad de disco se corresponden con las características lógicas y de administración de la unidad, y en algunos casos, es posible que no reflejen las características físicas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-105">The disk drive features correspond to the logical and management characteristics of the drive, and in some cases, may not reflect the physical characteristics of the device.</span></span> <span data-ttu-id="03fb0-106">Una interfaz a una unidad física es miembro de esta clase.</span><span class="sxs-lookup"><span data-stu-id="03fb0-106">An interface to a physical drive is a member of this class.</span></span> <span data-ttu-id="03fb0-107">Sin embargo, un objeto basado en otro dispositivo lógico no es miembro de esta clase.</span><span class="sxs-lookup"><span data-stu-id="03fb0-107">However, an object based on another logical device is not a member of this class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03fb0-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="03fb0-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="03fb0-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="03fb0-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="03fb0-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="03fb0-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="03fb0-111">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="03fb0-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="03fb0-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03fb0-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DiskDrive : CIM_MediaAccessDevice
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

## <a name="members"></a><span data-ttu-id="03fb0-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="03fb0-113">Members</span></span>

<span data-ttu-id="03fb0-114">La clase **CIM \_ DiskDrive** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="03fb0-114">The **CIM\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="03fb0-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="03fb0-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="03fb0-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="03fb0-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="03fb0-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="03fb0-117">Methods</span></span>

<span data-ttu-id="03fb0-118">La clase **CIM \_ DiskDrive** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="03fb0-118">The **CIM\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="03fb0-119">Método</span><span class="sxs-lookup"><span data-stu-id="03fb0-119">Method</span></span>                                                                | <span data-ttu-id="03fb0-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="03fb0-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03fb0-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="03fb0-121">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="03fb0-122">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="03fb0-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="03fb0-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="03fb0-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="03fb0-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="03fb0-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="03fb0-125">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="03fb0-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="03fb0-126">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="03fb0-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="03fb0-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="03fb0-127">Properties</span></span>

<span data-ttu-id="03fb0-128">La clase **CIM \_ DiskDrive** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="03fb0-128">The **CIM\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03fb0-129">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="03fb0-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-130">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03fb0-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-132">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="03fb0-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-133">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-133">Availability and status of the device.</span></span>

<span data-ttu-id="03fb0-134">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="03fb0-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="03fb0-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-136">Otros.</span><span class="sxs-lookup"><span data-stu-id="03fb0-136">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03fb0-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="03fb0-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-138">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="03fb0-138">Unknown.</span></span>

</dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="03fb0-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="03fb0-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-140">En ejecución o completa.</span><span class="sxs-lookup"><span data-stu-id="03fb0-140">Running/full power.</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="03fb0-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="03fb0-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-142">Advertencia.</span><span class="sxs-lookup"><span data-stu-id="03fb0-142">Warning.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="03fb0-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="03fb0-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-144">Pruebas.</span><span class="sxs-lookup"><span data-stu-id="03fb0-144">Testing.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="03fb0-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="03fb0-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-146">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="03fb0-146">Not applicable.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="03fb0-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="03fb0-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-148">Desconectar.</span><span class="sxs-lookup"><span data-stu-id="03fb0-148">Power off.</span></span>

</dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="03fb0-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="03fb0-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-150">N.</span><span class="sxs-lookup"><span data-stu-id="03fb0-150">Offline.</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="03fb0-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="03fb0-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-152">Fuera de servicio.</span><span class="sxs-lookup"><span data-stu-id="03fb0-152">Off duty.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="03fb0-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="03fb0-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-154">Degradado.</span><span class="sxs-lookup"><span data-stu-id="03fb0-154">Degraded.</span></span>

</dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="03fb0-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="03fb0-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-156">No instalado.</span><span class="sxs-lookup"><span data-stu-id="03fb0-156">Not installed.</span></span>

</dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="03fb0-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="03fb0-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-158">Error de instalación.</span><span class="sxs-lookup"><span data-stu-id="03fb0-158">Install error.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="03fb0-159"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="03fb0-159"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-160">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto en este modo es desconocido.</span><span class="sxs-lookup"><span data-stu-id="03fb0-160">Device is known to be in a power save mode, but its exact status in this mode is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="03fb0-161"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="03fb0-161"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-162">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="03fb0-162">Device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="03fb0-163"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="03fb0-163"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-164">El dispositivo no funciona, pero puede pasarse a la potencia completa "rápidamente".</span><span class="sxs-lookup"><span data-stu-id="03fb0-164">Device is not functioning but could be brought to full power 'quickly'.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="03fb0-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="03fb0-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-166">Ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="03fb0-166">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="03fb0-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="03fb0-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-168">El dispositivo está en un estado de advertencia y también en un modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="03fb0-168">Device is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="03fb0-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="03fb0-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-170">En pausa.</span><span class="sxs-lookup"><span data-stu-id="03fb0-170">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="03fb0-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="03fb0-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-172">No está listo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-172">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="03fb0-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="03fb0-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-174">No configurado.</span><span class="sxs-lookup"><span data-stu-id="03fb0-174">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="03fb0-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="03fb0-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-176">La unidad de disco no está disponible.</span><span class="sxs-lookup"><span data-stu-id="03fb0-176">The disk drive is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="03fb0-177">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="03fb0-177">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-178">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03fb0-178">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-180">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de almacenamiento DMTF \| 001,9 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,11 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,12 "," MIF. \|Discos DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="03fb0-180">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-181">Capacidades del dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="03fb0-181">Capabilities of the media access device.</span></span> <span data-ttu-id="03fb0-182">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-182">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03fb0-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="03fb0-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-184">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="03fb0-184">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="03fb0-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="03fb0-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-186">Otros.</span><span class="sxs-lookup"><span data-stu-id="03fb0-186">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="03fb0-187"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acceso secuencial** (2)</span><span class="sxs-lookup"><span data-stu-id="03fb0-187"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-188">Acceso secuencial.</span><span class="sxs-lookup"><span data-stu-id="03fb0-188">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="03fb0-189"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acceso aleatorio** (3)</span><span class="sxs-lookup"><span data-stu-id="03fb0-189"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-190">Acceso aleatorio.</span><span class="sxs-lookup"><span data-stu-id="03fb0-190">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="03fb0-191"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Admite escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="03fb0-191"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-192">Escritura.</span><span class="sxs-lookup"><span data-stu-id="03fb0-192">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="03fb0-193"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Cifrado** (5)</span><span class="sxs-lookup"><span data-stu-id="03fb0-193"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-194">Cifrado.</span><span class="sxs-lookup"><span data-stu-id="03fb0-194">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="03fb0-195"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compresión** (6)</span><span class="sxs-lookup"><span data-stu-id="03fb0-195"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-196">Compression.</span><span class="sxs-lookup"><span data-stu-id="03fb0-196">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="03fb0-197"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Admite medios** extraíbles (7)</span><span class="sxs-lookup"><span data-stu-id="03fb0-197"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-198">Medios extraíbles.</span><span class="sxs-lookup"><span data-stu-id="03fb0-198">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="03fb0-199"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpieza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="03fb0-199"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-200">Limpieza manual.</span><span class="sxs-lookup"><span data-stu-id="03fb0-200">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="03fb0-201"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpieza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="03fb0-201"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-202">Limpieza automática.</span><span class="sxs-lookup"><span data-stu-id="03fb0-202">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="03fb0-203"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificación inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="03fb0-203"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-204">Notificación inteligente.</span><span class="sxs-lookup"><span data-stu-id="03fb0-204">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="03fb0-205"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Admite medios de doble cara** (11)</span><span class="sxs-lookup"><span data-stu-id="03fb0-205"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-206">Distingue un dispositivo que puede tener acceso a ambos lados de un medio de dos caras desde un dispositivo que lee solo un lado y requiere que el medio se desactive.</span><span class="sxs-lookup"><span data-stu-id="03fb0-206">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="03fb0-207"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT no requerido** (12)</span><span class="sxs-lookup"><span data-stu-id="03fb0-207"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-208">Indica que el medio no tiene que extraerse explícitamente del dispositivo antes de que un elemento selector tenga acceso a él.</span><span class="sxs-lookup"><span data-stu-id="03fb0-208">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="03fb0-209">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="03fb0-209">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-210">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="03fb0-210">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-212">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="03fb0-212">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-213">Matriz de cadenas de formato libre que proporcionan explicaciones detalladas para las características del dispositivo de acceso indicadas en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="03fb0-213">Array of free-form strings that provide detailed explanations for access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="03fb0-214">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-214">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

> [!Note]  
> <span data-ttu-id="03fb0-215">Cada entrada de esta matriz está relacionada con la entrada de la matriz de **capacidades** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="03fb0-215">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="03fb0-216">**Caption**</span><span class="sxs-lookup"><span data-stu-id="03fb0-216">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03fb0-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-219">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="03fb0-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-220">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="03fb0-220">Short textual description of the object.</span></span>

<span data-ttu-id="03fb0-221">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-222">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="03fb0-222">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-223">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03fb0-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-225">Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="03fb0-225">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="03fb0-226">Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="03fb0-226">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="03fb0-227">Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido".</span><span class="sxs-lookup"><span data-stu-id="03fb0-227">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="03fb0-228">Si el archivo lógico no está comprimido, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="03fb0-228">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="03fb0-229">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-229">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="03fb0-230">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="03fb0-230">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-231">El esquema de compresión es desconocido o no se ha descrito.</span><span class="sxs-lookup"><span data-stu-id="03fb0-231">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="03fb0-232">("Comprimido")</span><span class="sxs-lookup"><span data-stu-id="03fb0-232">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-233">El archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito</span><span class="sxs-lookup"><span data-stu-id="03fb0-233">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="03fb0-234">("No comprimido")</span><span class="sxs-lookup"><span data-stu-id="03fb0-234">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-235">Si el archivo lógico no está comprimido</span><span class="sxs-lookup"><span data-stu-id="03fb0-235">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="03fb0-236">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="03fb0-236">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-237">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03fb0-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-239">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="03fb0-239">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-240">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="03fb0-240">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="03fb0-241">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-241">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="03fb0-242"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-242"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="03fb0-243"> (0)</span><span class="sxs-lookup"><span data-stu-id="03fb0-243">(0)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-244">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="03fb0-244">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="03fb0-245"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-245"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="03fb0-246">(1)</span><span class="sxs-lookup"><span data-stu-id="03fb0-246">(1)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-247">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="03fb0-247">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="03fb0-248"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-248"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="03fb0-249">(2)</span><span class="sxs-lookup"><span data-stu-id="03fb0-249">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="03fb0-250"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-250"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="03fb0-251">(3)</span><span class="sxs-lookup"><span data-stu-id="03fb0-251">(3)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-252">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="03fb0-252">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="03fb0-253"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-253"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="03fb0-254">(4)</span><span class="sxs-lookup"><span data-stu-id="03fb0-254">(4)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-255">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="03fb0-255">Device is not working properly.</span></span> <span data-ttu-id="03fb0-256">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="03fb0-256">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="03fb0-257"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-257"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="03fb0-258">(5)</span><span class="sxs-lookup"><span data-stu-id="03fb0-258">(5)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-259">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="03fb0-259">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="03fb0-260"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-260"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="03fb0-261"> (6)</span><span class="sxs-lookup"><span data-stu-id="03fb0-261">(6)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-262">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="03fb0-262">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="03fb0-263"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-263"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="03fb0-264">(7)</span><span class="sxs-lookup"><span data-stu-id="03fb0-264">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="03fb0-265"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-265"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="03fb0-266">(8)</span><span class="sxs-lookup"><span data-stu-id="03fb0-266">(8)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-267">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-267">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="03fb0-268"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-268"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="03fb0-269">(9)</span><span class="sxs-lookup"><span data-stu-id="03fb0-269">(9)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-270">El dispositivo no funciona correctamente. el firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-270">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="03fb0-271"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-271"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="03fb0-272">(10)</span><span class="sxs-lookup"><span data-stu-id="03fb0-272">(10)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-273">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="03fb0-273">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="03fb0-274"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-274"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="03fb0-275">(11)</span><span class="sxs-lookup"><span data-stu-id="03fb0-275">(11)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-276">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-276">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="03fb0-277"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-277"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="03fb0-278">(12)</span><span class="sxs-lookup"><span data-stu-id="03fb0-278">(12)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-279">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="03fb0-279">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="03fb0-280"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-280"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="03fb0-281">(13)</span><span class="sxs-lookup"><span data-stu-id="03fb0-281">(13)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-282">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-282">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="03fb0-283"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-283"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="03fb0-284">(14)</span><span class="sxs-lookup"><span data-stu-id="03fb0-284">(14)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-285">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-285">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="03fb0-286"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-286"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="03fb0-287">(15)</span><span class="sxs-lookup"><span data-stu-id="03fb0-287">(15)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-288">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="03fb0-288">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="03fb0-289"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-289"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="03fb0-290">(16)</span><span class="sxs-lookup"><span data-stu-id="03fb0-290">(16)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-291">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-291">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="03fb0-292"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-292"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="03fb0-293">(17)</span><span class="sxs-lookup"><span data-stu-id="03fb0-293">(17)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-294">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="03fb0-294">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="03fb0-295"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-295"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="03fb0-296">(18)</span><span class="sxs-lookup"><span data-stu-id="03fb0-296">(18)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-297">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="03fb0-297">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="03fb0-298"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-298"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="03fb0-299">(19)</span><span class="sxs-lookup"><span data-stu-id="03fb0-299">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="03fb0-300"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-300"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="03fb0-301">(20)</span><span class="sxs-lookup"><span data-stu-id="03fb0-301">(20)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-302">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="03fb0-302">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="03fb0-303"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-303"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="03fb0-304">(21)</span><span class="sxs-lookup"><span data-stu-id="03fb0-304">(21)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-305">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="03fb0-305">System failure.</span></span> <span data-ttu-id="03fb0-306">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="03fb0-306">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="03fb0-307">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-307">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="03fb0-308"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-308"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="03fb0-309">(22)</span><span class="sxs-lookup"><span data-stu-id="03fb0-309">(22)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-310">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="03fb0-310">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="03fb0-311"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-311"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="03fb0-312">(23)</span><span class="sxs-lookup"><span data-stu-id="03fb0-312">(23)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-313">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="03fb0-313">System failure.</span></span> <span data-ttu-id="03fb0-314">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="03fb0-314">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="03fb0-315"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-315"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="03fb0-316">(24)</span><span class="sxs-lookup"><span data-stu-id="03fb0-316">(24)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-317">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="03fb0-317">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="03fb0-318"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-318"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="03fb0-319">(25)</span><span class="sxs-lookup"><span data-stu-id="03fb0-319">(25)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-320">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-320">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="03fb0-321"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-321"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="03fb0-322">(26)</span><span class="sxs-lookup"><span data-stu-id="03fb0-322">(26)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-323">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-323">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="03fb0-324"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-324"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="03fb0-325">(27)</span><span class="sxs-lookup"><span data-stu-id="03fb0-325">(27)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-326">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="03fb0-326">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="03fb0-327"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-327"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="03fb0-328">(28)</span><span class="sxs-lookup"><span data-stu-id="03fb0-328">(28)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-329">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="03fb0-329">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="03fb0-330"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-330"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="03fb0-331">(29)</span><span class="sxs-lookup"><span data-stu-id="03fb0-331">(29)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-332">El dispositivo está deshabilitado; el firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="03fb0-332">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="03fb0-333"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-333"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="03fb0-334">(30)</span><span class="sxs-lookup"><span data-stu-id="03fb0-334">(30)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-335">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="03fb0-335">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="03fb0-336"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="03fb0-336"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="03fb0-337">31</span><span class="sxs-lookup"><span data-stu-id="03fb0-337">(31)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-338">El dispositivo no funciona correctamente. Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="03fb0-338">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="03fb0-339">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="03fb0-339">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-340">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="03fb0-340">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-342">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="03fb0-342">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-343">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="03fb0-343">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="03fb0-344">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-345">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="03fb0-345">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-346">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03fb0-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-348">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="03fb0-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-349">Nombre de la clase (o subclase) utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="03fb0-349">Name of the class (or subclass) used in the creation of an instance.</span></span> <span data-ttu-id="03fb0-350">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="03fb0-350">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="03fb0-351">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-352">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="03fb0-352">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-353">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="03fb0-353">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-355">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="03fb0-355">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-356">Tamaño de bloque predeterminado, en bytes, para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-356">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="03fb0-357">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-357">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="03fb0-358">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="03fb0-358">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-359">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="03fb0-359">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-360">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03fb0-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-362">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="03fb0-362">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-363">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="03fb0-363">Textual description of the object.</span></span>

<span data-ttu-id="03fb0-364">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-364">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-365">**ID**</span><span class="sxs-lookup"><span data-stu-id="03fb0-365">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-366">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03fb0-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-368">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="03fb0-368">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-369">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="03fb0-369">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="03fb0-370">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-371">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="03fb0-371">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-372">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="03fb0-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-373">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-374">Si es **true**, el error comunicado en la propiedad **LastErrorCode** está desactivado.</span><span class="sxs-lookup"><span data-stu-id="03fb0-374">If **TRUE**, the error reported in the **LastErrorCode** property is cleared.</span></span>

<span data-ttu-id="03fb0-375">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-376">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="03fb0-376">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-377">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03fb0-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-378">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-379">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="03fb0-379">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="03fb0-380">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-380">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-381">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="03fb0-381">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-382">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03fb0-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-384">Cadena de forma libre que describe el tipo de detección y corrección de errores admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-384">Free-form string that describes the type of error detection and correction supported by the device.</span></span>

<span data-ttu-id="03fb0-385">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-385">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-386">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="03fb0-386">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-387">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="03fb0-387">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-389">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="03fb0-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-390">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="03fb0-390">Date and time when the object was installed.</span></span> <span data-ttu-id="03fb0-391">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="03fb0-391">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="03fb0-392">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-393">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="03fb0-393">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-394">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03fb0-394">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-395">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-396">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="03fb0-396">Last error code reported by the logical device.</span></span>

<span data-ttu-id="03fb0-397">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-398">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="03fb0-398">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-399">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="03fb0-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-400">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-401">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="03fb0-401">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-402">Tamaño máximo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-402">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="03fb0-403">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-403">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="03fb0-404">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="03fb0-404">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-405">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="03fb0-405">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-406">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="03fb0-406">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-407">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-408">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acceso secuencial DMTF \| 001,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="03fb0-408">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-409">Tamaño máximo, en kilobytes, de los medios admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-409">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="03fb0-410">Los kilobytes se interpretan como el número de bytes multiplicado por 1000 (no por el número de bytes multiplicado por 1024).</span><span class="sxs-lookup"><span data-stu-id="03fb0-410">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="03fb0-411">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-411">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="03fb0-412">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="03fb0-412">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-413">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="03fb0-413">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-414">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="03fb0-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-415">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-416">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="03fb0-416">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-417">Tamaño mínimo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03fb0-417">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="03fb0-418">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-418">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="03fb0-419">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="03fb0-419">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-420">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="03fb0-420">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-421">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03fb0-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-422">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-423">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="03fb0-423">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-424">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="03fb0-424">Label by which the object is known.</span></span> <span data-ttu-id="03fb0-425">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="03fb0-425">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="03fb0-426">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-426">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-427">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="03fb0-427">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-428">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="03fb0-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-429">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-430">Si **es true**, el dispositivo de acceso a medios necesita limpieza.</span><span class="sxs-lookup"><span data-stu-id="03fb0-430">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="03fb0-431">Si la limpieza manual o automática es posible, se indica en la propiedad array de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="03fb0-431">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="03fb0-432">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-432">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-433">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="03fb0-433">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-434">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03fb0-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-436">Cuando el dispositivo de acceso a medios admite varios medios individuales, esta propiedad define el número máximo que se puede admitir o insertar.</span><span class="sxs-lookup"><span data-stu-id="03fb0-436">When the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="03fb0-437">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-437">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-438">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="03fb0-438">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-439">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03fb0-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-441">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="03fb0-441">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-442">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="03fb0-442">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="03fb0-443">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-443">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="03fb0-444">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="03fb0-444">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-445">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="03fb0-445">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-446">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03fb0-446">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-447">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-448">Capacidades específicas relacionadas con la energía del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="03fb0-448">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="03fb0-449">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-449">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03fb0-450"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="03fb0-450"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-451">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="03fb0-451">Unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="03fb0-452"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="03fb0-452"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-453">No se admite.</span><span class="sxs-lookup"><span data-stu-id="03fb0-453">Not supported.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="03fb0-454"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="03fb0-454"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-455">Deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="03fb0-455">Disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="03fb0-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="03fb0-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-457">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="03fb0-457">Power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="03fb0-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="03fb0-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-459">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="03fb0-459">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="03fb0-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="03fb0-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-461">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="03fb0-461">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="03fb0-462"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="03fb0-462"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-463">El método [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="03fb0-463">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="03fb0-464"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="03fb0-464"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="03fb0-465">El método [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o Interval, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="03fb0-465">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="03fb0-466">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="03fb0-466">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-467">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="03fb0-467">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-468">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-469">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="03fb0-469">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="03fb0-470">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="03fb0-470">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="03fb0-471">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="03fb0-471">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="03fb0-472">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="03fb0-472">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="03fb0-473">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-473">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-474">**Estado**</span><span class="sxs-lookup"><span data-stu-id="03fb0-474">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-475">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03fb0-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-476">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-477">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="03fb0-477">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-478">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="03fb0-478">Current status of the object.</span></span>

<span data-ttu-id="03fb0-479">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-479">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="03fb0-480">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="03fb0-480">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="03fb0-481">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="03fb0-481">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="03fb0-482">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="03fb0-482">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="03fb0-483">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="03fb0-483">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03fb0-484">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="03fb0-484">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="03fb0-485">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="03fb0-485">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="03fb0-486">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="03fb0-486">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="03fb0-487">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="03fb0-487">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="03fb0-488">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="03fb0-488">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="03fb0-489">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="03fb0-489">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="03fb0-490">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="03fb0-490">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="03fb0-491">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="03fb0-491">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="03fb0-492">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="03fb0-492">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03fb0-493">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="03fb0-493">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-494">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03fb0-494">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-495">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-496">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="03fb0-496">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-497">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="03fb0-497">State of the logical device.</span></span> <span data-ttu-id="03fb0-498">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="03fb0-498">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="03fb0-499">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-499">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="03fb0-500">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="03fb0-500">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="03fb0-501">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="03fb0-501">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="03fb0-502">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="03fb0-502">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="03fb0-503">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="03fb0-503">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="03fb0-504">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="03fb0-504">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03fb0-505">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="03fb0-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-506">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03fb0-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-507">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-508">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="03fb0-508">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-509">Propiedad **CreationClassName** del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="03fb0-509">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="03fb0-510">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="03fb0-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="03fb0-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03fb0-512">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03fb0-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-513">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03fb0-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03fb0-514">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="03fb0-514">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="03fb0-515">Propiedad de **nombre** del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="03fb0-515">Scoping system's **Name** property.</span></span>

<span data-ttu-id="03fb0-516">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03fb0-517">Observaciones</span><span class="sxs-lookup"><span data-stu-id="03fb0-517">Remarks</span></span>

<span data-ttu-id="03fb0-518">La clase **CIM \_ DiskDrive** se deriva de [**\_ MediaAccessDevice de CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="03fb0-518">The **CIM\_DiskDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="03fb0-519">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="03fb0-519">WMI does not implement this class.</span></span> <span data-ttu-id="03fb0-520">Vea [clases Win32](win32-provider.md) para clases derivadas de **CIM \_ DiskDrive**.</span><span class="sxs-lookup"><span data-stu-id="03fb0-520">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_DiskDrive**.</span></span>

<span data-ttu-id="03fb0-521">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="03fb0-521">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="03fb0-522">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="03fb0-522">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="03fb0-523">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03fb0-523">Requirements</span></span>



| <span data-ttu-id="03fb0-524">Requisito</span><span class="sxs-lookup"><span data-stu-id="03fb0-524">Requirement</span></span> | <span data-ttu-id="03fb0-525">Value</span><span class="sxs-lookup"><span data-stu-id="03fb0-525">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03fb0-526">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03fb0-526">Minimum supported client</span></span><br/> | <span data-ttu-id="03fb0-527">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03fb0-527">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03fb0-528">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03fb0-528">Minimum supported server</span></span><br/> | <span data-ttu-id="03fb0-529">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03fb0-529">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03fb0-530">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="03fb0-530">Namespace</span></span><br/>                | <span data-ttu-id="03fb0-531">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="03fb0-531">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="03fb0-532">MOF</span><span class="sxs-lookup"><span data-stu-id="03fb0-532">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03fb0-533"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03fb0-533"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="03fb0-534">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03fb0-534">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03fb0-535"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03fb0-535"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03fb0-536">Vea también</span><span class="sxs-lookup"><span data-stu-id="03fb0-536">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03fb0-537">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="03fb0-537">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

