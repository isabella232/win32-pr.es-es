---
description: La \_ clase AlarmDevice de CIM es un dispositivo de alarma que emite indicaciones auditivas o visibles relacionadas con una situación problemática.
ms.assetid: 1f64aea4-d0a4-480b-9802-e2c21e71c754
ms.tgt_platform: multiple
title: CIM_AlarmDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice
- CIM_AlarmDevice.Caption
- CIM_AlarmDevice.Description
- CIM_AlarmDevice.InstallDate
- CIM_AlarmDevice.Name
- CIM_AlarmDevice.Status
- CIM_AlarmDevice.Availability
- CIM_AlarmDevice.ConfigManagerErrorCode
- CIM_AlarmDevice.ConfigManagerUserConfig
- CIM_AlarmDevice.CreationClassName
- CIM_AlarmDevice.DeviceID
- CIM_AlarmDevice.PowerManagementCapabilities
- CIM_AlarmDevice.ErrorCleared
- CIM_AlarmDevice.ErrorDescription
- CIM_AlarmDevice.LastErrorCode
- CIM_AlarmDevice.PNPDeviceID
- CIM_AlarmDevice.PowerManagementSupported
- CIM_AlarmDevice.StatusInfo
- CIM_AlarmDevice.SystemCreationClassName
- CIM_AlarmDevice.SystemName
- CIM_AlarmDevice.AudibleAlarm
- CIM_AlarmDevice.Urgency
- CIM_AlarmDevice.VisibleAlarm
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 622a6031f36140e23514b925835cebae84b35025
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539075"
---
# <a name="cim_alarmdevice-class"></a><span data-ttu-id="f6871-103">\_Clase AlarmDevice de CIM</span><span class="sxs-lookup"><span data-stu-id="f6871-103">CIM\_AlarmDevice class</span></span>

<span data-ttu-id="f6871-104">La **clase \_ AlarmDevice de CIM** es un dispositivo de alarma que emite indicaciones auditivas o visibles relacionadas con una situación problemática.</span><span class="sxs-lookup"><span data-stu-id="f6871-104">The **CIM\_AlarmDevice** class is an alarm device that emits audible or visible indications related to a problem situation.</span></span>

