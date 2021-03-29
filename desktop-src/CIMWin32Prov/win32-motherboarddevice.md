---
description: La \_ clase WMI MotherboardDevice de Win32 representa un dispositivo que contiene los componentes centrales del sistema del equipo Windows.
ms.assetid: 2aed5fff-e994-4ce1-8a2e-aadb01adf28d
ms.tgt_platform: multiple
title: Win32_MotherboardDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MotherboardDevice
- Win32_MotherboardDevice.Reset
- Win32_MotherboardDevice.SetPowerState
- Win32_MotherboardDevice.Availability
- Win32_MotherboardDevice.Caption
- Win32_MotherboardDevice.ConfigManagerErrorCode
- Win32_MotherboardDevice.ConfigManagerUserConfig
- Win32_MotherboardDevice.CreationClassName
- Win32_MotherboardDevice.Description
- Win32_MotherboardDevice.DeviceID
- Win32_MotherboardDevice.ErrorCleared
- Win32_MotherboardDevice.ErrorDescription
- Win32_MotherboardDevice.InstallDate
- Win32_MotherboardDevice.LastErrorCode
- Win32_MotherboardDevice.Name
- Win32_MotherboardDevice.PNPDeviceID
- Win32_MotherboardDevice.PowerManagementCapabilities
- Win32_MotherboardDevice.PowerManagementSupported
- Win32_MotherboardDevice.PrimaryBusType
- Win32_MotherboardDevice.RevisionNumber
- Win32_MotherboardDevice.SecondaryBusType
- Win32_MotherboardDevice.Status
- Win32_MotherboardDevice.StatusInfo
- Win32_MotherboardDevice.SystemCreationClassName
- Win32_MotherboardDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6df116d1e4bc4e87d7201deb33f57bc8e91320e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807843"
---
# <a name="win32_motherboarddevice-class"></a><span data-ttu-id="857c1-103">\_Clase Win32 MotherboardDevice</span><span class="sxs-lookup"><span data-stu-id="857c1-103">Win32\_MotherboardDevice class</span></span>

<span data-ttu-id="857c1-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MotherboardDevice de Win32** representa un dispositivo que contiene los componentes centrales del sistema del equipo Windows.</span><span class="sxs-lookup"><span data-stu-id="857c1-104">The **Win32\_MotherboardDevice** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a device that contains the central components of the Windows computer system.</span></span>

