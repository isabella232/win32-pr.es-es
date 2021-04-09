---
description: Epresents las propiedades de un dispositivo Plug and Play.
ms.assetid: 621f4410-8d8f-4afa-b0f0-beed263f3a13
ms.tgt_platform: multiple
title: Win32_PnPEntity (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity
- Win32_PnPEntity.Reset
- Win32_PnPEntity.SetPowerState
- Win32_PnPEntity.Availability
- Win32_PnPEntity.Caption
- Win32_PnPEntity.ClassGuid
- Win32_PnPEntity.CompatibleID
- Win32_PnPEntity.ConfigManagerErrorCode
- Win32_PnPEntity.ConfigManagerUserConfig
- Win32_PnPEntity.CreationClassName
- Win32_PnPEntity.Description
- Win32_PnPEntity.DeviceID
- Win32_PnPEntity.ErrorCleared
- Win32_PnPEntity.ErrorDescription
- Win32_PnPEntity.HardwareID
- Win32_PnPEntity.InstallDate
- Win32_PnPEntity.LastErrorCode
- Win32_PnPEntity.Manufacturer
- Win32_PnPEntity.Name
- Win32_PnPEntity.PNPClass
- Win32_PnPEntity.PNPDeviceID
- Win32_PnPEntity.PowerManagementCapabilities
- Win32_PnPEntity.PowerManagementSupported
- Win32_PnPEntity.Present
- Win32_PnPEntity.Service
- Win32_PnPEntity.Status
- Win32_PnPEntity.StatusInfo
- Win32_PnPEntity.SystemCreationClassName
- Win32_PnPEntity.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62eaa59944c9b71a1b8b3520969122ab23350bba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152862"
---
# <a name="win32_pnpentity-class"></a><span data-ttu-id="20622-103">\_Clase Win32 PnPEntity</span><span class="sxs-lookup"><span data-stu-id="20622-103">Win32\_PnPEntity class</span></span>

<span data-ttu-id="20622-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PnPEntity de Win32** representa las propiedades de un dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="20622-104">The **Win32\_PnPEntity** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a Plug and Play device.</span></span> <span data-ttu-id="20622-105">Plug and Play entidades se muestran como entradas en el Administrador de dispositivos se encuentra en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="20622-105">Plug and Play entities are shown as entries in the Device Manager located in Control Panel.</span></span>

<span data-ttu-id="20622-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="20622-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="20622-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="20622-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="20622-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20622-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FE28FD98-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPEntity : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  string   ClassGuid;
  string   CompatibleID[];
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   HardwareID[];
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  string   Name;
  string   PNPClass;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  boolean  Present;
  string   Service;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="20622-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="20622-109">Members</span></span>

<span data-ttu-id="20622-110">La **clase \_ PnPEntity de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="20622-110">The **Win32\_PnPEntity** class has these types of members:</span></span>

-   [<span data-ttu-id="20622-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="20622-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="20622-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="20622-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="20622-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="20622-113">Methods</span></span>

<span data-ttu-id="20622-114">La clase **Win32 \_ PnPEntity** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="20622-114">The **Win32\_PnPEntity** class has these methods.</span></span>



| <span data-ttu-id="20622-115">Método</span><span class="sxs-lookup"><span data-stu-id="20622-115">Method</span></span>                                                             | <span data-ttu-id="20622-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="20622-116">Description</span></span>                                                                                                                                                                                    |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20622-117">**Activa**</span><span class="sxs-lookup"><span data-stu-id="20622-117">**Disable**</span></span>](disable-win32-pnpentity.md)                         | <span data-ttu-id="20622-118">Deshabilita este dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="20622-118">Disables this Plug and Play device.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="20622-119">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="20622-119">**Enable**</span></span>](enable-win32-pnpentity.md)                           | <span data-ttu-id="20622-120">Habilita este Plug and Play dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20622-120">Enables this Plug and Play device.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="20622-121">**GetDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="20622-121">**GetDeviceProperties**</span></span>](getdeviceproperties-win32-pnpentity.md) | <span data-ttu-id="20622-122">Obtiene las propiedades especificadas de este Plug and Play dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20622-122">Gets the specified properties of this Plug and Play device.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="20622-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="20622-123">**Reset**</span></span>                                                          | <span data-ttu-id="20622-124">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="20622-124">Not implemented.</span></span> <span data-ttu-id="20622-125">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**el \_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-125">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/>                 |
| <span data-ttu-id="20622-126">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="20622-126">**SetPowerState**</span></span>                                                  | <span data-ttu-id="20622-127">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="20622-127">Not implemented.</span></span> <span data-ttu-id="20622-128">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**el \_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-128">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="20622-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="20622-129">Properties</span></span>

