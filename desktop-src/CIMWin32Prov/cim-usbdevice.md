---
description: La \_ clase CIM USBDevice representa las características de administración de un dispositivo USB.
ms.assetid: 0ff39701-826a-434b-a628-0af586600a80
ms.tgt_platform: multiple
title: CIM_USBDevice (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice
- CIM_USBDevice.Availability
- CIM_USBDevice.Caption
- CIM_USBDevice.ClassCode
- CIM_USBDevice.ConfigManagerErrorCode
- CIM_USBDevice.ConfigManagerUserConfig
- CIM_USBDevice.CreationClassName
- CIM_USBDevice.CurrentAlternateSettings
- CIM_USBDevice.CurrentConfigValue
- CIM_USBDevice.Description
- CIM_USBDevice.DeviceID
- CIM_USBDevice.ErrorCleared
- CIM_USBDevice.ErrorDescription
- CIM_USBDevice.InstallDate
- CIM_USBDevice.LastErrorCode
- CIM_USBDevice.Name
- CIM_USBDevice.NumberOfConfigs
- CIM_USBDevice.PNPDeviceID
- CIM_USBDevice.PowerManagementCapabilities
- CIM_USBDevice.PowerManagementSupported
- CIM_USBDevice.ProtocolCode
- CIM_USBDevice.Status
- CIM_USBDevice.StatusInfo
- CIM_USBDevice.SubclassCode
- CIM_USBDevice.SystemCreationClassName
- CIM_USBDevice.SystemName
- CIM_USBDevice.USBVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 21b927980716d4ee7ee2e22a352c5c3b34b363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152770"
---
# <a name="cim_usbdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="22ed5-103">CIM_USBDevice (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="22ed5-103">CIM_USBDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="22ed5-104">La clase **CIM \_ USBDevice** representa las características de administración de un dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="22ed5-104">The **CIM\_USBDevice** class represents the management characteristics of a USB device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22ed5-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="22ed5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="22ed5-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="22ed5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="22ed5-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="22ed5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="22ed5-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="22ed5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="22ed5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22ed5-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBDevice : CIM_LogicalDevice
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
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint8    NumberOfConfigs;
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

## <a name="members"></a><span data-ttu-id="22ed5-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="22ed5-110">Members</span></span>

<span data-ttu-id="22ed5-111">La clase **CIM \_ USBDevice** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="22ed5-111">The **CIM\_USBDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="22ed5-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="22ed5-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="22ed5-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="22ed5-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="22ed5-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="22ed5-114">Methods</span></span>

<span data-ttu-id="22ed5-115">La clase **CIM \_ USBDevice** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="22ed5-115">The **CIM\_USBDevice** class has these methods.</span></span>



| <span data-ttu-id="22ed5-116">Método</span><span class="sxs-lookup"><span data-stu-id="22ed5-116">Method</span></span>                                                               | <span data-ttu-id="22ed5-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="22ed5-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22ed5-118">**GetDescriptor**</span><span class="sxs-lookup"><span data-stu-id="22ed5-118">**GetDescriptor**</span></span>](getdescriptor-method-in-class-cim-usbdevice.md) | <span data-ttu-id="22ed5-119">Devuelve el descriptor del dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="22ed5-119">Returns the USB device descriptor.</span></span> <span data-ttu-id="22ed5-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="22ed5-120">Not implemented by WMI.</span></span><br/>                                                                    |
| [<span data-ttu-id="22ed5-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="22ed5-121">**Reset**</span></span>](reset-method-in-class-cim-usbdevice.md)                 | <span data-ttu-id="22ed5-122">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="22ed5-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="22ed5-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="22ed5-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="22ed5-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="22ed5-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-usbdevice.md) | <span data-ttu-id="22ed5-125">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="22ed5-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="22ed5-126">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="22ed5-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="22ed5-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="22ed5-127">Properties</span></span>

<span data-ttu-id="22ed5-128">La clase **CIM \_ USBDevice** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="22ed5-128">The **CIM\_USBDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22ed5-129">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="22ed5-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-130">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22ed5-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-132">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="22ed5-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-133">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22ed5-133">Availability and status of the device.</span></span>

<span data-ttu-id="22ed5-134">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="22ed5-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="22ed5-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22ed5-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="22ed5-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="22ed5-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="22ed5-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-138">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="22ed5-138">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="22ed5-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="22ed5-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="22ed5-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="22ed5-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="22ed5-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="22ed5-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="22ed5-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="22ed5-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="22ed5-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="22ed5-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="22ed5-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="22ed5-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="22ed5-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="22ed5-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="22ed5-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="22ed5-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="22ed5-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="22ed5-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="22ed5-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="22ed5-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-149">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="22ed5-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="22ed5-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="22ed5-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-151">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="22ed5-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="22ed5-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="22ed5-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-153">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="22ed5-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="22ed5-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="22ed5-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="22ed5-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="22ed5-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-156">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="22ed5-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="22ed5-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="22ed5-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-158">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="22ed5-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="22ed5-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="22ed5-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-160">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="22ed5-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="22ed5-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="22ed5-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-162">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="22ed5-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="22ed5-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="22ed5-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-164">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="22ed5-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="22ed5-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="22ed5-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22ed5-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-168">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="22ed5-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-169">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="22ed5-169">Short textual description of the object.</span></span>

<span data-ttu-id="22ed5-170">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-171">**ClassCode**</span><span class="sxs-lookup"><span data-stu-id="22ed5-171">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-172">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="22ed5-172">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-174">Código de clase USB.</span><span class="sxs-lookup"><span data-stu-id="22ed5-174">USB class code.</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="22ed5-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-176">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22ed5-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-178">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="22ed5-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-179">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="22ed5-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="22ed5-180">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="22ed5-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="22ed5-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="22ed5-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-183">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="22ed5-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="22ed5-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="22ed5-185">(1)</span><span class="sxs-lookup"><span data-stu-id="22ed5-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-186">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="22ed5-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="22ed5-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="22ed5-188">(2)</span><span class="sxs-lookup"><span data-stu-id="22ed5-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="22ed5-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="22ed5-190">(3)</span><span class="sxs-lookup"><span data-stu-id="22ed5-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-191">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="22ed5-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="22ed5-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="22ed5-193">(4)</span><span class="sxs-lookup"><span data-stu-id="22ed5-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-194">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="22ed5-194">Device is not working properly.</span></span> <span data-ttu-id="22ed5-195">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="22ed5-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="22ed5-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="22ed5-197">(5)</span><span class="sxs-lookup"><span data-stu-id="22ed5-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-198">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="22ed5-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="22ed5-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="22ed5-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="22ed5-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-201">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="22ed5-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="22ed5-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="22ed5-203">(7)</span><span class="sxs-lookup"><span data-stu-id="22ed5-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="22ed5-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="22ed5-205">(8)</span><span class="sxs-lookup"><span data-stu-id="22ed5-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-206">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22ed5-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="22ed5-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="22ed5-208">(9)</span><span class="sxs-lookup"><span data-stu-id="22ed5-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-209">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="22ed5-209">Device is not working properly.</span></span> <span data-ttu-id="22ed5-210">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22ed5-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="22ed5-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="22ed5-212">(10)</span><span class="sxs-lookup"><span data-stu-id="22ed5-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-213">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="22ed5-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="22ed5-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="22ed5-215">(11)</span><span class="sxs-lookup"><span data-stu-id="22ed5-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-216">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22ed5-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="22ed5-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="22ed5-218">(12)</span><span class="sxs-lookup"><span data-stu-id="22ed5-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-219">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="22ed5-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="22ed5-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="22ed5-221">(13)</span><span class="sxs-lookup"><span data-stu-id="22ed5-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-222">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22ed5-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="22ed5-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="22ed5-224">(14)</span><span class="sxs-lookup"><span data-stu-id="22ed5-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-225">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="22ed5-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="22ed5-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="22ed5-227">(15)</span><span class="sxs-lookup"><span data-stu-id="22ed5-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-228">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="22ed5-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="22ed5-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="22ed5-230">(16)</span><span class="sxs-lookup"><span data-stu-id="22ed5-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-231">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22ed5-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="22ed5-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="22ed5-233">(17)</span><span class="sxs-lookup"><span data-stu-id="22ed5-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-234">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="22ed5-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="22ed5-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="22ed5-236">(18)</span><span class="sxs-lookup"><span data-stu-id="22ed5-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-237">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="22ed5-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="22ed5-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="22ed5-239">(19)</span><span class="sxs-lookup"><span data-stu-id="22ed5-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="22ed5-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="22ed5-241">(20)</span><span class="sxs-lookup"><span data-stu-id="22ed5-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-242">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="22ed5-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="22ed5-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="22ed5-244">(21)</span><span class="sxs-lookup"><span data-stu-id="22ed5-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-245">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="22ed5-245">System failure.</span></span> <span data-ttu-id="22ed5-246">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="22ed5-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="22ed5-247">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22ed5-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="22ed5-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="22ed5-249">(22)</span><span class="sxs-lookup"><span data-stu-id="22ed5-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-250">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="22ed5-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="22ed5-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="22ed5-252">(23)</span><span class="sxs-lookup"><span data-stu-id="22ed5-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-253">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="22ed5-253">System failure.</span></span> <span data-ttu-id="22ed5-254">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="22ed5-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="22ed5-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="22ed5-256">(24)</span><span class="sxs-lookup"><span data-stu-id="22ed5-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-257">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="22ed5-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="22ed5-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="22ed5-259">(25)</span><span class="sxs-lookup"><span data-stu-id="22ed5-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-260">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22ed5-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="22ed5-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="22ed5-262">(26)</span><span class="sxs-lookup"><span data-stu-id="22ed5-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-263">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22ed5-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="22ed5-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="22ed5-265">(27)</span><span class="sxs-lookup"><span data-stu-id="22ed5-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-266">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="22ed5-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="22ed5-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="22ed5-268">(28)</span><span class="sxs-lookup"><span data-stu-id="22ed5-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-269">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="22ed5-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="22ed5-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="22ed5-271">(29)</span><span class="sxs-lookup"><span data-stu-id="22ed5-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-272">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="22ed5-272">Device is disabled.</span></span> <span data-ttu-id="22ed5-273">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="22ed5-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="22ed5-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="22ed5-275">(30)</span><span class="sxs-lookup"><span data-stu-id="22ed5-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-276">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="22ed5-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="22ed5-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="22ed5-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="22ed5-278">31</span><span class="sxs-lookup"><span data-stu-id="22ed5-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-279">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="22ed5-279">Device is not working properly.</span></span> <span data-ttu-id="22ed5-280">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="22ed5-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="22ed5-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="22ed5-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-282">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22ed5-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-284">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="22ed5-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-285">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="22ed5-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="22ed5-286">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="22ed5-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-288">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22ed5-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-290">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="22ed5-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-291">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="22ed5-291">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="22ed5-292">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="22ed5-292">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="22ed5-293">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-294">**CurrentAlternateSettings**</span><span class="sxs-lookup"><span data-stu-id="22ed5-294">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-295">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="22ed5-295">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-297">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentConfigValue**")</span><span class="sxs-lookup"><span data-stu-id="22ed5-297">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-298">Configuración alternativa de USB para cada interfaz en la configuración seleccionada actualmente (indicada por la propiedad **CurrentConfigValue** ).</span><span class="sxs-lookup"><span data-stu-id="22ed5-298">USB alternate settings for each interface in the currently selected configuration (indicated by the **CurrentConfigValue** property).</span></span> <span data-ttu-id="22ed5-299">Esta matriz tiene una entrada para cada interfaz de la configuración.</span><span class="sxs-lookup"><span data-stu-id="22ed5-299">This array has one entry for each interface in the configuration.</span></span> <span data-ttu-id="22ed5-300">Si la propiedad **CurrentConfigValue** tiene un valor de 0 (cero), lo que indica que el dispositivo no está configurado, la matriz no está definida.</span><span class="sxs-lookup"><span data-stu-id="22ed5-300">If the **CurrentConfigValue** property has a value of 0 (zero), which indicates that the device is not configured, the array is undefined.</span></span> <span data-ttu-id="22ed5-301">Para obtener más información sobre el análisis de esta cadena de octetos, consulte la especificación USB.</span><span class="sxs-lookup"><span data-stu-id="22ed5-301">For more information about parsing this octet string, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-302">**CurrentConfigValue**</span><span class="sxs-lookup"><span data-stu-id="22ed5-302">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-303">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="22ed5-303">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-305">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ USBDevice**.**CurrentAlternateSettings**")</span><span class="sxs-lookup"><span data-stu-id="22ed5-305">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-306">Configuración seleccionada actualmente para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22ed5-306">Configuration currently selected for the device.</span></span> <span data-ttu-id="22ed5-307">Si el valor es 0 (cero), el dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="22ed5-307">If the value is 0 (zero), the device is unconfigured.</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-308">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="22ed5-308">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-309">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22ed5-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-311">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="22ed5-311">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-312">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="22ed5-312">Textual description of the object.</span></span>