<span data-ttu-id="f6871-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f6871-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f6871-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f6871-106">Properties are listed in alphabetic order, not MOF order.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f6871-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="f6871-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f6871-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f6871-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f6871-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6871-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B66-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AlarmDevice : CIM_LogicalDevice
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
  boolean  AudibleAlarm;
  uint16   Urgency;
  boolean  VisibleAlarm;
};
```

## <a name="members"></a><span data-ttu-id="f6871-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f6871-110">Members</span></span>

<span data-ttu-id="f6871-111">La clase **CIM \_ AlarmDevice** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f6871-111">The **CIM\_AlarmDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="f6871-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="f6871-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f6871-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6871-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f6871-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="f6871-114">Methods</span></span>

<span data-ttu-id="f6871-115">La clase **CIM \_ AlarmDevice** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f6871-115">The **CIM\_AlarmDevice** class has these methods.</span></span>



| <span data-ttu-id="f6871-116">Método</span><span class="sxs-lookup"><span data-stu-id="f6871-116">Method</span></span>                                                                 | <span data-ttu-id="f6871-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6871-117">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6871-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="f6871-118">**Reset**</span></span>](reset-method-in-class-cim-alarmdevice.md)                 | <span data-ttu-id="f6871-119">Solicita un restablecimiento de dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f6871-119">Requests a logical device reset.</span></span> <span data-ttu-id="f6871-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="f6871-120">Not implemented by WMI.</span></span><br/>                                                                     |
| [<span data-ttu-id="f6871-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f6871-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-alarmdevice.md) | <span data-ttu-id="f6871-122">Establece el estado de energía deseado para un dispositivo lógico y el momento en que el dispositivo debe ponerse en ese estado.</span><span class="sxs-lookup"><span data-stu-id="f6871-122">Sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="f6871-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="f6871-123">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="f6871-124">**SetUrgency**</span><span class="sxs-lookup"><span data-stu-id="f6871-124">**SetUrgency**</span></span>](seturgency-method-in-class-cim-alarmdevice.md)       | <span data-ttu-id="f6871-125">Establece el nivel de urgencia deseado para la alarma.</span><span class="sxs-lookup"><span data-stu-id="f6871-125">Sets the desired urgency level for the alarm.</span></span> <span data-ttu-id="f6871-126">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="f6871-126">Not implemented by WMI.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="f6871-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6871-127">Properties</span></span>

<span data-ttu-id="f6871-128">La clase **CIM \_ AlarmDevice** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f6871-128">The **CIM\_AlarmDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6871-129">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="f6871-129">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-130">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f6871-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6871-132">Si es **true**, la alarma es audible.</span><span class="sxs-lookup"><span data-stu-id="f6871-132">If **TRUE**, the alarm is audible.</span></span>

</dd> <dt>

<span data-ttu-id="f6871-133">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="f6871-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-134">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6871-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6871-136">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="f6871-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f6871-137">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f6871-137">Availability and status of the device.</span></span>

<span data-ttu-id="f6871-138">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f6871-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="f6871-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f6871-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="f6871-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f6871-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="f6871-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f6871-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="f6871-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f6871-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="f6871-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f6871-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="f6871-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f6871-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="f6871-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f6871-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="f6871-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f6871-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="f6871-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f6871-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="f6871-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f6871-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="f6871-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f6871-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="f6871-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f6871-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="f6871-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-152">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="f6871-152">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f6871-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="f6871-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-154">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="f6871-154">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f6871-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="f6871-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-156">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="f6871-156">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f6871-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="f6871-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f6871-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="f6871-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-159">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="f6871-159">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f6871-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="f6871-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-161">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="f6871-161">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f6871-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="f6871-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-163">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="f6871-163">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f6871-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="f6871-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-165">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="f6871-165">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f6871-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="f6871-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-167">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="f6871-167">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6871-168">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f6871-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6871-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6871-171">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f6871-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f6871-172">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f6871-172">A short textual description of the object.</span></span>

<span data-ttu-id="f6871-173">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6871-174">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f6871-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-175">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6871-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6871-177">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f6871-177">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f6871-178">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="f6871-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="f6871-179">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f6871-180">**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="f6871-180">**This device is working properly.**</span></span> <span data-ttu-id="f6871-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="f6871-181">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f6871-182">**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="f6871-182">**This device is not configured correctly.**</span></span> <span data-ttu-id="f6871-183">(1)</span><span class="sxs-lookup"><span data-stu-id="f6871-183">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f6871-184">**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f6871-184">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f6871-185">(2)</span><span class="sxs-lookup"><span data-stu-id="f6871-185">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f6871-186">**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="f6871-186">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f6871-187">(3)</span><span class="sxs-lookup"><span data-stu-id="f6871-187">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f6871-188">**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="f6871-188">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f6871-189">(4)</span><span class="sxs-lookup"><span data-stu-id="f6871-189">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f6871-190">**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="f6871-190">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f6871-191">(5)</span><span class="sxs-lookup"><span data-stu-id="f6871-191">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f6871-192">**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="f6871-192">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f6871-193"> (6)</span><span class="sxs-lookup"><span data-stu-id="f6871-193">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f6871-194">**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="f6871-194">**Cannot filter.**</span></span> <span data-ttu-id="f6871-195">(7)</span><span class="sxs-lookup"><span data-stu-id="f6871-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f6871-196">**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f6871-196">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f6871-197">(8)</span><span class="sxs-lookup"><span data-stu-id="f6871-197">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f6871-198">**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="f6871-198">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f6871-199">(9)</span><span class="sxs-lookup"><span data-stu-id="f6871-199">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f6871-200">**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="f6871-200">**This device cannot start.**</span></span> <span data-ttu-id="f6871-201">(10)</span><span class="sxs-lookup"><span data-stu-id="f6871-201">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f6871-202">**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f6871-202">**This device failed.**</span></span> <span data-ttu-id="f6871-203">(11)</span><span class="sxs-lookup"><span data-stu-id="f6871-203">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f6871-204">**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="f6871-204">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f6871-205">(12)</span><span class="sxs-lookup"><span data-stu-id="f6871-205">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f6871-206">**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f6871-206">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f6871-207">(13)</span><span class="sxs-lookup"><span data-stu-id="f6871-207">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f6871-208">**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="f6871-208">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f6871-209">(14)</span><span class="sxs-lookup"><span data-stu-id="f6871-209">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f6871-210">**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="f6871-210">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f6871-211">(15)</span><span class="sxs-lookup"><span data-stu-id="f6871-211">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f6871-212">**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f6871-212">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f6871-213">(16)</span><span class="sxs-lookup"><span data-stu-id="f6871-213">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f6871-214">**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="f6871-214">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f6871-215">(17)</span><span class="sxs-lookup"><span data-stu-id="f6871-215">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f6871-216">**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f6871-216">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f6871-217">(18)</span><span class="sxs-lookup"><span data-stu-id="f6871-217">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f6871-218">**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="f6871-218">**Failure using the VxD loader.**</span></span> <span data-ttu-id="f6871-219">(19)</span><span class="sxs-lookup"><span data-stu-id="f6871-219">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f6871-220">**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="f6871-220">**Your registry might be corrupted.**</span></span> <span data-ttu-id="f6871-221">(20)</span><span class="sxs-lookup"><span data-stu-id="f6871-221">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f6871-222">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f6871-222">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f6871-223">(21)</span><span class="sxs-lookup"><span data-stu-id="f6871-223">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f6871-224">**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="f6871-224">**This device is disabled.**</span></span> <span data-ttu-id="f6871-225">(22)</span><span class="sxs-lookup"><span data-stu-id="f6871-225">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f6871-226">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="f6871-226">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f6871-227">(23)</span><span class="sxs-lookup"><span data-stu-id="f6871-227">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f6871-228">**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="f6871-228">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f6871-229">(24)</span><span class="sxs-lookup"><span data-stu-id="f6871-229">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f6871-230">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f6871-230">**Windows is still setting up this device.**</span></span> <span data-ttu-id="f6871-231">(25)</span><span class="sxs-lookup"><span data-stu-id="f6871-231">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f6871-232">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f6871-232">**Windows is still setting up this device.**</span></span> <span data-ttu-id="f6871-233">(26)</span><span class="sxs-lookup"><span data-stu-id="f6871-233">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f6871-234">**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="f6871-234">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f6871-235">(27)</span><span class="sxs-lookup"><span data-stu-id="f6871-235">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f6871-236">**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="f6871-236">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f6871-237">(28)</span><span class="sxs-lookup"><span data-stu-id="f6871-237">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f6871-238">**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="f6871-238">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f6871-239">(29)</span><span class="sxs-lookup"><span data-stu-id="f6871-239">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f6871-240">**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="f6871-240">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f6871-241">(30)</span><span class="sxs-lookup"><span data-stu-id="f6871-241">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f6871-242">**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="f6871-242">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f6871-243">31</span><span class="sxs-lookup"><span data-stu-id="f6871-243">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6871-244">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="f6871-244">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-245">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f6871-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-246">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6871-247">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f6871-247">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f6871-248">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f6871-248">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f6871-249">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-249">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6871-250">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f6871-250">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-251">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6871-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6871-253">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f6871-253">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f6871-254">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="f6871-254">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f6871-255">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="f6871-255">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f6871-256">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-256">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6871-257">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f6871-257">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6871-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6871-260">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="f6871-260">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f6871-261">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f6871-261">A textual description of the object.</span></span>

<span data-ttu-id="f6871-262">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-262">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6871-263">**ID**</span><span class="sxs-lookup"><span data-stu-id="f6871-263">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-264">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6871-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6871-266">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f6871-266">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f6871-267">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f6871-267">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="f6871-268">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-268">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6871-269">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="f6871-269">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-270">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f6871-270">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-271">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6871-272">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="f6871-272">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="f6871-273">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-273">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6871-274">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f6871-274">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-275">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6871-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6871-277">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="f6871-277">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="f6871-278">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6871-279">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f6871-279">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-280">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f6871-280">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6871-282">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="f6871-282">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f6871-283">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="f6871-283">Indicates when the object was installed.</span></span> <span data-ttu-id="f6871-284">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="f6871-284">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f6871-285">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-285">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6871-286">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f6871-286">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-287">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6871-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6871-289">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f6871-289">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f6871-290">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6871-291">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f6871-291">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-292">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6871-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6871-294">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="f6871-294">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f6871-295">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="f6871-295">Label by which the object is known.</span></span> <span data-ttu-id="f6871-296">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="f6871-296">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f6871-297">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-297">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6871-298">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f6871-298">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-299">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6871-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6871-301">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f6871-301">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f6871-302">Indica el identificador de dispositivo Plug and Play Win32 del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f6871-302">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="f6871-303">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="f6871-303">Example: "\*PNP030b"</span></span>

<span data-ttu-id="f6871-304">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6871-305">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f6871-305">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-306">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6871-306">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f6871-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6871-308">Indica las capacidades de energía específicas relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f6871-308">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="f6871-309">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f6871-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="f6871-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-311">Las capacidades relacionadas con la energía son desconocidas.</span><span class="sxs-lookup"><span data-stu-id="f6871-311">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f6871-312"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="f6871-312"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-313">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f6871-313">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f6871-314"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="f6871-314"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-315">Se han deshabilitado las capacidades relacionadas con la energía.</span><span class="sxs-lookup"><span data-stu-id="f6871-315">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f6871-316"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="f6871-316"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-317">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="f6871-317">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f6871-318"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="f6871-318"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-319">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="f6871-319">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f6871-320"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="f6871-320"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-321">Se admite el método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="f6871-321">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="f6871-322">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="f6871-322">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="f6871-323">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="f6871-323">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f6871-324"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="f6871-324"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-325">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="f6871-325">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f6871-326"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="f6871-326"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-327">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o Interval, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="f6871-327">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6871-328">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="f6871-328">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-329">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f6871-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6871-331">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="f6871-331">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="f6871-332">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="f6871-332">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f6871-333">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="f6871-333">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="f6871-334">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="f6871-334">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f6871-335">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6871-336">**Estado**</span><span class="sxs-lookup"><span data-stu-id="f6871-336">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-337">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6871-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6871-339">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="f6871-339">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f6871-340">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="f6871-340">String that indicates the current status of the object.</span></span> <span data-ttu-id="f6871-341">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="f6871-341">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f6871-342">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="f6871-342">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f6871-343">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="f6871-343">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f6871-344">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="f6871-344">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f6871-345">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="f6871-345">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f6871-346">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="f6871-346">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f6871-347">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f6871-348">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f6871-348">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f6871-349">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="f6871-349">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f6871-350">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="f6871-350">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f6871-351">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="f6871-351">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f6871-352">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="f6871-352">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f6871-353">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="f6871-353">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f6871-354">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="f6871-354">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f6871-355">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="f6871-355">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f6871-356">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="f6871-356">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f6871-357">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="f6871-357">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f6871-358">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="f6871-358">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f6871-359">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="f6871-359">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f6871-360">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="f6871-360">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6871-361">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f6871-361">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-362">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6871-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6871-364">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="f6871-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f6871-365">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="f6871-365">State of the logical device.</span></span> <span data-ttu-id="f6871-366">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="f6871-366">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="f6871-367">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f6871-368">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="f6871-368">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f6871-369">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="f6871-369">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f6871-370">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="f6871-370">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f6871-371">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="f6871-371">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f6871-372">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="f6871-372">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f6871-373">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f6871-373">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-374">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6871-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6871-376">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f6871-376">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f6871-377">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="f6871-377">The scoping system's creation class name.</span></span>

<span data-ttu-id="f6871-378">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6871-379">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f6871-379">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-380">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6871-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6871-382">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f6871-382">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f6871-383">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="f6871-383">The scoping system's name.</span></span>

<span data-ttu-id="f6871-384">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-384">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6871-385">**Urgencia**</span><span class="sxs-lookup"><span data-stu-id="f6871-385">**Urgency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-386">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6871-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6871-388">Valor enumerado que indica la frecuencia relativa con la que la alarma parpadea, vibra o emite tonos sonoros.</span><span class="sxs-lookup"><span data-stu-id="f6871-388">Enumerated value that indicates the relative frequency at which the alarm flashes, vibrates, or emits audible tones.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f6871-389"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="f6871-389"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-390">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="f6871-390">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f6871-391"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="f6871-391"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-392">Otros.</span><span class="sxs-lookup"><span data-stu-id="f6871-392">Other.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f6871-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="f6871-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-394">No se admite.</span><span class="sxs-lookup"><span data-stu-id="f6871-394">Not supported.</span></span>

</dd> <dt>

<span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>

<span data-ttu-id="f6871-395"><span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>**Informativo** (3)</span><span class="sxs-lookup"><span data-stu-id="f6871-395"><span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>**Informational** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-396">Informativo.</span><span class="sxs-lookup"><span data-stu-id="f6871-396">Informational.</span></span>

</dd> <dt>

<span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>

<span data-ttu-id="f6871-397"><span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>**No crítico** (4)</span><span class="sxs-lookup"><span data-stu-id="f6871-397"><span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>**Non-Critical** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-398">No crítico.</span><span class="sxs-lookup"><span data-stu-id="f6871-398">Non-critical.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="f6871-399"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (5)</span><span class="sxs-lookup"><span data-stu-id="f6871-399"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-400">Crítico.</span><span class="sxs-lookup"><span data-stu-id="f6871-400">Critical.</span></span>

</dd> <dt>

<span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>

<span data-ttu-id="f6871-401"><span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>**Irrecuperable** (6)</span><span class="sxs-lookup"><span data-stu-id="f6871-401"><span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>**Unrecoverable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f6871-402">Irrecuperable.</span><span class="sxs-lookup"><span data-stu-id="f6871-402">Unrecoverable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f6871-403">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="f6871-403">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6871-404">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f6871-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6871-405">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6871-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6871-406">Si es **true**, la alarma es visible.</span><span class="sxs-lookup"><span data-stu-id="f6871-406">If **TRUE**, the alarm is visible.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6871-407">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6871-407">Remarks</span></span>

<span data-ttu-id="f6871-408">La **clase \_ AlarmDevice de CIM** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="f6871-408">The **CIM\_AlarmDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="f6871-409">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="f6871-409">WMI does not implement this class.</span></span>

<span data-ttu-id="f6871-410">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="f6871-410">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f6871-411">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="f6871-411">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6871-412">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6871-412">Requirements</span></span>



| <span data-ttu-id="f6871-413">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6871-413">Requirement</span></span> | <span data-ttu-id="f6871-414">Value</span><span class="sxs-lookup"><span data-stu-id="f6871-414">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6871-415">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6871-415">Minimum supported client</span></span><br/> | <span data-ttu-id="f6871-416">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6871-416">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f6871-417">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6871-417">Minimum supported server</span></span><br/> | <span data-ttu-id="f6871-418">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6871-418">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f6871-419">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f6871-419">Namespace</span></span><br/>                | <span data-ttu-id="f6871-420">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f6871-420">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f6871-421">MOF</span><span class="sxs-lookup"><span data-stu-id="f6871-421">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6871-422"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6871-422"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6871-423">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6871-423">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6871-424"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6871-424"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6871-425">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6871-425">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6871-426">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f6871-426">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

