---
description: La \_ clase WMI SerialPort de Win32 representa un puerto serie de un equipo que ejecuta Windows.
ms.assetid: f2e5cc5a-a12b-4079-92e1-6bb62fe797a0
ms.tgt_platform: multiple
title: Win32_SerialPort (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPort
- Win32_SerialPort.Reset
- Win32_SerialPort.SetPowerState
- Win32_SerialPort.Availability
- Win32_SerialPort.Binary
- Win32_SerialPort.Capabilities
- Win32_SerialPort.CapabilityDescriptions
- Win32_SerialPort.Caption
- Win32_SerialPort.ConfigManagerErrorCode
- Win32_SerialPort.ConfigManagerUserConfig
- Win32_SerialPort.CreationClassName
- Win32_SerialPort.Description
- Win32_SerialPort.DeviceID
- Win32_SerialPort.ErrorCleared
- Win32_SerialPort.ErrorDescription
- Win32_SerialPort.InstallDate
- Win32_SerialPort.LastErrorCode
- Win32_SerialPort.MaxBaudRate
- Win32_SerialPort.MaximumInputBufferSize
- Win32_SerialPort.MaximumOutputBufferSize
- Win32_SerialPort.MaxNumberControlled
- Win32_SerialPort.Name
- Win32_SerialPort.OSAutoDiscovered
- Win32_SerialPort.PNPDeviceID
- Win32_SerialPort.PowerManagementCapabilities
- Win32_SerialPort.PowerManagementSupported
- Win32_SerialPort.ProtocolSupported
- Win32_SerialPort.ProviderType
- Win32_SerialPort.SettableBaudRate
- Win32_SerialPort.SettableDataBits
- Win32_SerialPort.SettableFlowControl
- Win32_SerialPort.SettableParity
- Win32_SerialPort.SettableParityCheck
- Win32_SerialPort.SettableRLSD
- Win32_SerialPort.SettableStopBits
- Win32_SerialPort.Status
- Win32_SerialPort.StatusInfo
- Win32_SerialPort.Supports16BitMode
- Win32_SerialPort.SupportsDTRDSR
- Win32_SerialPort.SupportsElapsedTimeouts
- Win32_SerialPort.SupportsIntTimeouts
- Win32_SerialPort.SupportsParityCheck
- Win32_SerialPort.SupportsRLSD
- Win32_SerialPort.SupportsRTSCTS
- Win32_SerialPort.SupportsSpecialCharacters
- Win32_SerialPort.SupportsXOnXOff
- Win32_SerialPort.SupportsXOnXOffSet
- Win32_SerialPort.SystemCreationClassName
- Win32_SerialPort.SystemName
- Win32_SerialPort.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7fc2f25bc88d880ba9b10f10b5efde284a62624
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152825"
---
# <a name="win32_serialport-class"></a><span data-ttu-id="5c56f-103">\_Clase SerialPort de Win32</span><span class="sxs-lookup"><span data-stu-id="5c56f-103">Win32\_SerialPort class</span></span>

<span data-ttu-id="5c56f-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SerialPort de Win32** representa un puerto serie de un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="5c56f-104">The **Win32\_SerialPort** [WMI class](../wmisdk/retrieving-a-class.md) represents a serial port on a computer system running Windows.</span></span>

<span data-ttu-id="5c56f-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5c56f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5c56f-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="5c56f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c56f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c56f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPort : CIM_SerialController
{
  uint16   Availability;
  boolean  Binary;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRate;
  uint32   MaximumInputBufferSize;
  uint32   MaximumOutputBufferSize;
  uint32   MaxNumberControlled;
  string   Name;
  boolean  OSAutoDiscovered;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   ProviderType;
  boolean  SettableBaudRate;
  boolean  SettableDataBits;
  boolean  SettableFlowControl;
  boolean  SettableParity;
  boolean  SettableParityCheck;
  boolean  SettableRLSD;
  boolean  SettableStopBits;
  string   Status;
  uint16   StatusInfo;
  boolean  Supports16BitMode;
  boolean  SupportsDTRDSR;
  boolean  SupportsElapsedTimeouts;
  boolean  SupportsIntTimeouts;
  boolean  SupportsParityCheck;
  boolean  SupportsRLSD;
  boolean  SupportsRTSCTS;
  boolean  SupportsSpecialCharacters;
  boolean  SupportsXOnXOff;
  boolean  SupportsXOnXOffSet;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="5c56f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5c56f-108">Members</span></span>

<span data-ttu-id="5c56f-109">La **clase \_ SerialPort de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5c56f-109">The **Win32\_SerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="5c56f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c56f-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5c56f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c56f-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5c56f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c56f-112">Methods</span></span>

<span data-ttu-id="5c56f-113">La **clase \_ SerialPort de Win32** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5c56f-113">The **Win32\_SerialPort** class has these methods.</span></span>



| <span data-ttu-id="5c56f-114">Método</span><span class="sxs-lookup"><span data-stu-id="5c56f-114">Method</span></span>            | <span data-ttu-id="5c56f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c56f-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c56f-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="5c56f-116">**Reset**</span></span>         | <span data-ttu-id="5c56f-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="5c56f-117">Not implemented.</span></span> <span data-ttu-id="5c56f-118">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ SerialController**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_SerialController**](cim-serialcontroller.md).</span></span><br/>                 |
| <span data-ttu-id="5c56f-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5c56f-119">**SetPowerState**</span></span> | <span data-ttu-id="5c56f-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="5c56f-120">Not implemented.</span></span> <span data-ttu-id="5c56f-121">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ SerialController**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_SerialController**](cim-serialcontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5c56f-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c56f-122">Properties</span></span>

<span data-ttu-id="5c56f-123">La **clase \_ SerialPort de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5c56f-123">The **Win32\_SerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c56f-124">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="5c56f-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c56f-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-127">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="5c56f-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-128">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-128">Availability and status of the device.</span></span>

<span data-ttu-id="5c56f-129">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5c56f-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5c56f-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5c56f-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5c56f-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="5c56f-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="5c56f-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-133">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="5c56f-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="5c56f-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="5c56f-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="5c56f-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="5c56f-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5c56f-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="5c56f-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="5c56f-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="5c56f-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="5c56f-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="5c56f-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="5c56f-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="5c56f-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5c56f-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="5c56f-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="5c56f-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="5c56f-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="5c56f-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="5c56f-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="5c56f-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="5c56f-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-144">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="5c56f-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="5c56f-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="5c56f-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-146">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="5c56f-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="5c56f-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="5c56f-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-148">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="5c56f-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="5c56f-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="5c56f-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="5c56f-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="5c56f-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-151">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="5c56f-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="5c56f-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="5c56f-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-153">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="5c56f-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="5c56f-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="5c56f-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-155">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="5c56f-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="5c56f-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-157">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="5c56f-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="5c56f-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="5c56f-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-159">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="5c56f-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5c56f-160">**Binario**</span><span class="sxs-lookup"><span data-stu-id="5c56f-160">**Binary**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-161">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-163">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary")</span><span class="sxs-lookup"><span data-stu-id="5c56f-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fBinary")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-164">Si es **true**, el puerto serie está configurado para la transferencia de datos binarios.</span><span class="sxs-lookup"><span data-stu-id="5c56f-164">If **TRUE**, the serial port is configured for binary data transfer.</span></span> <span data-ttu-id="5c56f-165">Dado que la API de Windows no admite transferencias en modo no binario, esta propiedad debe ser **true**.</span><span class="sxs-lookup"><span data-stu-id="5c56f-165">Because the Windows API does not support nonbinary mode transfers, this property must be **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-166">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="5c56f-166">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-167">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c56f-167">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-169">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Puertos serie DMTF \| 004,7 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ SerialController**](cim-serialcontroller.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="5c56f-169">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_SerialController**](cim-serialcontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-170">Matriz de compatibilidad de nivel de chip para el controlador serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-170">Array of chip-level compatibility for the serial controller.</span></span> <span data-ttu-id="5c56f-171">Esta propiedad describe el almacenamiento en búfer y otras funciones del controlador serie que pueden ser inherentes en el hardware del chip.</span><span class="sxs-lookup"><span data-stu-id="5c56f-171">This property describes the buffering and other capabilities of the serial controller that may be inherent in the chip hardware.</span></span> <span data-ttu-id="5c56f-172">La propiedad es un entero enumerado.</span><span class="sxs-lookup"><span data-stu-id="5c56f-172">The property is an enumerated integer.</span></span>

<span data-ttu-id="5c56f-173">Esta propiedad se hereda de [**\_ SerialController CIM**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-173">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5c56f-174">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5c56f-174">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5c56f-175">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5c56f-175">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="5c56f-176">**XT/at compatible** (3)</span><span class="sxs-lookup"><span data-stu-id="5c56f-176">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="5c56f-177">**compatible con 16450** (4)</span><span class="sxs-lookup"><span data-stu-id="5c56f-177">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="5c56f-178">**16550 compatible** (5)</span><span class="sxs-lookup"><span data-stu-id="5c56f-178">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="5c56f-179">**compatible con 16550A** (6)</span><span class="sxs-lookup"><span data-stu-id="5c56f-179">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="5c56f-180">**compatible con 8251** (160)</span><span class="sxs-lookup"><span data-stu-id="5c56f-180">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="5c56f-181">**compatible con 8251FIFO** (161)</span><span class="sxs-lookup"><span data-stu-id="5c56f-181">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5c56f-182">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5c56f-182">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-183">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="5c56f-183">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-185">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ SerialController**](cim-serialcontroller.md).**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="5c56f-185">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_SerialController**](cim-serialcontroller.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-186">Matriz de cadenas de forma libre que proporcionan explicaciones más detalladas para cualquiera de las características de controlador serie indicadas en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="5c56f-186">Array of free-form strings providing more detailed explanations for any of the serial controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="5c56f-187">Tenga en cuenta que cada entrada de esta matriz está relacionada con la entrada de la matriz de **capacidades** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="5c56f-187">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="5c56f-188">Esta propiedad se hereda de [**\_ SerialController CIM**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-188">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5c56f-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c56f-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-192">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5c56f-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-193">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="5c56f-193">Short description of the object.</span></span>

<span data-ttu-id="5c56f-194">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-195">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5c56f-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-196">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c56f-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-198">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5c56f-198">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-199">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="5c56f-199">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="5c56f-200">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="5c56f-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="5c56f-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="5c56f-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-203">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="5c56f-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="5c56f-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="5c56f-205">(1)</span><span class="sxs-lookup"><span data-stu-id="5c56f-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-206">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5c56f-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5c56f-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="5c56f-208">(2)</span><span class="sxs-lookup"><span data-stu-id="5c56f-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="5c56f-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="5c56f-210">(3)</span><span class="sxs-lookup"><span data-stu-id="5c56f-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-211">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="5c56f-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5c56f-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="5c56f-213">(4)</span><span class="sxs-lookup"><span data-stu-id="5c56f-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-214">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="5c56f-214">Device is not working properly.</span></span> <span data-ttu-id="5c56f-215">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="5c56f-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="5c56f-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="5c56f-217">(5)</span><span class="sxs-lookup"><span data-stu-id="5c56f-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-218">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="5c56f-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="5c56f-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="5c56f-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="5c56f-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-221">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5c56f-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="5c56f-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="5c56f-223">(7)</span><span class="sxs-lookup"><span data-stu-id="5c56f-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="5c56f-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="5c56f-225">(8)</span><span class="sxs-lookup"><span data-stu-id="5c56f-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-226">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="5c56f-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="5c56f-228">(9)</span><span class="sxs-lookup"><span data-stu-id="5c56f-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-229">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="5c56f-229">Device is not working properly.</span></span> <span data-ttu-id="5c56f-230">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="5c56f-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="5c56f-232">(10)</span><span class="sxs-lookup"><span data-stu-id="5c56f-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-233">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="5c56f-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="5c56f-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="5c56f-235">(11)</span><span class="sxs-lookup"><span data-stu-id="5c56f-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-236">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="5c56f-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="5c56f-238">(12)</span><span class="sxs-lookup"><span data-stu-id="5c56f-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-239">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="5c56f-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="5c56f-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="5c56f-241">(13)</span><span class="sxs-lookup"><span data-stu-id="5c56f-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-242">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="5c56f-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="5c56f-244">(14)</span><span class="sxs-lookup"><span data-stu-id="5c56f-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-245">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="5c56f-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="5c56f-247">(15)</span><span class="sxs-lookup"><span data-stu-id="5c56f-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-248">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="5c56f-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="5c56f-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="5c56f-250">(16)</span><span class="sxs-lookup"><span data-stu-id="5c56f-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-251">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="5c56f-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="5c56f-253">(17)</span><span class="sxs-lookup"><span data-stu-id="5c56f-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-254">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="5c56f-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5c56f-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="5c56f-256">(18)</span><span class="sxs-lookup"><span data-stu-id="5c56f-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-257">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5c56f-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="5c56f-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="5c56f-259">(19)</span><span class="sxs-lookup"><span data-stu-id="5c56f-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5c56f-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="5c56f-261">(20)</span><span class="sxs-lookup"><span data-stu-id="5c56f-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-262">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="5c56f-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="5c56f-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="5c56f-264">(21)</span><span class="sxs-lookup"><span data-stu-id="5c56f-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-265">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="5c56f-265">System failure.</span></span> <span data-ttu-id="5c56f-266">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="5c56f-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="5c56f-267">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="5c56f-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="5c56f-269">(22)</span><span class="sxs-lookup"><span data-stu-id="5c56f-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-270">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="5c56f-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="5c56f-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="5c56f-272">(23)</span><span class="sxs-lookup"><span data-stu-id="5c56f-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-273">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="5c56f-273">System failure.</span></span> <span data-ttu-id="5c56f-274">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="5c56f-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="5c56f-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="5c56f-276">(24)</span><span class="sxs-lookup"><span data-stu-id="5c56f-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-277">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="5c56f-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5c56f-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5c56f-279">(25)</span><span class="sxs-lookup"><span data-stu-id="5c56f-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-280">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5c56f-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5c56f-282">(26)</span><span class="sxs-lookup"><span data-stu-id="5c56f-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-283">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="5c56f-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="5c56f-285">(27)</span><span class="sxs-lookup"><span data-stu-id="5c56f-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-286">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="5c56f-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="5c56f-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="5c56f-288">(28)</span><span class="sxs-lookup"><span data-stu-id="5c56f-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-289">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="5c56f-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="5c56f-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="5c56f-291">(29)</span><span class="sxs-lookup"><span data-stu-id="5c56f-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-292">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="5c56f-292">Device is disabled.</span></span> <span data-ttu-id="5c56f-293">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="5c56f-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="5c56f-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="5c56f-295">(30)</span><span class="sxs-lookup"><span data-stu-id="5c56f-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-296">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="5c56f-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5c56f-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5c56f-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="5c56f-298">31</span><span class="sxs-lookup"><span data-stu-id="5c56f-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-299">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="5c56f-299">Device is not working properly.</span></span> <span data-ttu-id="5c56f-300">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="5c56f-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5c56f-301">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="5c56f-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-302">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-304">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5c56f-304">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-305">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5c56f-305">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="5c56f-306">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5c56f-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-308">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c56f-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-310">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5c56f-310">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-311">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="5c56f-311">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="5c56f-312">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="5c56f-312">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5c56f-313">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-314">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5c56f-314">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-315">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c56f-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-317">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="5c56f-317">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-318">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="5c56f-318">Description of the object.</span></span>

<span data-ttu-id="5c56f-319">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-320">**ID**</span><span class="sxs-lookup"><span data-stu-id="5c56f-320">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-321">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c56f-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-323">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry de \| hardware \\ \\ DeviceMap \\ \\ SerialComm")</span><span class="sxs-lookup"><span data-stu-id="5c56f-323">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\SerialComm")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-324">Identificador único del puerto serie con otros dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="5c56f-324">Unique identifier of the serial port with other devices on the system.</span></span>

<span data-ttu-id="5c56f-325">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-326">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5c56f-326">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-327">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-329">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="5c56f-329">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="5c56f-330">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-331">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5c56f-331">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-332">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c56f-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-334">Cadena de forma libre que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="5c56f-334">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="5c56f-335">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-336">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5c56f-336">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-337">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5c56f-337">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-339">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="5c56f-339">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-340">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="5c56f-340">Date and time the object was installed.</span></span> <span data-ttu-id="5c56f-341">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="5c56f-341">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5c56f-342">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-343">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5c56f-343">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-344">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c56f-344">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-346">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5c56f-346">Last error code reported by the logical device.</span></span>

<span data-ttu-id="5c56f-347">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-347">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-348">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="5c56f-348">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-349">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c56f-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-351">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Puertos serie DMTF \| 004,6 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bits por segundo ")</span><span class="sxs-lookup"><span data-stu-id="5c56f-351">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Serial Ports\|004.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-352">Velocidad máxima en baudios (en bits por segundo) admitida por el controlador serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-352">Maximum baud rate (in bits per second) supported by the serial controller.</span></span>

<span data-ttu-id="5c56f-353">Esta propiedad se hereda de [**\_ SerialController CIM**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-353">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-354">**MaximumInputBufferSize**</span><span class="sxs-lookup"><span data-stu-id="5c56f-354">**MaximumInputBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-355">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c56f-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-357">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwMaxRxQueue"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="5c56f-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwMaxRxQueue"), [**units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-358">Tamaño máximo del búfer de entrada interno del controlador de puerto serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-358">Maximum size of the serial port driver's internal input buffer.</span></span> <span data-ttu-id="5c56f-359">Un valor de 0 (cero) indica que el proveedor de serie no impone ningún valor máximo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-359">A value of 0 (zero) indicates that no maximum value is imposed by the serial provider.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-360">**MaximumOutputBufferSize**</span><span class="sxs-lookup"><span data-stu-id="5c56f-360">**MaximumOutputBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-361">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c56f-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-363">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwMaxTxQueue"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="5c56f-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwMaxTxQueue"), [**units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-364">Tamaño máximo del búfer de salida interno del controlador de puerto serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-364">Maximum size of the serial port driver's internal output buffer.</span></span> <span data-ttu-id="5c56f-365">Un valor de 0 (cero) indica que el proveedor de serie no impone ningún valor máximo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-365">A value of 0 (zero) indicates that no maximum value is imposed by the serial provider.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-366">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="5c56f-366">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-367">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c56f-367">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-369">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Puerto de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="5c56f-369">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-370">Número máximo de entidades directamente direccionables admitidas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="5c56f-370">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="5c56f-371">Se debe utilizar un valor de 0 (cero) si se desconoce el número.</span><span class="sxs-lookup"><span data-stu-id="5c56f-371">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="5c56f-372">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-372">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-373">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="5c56f-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-374">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c56f-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-376">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5c56f-376">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-377">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="5c56f-377">Label by which the object is known.</span></span> <span data-ttu-id="5c56f-378">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="5c56f-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="5c56f-379">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-380">**OSAutoDiscovered**</span><span class="sxs-lookup"><span data-stu-id="5c56f-380">**OSAutoDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-381">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-383">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ Description \\ \\ System \\ \\ MultifunctionAdapter")</span><span class="sxs-lookup"><span data-stu-id="5c56f-383">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\DESCRIPTION\\\\SYSTEM\\\\MultifunctionAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-384">Si **es true**, el sistema operativo detectará automáticamente las instancias de esta clase.</span><span class="sxs-lookup"><span data-stu-id="5c56f-384">If **TRUE**, the instances of this class were automatically discovered by the operating system.</span></span> <span data-ttu-id="5c56f-385">Por ejemplo, si se agregó hardware a través del panel de control, el sistema operativo busca las instancias de esta clase consultando el hardware de las instancias de esta clase.</span><span class="sxs-lookup"><span data-stu-id="5c56f-385">If, for example, hardware was added through Control Panel, the operating system finds instances of this class by querying hardware from the instances of this class.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-386">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="5c56f-386">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-387">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c56f-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-389">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5c56f-389">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-390">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5c56f-390">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="5c56f-391">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="5c56f-392">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="5c56f-392">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-393">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5c56f-393">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-394">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c56f-394">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-395">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-396">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5c56f-396">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="5c56f-397">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="5c56f-397">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5c56f-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="5c56f-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5c56f-399"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="5c56f-399"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5c56f-400"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="5c56f-400"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5c56f-401"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5c56f-401"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-402">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="5c56f-402">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="5c56f-403"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="5c56f-403"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-404">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="5c56f-404">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="5c56f-405"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="5c56f-405"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-406">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="5c56f-406">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="5c56f-407">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="5c56f-407">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="5c56f-408">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-408">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="5c56f-409"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="5c56f-409"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-410">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="5c56f-410">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="5c56f-411"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="5c56f-411"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-412">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="5c56f-412">Timed Power-On Supported</span></span>

<span data-ttu-id="5c56f-413">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="5c56f-413">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5c56f-414">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5c56f-414">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-415">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-415">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-416">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-417">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="5c56f-417">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="5c56f-418">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="5c56f-418">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="5c56f-419">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-420">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="5c56f-420">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-421">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c56f-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-422">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-423">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Puerto de bus DMTF \| 001,2 "," MIF. \|Discos DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="5c56f-423">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-424">Protocolo usado por el controlador para tener acceso a dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="5c56f-424">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="5c56f-425">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-425">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="5c56f-426">En la lista siguiente se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="5c56f-426">The following list shows the possible values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5c56f-427"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5c56f-427"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5c56f-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5c56f-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="5c56f-429"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="5c56f-429"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="5c56f-430"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="5c56f-430"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="5c56f-431"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="5c56f-431"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="5c56f-432"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="5c56f-432"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5c56f-433">ATA o ATAPI</span><span class="sxs-lookup"><span data-stu-id="5c56f-433">ATA or ATAPI</span></span>

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="5c56f-434"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Disco flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="5c56f-434"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="5c56f-435"><span id="1496"></span>**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="5c56f-435"><span id="1496"></span>**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="5c56f-436"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**Interfaz paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="5c56f-436"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="5c56f-437"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**Protocolo SCSI canal de fibra** (10)</span><span class="sxs-lookup"><span data-stu-id="5c56f-437"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="5c56f-438"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**Protocolo de bus serie SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="5c56f-438"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="5c56f-439"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**Protocolo de bus serie SCSI: 2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="5c56f-439"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="5c56f-440"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**Arquitectura de almacenamiento en serie SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="5c56f-440"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="5c56f-441"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="5c56f-441"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="5c56f-442"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="5c56f-442"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="5c56f-443"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Bus serie universal** (16)</span><span class="sxs-lookup"><span data-stu-id="5c56f-443"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="5c56f-444"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="5c56f-444"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="5c56f-445"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="5c56f-445"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="5c56f-446"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="5c56f-446"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="5c56f-447"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="5c56f-447"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="5c56f-448"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Potencia** (21)</span><span class="sxs-lookup"><span data-stu-id="5c56f-448"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="5c56f-449"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="5c56f-449"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="5c56f-450"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="5c56f-450"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="5c56f-451"><span id="VME"></span><span id="vme"></span>**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="5c56f-451"><span id="VME"></span><span id="vme"></span>**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="5c56f-452"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="5c56f-452"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="5c56f-453"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="5c56f-453"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="5c56f-454"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="5c56f-454"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="5c56f-455"><span id="ieee_802.3_10base5"></span>**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="5c56f-455"><span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="5c56f-456"><span id="ieee_802.3_10base2"></span>**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="5c56f-456"><span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="5c56f-457"><span id="ieee_802.3_1base5"></span>**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="5c56f-457"><span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="5c56f-458"><span id="ieee_802.3_10broad36"></span>**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="5c56f-458"><span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="5c56f-459"><span id="ieee_802.3_100basevg"></span>**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="5c56f-459"><span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="5c56f-460"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="5c56f-460"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="5c56f-461"><span id="ansi_x3t9.5_fddi"></span>**FDDI ANSI x3t 9.5** (34)</span><span class="sxs-lookup"><span data-stu-id="5c56f-461"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="5c56f-462"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="5c56f-462"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="5c56f-463"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="5c56f-463"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="5c56f-464"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="5c56f-464"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="5c56f-465"><span id="CMD"></span><span id="cmd"></span>**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="5c56f-465"><span id="CMD"></span><span id="cmd"></span>**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="5c56f-466"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="5c56f-466"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="5c56f-467"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="5c56f-467"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="5c56f-468"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="5c56f-468"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="5c56f-469"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**ATA/IDE mejorado** (42)</span><span class="sxs-lookup"><span data-stu-id="5c56f-469"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="5c56f-470"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="5c56f-470"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="5c56f-471"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (infrarrojo bidireccional)** (44)</span><span class="sxs-lookup"><span data-stu-id="5c56f-471"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="5c56f-472"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (infrarrojo rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="5c56f-472"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="5c56f-473"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**Sir (infrarrojos serie)** (46)</span><span class="sxs-lookup"><span data-stu-id="5c56f-473"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="5c56f-474"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="5c56f-474"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5c56f-475">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="5c56f-475">**ProviderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-476">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c56f-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-477">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-478">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| comunicación de estructuras \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvSubType")</span><span class="sxs-lookup"><span data-stu-id="5c56f-478">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvSubType")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-479">Tipo de proveedor de comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="5c56f-479">Communications provider type.</span></span>

<span data-ttu-id="5c56f-480">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="5c56f-480">The values are:</span></span>

<dl> <dd><span data-ttu-id="5c56f-481">"Dispositivo de FAX"</span><span class="sxs-lookup"><span data-stu-id="5c56f-481">"FAX Device"</span></span></dd> <dd><span data-ttu-id="5c56f-482">"Protocolo LAT"</span><span class="sxs-lookup"><span data-stu-id="5c56f-482">"LAT Protocol"</span></span></dd> <dd><span data-ttu-id="5c56f-483">"Dispositivo de módem"</span><span class="sxs-lookup"><span data-stu-id="5c56f-483">"Modem Device"</span></span></dd> <dd><span data-ttu-id="5c56f-484">"Puente de red"</span><span class="sxs-lookup"><span data-stu-id="5c56f-484">"Network Bridge"</span></span></dd> <dd><span data-ttu-id="5c56f-485">"Puerto paralelo"</span><span class="sxs-lookup"><span data-stu-id="5c56f-485">"Parallel Port"</span></span></dd> <dd><span data-ttu-id="5c56f-486">"Puerto serie RS232"</span><span class="sxs-lookup"><span data-stu-id="5c56f-486">"RS232 Serial Port"</span></span></dd> <dd><span data-ttu-id="5c56f-487">"Puerto RS422"</span><span class="sxs-lookup"><span data-stu-id="5c56f-487">"RS422 Port"</span></span></dd> <dd><span data-ttu-id="5c56f-488">"Puerto RS423"</span><span class="sxs-lookup"><span data-stu-id="5c56f-488">"RS423 Port"</span></span></dd> <dd><span data-ttu-id="5c56f-489">"Puerto RS449"</span><span class="sxs-lookup"><span data-stu-id="5c56f-489">"RS449 Port"</span></span></dd> <dd><span data-ttu-id="5c56f-490">"Dispositivo de escáner"</span><span class="sxs-lookup"><span data-stu-id="5c56f-490">"Scanner Device"</span></span></dd> <dd><span data-ttu-id="5c56f-491">"TelNet TCP/IP"</span><span class="sxs-lookup"><span data-stu-id="5c56f-491">"TCP/IP TelNet"</span></span></dd> <dd><span data-ttu-id="5c56f-492">"X. 25"</span><span class="sxs-lookup"><span data-stu-id="5c56f-492">"X.25"</span></span></dd> <dd><span data-ttu-id="5c56f-493">No especificado</span><span class="sxs-lookup"><span data-stu-id="5c56f-493">"Unspecified"</span></span></dd> </dl>

<dt>

<span id="FAX_Device"></span><span id="fax_device"></span><span id="FAX_DEVICE"></span>

<span data-ttu-id="5c56f-494">**Dispositivo de fax** ("dispositivo de fax")</span><span class="sxs-lookup"><span data-stu-id="5c56f-494">**FAX Device** ("FAX Device")</span></span>


</dt> <dd></dd> <dt>

<span id="LAT_Protocol"></span><span id="lat_protocol"></span><span id="LAT_PROTOCOL"></span>

<span data-ttu-id="5c56f-495">**Protocolo lat** ("Protocolo lat")</span><span class="sxs-lookup"><span data-stu-id="5c56f-495">**LAT Protocol** ("LAT Protocol")</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Device"></span><span id="modem_device"></span><span id="MODEM_DEVICE"></span>

<span data-ttu-id="5c56f-496">**Dispositivo de módem** ("dispositivo de módem")</span><span class="sxs-lookup"><span data-stu-id="5c56f-496">**Modem Device** ("Modem Device")</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Bridge"></span><span id="network_bridge"></span><span id="NETWORK_BRIDGE"></span>

<span data-ttu-id="5c56f-497">**Puente de red** ("puente de red")</span><span class="sxs-lookup"><span data-stu-id="5c56f-497">**Network Bridge** ("Network Bridge")</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="5c56f-498">**Puerto paralelo** ("puerto paralelo")</span><span class="sxs-lookup"><span data-stu-id="5c56f-498">**Parallel Port** ("Parallel Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS232_Serial_Port"></span><span id="rs232_serial_port"></span><span id="RS232_SERIAL_PORT"></span>

<span data-ttu-id="5c56f-499">**Puerto serie RS232** ("puerto serie RS232")</span><span class="sxs-lookup"><span data-stu-id="5c56f-499">**RS232 Serial Port** ("RS232 Serial Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS422_Port"></span><span id="rs422_port"></span><span id="RS422_PORT"></span>

<span data-ttu-id="5c56f-500">**Puerto RS422** ("Puerto RS422")</span><span class="sxs-lookup"><span data-stu-id="5c56f-500">**RS422 Port** ("RS422 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS423_Port"></span><span id="rs423_port"></span><span id="RS423_PORT"></span>

<span data-ttu-id="5c56f-501">**Puerto RS423** ("Puerto RS423")</span><span class="sxs-lookup"><span data-stu-id="5c56f-501">**RS423 Port** ("RS423 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS449_Port"></span><span id="rs449_port"></span><span id="RS449_PORT"></span>

<span data-ttu-id="5c56f-502">**Puerto RS449** ("Puerto RS449")</span><span class="sxs-lookup"><span data-stu-id="5c56f-502">**RS449 Port** ("RS449 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="Scanner_Device"></span><span id="scanner_device"></span><span id="SCANNER_DEVICE"></span>

<span data-ttu-id="5c56f-503">**Dispositivo de escáner** ("dispositivo de escáner")</span><span class="sxs-lookup"><span data-stu-id="5c56f-503">**Scanner Device** ("Scanner Device")</span></span>


</dt> <dd></dd> <dt>

<span id="TCP_IP_TelNet"></span><span id="tcp_ip_telnet"></span><span id="TCP_IP_TELNET"></span>

<span data-ttu-id="5c56f-504">**TCP/IP Telnet** ("TCP/IP Telnet")</span><span class="sxs-lookup"><span data-stu-id="5c56f-504">**TCP/IP TelNet** ("TCP/IP TelNet")</span></span>


</dt> <dd></dd> <dt>

<span id="X.25"></span><span id="x.25"></span>

<span data-ttu-id="5c56f-505">**X. 25** ("x. 25")</span><span class="sxs-lookup"><span data-stu-id="5c56f-505">**X.25** ("X.25")</span></span>


</dt> <dd></dd> <dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="5c56f-506">No **especificado** ("sin especificar")</span><span class="sxs-lookup"><span data-stu-id="5c56f-506">**Unspecified** ("Unspecified")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5c56f-507">**SettableBaudRate**</span><span class="sxs-lookup"><span data-stu-id="5c56f-507">**SettableBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-508">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-508">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-509">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-510">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| comunicación de \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| Sp \_ Baud")</span><span class="sxs-lookup"><span data-stu-id="5c56f-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_BAUD")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-511">Si **es true**, se puede cambiar la velocidad en baudios para este puerto serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-511">If **TRUE**, the baud rate can be changed for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-512">**SettableDataBits**</span><span class="sxs-lookup"><span data-stu-id="5c56f-512">**SettableDataBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-513">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-513">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-514">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-515">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| Sp \_ bits")</span><span class="sxs-lookup"><span data-stu-id="5c56f-515">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_DATABITS")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-516">Si **es true**, se pueden establecer bits de datos para este puerto serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-516">If **TRUE**, data bits can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-517">**SettableFlowControl**</span><span class="sxs-lookup"><span data-stu-id="5c56f-517">**SettableFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-518">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-518">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-519">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-520">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| comunicaciones de \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams de protocolo de enlace de \| Sp \_ ")</span><span class="sxs-lookup"><span data-stu-id="5c56f-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_HANDSHAKING")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-521">Si **es true**, se puede establecer el control de flujo para este puerto serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-521">If **TRUE**, flow control can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-522">**SettableParity**</span><span class="sxs-lookup"><span data-stu-id="5c56f-522">**SettableParity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-523">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-523">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-524">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-525">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| comunicación de \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| Sp \_ PARITY")</span><span class="sxs-lookup"><span data-stu-id="5c56f-525">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_PARITY")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-526">Si **es true**, se puede establecer la paridad para este puerto serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-526">If **TRUE**, parity can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-527">**SettableParityCheck**</span><span class="sxs-lookup"><span data-stu-id="5c56f-527">**SettableParityCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-528">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-528">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-529">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-529">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-530">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| Sp \_ PARITY \_ check")</span><span class="sxs-lookup"><span data-stu-id="5c56f-530">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_PARITY\_CHECK")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-531">Si es **true**, se puede establecer la comprobación de paridad para este puerto serie (si se admite la comprobación de paridad).</span><span class="sxs-lookup"><span data-stu-id="5c56f-531">If **TRUE**, parity checking can be set for this serial port (if parity checking is supported).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-532">**SettableRLSD**</span><span class="sxs-lookup"><span data-stu-id="5c56f-532">**SettableRLSD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-533">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-533">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-534">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-535">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| Sp \_ RLSD")</span><span class="sxs-lookup"><span data-stu-id="5c56f-535">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_RLSD")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-536">Si es **true**, se puede establecer la detección de señal de línea recibida (RLSD) para este puerto serie (si se admite RLSD).</span><span class="sxs-lookup"><span data-stu-id="5c56f-536">If **TRUE**, Received Line Signal Detect (RLSD) can be set for this serial port (if RLSD is supported).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-537">**SettableStopBits**</span><span class="sxs-lookup"><span data-stu-id="5c56f-537">**SettableStopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-538">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-538">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-539">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-539">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-540">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| comunicación de \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| Sp \_ parada")</span><span class="sxs-lookup"><span data-stu-id="5c56f-540">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_STOPBITS")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-541">Si **es true**, se pueden establecer bits de parada para este puerto serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-541">If **TRUE**, stop bits can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-542">**Estado**</span><span class="sxs-lookup"><span data-stu-id="5c56f-542">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-543">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c56f-543">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-544">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-544">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-545">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="5c56f-545">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-546">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5c56f-546">Current status of the object.</span></span> <span data-ttu-id="5c56f-547">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="5c56f-547">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5c56f-548">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="5c56f-548">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5c56f-549">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="5c56f-549">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5c56f-550">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-550">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5c56f-551">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="5c56f-551">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5c56f-552">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-552">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5c56f-553">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5c56f-553">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5c56f-554">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="5c56f-554">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5c56f-555">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="5c56f-555">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5c56f-556">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5c56f-556">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5c56f-557">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="5c56f-557">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5c56f-558">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="5c56f-558">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5c56f-559">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="5c56f-559">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5c56f-560">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="5c56f-560">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5c56f-561">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="5c56f-561">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5c56f-562">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="5c56f-562">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5c56f-563">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5c56f-563">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5c56f-564">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="5c56f-564">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5c56f-565">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="5c56f-565">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5c56f-566">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5c56f-566">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-567">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5c56f-567">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-568">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-568">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-569">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="5c56f-569">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-570">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5c56f-570">State of the logical device.</span></span> <span data-ttu-id="5c56f-571">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="5c56f-571">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="5c56f-572">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-572">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5c56f-573">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5c56f-573">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5c56f-574">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5c56f-574">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5c56f-575">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5c56f-575">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5c56f-576">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="5c56f-576">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5c56f-577">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="5c56f-577">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5c56f-578">**Supports16BitMode**</span><span class="sxs-lookup"><span data-stu-id="5c56f-578">**Supports16BitMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-579">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-579">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-580">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-581">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ 16BITMODE")</span><span class="sxs-lookup"><span data-stu-id="5c56f-581">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_16BITMODE")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-582">Si es **true**, se admite el modo de 16 bits en este puerto serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-582">If **TRUE**, 16-bit mode is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-583">**SupportsDTRDSR**</span><span class="sxs-lookup"><span data-stu-id="5c56f-583">**SupportsDTRDSR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-584">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-585">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-585">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-586">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ DTRDSR")</span><span class="sxs-lookup"><span data-stu-id="5c56f-586">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_DTRDSR")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-587">Si **es true**, se admiten señales de terminal de datos preparado (DTR) y conjunto de datos preparado (DSR) en este puerto serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-587">If **TRUE**, data terminal ready (DTR) and data set ready (DSR) signals are supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-588">**SupportsElapsedTimeouts**</span><span class="sxs-lookup"><span data-stu-id="5c56f-588">**SupportsElapsedTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-589">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-589">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-590">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-591">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ TOTALTIMEOUTS")</span><span class="sxs-lookup"><span data-stu-id="5c56f-591">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_TOTALTIMEOUTS")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-592">Si **es true**, los tiempos de espera transcurridos se admiten en este puerto serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-592">If **TRUE**, elapsed time-outs are supported on this serial port.</span></span> <span data-ttu-id="5c56f-593">Los tiempos de espera transcurridos realizan el seguimiento de la cantidad total de tiempo entre transmisiones de datos.</span><span class="sxs-lookup"><span data-stu-id="5c56f-593">Elapsed timeouts track the total amount of time between data transmissions.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-594">**SupportsIntTimeouts**</span><span class="sxs-lookup"><span data-stu-id="5c56f-594">**SupportsIntTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-595">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-595">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-596">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-596">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-597">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ INTTIMEOUTS")</span><span class="sxs-lookup"><span data-stu-id="5c56f-597">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_INTTIMEOUTS")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-598">Si **es true**, se admiten los tiempos de espera de intervalo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-598">If **TRUE**, interval time-outs are supported.</span></span> <span data-ttu-id="5c56f-599">Un tiempo de espera de intervalo es la cantidad de tiempo que puede transcurrir entre la llegada de cada fragmento de datos.</span><span class="sxs-lookup"><span data-stu-id="5c56f-599">An interval timeout is the amount of time allowed to elapse between the arrival of each piece of data.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-600">**SupportsParityCheck**</span><span class="sxs-lookup"><span data-stu-id="5c56f-600">**SupportsParityCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-601">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-601">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-602">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-603">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ PARITY \_ check")</span><span class="sxs-lookup"><span data-stu-id="5c56f-603">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_PARITY\_CHECK")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-604">Si es **true**, se admite la comprobación de paridad en este puerto serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-604">If **TRUE**, parity checking is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-605">**SupportsRLSD**</span><span class="sxs-lookup"><span data-stu-id="5c56f-605">**SupportsRLSD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-606">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-606">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-607">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-608">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communication Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ RLSD")</span><span class="sxs-lookup"><span data-stu-id="5c56f-608">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_RLSD")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-609">Si **es true**, se admite la detección de señal de línea recibida (RLSD) en este puerto serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-609">If **TRUE**, Received Line Signal Detect (RLSD) is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-610">**SupportsRTSCTS**</span><span class="sxs-lookup"><span data-stu-id="5c56f-610">**SupportsRTSCTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-611">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-611">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-612">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-612">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-613">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ RTSCTS")</span><span class="sxs-lookup"><span data-stu-id="5c56f-613">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_RTSCTS")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-614">Si **es true**, las señales Ready to send (RTS) y Clear to send (CTS) se admiten en este puerto serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-614">If **TRUE**, ready to send (RTS) and clear to send (CTS) signals are supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-615">**SupportsSpecialCharacters**</span><span class="sxs-lookup"><span data-stu-id="5c56f-615">**SupportsSpecialCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-616">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-616">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-617">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-617">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-618">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ SPECIALCHARS")</span><span class="sxs-lookup"><span data-stu-id="5c56f-618">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_SPECIALCHARS")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-619">Si **es true**, se admiten los caracteres de control de puerto serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-619">If **TRUE**, serial port control characters are supported.</span></span> <span data-ttu-id="5c56f-620">Estos caracteres señalan eventos en lugar de datos.</span><span class="sxs-lookup"><span data-stu-id="5c56f-620">These characters signal events rather than data.</span></span> <span data-ttu-id="5c56f-621">Estos caracteres no se pueden mostrar y los establece el controlador.</span><span class="sxs-lookup"><span data-stu-id="5c56f-621">These characters are not displayable and are set by the driver.</span></span> <span data-ttu-id="5c56f-622">Incluyen EofChar, ErrorChar, BreakChar, EventChar, XonChar y XoffChar.</span><span class="sxs-lookup"><span data-stu-id="5c56f-622">They include EofChar, ErrorChar, BreakChar, EventChar, XonChar, and XoffChar.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-623">**SupportsXOnXOff**</span><span class="sxs-lookup"><span data-stu-id="5c56f-623">**SupportsXOnXOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-624">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-624">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-625">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-625">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-626">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ XONXOFF")</span><span class="sxs-lookup"><span data-stu-id="5c56f-626">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_XONXOFF")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-627">Si es **true**, se admite el control de flujo XON o XOFF en este puerto serie.</span><span class="sxs-lookup"><span data-stu-id="5c56f-627">If **TRUE**, XON or XOFF flow-control is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-628">**SupportsXOnXOffSet**</span><span class="sxs-lookup"><span data-stu-id="5c56f-628">**SupportsXOnXOffSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-629">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5c56f-629">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-630">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-630">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-631">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Communications Structures \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ SETXCHAR")</span><span class="sxs-lookup"><span data-stu-id="5c56f-631">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_SETXCHAR")</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-632">Si **es true**, el proveedor de comunicaciones admite la configuración de la configuración de control de flujo de XONor XOFF.</span><span class="sxs-lookup"><span data-stu-id="5c56f-632">If **TRUE**, the communications provider supports configuration of the XONor XOFF flow-control setting.</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-633">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5c56f-633">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-634">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c56f-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-635">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-636">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5c56f-636">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-637">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5c56f-637">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="5c56f-638">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-638">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-639">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5c56f-639">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-640">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5c56f-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-641">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-641">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-642">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5c56f-642">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-643">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5c56f-643">Name of the scoping system.</span></span>