<span data-ttu-id="22ed5-313">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-314">**ID**</span><span class="sxs-lookup"><span data-stu-id="22ed5-314">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-315">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22ed5-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-317">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="22ed5-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-318">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="22ed5-318">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="22ed5-319">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="22ed5-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-321">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22ed5-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-323">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="22ed5-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="22ed5-324">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="22ed5-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-326">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22ed5-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-328">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="22ed5-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="22ed5-329">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-330">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="22ed5-330">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-331">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="22ed5-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-333">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="22ed5-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-334">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="22ed5-334">Date and time the object was installed.</span></span> <span data-ttu-id="22ed5-335">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="22ed5-335">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="22ed5-336">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-336">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-337">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="22ed5-337">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-338">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22ed5-338">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-340">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="22ed5-340">Last error code reported by the logical device.</span></span>

<span data-ttu-id="22ed5-341">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-342">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="22ed5-342">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-343">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22ed5-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-345">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="22ed5-345">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-346">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="22ed5-346">Label by which the object is known.</span></span> <span data-ttu-id="22ed5-347">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="22ed5-347">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="22ed5-348">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-349">**NumberOfConfigs**</span><span class="sxs-lookup"><span data-stu-id="22ed5-349">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-350">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="22ed5-350">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-352">Número de configuraciones de dispositivo definidas para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22ed5-352">Number of device configurations that are defined for the device.</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-353">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="22ed5-353">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-354">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22ed5-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-356">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="22ed5-356">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-357">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="22ed5-357">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="22ed5-358">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="22ed5-359">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="22ed5-359">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-360">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="22ed5-360">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-361">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22ed5-361">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-363">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="22ed5-363">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="22ed5-364">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="22ed5-364">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22ed5-365"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="22ed5-365"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="22ed5-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="22ed5-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="22ed5-367"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="22ed5-367"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="22ed5-368"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="22ed5-368"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-369">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="22ed5-369">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="22ed5-370"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="22ed5-370"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-371">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="22ed5-371">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="22ed5-372"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="22ed5-372"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-373">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="22ed5-373">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="22ed5-374">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="22ed5-374">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="22ed5-375">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="22ed5-375">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="22ed5-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="22ed5-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-377">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="22ed5-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="22ed5-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="22ed5-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="22ed5-379">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="22ed5-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="22ed5-380">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="22ed5-380">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-381">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22ed5-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-383">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="22ed5-383">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="22ed5-384">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="22ed5-384">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="22ed5-385">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="22ed5-385">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="22ed5-386">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="22ed5-386">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="22ed5-387">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-387">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-388">**ProtocolCode**</span><span class="sxs-lookup"><span data-stu-id="22ed5-388">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-389">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="22ed5-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-391">Código de protocolo USB.</span><span class="sxs-lookup"><span data-stu-id="22ed5-391">USB protocol code.</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-392">**Estado**</span><span class="sxs-lookup"><span data-stu-id="22ed5-392">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-393">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22ed5-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-395">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="22ed5-395">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-396">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="22ed5-396">Current status of the object.</span></span> <span data-ttu-id="22ed5-397">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-397">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="22ed5-398">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="22ed5-398">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="22ed5-399">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="22ed5-399">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="22ed5-400">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="22ed5-400">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="22ed5-401">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="22ed5-401">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22ed5-402">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="22ed5-402">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="22ed5-403">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="22ed5-403">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="22ed5-404">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="22ed5-404">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="22ed5-405">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="22ed5-405">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="22ed5-406">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="22ed5-406">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="22ed5-407">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="22ed5-407">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="22ed5-408">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="22ed5-408">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="22ed5-409">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="22ed5-409">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="22ed5-410">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="22ed5-410">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="22ed5-411">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="22ed5-411">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-412">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22ed5-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-414">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="22ed5-414">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-415">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="22ed5-415">State of the logical device.</span></span> <span data-ttu-id="22ed5-416">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="22ed5-416">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="22ed5-417">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="22ed5-418">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="22ed5-418">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22ed5-419">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="22ed5-419">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="22ed5-420">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="22ed5-420">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="22ed5-421">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="22ed5-421">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="22ed5-422">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="22ed5-422">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="22ed5-423">**SubclassCode**</span><span class="sxs-lookup"><span data-stu-id="22ed5-423">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-424">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="22ed5-424">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-425">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-426">Código de subclase USB.</span><span class="sxs-lookup"><span data-stu-id="22ed5-426">USB subclass code.</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="22ed5-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-428">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22ed5-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-429">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-430">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="22ed5-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-431">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="22ed5-431">Scoping system's creation class name.</span></span>

