---
description: La \_ clase CIM MediaAccessDevice representa la capacidad de obtener acceso a uno o más medios y, a continuación, utilizar los medios para almacenar y recuperar datos.
ms.assetid: 224a7b08-1566-4b0b-90d8-9991fa188d93
ms.tgt_platform: multiple
title: CIM_MediaAccessDevice (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Caption
- CIM_MediaAccessDevice.Description
- CIM_MediaAccessDevice.InstallDate
- CIM_MediaAccessDevice.Name
- CIM_MediaAccessDevice.Status
- CIM_MediaAccessDevice.Availability
- CIM_MediaAccessDevice.ConfigManagerErrorCode
- CIM_MediaAccessDevice.ConfigManagerUserConfig
- CIM_MediaAccessDevice.CreationClassName
- CIM_MediaAccessDevice.DeviceID
- CIM_MediaAccessDevice.PowerManagementCapabilities
- CIM_MediaAccessDevice.ErrorCleared
- CIM_MediaAccessDevice.ErrorDescription
- CIM_MediaAccessDevice.LastErrorCode
- CIM_MediaAccessDevice.PNPDeviceID
- CIM_MediaAccessDevice.PowerManagementSupported
- CIM_MediaAccessDevice.StatusInfo
- CIM_MediaAccessDevice.SystemCreationClassName
- CIM_MediaAccessDevice.SystemName
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.NumberOfMediaSupported
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0de0b993b4cc1da46b19b1c296fae44e855c5816
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914206"
---
# <a name="cim_mediaaccessdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="fc5f1-103">CIM_MediaAccessDevice (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-103">CIM_MediaAccessDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="fc5f1-104">La clase **CIM \_ MediaAccessDevice** representa la capacidad de obtener acceso a uno o más medios y, a continuación, utilizar los medios para almacenar y recuperar datos.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-104">The **CIM\_MediaAccessDevice** class represents the ability to access one or more media, and then use the media to store and retrieve data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc5f1-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fc5f1-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fc5f1-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fc5f1-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc5f1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc5f1-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
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

## <a name="members"></a><span data-ttu-id="fc5f1-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="fc5f1-110">Members</span></span>

<span data-ttu-id="fc5f1-111">La clase **CIM \_ MediaAccessDevice** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fc5f1-111">The **CIM\_MediaAccessDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="fc5f1-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="fc5f1-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="fc5f1-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc5f1-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fc5f1-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="fc5f1-114">Methods</span></span>

<span data-ttu-id="fc5f1-115">La clase **CIM \_ MediaAccessDevice** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-115">The **CIM\_MediaAccessDevice** class has these methods.</span></span>



| <span data-ttu-id="fc5f1-116">Método</span><span class="sxs-lookup"><span data-stu-id="fc5f1-116">Method</span></span>                                                                       | <span data-ttu-id="fc5f1-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc5f1-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc5f1-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-118">**Reset**</span></span>](reset-method-in-class-cim-mediaaccessdevice.md)                 | <span data-ttu-id="fc5f1-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="fc5f1-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="fc5f1-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-mediaaccessdevice.md) | <span data-ttu-id="fc5f1-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="fc5f1-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fc5f1-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc5f1-124">Properties</span></span>

<span data-ttu-id="fc5f1-125">La clase **CIM \_ MediaAccessDevice** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-125">The **CIM\_MediaAccessDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc5f1-126">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-129">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-130">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-130">Availability and status of the device.</span></span>

<span data-ttu-id="fc5f1-131">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fc5f1-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fc5f1-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="fc5f1-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="fc5f1-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="fc5f1-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="fc5f1-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="fc5f1-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="fc5f1-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="fc5f1-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="fc5f1-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="fc5f1-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fc5f1-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="fc5f1-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="fc5f1-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="fc5f1-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-145">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="fc5f1-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-147">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="fc5f1-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-149">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="fc5f1-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="fc5f1-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-152">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="fc5f1-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-154">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="fc5f1-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-156">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="fc5f1-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-158">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="fc5f1-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-160">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc5f1-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-162">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-164">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de almacenamiento DMTF \| 001,9 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,11 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,12 "," MIF. \|Discos DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-165">Capacidades del dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-165">Capabilities of the media access device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fc5f1-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-167">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-167">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fc5f1-168"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-168"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-169">Otros.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-169">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="fc5f1-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acceso secuencial** (2)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-171">Acceso secuencial.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-171">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="fc5f1-172"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acceso aleatorio** (3)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-172"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-173">Acceso aleatorio.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-173">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="fc5f1-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Admite escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-175">Escritura.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-175">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="fc5f1-176"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Cifrado** (5)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-176"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-177">Cifrado.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-177">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="fc5f1-178"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compresión** (6)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-178"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-179">Compression.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-179">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="fc5f1-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Admite medios** extraíbles (7)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-181">Medios extraíbles.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-181">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="fc5f1-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpieza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-183">Limpieza manual.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-183">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="fc5f1-184"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpieza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-184"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-185">Limpieza automática.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-185">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="fc5f1-186"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificación inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-186"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-187">Notificación inteligente.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-187">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="fc5f1-188"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Admite medios de doble cara** (11)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-188"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-189">Medios de doble cara.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-189">Dual-sided media.</span></span>