<span data-ttu-id="857c1-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="857c1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="857c1-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="857c1-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="857c1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="857c1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_MotherboardDevice : CIM_LogicalDevice
{
  uint16   Availability;
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
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   PrimaryBusType;
  string   RevisionNumber;
  string   SecondaryBusType;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="857c1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="857c1-108">Members</span></span>

<span data-ttu-id="857c1-109">La **clase \_ MotherboardDevice de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="857c1-109">The **Win32\_MotherboardDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="857c1-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="857c1-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="857c1-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="857c1-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="857c1-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="857c1-112">Methods</span></span>

<span data-ttu-id="857c1-113">La clase **Win32 \_ MotherboardDevice** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="857c1-113">The **Win32\_MotherboardDevice** class has these methods.</span></span>



| <span data-ttu-id="857c1-114">Método</span><span class="sxs-lookup"><span data-stu-id="857c1-114">Method</span></span>            | <span data-ttu-id="857c1-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="857c1-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="857c1-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="857c1-116">**Reset**</span></span>         | <span data-ttu-id="857c1-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="857c1-117">Not implemented.</span></span> <span data-ttu-id="857c1-118">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**el \_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/>                 |
| <span data-ttu-id="857c1-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="857c1-119">**SetPowerState**</span></span> | <span data-ttu-id="857c1-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="857c1-120">Not implemented.</span></span> <span data-ttu-id="857c1-121">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**el \_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="857c1-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="857c1-122">Properties</span></span>

<span data-ttu-id="857c1-123">La **clase \_ MotherboardDevice de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="857c1-123">The **Win32\_MotherboardDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="857c1-124">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="857c1-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="857c1-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-127">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="857c1-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="857c1-128">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="857c1-128">Availability and status of the device.</span></span>

<span data-ttu-id="857c1-129">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="857c1-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="857c1-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="857c1-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="857c1-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="857c1-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="857c1-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-133">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="857c1-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="857c1-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="857c1-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="857c1-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="857c1-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="857c1-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="857c1-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="857c1-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="857c1-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="857c1-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="857c1-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="857c1-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="857c1-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="857c1-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="857c1-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="857c1-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="857c1-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="857c1-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="857c1-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="857c1-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="857c1-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-144">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="857c1-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="857c1-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="857c1-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-146">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="857c1-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="857c1-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="857c1-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-148">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="857c1-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="857c1-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="857c1-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="857c1-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="857c1-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-151">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="857c1-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="857c1-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="857c1-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-153">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="857c1-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="857c1-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="857c1-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-155">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="857c1-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="857c1-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="857c1-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-157">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="857c1-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="857c1-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="857c1-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-159">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="857c1-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="857c1-160">**Caption**</span><span class="sxs-lookup"><span data-stu-id="857c1-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="857c1-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-163">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="857c1-163">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="857c1-164">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="857c1-164">Short description of the object a one-line string.</span></span>

<span data-ttu-id="857c1-165">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="857c1-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="857c1-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-167">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="857c1-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-169">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="857c1-169">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="857c1-170">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="857c1-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="857c1-171">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="857c1-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="857c1-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="857c1-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="857c1-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-174">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="857c1-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="857c1-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="857c1-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="857c1-176">(1)</span><span class="sxs-lookup"><span data-stu-id="857c1-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-177">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="857c1-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="857c1-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="857c1-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="857c1-179">(2)</span><span class="sxs-lookup"><span data-stu-id="857c1-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="857c1-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="857c1-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="857c1-181">(3)</span><span class="sxs-lookup"><span data-stu-id="857c1-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-182">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="857c1-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="857c1-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="857c1-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="857c1-184">(4)</span><span class="sxs-lookup"><span data-stu-id="857c1-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-185">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="857c1-185">Device is not working properly.</span></span> <span data-ttu-id="857c1-186">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="857c1-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="857c1-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="857c1-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="857c1-188">(5)</span><span class="sxs-lookup"><span data-stu-id="857c1-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-189">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="857c1-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="857c1-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="857c1-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="857c1-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="857c1-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-192">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="857c1-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="857c1-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="857c1-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="857c1-194">(7)</span><span class="sxs-lookup"><span data-stu-id="857c1-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="857c1-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="857c1-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="857c1-196">(8)</span><span class="sxs-lookup"><span data-stu-id="857c1-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-197">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="857c1-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="857c1-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="857c1-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="857c1-199">(9)</span><span class="sxs-lookup"><span data-stu-id="857c1-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-200">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="857c1-200">Device is not working properly.</span></span> <span data-ttu-id="857c1-201">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="857c1-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="857c1-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="857c1-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="857c1-203">(10)</span><span class="sxs-lookup"><span data-stu-id="857c1-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-204">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="857c1-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="857c1-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="857c1-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="857c1-206">(11)</span><span class="sxs-lookup"><span data-stu-id="857c1-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-207">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="857c1-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="857c1-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="857c1-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="857c1-209">(12)</span><span class="sxs-lookup"><span data-stu-id="857c1-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-210">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="857c1-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="857c1-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="857c1-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="857c1-212">(13)</span><span class="sxs-lookup"><span data-stu-id="857c1-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-213">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="857c1-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="857c1-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="857c1-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="857c1-215">(14)</span><span class="sxs-lookup"><span data-stu-id="857c1-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-216">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="857c1-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="857c1-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="857c1-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="857c1-218">(15)</span><span class="sxs-lookup"><span data-stu-id="857c1-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-219">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="857c1-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="857c1-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="857c1-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="857c1-221">(16)</span><span class="sxs-lookup"><span data-stu-id="857c1-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-222">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="857c1-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="857c1-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="857c1-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="857c1-224">(17)</span><span class="sxs-lookup"><span data-stu-id="857c1-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-225">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="857c1-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="857c1-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="857c1-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="857c1-227">(18)</span><span class="sxs-lookup"><span data-stu-id="857c1-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-228">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="857c1-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="857c1-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="857c1-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="857c1-230">(19)</span><span class="sxs-lookup"><span data-stu-id="857c1-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="857c1-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="857c1-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="857c1-232">(20)</span><span class="sxs-lookup"><span data-stu-id="857c1-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-233">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="857c1-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="857c1-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="857c1-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="857c1-235">(21)</span><span class="sxs-lookup"><span data-stu-id="857c1-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-236">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="857c1-236">System failure.</span></span> <span data-ttu-id="857c1-237">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="857c1-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="857c1-238">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="857c1-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="857c1-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="857c1-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="857c1-240">(22)</span><span class="sxs-lookup"><span data-stu-id="857c1-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-241">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="857c1-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="857c1-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="857c1-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="857c1-243">(23)</span><span class="sxs-lookup"><span data-stu-id="857c1-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-244">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="857c1-244">System failure.</span></span> <span data-ttu-id="857c1-245">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="857c1-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="857c1-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="857c1-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="857c1-247">(24)</span><span class="sxs-lookup"><span data-stu-id="857c1-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-248">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="857c1-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="857c1-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="857c1-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="857c1-250">(25)</span><span class="sxs-lookup"><span data-stu-id="857c1-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-251">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="857c1-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="857c1-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="857c1-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="857c1-253">(26)</span><span class="sxs-lookup"><span data-stu-id="857c1-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-254">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="857c1-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="857c1-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="857c1-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="857c1-256">(27)</span><span class="sxs-lookup"><span data-stu-id="857c1-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-257">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="857c1-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="857c1-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="857c1-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="857c1-259">(28)</span><span class="sxs-lookup"><span data-stu-id="857c1-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-260">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="857c1-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="857c1-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="857c1-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="857c1-262">(29)</span><span class="sxs-lookup"><span data-stu-id="857c1-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-263">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="857c1-263">Device is disabled.</span></span> <span data-ttu-id="857c1-264">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="857c1-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="857c1-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="857c1-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="857c1-266">(30)</span><span class="sxs-lookup"><span data-stu-id="857c1-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-267">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="857c1-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="857c1-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="857c1-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="857c1-269">31</span><span class="sxs-lookup"><span data-stu-id="857c1-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-270">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="857c1-270">Device is not working properly.</span></span> <span data-ttu-id="857c1-271">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="857c1-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="857c1-272">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="857c1-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-273">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="857c1-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-275">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="857c1-275">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="857c1-276">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="857c1-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="857c1-277">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="857c1-278">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="857c1-278">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-279">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="857c1-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-281">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="857c1-281">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="857c1-282">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="857c1-282">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="857c1-283">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="857c1-283">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="857c1-284">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="857c1-285">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="857c1-285">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="857c1-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-288">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="857c1-288">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="857c1-289">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="857c1-289">Description of the object.</span></span>

<span data-ttu-id="857c1-290">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="857c1-291">**ID**</span><span class="sxs-lookup"><span data-stu-id="857c1-291">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-292">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="857c1-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-294">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="857c1-294">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="857c1-295">Identificador único de esta placa base.</span><span class="sxs-lookup"><span data-stu-id="857c1-295">Unique identifier of this motherboard.</span></span>

<span data-ttu-id="857c1-296">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="857c1-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="857c1-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-298">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="857c1-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="857c1-300">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="857c1-300">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="857c1-301">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="857c1-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="857c1-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="857c1-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="857c1-305">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="857c1-305">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="857c1-306">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="857c1-307">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="857c1-307">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-308">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="857c1-308">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-310">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="857c1-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="857c1-311">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="857c1-311">Date and time the object was installed.</span></span> <span data-ttu-id="857c1-312">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="857c1-312">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="857c1-313">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="857c1-314">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="857c1-314">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-315">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="857c1-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="857c1-317">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="857c1-317">Last error code reported by the logical device.</span></span>

<span data-ttu-id="857c1-318">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="857c1-319">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="857c1-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-320">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="857c1-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-322">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="857c1-322">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="857c1-323">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="857c1-323">Label by which the object is known.</span></span> <span data-ttu-id="857c1-324">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="857c1-324">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="857c1-325">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-325">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="857c1-326">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="857c1-326">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-327">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="857c1-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-329">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="857c1-329">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="857c1-330">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="857c1-330">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="857c1-331">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="857c1-332">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="857c1-332">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="857c1-333">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="857c1-333">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-334">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="857c1-334">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="857c1-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="857c1-336">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="857c1-336">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="857c1-337">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="857c1-337">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="857c1-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="857c1-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="857c1-339"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="857c1-339"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="857c1-340"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="857c1-340"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="857c1-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="857c1-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-342">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="857c1-342">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="857c1-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="857c1-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-344">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="857c1-344">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="857c1-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="857c1-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-346">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="857c1-346">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="857c1-347">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="857c1-347">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="857c1-348">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="857c1-348">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="857c1-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="857c1-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-350">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="857c1-350">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="857c1-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="857c1-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="857c1-352">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="857c1-352">Timed Power-On Supported</span></span>

<span data-ttu-id="857c1-353">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="857c1-353">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="857c1-354">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="857c1-354">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-355">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="857c1-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="857c1-357">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="857c1-357">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="857c1-358">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="857c1-358">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="857c1-359">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="857c1-360">**PrimaryBusType**</span><span class="sxs-lookup"><span data-stu-id="857c1-360">**PrimaryBusType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-361">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="857c1-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-363">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ hardware \\ \\ Description \\ \\ System \\ \\ MultifunctionAdapter \| Identifier")</span><span class="sxs-lookup"><span data-stu-id="857c1-363">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DESCRIPTION\\\\System\\\\MultifunctionAdapter\|Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="857c1-364">Tipo de bus principal de la placa base.</span><span class="sxs-lookup"><span data-stu-id="857c1-364">Primary bus type of the motherboard.</span></span>