<span data-ttu-id="20622-130">La **clase \_ PnPEntity de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="20622-130">The **Win32\_PnPEntity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20622-131">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="20622-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-132">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20622-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20622-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-134">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="20622-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="20622-135">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20622-135">Availability and status of the device.</span></span>

<span data-ttu-id="20622-136">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20622-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="20622-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20622-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="20622-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="20622-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="20622-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="20622-140">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="20622-140">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="20622-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="20622-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="20622-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="20622-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="20622-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="20622-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="20622-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="20622-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="20622-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="20622-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="20622-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="20622-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="20622-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="20622-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="20622-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="20622-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="20622-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="20622-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="20622-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="20622-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="20622-151">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="20622-151">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="20622-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="20622-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="20622-153">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="20622-153">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="20622-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="20622-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="20622-155">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="20622-155">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="20622-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="20622-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="20622-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="20622-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="20622-158">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="20622-158">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="20622-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="20622-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="20622-160">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="20622-160">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="20622-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="20622-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="20622-162">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="20622-162">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="20622-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="20622-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="20622-164">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="20622-164">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="20622-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="20622-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="20622-166">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="20622-166">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20622-167">**Caption**</span><span class="sxs-lookup"><span data-stu-id="20622-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="20622-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20622-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-170">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="20622-170">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="20622-171">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="20622-171">Short description of the object.</span></span>

<span data-ttu-id="20622-172">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20622-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20622-173">**ClassGuid**</span><span class="sxs-lookup"><span data-stu-id="20622-173">**ClassGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="20622-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20622-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-176">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="20622-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="20622-177">Identificador único global (GUID) de este Plug and Play dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20622-177">Globally unique identifier (GUID) of this Plug and Play device.</span></span>

</dd> <dt>

<span data-ttu-id="20622-178">**CompatibleID**</span><span class="sxs-lookup"><span data-stu-id="20622-178">**CompatibleID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-179">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="20622-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="20622-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20622-181">Cadena de identificación definida por el proveedor que el programa de instalación utiliza para hacer coincidir un dispositivo con un archivo INF.</span><span class="sxs-lookup"><span data-stu-id="20622-181">A vendor-defined identification string that Setup uses to match a device to an INF file.</span></span> <span data-ttu-id="20622-182">Un dispositivo puede tener una lista de identificadores compatibles asociados.</span><span class="sxs-lookup"><span data-stu-id="20622-182">A device can have a list of compatible IDs associated with it.</span></span> <span data-ttu-id="20622-183">Los identificadores compatibles deben aparecer en orden de idoneidad decreciente.</span><span class="sxs-lookup"><span data-stu-id="20622-183">The compatible IDs should be listed in order of decreasing suitability.</span></span> <span data-ttu-id="20622-184">Si el programa de instalación no encuentra un archivo INF que coincida con uno de los identificadores de hardware de un dispositivo, utiliza identificadores compatibles para buscar un archivo INF.</span><span class="sxs-lookup"><span data-stu-id="20622-184">If Setup cannot locate an INF file that matches one of a device's hardware IDs, it uses compatible IDs to locate an INF file.</span></span> <span data-ttu-id="20622-185">Un identificador compatible tiene el mismo formato que un **HardwareID**.</span><span class="sxs-lookup"><span data-stu-id="20622-185">A compatible ID has the same format as a **HardwareID**.</span></span> <span data-ttu-id="20622-186">Para obtener más información, vea [Kit de controladores de Windows](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span><span class="sxs-lookup"><span data-stu-id="20622-186">For more information, see [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span></span>

</dd> <dt>

<span data-ttu-id="20622-187">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="20622-187">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-188">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20622-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20622-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-190">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="20622-190">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="20622-191">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="20622-191">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="20622-192">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-192">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="20622-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="20622-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="20622-194"> (0)</span><span class="sxs-lookup"><span data-stu-id="20622-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="20622-195">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="20622-195">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="20622-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="20622-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="20622-197">(1)</span><span class="sxs-lookup"><span data-stu-id="20622-197">(1)</span></span>