<span data-ttu-id="fc5f1-190">Distingue un dispositivo que puede tener acceso a ambos lados de un medio de dos caras desde un dispositivo que lee solo un lado y requiere que el medio se desactive.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-190">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="fc5f1-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT no requerido** (12)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-192">Indica que el medio no tiene que extraerse explícitamente del dispositivo antes de que un elemento selector tenga acceso a él.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-192">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc5f1-193">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-193">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-194">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-194">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-196">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-196">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-197">Matriz de cadenas de formato libre que proporciona explicaciones detalladas para las características del dispositivo de acceso indicadas en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="fc5f1-197">Array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="fc5f1-198">Cada entrada de esta matriz está relacionada con la entrada de la matriz de **funciones** , que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-198">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="fc5f1-199">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-199">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-200">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-202">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-202">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-203">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-203">A short textual description of the object.</span></span>

<span data-ttu-id="fc5f1-204">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-205">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-205">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-206">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-208">Cadena de forma libre que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-208">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="fc5f1-209">Si no es posible describir el esquema de compresión (porque es desconocido), use lo siguiente: si es, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="fc5f1-209">If it is not possible to describe the compression scheme (because it is unknown), use the following:If , use "Unknown".</span></span> <span data-ttu-id="fc5f1-210">Si es, use "Compressed".</span><span class="sxs-lookup"><span data-stu-id="fc5f1-210">If , use "Compressed".</span></span> <span data-ttu-id="fc5f1-211">, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="fc5f1-211">, use "Not Compressed".</span></span>

<dt>

<span data-ttu-id="fc5f1-212">Unknown</span><span class="sxs-lookup"><span data-stu-id="fc5f1-212">"Unknown"</span></span>
</dt> <dd>

<span data-ttu-id="fc5f1-213">El esquema de compresión es desconocido o no se ha descrito.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-213">The compression scheme is unknown or not described.</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-214">Comprimido</span><span class="sxs-lookup"><span data-stu-id="fc5f1-214">"Compressed"</span></span>
</dt> <dd>

<span data-ttu-id="fc5f1-215">El archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito</span><span class="sxs-lookup"><span data-stu-id="fc5f1-215">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-216">"No comprimido"</span><span class="sxs-lookup"><span data-stu-id="fc5f1-216">"Not Compressed"</span></span>
</dt> <dd>