<span data-ttu-id="857c1-365">Ejemplo: "PCI"</span><span class="sxs-lookup"><span data-stu-id="857c1-365">Example: "PCI"</span></span>

</dd> <dt>

<span data-ttu-id="857c1-366">**RevisionNumber**</span><span class="sxs-lookup"><span data-stu-id="857c1-366">**RevisionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-367">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="857c1-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-369">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Description \\ \\ System")</span><span class="sxs-lookup"><span data-stu-id="857c1-369">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DESCRIPTION\\\\System")</span></span>
</dt> </dl>

<span data-ttu-id="857c1-370">Número de revisión de la placa base.</span><span class="sxs-lookup"><span data-stu-id="857c1-370">Revision number of the motherboard.</span></span>

<span data-ttu-id="857c1-371">Ejemplo: "00"</span><span class="sxs-lookup"><span data-stu-id="857c1-371">Example: "00"</span></span>

</dd> <dt>

<span data-ttu-id="857c1-372">**SecondaryBusType**</span><span class="sxs-lookup"><span data-stu-id="857c1-372">**SecondaryBusType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-373">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="857c1-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-374">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-375">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ hardware \\ \\ Description \\ \\ System \\ \\ MultifunctionAdapter \| Identifier")</span><span class="sxs-lookup"><span data-stu-id="857c1-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DESCRIPTION\\\\System\\\\MultifunctionAdapter\|Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="857c1-376">Tipo de bus secundario de la placa base.</span><span class="sxs-lookup"><span data-stu-id="857c1-376">Secondary bus type of the motherboard.</span></span>