</dt> <dd>

<span data-ttu-id="20622-198">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="20622-198">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="20622-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20622-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="20622-200">(2)</span><span class="sxs-lookup"><span data-stu-id="20622-200">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="20622-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="20622-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="20622-202">(3)</span><span class="sxs-lookup"><span data-stu-id="20622-202">(3)</span></span>


</dt> <dd>

<span data-ttu-id="20622-203">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="20622-203">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="20622-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="20622-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="20622-205">(4)</span><span class="sxs-lookup"><span data-stu-id="20622-205">(4)</span></span>


</dt> <dd>

<span data-ttu-id="20622-206">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="20622-206">Device is not working properly.</span></span> <span data-ttu-id="20622-207">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="20622-207">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="20622-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="20622-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="20622-209">(5)</span><span class="sxs-lookup"><span data-stu-id="20622-209">(5)</span></span>


</dt> <dd>

<span data-ttu-id="20622-210">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="20622-210">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="20622-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="20622-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="20622-212"> (6)</span><span class="sxs-lookup"><span data-stu-id="20622-212">(6)</span></span>


</dt> <dd>

<span data-ttu-id="20622-213">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="20622-213">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="20622-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="20622-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="20622-215">(7)</span><span class="sxs-lookup"><span data-stu-id="20622-215">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="20622-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20622-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="20622-217">(8)</span><span class="sxs-lookup"><span data-stu-id="20622-217">(8)</span></span>


</dt> <dd>

<span data-ttu-id="20622-218">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20622-218">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="20622-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="20622-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="20622-220">(9)</span><span class="sxs-lookup"><span data-stu-id="20622-220">(9)</span></span>


</dt> <dd>

<span data-ttu-id="20622-221">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="20622-221">Device is not working properly.</span></span> <span data-ttu-id="20622-222">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20622-222">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="20622-223"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="20622-223"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="20622-224">(10)</span><span class="sxs-lookup"><span data-stu-id="20622-224">(10)</span></span>


</dt> <dd>

<span data-ttu-id="20622-225">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="20622-225">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="20622-226"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20622-226"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="20622-227">(11)</span><span class="sxs-lookup"><span data-stu-id="20622-227">(11)</span></span>


</dt> <dd>

<span data-ttu-id="20622-228">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20622-228">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="20622-229"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="20622-229"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="20622-230">(12)</span><span class="sxs-lookup"><span data-stu-id="20622-230">(12)</span></span>


</dt> <dd>

<span data-ttu-id="20622-231">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="20622-231">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="20622-232"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20622-232"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="20622-233">(13)</span><span class="sxs-lookup"><span data-stu-id="20622-233">(13)</span></span>


</dt> <dd>

<span data-ttu-id="20622-234">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20622-234">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="20622-235"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="20622-235"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="20622-236">(14)</span><span class="sxs-lookup"><span data-stu-id="20622-236">(14)</span></span>


</dt> <dd>

<span data-ttu-id="20622-237">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="20622-237">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="20622-238"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="20622-238"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="20622-239">(15)</span><span class="sxs-lookup"><span data-stu-id="20622-239">(15)</span></span>


</dt> <dd>

<span data-ttu-id="20622-240">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="20622-240">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="20622-241"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20622-241"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="20622-242">(16)</span><span class="sxs-lookup"><span data-stu-id="20622-242">(16)</span></span>


</dt> <dd>

<span data-ttu-id="20622-243">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20622-243">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="20622-244"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="20622-244"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="20622-245">(17)</span><span class="sxs-lookup"><span data-stu-id="20622-245">(17)</span></span>


</dt> <dd>

<span data-ttu-id="20622-246">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="20622-246">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="20622-247"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20622-247"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="20622-248">(18)</span><span class="sxs-lookup"><span data-stu-id="20622-248">(18)</span></span>


</dt> <dd>

<span data-ttu-id="20622-249">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="20622-249">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="20622-250"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="20622-250"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="20622-251">(19)</span><span class="sxs-lookup"><span data-stu-id="20622-251">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="20622-252"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="20622-252"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="20622-253">(20)</span><span class="sxs-lookup"><span data-stu-id="20622-253">(20)</span></span>