<span data-ttu-id="fc5f1-217">Si el archivo lógico no está comprimido</span><span class="sxs-lookup"><span data-stu-id="fc5f1-217">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc5f1-218">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-218">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-219">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-219">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-221">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-221">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-222">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-222">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="fc5f1-223">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-223">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="fc5f1-224">**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-224">**This device is working properly.**</span></span> <span data-ttu-id="fc5f1-225"> (0)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-225">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="fc5f1-226">**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-226">**This device is not configured correctly.**</span></span> <span data-ttu-id="fc5f1-227">(1)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-227">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="fc5f1-228">**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-228">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="fc5f1-229">(2)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-229">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="fc5f1-230">**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-230">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="fc5f1-231">(3)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-231">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="fc5f1-232">**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-232">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="fc5f1-233">(4)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-233">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="fc5f1-234">**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-234">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="fc5f1-235">(5)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-235">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="fc5f1-236">**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-236">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="fc5f1-237"> (6)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-237">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="fc5f1-238">**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-238">**Cannot filter.**</span></span> <span data-ttu-id="fc5f1-239">(7)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-239">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="fc5f1-240">**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-240">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="fc5f1-241">(8)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-241">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="fc5f1-242">**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-242">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="fc5f1-243">(9)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-243">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="fc5f1-244">**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-244">**This device cannot start.**</span></span> <span data-ttu-id="fc5f1-245">(10)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-245">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="fc5f1-246">**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-246">**This device failed.**</span></span> <span data-ttu-id="fc5f1-247">(11)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-247">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="fc5f1-248">**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-248">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="fc5f1-249">(12)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-249">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="fc5f1-250">**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-250">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="fc5f1-251">(13)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-251">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="fc5f1-252">**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-252">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="fc5f1-253">(14)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-253">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="fc5f1-254">**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-254">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="fc5f1-255">(15)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-255">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="fc5f1-256">**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-256">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="fc5f1-257">(16)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-257">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="fc5f1-258">**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-258">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="fc5f1-259">(17)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-259">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="fc5f1-260">**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-260">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="fc5f1-261">(18)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-261">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="fc5f1-262">**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-262">**Failure using the VxD loader.**</span></span> <span data-ttu-id="fc5f1-263">(19)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-263">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="fc5f1-264">**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-264">**Your registry might be corrupted.**</span></span> <span data-ttu-id="fc5f1-265">(20)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-265">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="fc5f1-266">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-266">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="fc5f1-267">(21)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-267">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="fc5f1-268">**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-268">**This device is disabled.**</span></span> <span data-ttu-id="fc5f1-269">(22)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-269">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="fc5f1-270">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-270">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="fc5f1-271">(23)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-271">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="fc5f1-272">**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-272">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="fc5f1-273">(24)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-273">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="fc5f1-274">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-274">**Windows is still setting up this device.**</span></span> <span data-ttu-id="fc5f1-275">(25)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-275">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="fc5f1-276">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-276">**Windows is still setting up this device.**</span></span> <span data-ttu-id="fc5f1-277">(26)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-277">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="fc5f1-278">**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-278">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="fc5f1-279">(27)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-279">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="fc5f1-280">**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-280">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="fc5f1-281">(28)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-281">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="fc5f1-282">**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-282">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="fc5f1-283">(29)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-283">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="fc5f1-284">**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-284">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="fc5f1-285">(30)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-285">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="fc5f1-286">**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-286">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="fc5f1-287">31</span><span class="sxs-lookup"><span data-stu-id="fc5f1-287">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc5f1-288">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-288">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-289">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-289">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-291">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-291">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-292">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-292">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="fc5f1-293">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-294">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-294">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-295">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-297">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-297">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-298">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-298">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="fc5f1-299">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-299">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="fc5f1-300">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-301">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-301">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-302">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-302">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-304">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-304">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-305">Tamaño de bloque predeterminado, en bytes, para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-305">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="fc5f1-306">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-306">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-307">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-308">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-310">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-311">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-311">A textual description of the object.</span></span>

<span data-ttu-id="fc5f1-312">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-313">**ID**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-314">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-316">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-317">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="fc5f1-318">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-319">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-320">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-322">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="fc5f1-323">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-325">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-327">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="fc5f1-328">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-329">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-329">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-330">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-332">Cadena de forma libre que describe los tipos de detección y corrección de errores admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-332">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-333">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-333">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-334">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-334">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-336">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-336">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-337">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-337">Indicates when the object was installed.</span></span> <span data-ttu-id="fc5f1-338">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-338">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="fc5f1-339">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-340">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-341">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-343">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="fc5f1-344">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-345">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-345">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-346">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-346">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-348">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-348">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-349">Tamaño máximo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-349">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="fc5f1-350">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-350">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-351">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-351">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-352">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-354">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acceso secuencial DMTF \| 001,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-355">Tamaño máximo, en kilobytes, de los medios admitidos por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-355">Maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="fc5f1-356">Los kilobytes se interpretan como el número de bytes multiplicado por 1000 (no por el número de bytes multiplicado por 1024).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-356">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="fc5f1-357">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-357">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-358">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-358">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-359">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-359">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-360">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-361">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-361">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-362">Tamaño mínimo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-362">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="fc5f1-363">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-363">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-364">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-364">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-365">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-367">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-367">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-368">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-368">Label by which the object is known.</span></span> <span data-ttu-id="fc5f1-369">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-369">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="fc5f1-370">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-370">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-371">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-371">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-372">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-373">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-374">Si **es true**, el dispositivo de acceso a medios necesita limpieza.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-374">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="fc5f1-375">Si la limpieza manual o automática es posible, se indica en la propiedad array de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="fc5f1-375">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-376">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-376">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-377">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-377">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-378">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-379">Número máximo de medios individuales que se pueden admitir o insertar.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-379">Maximum number of multiple individual media that can be supported or inserted.</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-380">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-380">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-381">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-383">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-383">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-384">Indica el identificador de dispositivo Plug and Play Win32 del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-384">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="fc5f1-385">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="fc5f1-385">Example: "\*PNP030b"</span></span>