<span data-ttu-id="857c1-377">Ejemplo: "ISA"</span><span class="sxs-lookup"><span data-stu-id="857c1-377">Example: "ISA"</span></span>

</dd> <dt>

<span data-ttu-id="857c1-378">**Estado**</span><span class="sxs-lookup"><span data-stu-id="857c1-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-379">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="857c1-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-381">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="857c1-381">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="857c1-382">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="857c1-382">Current status of the object.</span></span> <span data-ttu-id="857c1-383">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="857c1-383">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="857c1-384">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="857c1-384">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="857c1-385">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="857c1-385">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="857c1-386">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="857c1-386">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="857c1-387">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="857c1-387">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="857c1-388">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-388">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="857c1-389">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="857c1-389">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="857c1-390">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="857c1-390">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="857c1-391">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="857c1-391">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="857c1-392">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="857c1-392">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="857c1-393">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="857c1-393">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="857c1-394">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="857c1-394">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="857c1-395">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="857c1-395">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="857c1-396">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="857c1-396">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="857c1-397">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="857c1-397">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="857c1-398">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="857c1-398">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="857c1-399">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="857c1-399">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="857c1-400">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="857c1-400">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="857c1-401">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="857c1-401">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="857c1-402">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="857c1-402">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-403">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="857c1-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-405">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="857c1-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="857c1-406">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="857c1-406">State of the logical device.</span></span> <span data-ttu-id="857c1-407">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="857c1-407">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="857c1-408">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="857c1-409">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="857c1-409">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="857c1-410">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="857c1-410">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="857c1-411">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="857c1-411">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="857c1-412">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="857c1-412">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="857c1-413">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="857c1-413">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="857c1-414">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="857c1-414">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-415">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="857c1-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-416">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-417">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="857c1-417">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="857c1-418">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="857c1-418">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="857c1-419">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="857c1-420">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="857c1-420">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="857c1-421">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="857c1-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="857c1-422">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="857c1-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="857c1-423">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="857c1-423">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="857c1-424">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="857c1-424">Name of the scoping system.</span></span>