<span data-ttu-id="5c56f-644">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-644">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c56f-645">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="5c56f-645">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c56f-646">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5c56f-646">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5c56f-647">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c56f-647">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c56f-648">Fecha y hora en que se restableció por última vez este controlador.</span><span class="sxs-lookup"><span data-stu-id="5c56f-648">Date and time this controller was last reset.</span></span> <span data-ttu-id="5c56f-649">Esto podría significar que el controlador se apagó o reinicializó.</span><span class="sxs-lookup"><span data-stu-id="5c56f-649">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="5c56f-650">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-650">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c56f-651">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c56f-651">Remarks</span></span>

<span data-ttu-id="5c56f-652">La **clase \_ SerialPort de Win32** se deriva [**del \_ SerialController CIM**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="5c56f-652">The **Win32\_SerialPort** class is derived from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5c56f-653">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5c56f-653">Examples</span></span>

<span data-ttu-id="5c56f-654">Para obtener un método alternativo para recuperar la información del puerto serie (desde el registro), consulte el ejemplo [enumerar puertos](https://Gallery.TechNet.Microsoft.Com/scriptcenter/087b4d73-4a5e-4746-b365-ad682911360e) Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5c56f-654">For an alternate method of retrieving serial port information (from the registry), see the [Enumerate Ports](https://Gallery.TechNet.Microsoft.Com/scriptcenter/087b4d73-4a5e-4746-b365-ad682911360e) Visual Basic sample.</span></span>

<span data-ttu-id="5c56f-655">En el ejemplo de la [lista de propiedades de puerto serie](https://Gallery.TechNet.Microsoft.Com/42ff8eab-7d2b-4549-b178-835daecf4f12) de PowerShell se devuelve información acerca de los puertos serie instalados en un equipo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-655">The [List Serial Port Properties](https://Gallery.TechNet.Microsoft.Com/42ff8eab-7d2b-4549-b178-835daecf4f12) PowerShell example returns information about the serial ports installed on a computer.</span></span>

<span data-ttu-id="5c56f-656">El siguiente ejemplo de VBScript devuelve información acerca de los puertos serie instalados en un equipo.</span><span class="sxs-lookup"><span data-stu-id="5c56f-656">The following VBScript sample returns information about the serial ports installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_SerialPort") 
 
For Each objItem in colItems 
    Wscript.Echo "Binary: " & objItem.Binary 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Maximum Baud Rate: " & objItem.MaxBaudRate 
    Wscript.Echo "Maximum Input Buffer Size: " & objItem.MaximumInputBufferSize 
    Wscript.Echo "Maximum Output Buffer Size: " & _ 
        objItem.MaximumOutputBufferSize 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "OS Auto Discovered: " & objItem.OSAutoDiscovered 
    Wscript.Echo "PNP Device ID: " & objItem.PNPDeviceID 
    Wscript.Echo "Provider Type: " & objItem.ProviderType 
    Wscript.Echo "Settable Baud Rate: " & objItem.SettableBaudRate 
    Wscript.Echo "Settable Data Bits: " & objItem.SettableDataBits 
    Wscript.Echo "Settable Flow Control: " & objItem.SettableFlowControl 
    Wscript.Echo "Settable Parity: " & objItem.SettableParity 
    Wscript.Echo "Settable Parity Check: " & objItem.SettableParityCheck 
    Wscript.Echo "Settable RLSD: " & objItem.SettableRLSD 
    Wscript.Echo "Settable Stop Bits: " & objItem.SettableStopBits 
    Wscript.Echo "Supports 16-Bit Mode: " & objItem.Supports16BitMode 
    Wscript.Echo "Supports DTRDSR: " & objItem.SupportsDTRDSR 
    Wscript.Echo "Supports Elapsed Timeouts: " & _ 
        objItem.SupportsElapsedTimeouts 
    Wscript.Echo "Supports Int Timeouts: " & objItem.SupportsIntTimeouts 
    Wscript.Echo "Supports Parity Check: " & objItem.SupportsParityCheck 
    Wscript.Echo "Supports RLSD: " & objItem.SupportsRLSD 
    Wscript.Echo "Supports RTSCTS: " & objItem.SupportsRTSCTS 
    Wscript.Echo "Supports Special Characters: " & _ 
        objItem.SupportsSpecialCharacters 
    Wscript.Echo "Supports XOn XOff: " & objItem.SupportsXOnXOff 
    Wscript.Echo "Supports XOn XOff Setting: " & objItem.SupportsXOnXOffSet 
Next
```



## <a name="requirements"></a><span data-ttu-id="5c56f-657">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c56f-657">Requirements</span></span>



| <span data-ttu-id="5c56f-658">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c56f-658">Requirement</span></span> | <span data-ttu-id="5c56f-659">Value</span><span class="sxs-lookup"><span data-stu-id="5c56f-659">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c56f-660">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c56f-660">Minimum supported client</span></span><br/> | <span data-ttu-id="5c56f-661">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c56f-661">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c56f-662">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c56f-662">Minimum supported server</span></span><br/> | <span data-ttu-id="5c56f-663">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c56f-663">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c56f-664">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5c56f-664">Namespace</span></span><br/>                | <span data-ttu-id="5c56f-665">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5c56f-665">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5c56f-666">MOF</span><span class="sxs-lookup"><span data-stu-id="5c56f-666">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c56f-667"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c56f-667"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c56f-668">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5c56f-668">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c56f-669"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c56f-669"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c56f-670">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c56f-670">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c56f-671">**\_SERIALCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="5c56f-671">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dt>

[<span data-ttu-id="5c56f-672">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="5c56f-672">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