<span data-ttu-id="fc5f1-386">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-386">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-387">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-387">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-388">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-388">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-389">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-390">Indica las capacidades de energía específicas relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-390">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="fc5f1-391">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fc5f1-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-393">Las capacidades relacionadas con la energía son desconocidas.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-393">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="fc5f1-394"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-394"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-395">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-395">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fc5f1-396"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-396"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-397">Se han deshabilitado las capacidades relacionadas con la energía.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-397">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="fc5f1-398"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-398"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-399">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-399">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="fc5f1-400"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-400"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-401">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-401">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="fc5f1-402"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-402"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-403">Se admite el método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="fc5f1-403">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="fc5f1-404">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-404">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="fc5f1-405">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-405">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="fc5f1-406"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-406"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-407">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="fc5f1-407">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="fc5f1-408"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-408"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="fc5f1-409">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o Interval, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-409">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fc5f1-410">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-410">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-411">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-411">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-412">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-413">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-413">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="fc5f1-414">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="fc5f1-414">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="fc5f1-415">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-415">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="fc5f1-416">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="fc5f1-416">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="fc5f1-417">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-418">**Estado**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-418">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-419">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-420">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-421">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-421">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-422">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-422">String that indicates the current status of the object.</span></span> <span data-ttu-id="fc5f1-423">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-423">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="fc5f1-424">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="fc5f1-424">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="fc5f1-425">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-425">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="fc5f1-426">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="fc5f1-426">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="fc5f1-427">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-427">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="fc5f1-428">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-428">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="fc5f1-429">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-429">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="fc5f1-430">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="fc5f1-430">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="fc5f1-431">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-431">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="fc5f1-432">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-432">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="fc5f1-433">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-433">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fc5f1-434">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-434">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="fc5f1-435">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-435">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="fc5f1-436">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-436">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="fc5f1-437">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-437">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="fc5f1-438">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-438">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="fc5f1-439">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-439">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="fc5f1-440">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-440">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="fc5f1-441">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-441">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="fc5f1-442">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-442">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc5f1-443">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-443">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-444">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-444">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-445">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-446">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="fc5f1-446">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-447">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-447">State of the logical device.</span></span> <span data-ttu-id="fc5f1-448">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="fc5f1-448">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="fc5f1-449">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-449">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fc5f1-450">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-450">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fc5f1-451">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-451">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="fc5f1-452">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-452">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="fc5f1-453">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-453">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="fc5f1-454">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-454">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fc5f1-455">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-455">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-456">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-457">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-458">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-458">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-459">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-459">The scoping system's creation class name.</span></span>

<span data-ttu-id="fc5f1-460">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-460">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc5f1-461">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-461">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5f1-462">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-463">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc5f1-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5f1-464">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fc5f1-464">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fc5f1-465">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-465">The scoping system's name.</span></span>

<span data-ttu-id="fc5f1-466">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-466">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc5f1-467">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc5f1-467">Remarks</span></span>

<span data-ttu-id="fc5f1-468">La **clase \_ MediaAccessDevice de CIM** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-468">The **CIM\_MediaAccessDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="fc5f1-469">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-469">WMI does not implement this class.</span></span> <span data-ttu-id="fc5f1-470">Para las clases derivadas de **CIM \_ MediaAccessDevice**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f1-470">For classes derived from **CIM\_MediaAccessDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="fc5f1-471">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-471">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fc5f1-472">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="fc5f1-472">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc5f1-473">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc5f1-473">Requirements</span></span>



| <span data-ttu-id="fc5f1-474">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc5f1-474">Requirement</span></span> | <span data-ttu-id="fc5f1-475">Value</span><span class="sxs-lookup"><span data-stu-id="fc5f1-475">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc5f1-476">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc5f1-476">Minimum supported client</span></span><br/> | <span data-ttu-id="fc5f1-477">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc5f1-477">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fc5f1-478">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc5f1-478">Minimum supported server</span></span><br/> | <span data-ttu-id="fc5f1-479">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc5f1-479">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fc5f1-480">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fc5f1-480">Namespace</span></span><br/>                | <span data-ttu-id="fc5f1-481">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fc5f1-481">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fc5f1-482">MOF</span><span class="sxs-lookup"><span data-stu-id="fc5f1-482">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc5f1-483"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc5f1-483"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc5f1-484">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fc5f1-484">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc5f1-485"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc5f1-485"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc5f1-486">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc5f1-486">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc5f1-487">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="fc5f1-487">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