<span data-ttu-id="857c1-425">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-425">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="857c1-426">Observaciones</span><span class="sxs-lookup"><span data-stu-id="857c1-426">Remarks</span></span>

<span data-ttu-id="857c1-427">La **clase \_ MotherboardDevice de Win32** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="857c1-427">The **Win32\_MotherboardDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="857c1-428">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="857c1-428">Examples</span></span>

<span data-ttu-id="857c1-429">Los siguientes ejemplos de código de [JavaScript](https://Gallery.TechNet.Microsoft.Com/05bbadf8-1356-43a6-82fc-fcab40233fe5) y [PowerShell](https://Gallery.TechNet.Microsoft.Com/cb520044-836e-425c-8c12-a9586d1c0e6e) recuperan información de la placa base.</span><span class="sxs-lookup"><span data-stu-id="857c1-429">The following [JavaScript](https://Gallery.TechNet.Microsoft.Com/05bbadf8-1356-43a6-82fc-fcab40233fe5) and [PowerShell](https://Gallery.TechNet.Microsoft.Com/cb520044-836e-425c-8c12-a9586d1c0e6e) code samples retrieve motherboard information.</span></span>

<span data-ttu-id="857c1-430">El siguiente ejemplo de código de VBScript recupera información de la placa base.</span><span class="sxs-lookup"><span data-stu-id="857c1-430">The following VBScript code sample retrieves motherboard information.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_MotherboardDevice") 
 
For Each objItem in colItems 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Primary Bus Type: " & objItem.PrimaryBusType 
    Wscript.Echo "Secondary Bus Type: " & objItem.SecondaryBusType 
    Wscript.Echo 
Next 
```



## <a name="requirements"></a><span data-ttu-id="857c1-431">Requisitos</span><span class="sxs-lookup"><span data-stu-id="857c1-431">Requirements</span></span>



| <span data-ttu-id="857c1-432">Requisito</span><span class="sxs-lookup"><span data-stu-id="857c1-432">Requirement</span></span> | <span data-ttu-id="857c1-433">Value</span><span class="sxs-lookup"><span data-stu-id="857c1-433">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="857c1-434">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="857c1-434">Minimum supported client</span></span><br/> | <span data-ttu-id="857c1-435">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="857c1-435">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="857c1-436">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="857c1-436">Minimum supported server</span></span><br/> | <span data-ttu-id="857c1-437">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="857c1-437">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="857c1-438">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="857c1-438">Namespace</span></span><br/>                | <span data-ttu-id="857c1-439">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="857c1-439">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="857c1-440">MOF</span><span class="sxs-lookup"><span data-stu-id="857c1-440">MOF</span></span><br/>                      | <dl> <span data-ttu-id="857c1-441"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="857c1-441"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="857c1-442">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="857c1-442">DLL</span></span><br/>                      | <dl> <span data-ttu-id="857c1-443"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="857c1-443"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="857c1-444">Vea también</span><span class="sxs-lookup"><span data-stu-id="857c1-444">See also</span></span>

<dl> <dt>

[<span data-ttu-id="857c1-445">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="857c1-445">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="857c1-446">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="857c1-446">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

