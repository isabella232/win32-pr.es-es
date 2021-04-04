---
description: La \_ clase de USBHub de CIM representa las capacidades y la administración de un concentrador USB.
ms.assetid: 33618963-3053-4c01-992e-aa6d9774f84b
ms.tgt_platform: multiple
title: CIM_USBHub (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBHub
- CIM_USBHub.Availability
- CIM_USBHub.Caption
- CIM_USBHub.ClassCode
- CIM_USBHub.ConfigManagerErrorCode
- CIM_USBHub.ConfigManagerUserConfig
- CIM_USBHub.CreationClassName
- CIM_USBHub.CurrentAlternateSettings
- CIM_USBHub.CurrentConfigValue
- CIM_USBHub.Description
- CIM_USBHub.DeviceID
- CIM_USBHub.ErrorCleared
- CIM_USBHub.ErrorDescription
- CIM_USBHub.GangSwitched
- CIM_USBHub.InstallDate
- CIM_USBHub.LastErrorCode
- CIM_USBHub.Name
- CIM_USBHub.NumberOfConfigs
- CIM_USBHub.NumberOfPorts
- CIM_USBHub.PNPDeviceID
- CIM_USBHub.PowerManagementCapabilities
- CIM_USBHub.PowerManagementSupported
- CIM_USBHub.ProtocolCode
- CIM_USBHub.Status
- CIM_USBHub.StatusInfo
- CIM_USBHub.SubclassCode
- CIM_USBHub.SystemCreationClassName
- CIM_USBHub.SystemName
- CIM_USBHub.USBVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9213b155b069b4aa19f2cbe910c0614f511ff8bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998077"
---
# <a name="cim_usbhub-class"></a><span data-ttu-id="56fde-103">CIM \_ USBHub (clase)</span><span class="sxs-lookup"><span data-stu-id="56fde-103">CIM\_USBHub class</span></span>

<span data-ttu-id="56fde-104">La clase de **\_ USBHub de CIM** representa las capacidades y la administración de un concentrador USB.</span><span class="sxs-lookup"><span data-stu-id="56fde-104">The **CIM\_USBHub** class represents the capabilities and management of a USB hub.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="56fde-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="56fde-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="56fde-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="56fde-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="56fde-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="56fde-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="56fde-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="56fde-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="56fde-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56fde-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBHub : CIM_USBDevice
{
  uint16   Availability;
  string   Caption;
  uint8    ClassCode;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint8    CurrentAlternateSettings[];
  uint8    CurrentConfigValue;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  boolean  GangSwitched;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint8    NumberOfConfigs;
  uint8    NumberOfPorts;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint8    ProtocolCode;
  string   Status;
  uint16   StatusInfo;
  uint8    SubclassCode;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   USBVersion;
};
```

## <a name="members"></a><span data-ttu-id="56fde-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="56fde-110">Members</span></span>

<span data-ttu-id="56fde-111">La clase de **\_ USBHub de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="56fde-111">The **CIM\_USBHub** class has these types of members:</span></span>

-   [<span data-ttu-id="56fde-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="56fde-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="56fde-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="56fde-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="56fde-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="56fde-114">Methods</span></span>

<span data-ttu-id="56fde-115">La clase de **\_ USBHub de CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="56fde-115">The **CIM\_USBHub** class has these methods.</span></span>



| <span data-ttu-id="56fde-116">Método</span><span class="sxs-lookup"><span data-stu-id="56fde-116">Method</span></span>                                                            | <span data-ttu-id="56fde-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="56fde-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56fde-118">**GetDescriptor**</span><span class="sxs-lookup"><span data-stu-id="56fde-118">**GetDescriptor**</span></span>](getdescriptor-method-in-class-cim-usbhub.md) | <span data-ttu-id="56fde-119">Devuelve el descriptor del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="56fde-119">Returns the USB device descriptor.</span></span> <span data-ttu-id="56fde-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="56fde-120">Not implemented by WMI.</span></span><br/>                                                                    |
| [<span data-ttu-id="56fde-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="56fde-121">**Reset**</span></span>](reset-method-in-class-cim-usbhub.md)                 | <span data-ttu-id="56fde-122">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="56fde-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="56fde-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="56fde-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="56fde-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="56fde-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-usbhub.md) | <span data-ttu-id="56fde-125">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="56fde-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="56fde-126">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="56fde-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="56fde-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="56fde-127">Properties</span></span>

<span data-ttu-id="56fde-128">La clase de **\_ USBHub de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="56fde-128">The **CIM\_USBHub** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="56fde-129">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="56fde-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-130">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56fde-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56fde-132">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="56fde-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="56fde-133">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56fde-133">Availability and status of the device.</span></span>

<span data-ttu-id="56fde-134">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="56fde-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="56fde-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="56fde-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="56fde-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="56fde-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="56fde-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-138">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="56fde-138">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="56fde-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="56fde-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="56fde-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="56fde-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="56fde-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="56fde-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="56fde-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="56fde-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="56fde-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="56fde-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="56fde-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="56fde-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="56fde-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="56fde-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="56fde-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="56fde-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="56fde-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="56fde-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="56fde-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="56fde-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-149">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="56fde-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="56fde-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="56fde-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-151">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="56fde-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="56fde-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="56fde-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-153">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="56fde-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="56fde-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="56fde-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="56fde-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="56fde-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-156">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="56fde-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="56fde-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="56fde-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-158">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="56fde-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="56fde-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="56fde-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-160">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="56fde-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="56fde-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="56fde-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-162">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="56fde-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="56fde-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="56fde-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-164">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="56fde-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="56fde-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="56fde-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="56fde-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56fde-168">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="56fde-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="56fde-169">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="56fde-169">Short textual description of the object.</span></span>

<span data-ttu-id="56fde-170">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-171">**ClassCode**</span><span class="sxs-lookup"><span data-stu-id="56fde-171">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-172">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="56fde-172">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56fde-174">Código de clase USB.</span><span class="sxs-lookup"><span data-stu-id="56fde-174">USB class code.</span></span>

<span data-ttu-id="56fde-175">Esta propiedad se hereda de [**\_ USBDevice CIM**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-175">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-176">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="56fde-176">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-177">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56fde-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56fde-179">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="56fde-179">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="56fde-180">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="56fde-180">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="56fde-181">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-181">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="56fde-182"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="56fde-182"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="56fde-183"> (0)</span><span class="sxs-lookup"><span data-stu-id="56fde-183">(0)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-184">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="56fde-184">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="56fde-185"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="56fde-185"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="56fde-186">(1)</span><span class="sxs-lookup"><span data-stu-id="56fde-186">(1)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-187">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="56fde-187">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="56fde-188"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56fde-188"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="56fde-189">(2)</span><span class="sxs-lookup"><span data-stu-id="56fde-189">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="56fde-190"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="56fde-190"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="56fde-191">(3)</span><span class="sxs-lookup"><span data-stu-id="56fde-191">(3)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-192">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="56fde-192">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="56fde-193"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="56fde-193"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="56fde-194">(4)</span><span class="sxs-lookup"><span data-stu-id="56fde-194">(4)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-195">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="56fde-195">Device is not working properly.</span></span> <span data-ttu-id="56fde-196">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="56fde-196">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="56fde-197"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="56fde-197"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="56fde-198">(5)</span><span class="sxs-lookup"><span data-stu-id="56fde-198">(5)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-199">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="56fde-199">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="56fde-200"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="56fde-200"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="56fde-201"> (6)</span><span class="sxs-lookup"><span data-stu-id="56fde-201">(6)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-202">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="56fde-202">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="56fde-203"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="56fde-203"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="56fde-204">(7)</span><span class="sxs-lookup"><span data-stu-id="56fde-204">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="56fde-205"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56fde-205"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="56fde-206">(8)</span><span class="sxs-lookup"><span data-stu-id="56fde-206">(8)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-207">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56fde-207">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="56fde-208"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="56fde-208"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="56fde-209">(9)</span><span class="sxs-lookup"><span data-stu-id="56fde-209">(9)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-210">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="56fde-210">Device is not working properly.</span></span> <span data-ttu-id="56fde-211">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56fde-211">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="56fde-212"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="56fde-212"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="56fde-213">(10)</span><span class="sxs-lookup"><span data-stu-id="56fde-213">(10)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-214">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="56fde-214">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="56fde-215"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56fde-215"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="56fde-216">(11)</span><span class="sxs-lookup"><span data-stu-id="56fde-216">(11)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-217">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56fde-217">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="56fde-218"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="56fde-218"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="56fde-219">(12)</span><span class="sxs-lookup"><span data-stu-id="56fde-219">(12)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-220">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="56fde-220">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="56fde-221"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56fde-221"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="56fde-222">(13)</span><span class="sxs-lookup"><span data-stu-id="56fde-222">(13)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-223">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56fde-223">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="56fde-224"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="56fde-224"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="56fde-225">(14)</span><span class="sxs-lookup"><span data-stu-id="56fde-225">(14)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-226">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="56fde-226">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="56fde-227"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="56fde-227"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="56fde-228">(15)</span><span class="sxs-lookup"><span data-stu-id="56fde-228">(15)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-229">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="56fde-229">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="56fde-230"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56fde-230"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="56fde-231">(16)</span><span class="sxs-lookup"><span data-stu-id="56fde-231">(16)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-232">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56fde-232">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="56fde-233"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="56fde-233"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="56fde-234">(17)</span><span class="sxs-lookup"><span data-stu-id="56fde-234">(17)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-235">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="56fde-235">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="56fde-236"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56fde-236"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="56fde-237">(18)</span><span class="sxs-lookup"><span data-stu-id="56fde-237">(18)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-238">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="56fde-238">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="56fde-239"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="56fde-239"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="56fde-240">(19)</span><span class="sxs-lookup"><span data-stu-id="56fde-240">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="56fde-241"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="56fde-241"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="56fde-242">(20)</span><span class="sxs-lookup"><span data-stu-id="56fde-242">(20)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-243">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="56fde-243">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="56fde-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56fde-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="56fde-245">(21)</span><span class="sxs-lookup"><span data-stu-id="56fde-245">(21)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-246">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="56fde-246">System failure.</span></span> <span data-ttu-id="56fde-247">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="56fde-247">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="56fde-248">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56fde-248">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="56fde-249"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="56fde-249"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="56fde-250">(22)</span><span class="sxs-lookup"><span data-stu-id="56fde-250">(22)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-251">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="56fde-251">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="56fde-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="56fde-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="56fde-253">(23)</span><span class="sxs-lookup"><span data-stu-id="56fde-253">(23)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-254">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="56fde-254">System failure.</span></span> <span data-ttu-id="56fde-255">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="56fde-255">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="56fde-256"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="56fde-256"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="56fde-257">(24)</span><span class="sxs-lookup"><span data-stu-id="56fde-257">(24)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-258">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="56fde-258">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="56fde-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56fde-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="56fde-260">(25)</span><span class="sxs-lookup"><span data-stu-id="56fde-260">(25)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-261">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56fde-261">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="56fde-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56fde-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="56fde-263">(26)</span><span class="sxs-lookup"><span data-stu-id="56fde-263">(26)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-264">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56fde-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="56fde-265"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="56fde-265"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="56fde-266">(27)</span><span class="sxs-lookup"><span data-stu-id="56fde-266">(27)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-267">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="56fde-267">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="56fde-268"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="56fde-268"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="56fde-269">(28)</span><span class="sxs-lookup"><span data-stu-id="56fde-269">(28)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-270">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="56fde-270">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="56fde-271"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="56fde-271"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="56fde-272">(29)</span><span class="sxs-lookup"><span data-stu-id="56fde-272">(29)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-273">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="56fde-273">Device is disabled.</span></span> <span data-ttu-id="56fde-274">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="56fde-274">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="56fde-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="56fde-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="56fde-276">(30)</span><span class="sxs-lookup"><span data-stu-id="56fde-276">(30)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-277">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="56fde-277">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="56fde-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="56fde-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="56fde-279">31</span><span class="sxs-lookup"><span data-stu-id="56fde-279">(31)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-280">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="56fde-280">Device is not working properly.</span></span> <span data-ttu-id="56fde-281">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="56fde-281">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="56fde-282">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="56fde-282">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-283">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="56fde-283">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56fde-285">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="56fde-285">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="56fde-286">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="56fde-286">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="56fde-287">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-288">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="56fde-288">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-289">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="56fde-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56fde-291">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="56fde-291">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="56fde-292">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="56fde-292">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="56fde-293">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="56fde-293">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="56fde-294">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-295">**CurrentAlternateSettings**</span><span class="sxs-lookup"><span data-stu-id="56fde-295">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-296">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="56fde-296">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="56fde-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56fde-298">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ USBDevice**](cim-usbdevice.md).**CurrentConfigValue**")</span><span class="sxs-lookup"><span data-stu-id="56fde-298">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_USBDevice**](cim-usbdevice.md).**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="56fde-299">Configuración alternativa de USB para cada interfaz en la configuración seleccionada actualmente (indicada por la propiedad **CurrentConfigValue** ).</span><span class="sxs-lookup"><span data-stu-id="56fde-299">USB alternate settings for each interface in the currently selected configuration (indicated by the **CurrentConfigValue** property).</span></span> <span data-ttu-id="56fde-300">Esta matriz tiene una entrada para cada interfaz de la configuración.</span><span class="sxs-lookup"><span data-stu-id="56fde-300">This array has one entry for each interface in the configuration.</span></span> <span data-ttu-id="56fde-301">Si la propiedad **CurrentConfigValue** tiene un valor de 0 (cero), lo que indica que el dispositivo no está configurado, la matriz no está definida.</span><span class="sxs-lookup"><span data-stu-id="56fde-301">If the **CurrentConfigValue** property has a value of 0 (zero), which indicates that the device is not configured, the array is undefined.</span></span> <span data-ttu-id="56fde-302">Para obtener más información sobre el análisis de esta cadena de octetos, consulte la especificación USB.</span><span class="sxs-lookup"><span data-stu-id="56fde-302">For more information about parsing this octet string, see the USB specification.</span></span>

<span data-ttu-id="56fde-303">Esta propiedad se hereda de [**\_ USBDevice CIM**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-303">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-304">**CurrentConfigValue**</span><span class="sxs-lookup"><span data-stu-id="56fde-304">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-305">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="56fde-305">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56fde-307">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ USBDevice**](cim-usbdevice.md).**CurrentAlternateSettings**")</span><span class="sxs-lookup"><span data-stu-id="56fde-307">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_USBDevice**](cim-usbdevice.md).**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="56fde-308">Configuración seleccionada actualmente para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56fde-308">Configuration currently selected for the device.</span></span> <span data-ttu-id="56fde-309">Si este valor es 0 (cero), el dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="56fde-309">If this value is 0 (zero), the device is unconfigured.</span></span>

<span data-ttu-id="56fde-310">Esta propiedad se hereda de [**\_ USBDevice CIM**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-310">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-311">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="56fde-311">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-312">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="56fde-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56fde-314">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="56fde-314">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="56fde-315">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="56fde-315">Textual description of the object.</span></span>

<span data-ttu-id="56fde-316">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-317">**ID**</span><span class="sxs-lookup"><span data-stu-id="56fde-317">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-318">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="56fde-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56fde-320">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="56fde-320">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="56fde-321">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="56fde-321">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="56fde-322">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-323">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="56fde-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-324">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="56fde-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56fde-326">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="56fde-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="56fde-327">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-328">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="56fde-328">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-329">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="56fde-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56fde-331">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="56fde-331">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="56fde-332">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-333">**GangSwitched**</span><span class="sxs-lookup"><span data-stu-id="56fde-333">**GangSwitched**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-334">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="56fde-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56fde-336">Si es **true**, la alimentación se cambia a todos los puertos del centro simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="56fde-336">If **TRUE**, power is switched to all ports on the hub simultaneously.</span></span> <span data-ttu-id="56fde-337">Si es **false**, la alimentación se cambia individualmente para cada puerto.</span><span class="sxs-lookup"><span data-stu-id="56fde-337">If **FALSE**, power is switched individually for each port.</span></span>

</dd> <dt>

<span data-ttu-id="56fde-338">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="56fde-338">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-339">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="56fde-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56fde-341">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="56fde-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="56fde-342">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="56fde-342">Date and time the object was installed.</span></span> <span data-ttu-id="56fde-343">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="56fde-343">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="56fde-344">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-345">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="56fde-345">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-346">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="56fde-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56fde-348">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="56fde-348">Last error code reported by the logical device.</span></span>

<span data-ttu-id="56fde-349">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-350">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="56fde-350">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-351">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="56fde-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-352">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56fde-353">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="56fde-353">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="56fde-354">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="56fde-354">Label by which the object is known.</span></span> <span data-ttu-id="56fde-355">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="56fde-355">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="56fde-356">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-356">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-357">**NumberOfConfigs**</span><span class="sxs-lookup"><span data-stu-id="56fde-357">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-358">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="56fde-358">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56fde-360">Número de configuraciones de dispositivo definidas para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56fde-360">Number of device configurations that are defined for the device.</span></span>

<span data-ttu-id="56fde-361">Esta propiedad se hereda de [**\_ USBDevice CIM**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-361">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-362">**NumberOfPorts**</span><span class="sxs-lookup"><span data-stu-id="56fde-362">**NumberOfPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-363">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="56fde-363">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-364">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56fde-365">Número de puertos de bajada en el concentrador, incluidos los insertados en el silicio del centro.</span><span class="sxs-lookup"><span data-stu-id="56fde-365">Number of downstream ports on the hub, including those embedded in the hub's silicon.</span></span>

</dd> <dt>

<span data-ttu-id="56fde-366">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="56fde-366">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-367">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="56fde-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56fde-369">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="56fde-369">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="56fde-370">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="56fde-370">Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="56fde-371">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="56fde-371">Example: "\*PNP030b"</span></span>

<span data-ttu-id="56fde-372">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-373">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="56fde-373">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-374">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56fde-374">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="56fde-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56fde-376">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="56fde-376">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="56fde-377">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="56fde-378"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="56fde-378"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="56fde-379"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="56fde-379"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="56fde-380"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="56fde-380"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="56fde-381"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="56fde-381"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-382">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="56fde-382">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="56fde-383"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="56fde-383"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-384">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="56fde-384">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="56fde-385"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="56fde-385"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-386">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="56fde-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="56fde-387">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="56fde-387">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="56fde-388">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="56fde-388">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="56fde-389"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="56fde-389"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-390">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="56fde-390">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="56fde-391"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="56fde-391"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="56fde-392">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="56fde-392">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="56fde-393">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="56fde-393">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-394">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="56fde-394">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-395">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56fde-396">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="56fde-396">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="56fde-397">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="56fde-397">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="56fde-398">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="56fde-398">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="56fde-399">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="56fde-399">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="56fde-400">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-401">**ProtocolCode**</span><span class="sxs-lookup"><span data-stu-id="56fde-401">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-402">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="56fde-402">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56fde-404">Código de protocolo USB.</span><span class="sxs-lookup"><span data-stu-id="56fde-404">USB protocol code.</span></span>

<span data-ttu-id="56fde-405">Esta propiedad se hereda de [**\_ USBDevice CIM**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-405">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-406">**Estado**</span><span class="sxs-lookup"><span data-stu-id="56fde-406">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-407">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="56fde-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-408">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56fde-409">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="56fde-409">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="56fde-410">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="56fde-410">Current status of the object.</span></span>

<span data-ttu-id="56fde-411">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-411">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="56fde-412">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="56fde-412">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="56fde-413">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="56fde-413">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="56fde-414">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="56fde-414">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="56fde-415">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="56fde-415">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="56fde-416">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="56fde-416">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="56fde-417">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="56fde-417">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="56fde-418">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="56fde-418">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="56fde-419">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="56fde-419">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="56fde-420">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="56fde-420">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="56fde-421">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="56fde-421">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="56fde-422">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="56fde-422">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="56fde-423">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="56fde-423">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="56fde-424">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="56fde-424">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="56fde-425">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="56fde-425">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-426">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56fde-426">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-427">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56fde-428">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="56fde-428">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="56fde-429">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="56fde-429">State of the logical device.</span></span> <span data-ttu-id="56fde-430">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="56fde-430">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="56fde-431">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="56fde-432">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="56fde-432">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="56fde-433">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="56fde-433">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="56fde-434">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="56fde-434">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="56fde-435">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="56fde-435">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="56fde-436">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="56fde-436">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="56fde-437">**SubclassCode**</span><span class="sxs-lookup"><span data-stu-id="56fde-437">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-438">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="56fde-438">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-439">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56fde-440">Código de subclase USB.</span><span class="sxs-lookup"><span data-stu-id="56fde-440">USB subclass code.</span></span>

<span data-ttu-id="56fde-441">Esta propiedad se hereda de [**\_ USBDevice CIM**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-441">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-442">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="56fde-442">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-443">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="56fde-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-444">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56fde-445">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="56fde-445">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="56fde-446">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="56fde-446">Scoping system's creation class name.</span></span>

<span data-ttu-id="56fde-447">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-448">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="56fde-448">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-449">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="56fde-449">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-450">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56fde-451">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="56fde-451">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="56fde-452">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="56fde-452">Scoping system's name.</span></span>

<span data-ttu-id="56fde-453">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-453">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="56fde-454">**USBVersion**</span><span class="sxs-lookup"><span data-stu-id="56fde-454">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56fde-455">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="56fde-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56fde-456">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56fde-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56fde-457">Versión USB más reciente compatible con el dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="56fde-457">Latest USB version supported by the USB device.</span></span> <span data-ttu-id="56fde-458">Esta propiedad se expresa como un decimal con codificación binaria (BCD) donde se implica un punto decimal entre el segundo y el tercer dígito.</span><span class="sxs-lookup"><span data-stu-id="56fde-458">This property is expressed as a binary-coded decimal (BCD) where a decimal point is implied between the second and third digits.</span></span> <span data-ttu-id="56fde-459">Por ejemplo, un valor de 0x201 indica que se admite la versión 2,01.</span><span class="sxs-lookup"><span data-stu-id="56fde-459">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

<span data-ttu-id="56fde-460">Esta propiedad se hereda de [**\_ USBDevice CIM**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-460">This property is inherited from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56fde-461">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56fde-461">Remarks</span></span>

<span data-ttu-id="56fde-462">La clase de **\_ USBHub de CIM** se deriva de [**\_ USBDevice de CIM**](cim-usbdevice.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-462">The **CIM\_USBHub** class is derived from [**CIM\_USBDevice**](cim-usbdevice.md).</span></span>

<span data-ttu-id="56fde-463">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="56fde-463">WMI does not implement this class.</span></span> <span data-ttu-id="56fde-464">Para las clases WMI derivadas de la **\_ USBHub de CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="56fde-464">For WMI classes derived from **CIM\_USBHub**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="56fde-465">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="56fde-465">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="56fde-466">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="56fde-466">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="56fde-467">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56fde-467">Requirements</span></span>



| <span data-ttu-id="56fde-468">Requisito</span><span class="sxs-lookup"><span data-stu-id="56fde-468">Requirement</span></span> | <span data-ttu-id="56fde-469">Value</span><span class="sxs-lookup"><span data-stu-id="56fde-469">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56fde-470">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56fde-470">Minimum supported client</span></span><br/> | <span data-ttu-id="56fde-471">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56fde-471">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="56fde-472">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56fde-472">Minimum supported server</span></span><br/> | <span data-ttu-id="56fde-473">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56fde-473">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="56fde-474">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="56fde-474">Namespace</span></span><br/>                | <span data-ttu-id="56fde-475">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="56fde-475">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="56fde-476">MOF</span><span class="sxs-lookup"><span data-stu-id="56fde-476">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56fde-477"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56fde-477"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="56fde-478">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="56fde-478">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56fde-479"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56fde-479"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56fde-480">Vea también</span><span class="sxs-lookup"><span data-stu-id="56fde-480">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56fde-481">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="56fde-481">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> </dl>

 

