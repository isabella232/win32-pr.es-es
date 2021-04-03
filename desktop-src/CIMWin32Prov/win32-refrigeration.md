---
description: La refrigeración de Win32 \_ &\# 32; La clase WMI representa las propiedades de un dispositivo de refrigeración.
ms.assetid: d67ce648-5659-49e5-9427-7c4dbcdfda8c
ms.tgt_platform: multiple
title: Win32_Refrigeration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Refrigeration
- Win32_Refrigeration.Reset
- Win32_Refrigeration.SetPowerState
- Win32_Refrigeration.ActiveCooling
- Win32_Refrigeration.Availability
- Win32_Refrigeration.Caption
- Win32_Refrigeration.ConfigManagerErrorCode
- Win32_Refrigeration.ConfigManagerUserConfig
- Win32_Refrigeration.CreationClassName
- Win32_Refrigeration.Description
- Win32_Refrigeration.DeviceID
- Win32_Refrigeration.ErrorCleared
- Win32_Refrigeration.ErrorDescription
- Win32_Refrigeration.InstallDate
- Win32_Refrigeration.LastErrorCode
- Win32_Refrigeration.Name
- Win32_Refrigeration.PNPDeviceID
- Win32_Refrigeration.PowerManagementCapabilities
- Win32_Refrigeration.PowerManagementSupported
- Win32_Refrigeration.Status
- Win32_Refrigeration.StatusInfo
- Win32_Refrigeration.SystemCreationClassName
- Win32_Refrigeration.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 23db1490d184cbfe38d6c5b65fa7190273ad2a87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998148"
---
# <a name="win32_refrigeration-class"></a><span data-ttu-id="15ad6-103">\_Clase de refrigeración Win32</span><span class="sxs-lookup"><span data-stu-id="15ad6-103">Win32\_Refrigeration class</span></span>

<span data-ttu-id="15ad6-104">La [clase WMI](../wmisdk/retrieving-a-class.md) de **\_ refrigeración de Win32** representa las propiedades de un dispositivo de refrigeración.</span><span class="sxs-lookup"><span data-stu-id="15ad6-104">The **Win32\_Refrigeration** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a refrigeration device.</span></span>