<span data-ttu-id="22ed5-432">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="22ed5-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-434">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22ed5-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-436">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="22ed5-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-437">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="22ed5-437">Scoping system's name.</span></span>

<span data-ttu-id="22ed5-438">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="22ed5-439">**USBVersion**</span><span class="sxs-lookup"><span data-stu-id="22ed5-439">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22ed5-440">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22ed5-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22ed5-441">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22ed5-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22ed5-442">Versión USB más reciente compatible con el dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="22ed5-442">Latest USB version supported by the USB device.</span></span> <span data-ttu-id="22ed5-443">Esta propiedad se expresa como un decimal con codificación binaria (BCD) donde se implica un punto decimal entre el segundo y el tercer dígito.</span><span class="sxs-lookup"><span data-stu-id="22ed5-443">This property is expressed as a binary-coded decimal (BCD) where a decimal point is implied between the second and third digits.</span></span> <span data-ttu-id="22ed5-444">Por ejemplo, un valor de 0x201 indica que se admite la versión 2,01.</span><span class="sxs-lookup"><span data-stu-id="22ed5-444">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22ed5-445">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22ed5-445">Remarks</span></span>

<span data-ttu-id="22ed5-446">La **clase \_ USBDevice de CIM** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-446">The **CIM\_USBDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="22ed5-447">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="22ed5-447">WMI does not implement this class.</span></span> <span data-ttu-id="22ed5-448">Para las clases WMI que implementan **\_ USBDevice CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="22ed5-448">For WMI classes that implement **CIM\_USBDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="22ed5-449">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="22ed5-449">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="22ed5-450">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="22ed5-450">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="22ed5-451">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22ed5-451">Requirements</span></span>



| <span data-ttu-id="22ed5-452">Requisito</span><span class="sxs-lookup"><span data-stu-id="22ed5-452">Requirement</span></span> | <span data-ttu-id="22ed5-453">Value</span><span class="sxs-lookup"><span data-stu-id="22ed5-453">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22ed5-454">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22ed5-454">Minimum supported client</span></span><br/> | <span data-ttu-id="22ed5-455">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22ed5-455">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="22ed5-456">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22ed5-456">Minimum supported server</span></span><br/> | <span data-ttu-id="22ed5-457">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22ed5-457">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="22ed5-458">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="22ed5-458">Namespace</span></span><br/>                | <span data-ttu-id="22ed5-459">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="22ed5-459">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="22ed5-460">MOF</span><span class="sxs-lookup"><span data-stu-id="22ed5-460">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22ed5-461"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22ed5-461"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="22ed5-462">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="22ed5-462">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22ed5-463"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22ed5-463"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22ed5-464">Vea también</span><span class="sxs-lookup"><span data-stu-id="22ed5-464">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22ed5-465">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="22ed5-465">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