</dt> <dd>

<span data-ttu-id="20622-254">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="20622-254">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="20622-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20622-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="20622-256">(21)</span><span class="sxs-lookup"><span data-stu-id="20622-256">(21)</span></span>


</dt> <dd>

<span data-ttu-id="20622-257">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="20622-257">System failure.</span></span> <span data-ttu-id="20622-258">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="20622-258">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="20622-259">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20622-259">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="20622-260"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="20622-260"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="20622-261">(22)</span><span class="sxs-lookup"><span data-stu-id="20622-261">(22)</span></span>


</dt> <dd>

<span data-ttu-id="20622-262">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="20622-262">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="20622-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="20622-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="20622-264">(23)</span><span class="sxs-lookup"><span data-stu-id="20622-264">(23)</span></span>


</dt> <dd>

<span data-ttu-id="20622-265">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="20622-265">System failure.</span></span> <span data-ttu-id="20622-266">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="20622-266">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="20622-267"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="20622-267"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="20622-268">(24)</span><span class="sxs-lookup"><span data-stu-id="20622-268">(24)</span></span>


</dt> <dd>

<span data-ttu-id="20622-269">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="20622-269">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="20622-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20622-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="20622-271">(25)</span><span class="sxs-lookup"><span data-stu-id="20622-271">(25)</span></span>


</dt> <dd>

<span data-ttu-id="20622-272">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20622-272">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="20622-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20622-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="20622-274">(26)</span><span class="sxs-lookup"><span data-stu-id="20622-274">(26)</span></span>


</dt> <dd>

<span data-ttu-id="20622-275">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20622-275">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="20622-276"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="20622-276"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="20622-277">(27)</span><span class="sxs-lookup"><span data-stu-id="20622-277">(27)</span></span>


</dt> <dd>

<span data-ttu-id="20622-278">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="20622-278">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="20622-279"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="20622-279"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="20622-280">(28)</span><span class="sxs-lookup"><span data-stu-id="20622-280">(28)</span></span>


</dt> <dd>

<span data-ttu-id="20622-281">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="20622-281">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="20622-282"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="20622-282"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="20622-283">(29)</span><span class="sxs-lookup"><span data-stu-id="20622-283">(29)</span></span>


</dt> <dd>

<span data-ttu-id="20622-284">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="20622-284">Device is disabled.</span></span> <span data-ttu-id="20622-285">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="20622-285">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="20622-286"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="20622-286"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="20622-287">(30)</span><span class="sxs-lookup"><span data-stu-id="20622-287">(30)</span></span>


</dt> <dd>

<span data-ttu-id="20622-288">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="20622-288">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="20622-289"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="20622-289"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="20622-290">31</span><span class="sxs-lookup"><span data-stu-id="20622-290">(31)</span></span>


</dt> <dd>

<span data-ttu-id="20622-291">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="20622-291">Device is not working properly.</span></span> <span data-ttu-id="20622-292">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="20622-292">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20622-293">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="20622-293">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-294">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="20622-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20622-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-296">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="20622-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="20622-297">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="20622-297">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="20622-298">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20622-299">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="20622-299">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-300">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="20622-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20622-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-302">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="20622-302">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="20622-303">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="20622-303">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="20622-304">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="20622-304">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="20622-305">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20622-306">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="20622-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="20622-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20622-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-309">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="20622-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="20622-310">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="20622-310">Description of the object.</span></span>

<span data-ttu-id="20622-311">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20622-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20622-312">**ID**</span><span class="sxs-lookup"><span data-stu-id="20622-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-313">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="20622-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20622-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-315">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="20622-315">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="20622-316">Identificador del dispositivo de Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="20622-316">Identifier of the Plug and Play device.</span></span>