<span data-ttu-id="15ad6-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="15ad6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="15ad6-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="15ad6-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="15ad6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15ad6-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB6-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_Refrigeration : CIM_Refrigeration
{
  boolean  ActiveCooling;
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
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="15ad6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="15ad6-108">Members</span></span>

<span data-ttu-id="15ad6-109">La clase de **\_ refrigeración Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="15ad6-109">The **Win32\_Refrigeration** class has these types of members:</span></span>

-   [<span data-ttu-id="15ad6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="15ad6-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="15ad6-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15ad6-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="15ad6-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="15ad6-112">Methods</span></span>

<span data-ttu-id="15ad6-113">La clase de **\_ refrigeración Win32** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="15ad6-113">The **Win32\_Refrigeration** class has these methods.</span></span>



| <span data-ttu-id="15ad6-114">Método</span><span class="sxs-lookup"><span data-stu-id="15ad6-114">Method</span></span>            | <span data-ttu-id="15ad6-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="15ad6-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15ad6-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="15ad6-116">**Reset**</span></span>         | <span data-ttu-id="15ad6-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="15ad6-117">Not implemented.</span></span> <span data-ttu-id="15ad6-118">Para implementar este método, consulte el método de [**restablecimiento**](reset-method-in-class-cim-controller.md) en el [**\_ frigorífico de CIM**](cim-refrigeration.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Refrigeration**](cim-refrigeration.md).</span></span><br/>                 |
| <span data-ttu-id="15ad6-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="15ad6-119">**SetPowerState**</span></span> | <span data-ttu-id="15ad6-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="15ad6-120">Not implemented.</span></span> <span data-ttu-id="15ad6-121">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**la \_ refrigeración CIM**](cim-refrigeration.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Refrigeration**](cim-refrigeration.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="15ad6-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15ad6-122">Properties</span></span>

<span data-ttu-id="15ad6-123">La clase de **\_ refrigeración Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="15ad6-123">The **Win32\_Refrigeration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15ad6-124">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="15ad6-124">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-125">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="15ad6-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-127">Si **es true**, el dispositivo de enfriamiento proporciona enfriamiento activo, no enfriamiento pasivo.</span><span class="sxs-lookup"><span data-stu-id="15ad6-127">If **TRUE**, the cooling device provides active cooling—not passive cooling.</span></span>

<span data-ttu-id="15ad6-128">Esta propiedad se hereda de [**\_ CoolingDevice CIM**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-128">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="15ad6-129">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="15ad6-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-130">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15ad6-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-132">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="15ad6-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-133">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15ad6-133">Availability and status of the device.</span></span>

<span data-ttu-id="15ad6-134">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="15ad6-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="15ad6-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="15ad6-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="15ad6-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="15ad6-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="15ad6-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-138">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="15ad6-138">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="15ad6-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="15ad6-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="15ad6-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="15ad6-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="15ad6-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="15ad6-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="15ad6-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="15ad6-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="15ad6-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="15ad6-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="15ad6-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="15ad6-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="15ad6-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="15ad6-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="15ad6-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="15ad6-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="15ad6-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="15ad6-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="15ad6-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="15ad6-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-149">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="15ad6-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="15ad6-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="15ad6-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-151">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="15ad6-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="15ad6-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="15ad6-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-153">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="15ad6-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="15ad6-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="15ad6-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="15ad6-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="15ad6-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-156">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="15ad6-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="15ad6-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="15ad6-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-158">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="15ad6-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="15ad6-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="15ad6-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-160">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="15ad6-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="15ad6-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="15ad6-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-162">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="15ad6-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="15ad6-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="15ad6-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-164">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="15ad6-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="15ad6-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="15ad6-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15ad6-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-168">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="15ad6-168">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-169">Breve descripción del objeto: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="15ad6-169">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="15ad6-170">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="15ad6-171">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="15ad6-171">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-172">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15ad6-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-174">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="15ad6-174">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-175">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="15ad6-175">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="15ad6-176">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-176">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="15ad6-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="15ad6-178"> (0)</span><span class="sxs-lookup"><span data-stu-id="15ad6-178">(0)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-179">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="15ad6-179">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="15ad6-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="15ad6-181">(1)</span><span class="sxs-lookup"><span data-stu-id="15ad6-181">(1)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-182">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="15ad6-182">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="15ad6-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="15ad6-184">(2)</span><span class="sxs-lookup"><span data-stu-id="15ad6-184">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="15ad6-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="15ad6-186">(3)</span><span class="sxs-lookup"><span data-stu-id="15ad6-186">(3)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-187">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="15ad6-187">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="15ad6-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="15ad6-189">(4)</span><span class="sxs-lookup"><span data-stu-id="15ad6-189">(4)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-190">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="15ad6-190">Device is not working properly.</span></span> <span data-ttu-id="15ad6-191">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="15ad6-191">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="15ad6-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="15ad6-193">(5)</span><span class="sxs-lookup"><span data-stu-id="15ad6-193">(5)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-194">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="15ad6-194">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="15ad6-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="15ad6-196"> (6)</span><span class="sxs-lookup"><span data-stu-id="15ad6-196">(6)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-197">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="15ad6-197">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="15ad6-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="15ad6-199">(7)</span><span class="sxs-lookup"><span data-stu-id="15ad6-199">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="15ad6-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="15ad6-201">(8)</span><span class="sxs-lookup"><span data-stu-id="15ad6-201">(8)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-202">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15ad6-202">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="15ad6-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="15ad6-204">(9)</span><span class="sxs-lookup"><span data-stu-id="15ad6-204">(9)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-205">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="15ad6-205">Device is not working properly.</span></span> <span data-ttu-id="15ad6-206">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15ad6-206">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="15ad6-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="15ad6-208">(10)</span><span class="sxs-lookup"><span data-stu-id="15ad6-208">(10)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-209">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="15ad6-209">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="15ad6-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="15ad6-211">(11)</span><span class="sxs-lookup"><span data-stu-id="15ad6-211">(11)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-212">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15ad6-212">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="15ad6-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="15ad6-214">(12)</span><span class="sxs-lookup"><span data-stu-id="15ad6-214">(12)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-215">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="15ad6-215">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="15ad6-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="15ad6-217">(13)</span><span class="sxs-lookup"><span data-stu-id="15ad6-217">(13)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-218">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15ad6-218">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="15ad6-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="15ad6-220">(14)</span><span class="sxs-lookup"><span data-stu-id="15ad6-220">(14)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-221">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="15ad6-221">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="15ad6-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="15ad6-223">(15)</span><span class="sxs-lookup"><span data-stu-id="15ad6-223">(15)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-224">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="15ad6-224">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="15ad6-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="15ad6-226">(16)</span><span class="sxs-lookup"><span data-stu-id="15ad6-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-227">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15ad6-227">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="15ad6-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="15ad6-229">(17)</span><span class="sxs-lookup"><span data-stu-id="15ad6-229">(17)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-230">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="15ad6-230">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="15ad6-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="15ad6-232">(18)</span><span class="sxs-lookup"><span data-stu-id="15ad6-232">(18)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-233">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="15ad6-233">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="15ad6-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="15ad6-235">(19)</span><span class="sxs-lookup"><span data-stu-id="15ad6-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="15ad6-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="15ad6-237">(20)</span><span class="sxs-lookup"><span data-stu-id="15ad6-237">(20)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-238">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="15ad6-238">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="15ad6-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="15ad6-240">(21)</span><span class="sxs-lookup"><span data-stu-id="15ad6-240">(21)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-241">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="15ad6-241">System failure.</span></span> <span data-ttu-id="15ad6-242">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="15ad6-242">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="15ad6-243">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15ad6-243">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="15ad6-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="15ad6-245">(22)</span><span class="sxs-lookup"><span data-stu-id="15ad6-245">(22)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-246">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="15ad6-246">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="15ad6-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="15ad6-248">(23)</span><span class="sxs-lookup"><span data-stu-id="15ad6-248">(23)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-249">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="15ad6-249">System failure.</span></span> <span data-ttu-id="15ad6-250">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="15ad6-250">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="15ad6-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="15ad6-252">(24)</span><span class="sxs-lookup"><span data-stu-id="15ad6-252">(24)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-253">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="15ad6-253">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="15ad6-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="15ad6-255">(25)</span><span class="sxs-lookup"><span data-stu-id="15ad6-255">(25)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-256">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15ad6-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="15ad6-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="15ad6-258">(26)</span><span class="sxs-lookup"><span data-stu-id="15ad6-258">(26)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-259">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15ad6-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="15ad6-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="15ad6-261">(27)</span><span class="sxs-lookup"><span data-stu-id="15ad6-261">(27)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-262">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="15ad6-262">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="15ad6-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="15ad6-264">(28)</span><span class="sxs-lookup"><span data-stu-id="15ad6-264">(28)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-265">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="15ad6-265">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="15ad6-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="15ad6-267">(29)</span><span class="sxs-lookup"><span data-stu-id="15ad6-267">(29)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-268">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="15ad6-268">Device is disabled.</span></span> <span data-ttu-id="15ad6-269">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="15ad6-269">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="15ad6-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="15ad6-271">(30)</span><span class="sxs-lookup"><span data-stu-id="15ad6-271">(30)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-272">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="15ad6-272">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="15ad6-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="15ad6-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="15ad6-274">31</span><span class="sxs-lookup"><span data-stu-id="15ad6-274">(31)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-275">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="15ad6-275">Device is not working properly.</span></span> <span data-ttu-id="15ad6-276">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="15ad6-276">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="15ad6-277">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="15ad6-277">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-278">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="15ad6-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-280">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="15ad6-280">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-281">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="15ad6-281">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="15ad6-282">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="15ad6-283">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="15ad6-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-284">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15ad6-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-286">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="15ad6-286">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-287">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="15ad6-287">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="15ad6-288">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="15ad6-288">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="15ad6-289">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="15ad6-290">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="15ad6-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-291">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15ad6-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-293">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="15ad6-293">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-294">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="15ad6-294">Description of the object.</span></span>

<span data-ttu-id="15ad6-295">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="15ad6-296">**ID**</span><span class="sxs-lookup"><span data-stu-id="15ad6-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-297">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15ad6-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-299">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="15ad6-299">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-300">Identificador único del dispositivo de refrigeración.</span><span class="sxs-lookup"><span data-stu-id="15ad6-300">Unique identifier of the refrigeration device.</span></span>

<span data-ttu-id="15ad6-301">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="15ad6-302">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="15ad6-302">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-303">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="15ad6-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-305">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="15ad6-305">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="15ad6-306">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="15ad6-307">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="15ad6-307">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-308">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15ad6-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-310">Más información sobre el error registrado en **LastErrorCode** y las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="15ad6-310">More information about the error recorded in **LastErrorCode**, and any corrective actions that may be taken.</span></span>

<span data-ttu-id="15ad6-311">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="15ad6-312">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="15ad6-312">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-313">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="15ad6-313">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-315">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="15ad6-315">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-316">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="15ad6-316">Date and time the object was installed.</span></span> <span data-ttu-id="15ad6-317">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="15ad6-317">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="15ad6-318">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="15ad6-319">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="15ad6-319">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-320">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15ad6-320">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-322">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="15ad6-322">Last error code reported by the logical device.</span></span>

<span data-ttu-id="15ad6-323">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="15ad6-324">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="15ad6-324">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-325">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15ad6-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-327">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="15ad6-327">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-328">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="15ad6-328">Label by which the object is known.</span></span> <span data-ttu-id="15ad6-329">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="15ad6-329">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="15ad6-330">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="15ad6-331">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="15ad6-331">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-332">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15ad6-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-334">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="15ad6-334">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-335">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="15ad6-335">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="15ad6-336">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="15ad6-337">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="15ad6-337">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="15ad6-338">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="15ad6-338">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-339">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15ad6-339">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-341">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="15ad6-341">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="15ad6-342">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="15ad6-342">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="15ad6-343"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="15ad6-343"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="15ad6-344"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="15ad6-344"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-345">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15ad6-345">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="15ad6-346"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="15ad6-346"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="15ad6-347"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="15ad6-347"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-348">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="15ad6-348">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="15ad6-349"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="15ad6-349"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-350">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="15ad6-350">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="15ad6-351"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="15ad6-351"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-352">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="15ad6-352">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="15ad6-353">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="15ad6-353">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="15ad6-354">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-354">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="15ad6-355"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="15ad6-355"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-356">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="15ad6-356">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="15ad6-357"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="15ad6-357"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="15ad6-358">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="15ad6-358">Timed Power-On Supported</span></span>

<span data-ttu-id="15ad6-359">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="15ad6-359">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="15ad6-360">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="15ad6-360">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-361">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="15ad6-361">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-363">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="15ad6-363">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="15ad6-364">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="15ad6-364">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="15ad6-365">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="15ad6-366">**Estado**</span><span class="sxs-lookup"><span data-stu-id="15ad6-366">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-367">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15ad6-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-369">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="15ad6-369">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-370">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="15ad6-370">Current status of the object.</span></span> <span data-ttu-id="15ad6-371">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="15ad6-371">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="15ad6-372">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="15ad6-372">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="15ad6-373">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="15ad6-373">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="15ad6-374">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="15ad6-374">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="15ad6-375">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="15ad6-375">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="15ad6-376">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-376">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="15ad6-377">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="15ad6-377">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="15ad6-378">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="15ad6-378">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="15ad6-379">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="15ad6-379">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="15ad6-380">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="15ad6-380">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="15ad6-381">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="15ad6-381">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="15ad6-382">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="15ad6-382">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="15ad6-383">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="15ad6-383">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="15ad6-384">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="15ad6-384">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="15ad6-385">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="15ad6-385">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="15ad6-386">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="15ad6-386">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="15ad6-387">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="15ad6-387">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="15ad6-388">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="15ad6-388">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="15ad6-389">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="15ad6-389">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="15ad6-390">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="15ad6-390">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-391">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="15ad6-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-392">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-393">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="15ad6-393">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-394">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="15ad6-394">State of the logical device.</span></span> <span data-ttu-id="15ad6-395">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="15ad6-395">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="15ad6-396">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="15ad6-397">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="15ad6-397">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="15ad6-398">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="15ad6-398">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="15ad6-399">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="15ad6-399">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="15ad6-400">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="15ad6-400">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="15ad6-401">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="15ad6-401">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="15ad6-402">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="15ad6-402">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-403">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15ad6-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-405">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="15ad6-405">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-406">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="15ad6-406">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="15ad6-407">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-407">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="15ad6-408">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="15ad6-408">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15ad6-409">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15ad6-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15ad6-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15ad6-411">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="15ad6-411">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="15ad6-412">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="15ad6-412">Name of the scoping system.</span></span>

<span data-ttu-id="15ad6-413">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15ad6-414">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15ad6-414">Remarks</span></span>

<span data-ttu-id="15ad6-415">La clase de **\_ refrigeración de Win32** deriva de [**la \_ refrigeración CIM**](cim-refrigeration.md).</span><span class="sxs-lookup"><span data-stu-id="15ad6-415">The **Win32\_Refrigeration** class is derived from [**CIM\_Refrigeration**](cim-refrigeration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15ad6-416">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15ad6-416">Requirements</span></span>



| <span data-ttu-id="15ad6-417">Requisito</span><span class="sxs-lookup"><span data-stu-id="15ad6-417">Requirement</span></span> | <span data-ttu-id="15ad6-418">Value</span><span class="sxs-lookup"><span data-stu-id="15ad6-418">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15ad6-419">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15ad6-419">Minimum supported client</span></span><br/> | <span data-ttu-id="15ad6-420">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15ad6-420">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15ad6-421">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15ad6-421">Minimum supported server</span></span><br/> | <span data-ttu-id="15ad6-422">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15ad6-422">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15ad6-423">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="15ad6-423">Namespace</span></span><br/>                | <span data-ttu-id="15ad6-424">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="15ad6-424">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="15ad6-425">MOF</span><span class="sxs-lookup"><span data-stu-id="15ad6-425">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15ad6-426"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15ad6-426"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="15ad6-427">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="15ad6-427">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15ad6-428"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15ad6-428"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15ad6-429">Vea también</span><span class="sxs-lookup"><span data-stu-id="15ad6-429">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ad6-430">**\_Refrigeración CIM**</span><span class="sxs-lookup"><span data-stu-id="15ad6-430">**CIM\_Refrigeration**</span></span>](cim-refrigeration.md)
</dt> <dt>

[<span data-ttu-id="15ad6-431">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="15ad6-431">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