<span data-ttu-id="20622-317">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20622-318">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="20622-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-319">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="20622-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20622-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20622-321">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="20622-321">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="20622-322">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20622-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="20622-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="20622-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20622-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20622-326">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="20622-326">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="20622-327">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20622-328">**HardwareID**</span><span class="sxs-lookup"><span data-stu-id="20622-328">**HardwareID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-329">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="20622-329">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="20622-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20622-331">Cadena de identificación definida por el proveedor que el programa de instalación utiliza para hacer coincidir un dispositivo con un archivo INF.</span><span class="sxs-lookup"><span data-stu-id="20622-331">A vendor-defined identification string that Setup uses to match a device to an INF file.</span></span> <span data-ttu-id="20622-332">Normalmente, un dispositivo tiene una lista asociada de identificadores de hardware.</span><span class="sxs-lookup"><span data-stu-id="20622-332">Normally, a device has an associated list of hardware IDs.</span></span> <span data-ttu-id="20622-333">Una excepción es el controlador de bus 1394, que no utiliza identificadores de hardware.</span><span class="sxs-lookup"><span data-stu-id="20622-333">An exception is the 1394 bus driver, which does not use hardware IDs.</span></span> <span data-ttu-id="20622-334">El primer identificador de hardware de la lista debe ser el identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20622-334">The first hardware ID in the list should be the device ID.</span></span> <span data-ttu-id="20622-335">Los identificadores restantes deben aparecer en orden de idoneidad para reducir.</span><span class="sxs-lookup"><span data-stu-id="20622-335">The remaining IDs should be listed in order of decreasing suitability.</span></span>

<span data-ttu-id="20622-336">Los identificadores de hardware aparecen en uno de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="20622-336">Hardware IDs appear in one the following formats:</span></span>

-   <span data-ttu-id="20622-337">\\enumerador de enumerador: ID. de dispositivo específico</span><span class="sxs-lookup"><span data-stu-id="20622-337">enumerator\\enumerator-specific-device-ID</span></span>

    <span data-ttu-id="20622-338">Este es el formato más común para dispositivos Plug and Play individuales.</span><span class="sxs-lookup"><span data-stu-id="20622-338">This is the most common format for individual PnP devices.</span></span> <span data-ttu-id="20622-339">Un ejemplo de un enumerador es el BIOS o ISAPNP.</span><span class="sxs-lookup"><span data-stu-id="20622-339">An example of an enumerator is the BIOS or ISAPNP.</span></span>

-   <span data-ttu-id="20622-340">\*IDENTIFICADOR específico del enumerador</span><span class="sxs-lookup"><span data-stu-id="20622-340">\*enumerator-specific ID</span></span>

    <span data-ttu-id="20622-341">Un asterisco ( \* ) indica el uso por parte de más de un enumerador.</span><span class="sxs-lookup"><span data-stu-id="20622-341">An asterisk (\*) indicates use by more than one enumerator.</span></span>

-   <span data-ttu-id="20622-342">IDENTIFICADOR específico de la clase de dispositivo</span><span class="sxs-lookup"><span data-stu-id="20622-342">device-class-specific ID</span></span>

    <span data-ttu-id="20622-343">Un formato personalizado.</span><span class="sxs-lookup"><span data-stu-id="20622-343">A custom format.</span></span>

<span data-ttu-id="20622-344">Ejemplos de identificadores de hardware:</span><span class="sxs-lookup"><span data-stu-id="20622-344">Examples of Hardware IDs are:</span></span>

<dl> <dd><span data-ttu-id="20622-345">\\ \* PNPOF08 raíz</span><span class="sxs-lookup"><span data-stu-id="20622-345">root\\\*PNPOF08</span></span></dd> <dd><span data-ttu-id="20622-346">PC \\ VEN \_ 1000&DEV \_ 001&subsis \_ 00000000&Rev \_ 02</span><span class="sxs-lookup"><span data-stu-id="20622-346">PC\\VEN\_1000&DEV\_001&SUBSYS\_00000000&REV\_02</span></span></dd> </dl>

<span data-ttu-id="20622-347">Para obtener más información, consulte el [Kit de controladores de Windows](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span><span class="sxs-lookup"><span data-stu-id="20622-347">For more information, see the [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span></span>

</dd> <dt>

<span data-ttu-id="20622-348">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="20622-348">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-349">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="20622-349">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="20622-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-351">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="20622-351">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="20622-352">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="20622-352">Date and time the object was installed.</span></span> <span data-ttu-id="20622-353">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="20622-353">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="20622-354">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20622-354">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20622-355">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="20622-355">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-356">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20622-356">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20622-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20622-358">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="20622-358">Last error code reported by the logical device.</span></span>

<span data-ttu-id="20622-359">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20622-360">**Le**</span><span class="sxs-lookup"><span data-stu-id="20622-360">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-361">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="20622-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20622-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-363">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="20622-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="20622-364">Nombre del fabricante del Plug and Play dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20622-364">Name of the manufacturer of the Plug and Play device.</span></span>

<span data-ttu-id="20622-365">Ejemplo: "Acme"</span><span class="sxs-lookup"><span data-stu-id="20622-365">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="20622-366">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="20622-366">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-367">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="20622-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20622-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-369">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="20622-369">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="20622-370">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="20622-370">Label by which the object is known.</span></span> <span data-ttu-id="20622-371">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="20622-371">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="20622-372">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20622-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20622-373">**PNPClass**</span><span class="sxs-lookup"><span data-stu-id="20622-373">**PNPClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-374">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="20622-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20622-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-376">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="20622-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

> [!WARNING]
> <span data-ttu-id="20622-377">Esta propiedad, a pesar de aparecer en el archivo MOF, no existe realmente en la clase.</span><span class="sxs-lookup"><span data-stu-id="20622-377">This property, despite being listed in the MOF file, does not actually exist in the class.</span></span> <span data-ttu-id="20622-378">La propiedad se describe aquí solo por motivos de integridad y para aclarar el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="20622-378">The property is described here only for the sake of completeness, and to clarify the MOF file itself.</span></span>

 

<span data-ttu-id="20622-379">Nombre del tipo de este Plug and Play dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20622-379">The name of the type of this Plug and Play device.</span></span>

<span data-ttu-id="20622-380">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no está en el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="20622-380">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not in the MOF file.</span></span>

</dd> <dt>

<span data-ttu-id="20622-381">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="20622-381">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-382">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="20622-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20622-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-384">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="20622-384">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="20622-385">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="20622-385">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="20622-386">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-386">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="20622-387">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="20622-387">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="20622-388">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="20622-388">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-389">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20622-389">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="20622-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20622-391">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="20622-391">Not implemented.</span></span>

<span data-ttu-id="20622-392">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20622-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="20622-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="20622-394">Las capacidades relacionadas con la energía son desconocidas.</span><span class="sxs-lookup"><span data-stu-id="20622-394">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="20622-395"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="20622-395"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="20622-396">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20622-396">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="20622-397"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="20622-397"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="20622-398">Se han deshabilitado las capacidades relacionadas con la energía.</span><span class="sxs-lookup"><span data-stu-id="20622-398">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="20622-399"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="20622-399"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="20622-400">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="20622-400">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="20622-401"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="20622-401"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="20622-402">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="20622-402">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="20622-403"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="20622-403"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="20622-404">Se admite el método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="20622-404">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="20622-405">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="20622-405">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="20622-406">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="20622-406">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="20622-407"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="20622-407"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="20622-408">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="20622-408">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="20622-409"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="20622-409"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="20622-410">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o Interval, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="20622-410">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20622-411">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="20622-411">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-412">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="20622-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20622-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20622-414">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="20622-414">Not implemented.</span></span>

<span data-ttu-id="20622-415">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20622-416">**Presente**</span><span class="sxs-lookup"><span data-stu-id="20622-416">**Present**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-417">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="20622-417">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20622-418">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-419">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="20622-419">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="20622-420">Si este Plug and Play dispositivo está actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="20622-420">Whether this Plug and Play device is currently in the system.</span></span>

<span data-ttu-id="20622-421">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite.</span><span class="sxs-lookup"><span data-stu-id="20622-421">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="20622-422">**Servicio**</span><span class="sxs-lookup"><span data-stu-id="20622-422">**Service**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-423">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="20622-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20622-424">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-425">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="20622-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="20622-426">Nombre del servicio que admite este dispositivo Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="20622-426">Name of the service that supports this Plug and Play device.</span></span> <span data-ttu-id="20622-427">Para obtener más información, vea [**Win32 \_ SystemDriverPnPEntity**](win32-systemdriverpnpentity.md).</span><span class="sxs-lookup"><span data-stu-id="20622-427">For more information, see [**Win32\_SystemDriverPnPEntity**](win32-systemdriverpnpentity.md).</span></span>

<span data-ttu-id="20622-428">Ejemplo: "ATAPI"</span><span class="sxs-lookup"><span data-stu-id="20622-428">Example: "atapi"</span></span>

</dd> <dt>

<span data-ttu-id="20622-429">**Estado**</span><span class="sxs-lookup"><span data-stu-id="20622-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-430">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="20622-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20622-431">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-432">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="20622-432">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="20622-433">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="20622-433">Current status of the object.</span></span> <span data-ttu-id="20622-434">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="20622-434">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="20622-435">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="20622-435">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="20622-436">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="20622-436">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="20622-437">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="20622-437">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="20622-438">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="20622-438">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="20622-439">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20622-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="20622-440">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="20622-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="20622-441">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="20622-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="20622-442">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="20622-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="20622-443">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="20622-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20622-444">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="20622-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="20622-445">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="20622-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="20622-446">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="20622-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="20622-447">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="20622-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="20622-448">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="20622-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="20622-449">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="20622-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="20622-450">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="20622-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="20622-451">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="20622-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="20622-452">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="20622-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20622-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="20622-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-454">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20622-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20622-455">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-456">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="20622-456">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="20622-457">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="20622-457">State of the logical device.</span></span> <span data-ttu-id="20622-458">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="20622-458">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="20622-459">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20622-460">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="20622-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20622-461">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="20622-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="20622-462">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="20622-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="20622-463">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="20622-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="20622-464">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="20622-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20622-465">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="20622-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-466">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="20622-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20622-467">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-468">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="20622-468">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="20622-469">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="20622-469">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="20622-470">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20622-471">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="20622-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20622-472">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="20622-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20622-473">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="20622-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20622-474">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="20622-474">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="20622-475">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="20622-475">Name of the scoping system.</span></span>

<span data-ttu-id="20622-476">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20622-477">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20622-477">Remarks</span></span>

<span data-ttu-id="20622-478">La **clase \_ PnPEntity de Win32** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="20622-478">The **Win32\_PnPEntity** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="20622-479">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="20622-479">Examples</span></span>

<span data-ttu-id="20622-480">En el ejemplo de PowerShell de [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) en la galería de TechNet se usa to **Win32 \_ PnPEntity** para recuperar una lista de hardware que no funciona mediante WMI.</span><span class="sxs-lookup"><span data-stu-id="20622-480">The [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell sample on TechNet Gallery uses to **Win32\_PnPEntity** to retrieve a list of non-working hardware using WMI.</span></span>

<span data-ttu-id="20622-481">El siguiente ejemplo de código de VBScript se conecta a un grupo de equipos remotos en el mismo dominio mediante la creación de una matriz de nombres de equipo remoto y, a continuación, la visualización de los nombres de los Plug and Play dispositivos (instancias de Win32 \_ PnPEntity) en cada equipo.</span><span class="sxs-lookup"><span data-stu-id="20622-481">The following VBScript code example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of Win32\_PnPEntity—on each computer.</span></span>


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer& "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



## <a name="requirements"></a><span data-ttu-id="20622-482">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20622-482">Requirements</span></span>



| <span data-ttu-id="20622-483">Requisito</span><span class="sxs-lookup"><span data-stu-id="20622-483">Requirement</span></span> | <span data-ttu-id="20622-484">Value</span><span class="sxs-lookup"><span data-stu-id="20622-484">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20622-485">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20622-485">Minimum supported client</span></span><br/> | <span data-ttu-id="20622-486">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20622-486">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="20622-487">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20622-487">Minimum supported server</span></span><br/> | <span data-ttu-id="20622-488">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20622-488">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="20622-489">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="20622-489">Namespace</span></span><br/>                | <span data-ttu-id="20622-490">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="20622-490">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="20622-491">MOF</span><span class="sxs-lookup"><span data-stu-id="20622-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20622-492"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20622-492"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="20622-493">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="20622-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20622-494"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20622-494"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20622-495">Vea también</span><span class="sxs-lookup"><span data-stu-id="20622-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20622-496">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="20622-496">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="20622-497">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="20622-497">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="20622-498">Conexión a WMI en un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="20622-498">Connecting to WMI on a Remote Computer</span></span>](../wmisdk/connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="20622-499">Tareas WMI: hardware del equipo</span><span class="sxs-lookup"><span data-stu-id="20622-499">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 
