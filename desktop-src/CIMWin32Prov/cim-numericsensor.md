---
description: La \_ clase CIM NumericSensor representa un sensor numérico que devuelve lecturas numéricas y, opcionalmente, admite valores de umbral.
ms.assetid: 9be9ee28-24ee-49d1-871f-73b504c77518
ms.tgt_platform: multiple
title: CIM_NumericSensor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NumericSensor
- CIM_NumericSensor.Accuracy
- CIM_NumericSensor.Availability
- CIM_NumericSensor.Caption
- CIM_NumericSensor.ConfigManagerErrorCode
- CIM_NumericSensor.ConfigManagerUserConfig
- CIM_NumericSensor.CreationClassName
- CIM_NumericSensor.CurrentReading
- CIM_NumericSensor.Description
- CIM_NumericSensor.DeviceID
- CIM_NumericSensor.ErrorCleared
- CIM_NumericSensor.ErrorDescription
- CIM_NumericSensor.InstallDate
- CIM_NumericSensor.IsLinear
- CIM_NumericSensor.LastErrorCode
- CIM_NumericSensor.LowerThresholdCritical
- CIM_NumericSensor.LowerThresholdFatal
- CIM_NumericSensor.LowerThresholdNonCritical
- CIM_NumericSensor.MaxReadable
- CIM_NumericSensor.MinReadable
- CIM_NumericSensor.Name
- CIM_NumericSensor.NominalReading
- CIM_NumericSensor.NormalMax
- CIM_NumericSensor.NormalMin
- CIM_NumericSensor.PNPDeviceID
- CIM_NumericSensor.PowerManagementCapabilities
- CIM_NumericSensor.PowerManagementSupported
- CIM_NumericSensor.Resolution
- CIM_NumericSensor.Status
- CIM_NumericSensor.StatusInfo
- CIM_NumericSensor.SystemCreationClassName
- CIM_NumericSensor.SystemName
- CIM_NumericSensor.Tolerance
- CIM_NumericSensor.UpperThresholdCritical
- CIM_NumericSensor.UpperThresholdFatal
- CIM_NumericSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2888b56e39184b05484cacd587be140b94dc732e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659419"
---
# <a name="cim_numericsensor-class"></a><span data-ttu-id="cc3aa-103">CIM \_ NumericSensor (clase)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-103">CIM\_NumericSensor class</span></span>

<span data-ttu-id="cc3aa-104">La clase **CIM \_ NumericSensor** representa un sensor numérico que devuelve lecturas numéricas y, opcionalmente, admite valores de umbral.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-104">The **CIM\_NumericSensor** class represents a numeric sensor that returns numeric readings and optionally supports thresholds settings.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc3aa-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cc3aa-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cc3aa-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cc3aa-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc3aa-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc3aa-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979C-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_NumericSensor : CIM_Sensor
{
  sint32   Accuracy;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  sint32   CurrentReading;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLinear;
  uint32   LastErrorCode;
  sint32   LowerThresholdCritical;
  sint32   LowerThresholdFatal;
  sint32   LowerThresholdNonCritical;
  sint32   MaxReadable;
  sint32   MinReadable;
  string   Name;
  sint32   NominalReading;
  sint32   NormalMax;
  sint32   NormalMin;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Resolution;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  sint32   Tolerance;
  sint32   UpperThresholdCritical;
  sint32   UpperThresholdFatal;
  sint32   UpperThresholdNonCritical;
};
```

## <a name="members"></a><span data-ttu-id="cc3aa-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="cc3aa-110">Members</span></span>

<span data-ttu-id="cc3aa-111">La clase **CIM \_ NumericSensor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cc3aa-111">The **CIM\_NumericSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="cc3aa-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="cc3aa-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="cc3aa-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cc3aa-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cc3aa-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="cc3aa-114">Methods</span></span>

<span data-ttu-id="cc3aa-115">La clase **CIM \_ NumericSensor** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-115">The **CIM\_NumericSensor** class has these methods.</span></span>



| <span data-ttu-id="cc3aa-116">Método</span><span class="sxs-lookup"><span data-stu-id="cc3aa-116">Method</span></span>                                                                   | <span data-ttu-id="cc3aa-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc3aa-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc3aa-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-118">**Reset**</span></span>](reset-method-in-class-cim-numericsensor.md)                 | <span data-ttu-id="cc3aa-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="cc3aa-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="cc3aa-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-numericsensor.md) | <span data-ttu-id="cc3aa-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="cc3aa-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cc3aa-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cc3aa-124">Properties</span></span>

<span data-ttu-id="cc3aa-125">La clase **CIM \_ NumericSensor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-125">The **CIM\_NumericSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cc3aa-126">**Precisión**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-126">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-127">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-129">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("centésimas de porcentaje")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hundredths of percent")</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-130">Precisión del sensor para la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-130">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="cc3aa-131">Su valor se registra como más o menos centésimas de un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-131">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="cc3aa-132">Esta propiedad, y las propiedades de **resolución** y **tolerancia** , se usan para calcular el valor real de la propiedad física medida.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-132">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="cc3aa-133">La precisión puede variar en función de si el dispositivo es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-133">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-134">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-134">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-135">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-137">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-138">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-138">Availability and status of the device.</span></span>

<span data-ttu-id="cc3aa-139">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cc3aa-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cc3aa-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="cc3aa-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="cc3aa-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="cc3aa-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="cc3aa-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="cc3aa-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="cc3aa-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="cc3aa-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="cc3aa-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="cc3aa-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cc3aa-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="cc3aa-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="cc3aa-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="cc3aa-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-153">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="cc3aa-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-155">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="cc3aa-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-157">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-157">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="cc3aa-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="cc3aa-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-160">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="cc3aa-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-162">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-162">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="cc3aa-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-164">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-164">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="cc3aa-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-166">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-166">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="cc3aa-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-168">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-168">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cc3aa-169">**Caption**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-172">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-173">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-173">Short textual description of the object.</span></span>

<span data-ttu-id="cc3aa-174">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-176">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-178">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-179">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="cc3aa-180">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="cc3aa-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="cc3aa-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-183">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="cc3aa-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="cc3aa-185">(1)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-186">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cc3aa-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="cc3aa-188">(2)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="cc3aa-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="cc3aa-190">(3)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-191">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="cc3aa-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="cc3aa-193">(4)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-194">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-194">Device is not working properly.</span></span> <span data-ttu-id="cc3aa-195">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="cc3aa-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="cc3aa-197">(5)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-198">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="cc3aa-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="cc3aa-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-201">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="cc3aa-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="cc3aa-203">(7)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="cc3aa-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="cc3aa-205">(8)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-206">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="cc3aa-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="cc3aa-208">(9)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-209">El dispositivo no funciona correctamente. el firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-209">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="cc3aa-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="cc3aa-211">(10)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-212">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="cc3aa-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="cc3aa-214">(11)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-215">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="cc3aa-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="cc3aa-217">(12)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-218">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="cc3aa-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="cc3aa-220">(13)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-221">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="cc3aa-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="cc3aa-223">(14)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-224">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="cc3aa-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="cc3aa-226">(15)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-227">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="cc3aa-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="cc3aa-229">(16)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-230">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="cc3aa-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="cc3aa-232">(17)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-233">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cc3aa-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="cc3aa-235">(18)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-236">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="cc3aa-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="cc3aa-238">(19)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="cc3aa-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="cc3aa-240">(20)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-241">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="cc3aa-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="cc3aa-243">(21)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-244">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-244">System failure.</span></span> <span data-ttu-id="cc3aa-245">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="cc3aa-246">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="cc3aa-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="cc3aa-248">(22)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-249">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="cc3aa-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="cc3aa-251">(23)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-252">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-252">System failure.</span></span> <span data-ttu-id="cc3aa-253">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="cc3aa-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="cc3aa-255">(24)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-256">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="cc3aa-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="cc3aa-258">(25)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-259">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="cc3aa-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="cc3aa-261">(26)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-262">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="cc3aa-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="cc3aa-264">(27)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-265">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="cc3aa-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="cc3aa-267">(28)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-268">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="cc3aa-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="cc3aa-270">(29)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-271">El dispositivo está deshabilitado; el firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-271">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="cc3aa-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="cc3aa-273">(30)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-274">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cc3aa-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="cc3aa-276">31</span><span class="sxs-lookup"><span data-stu-id="cc3aa-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-277">El dispositivo no funciona correctamente. Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-277">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cc3aa-278">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-278">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-279">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-281">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-281">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-282">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-282">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="cc3aa-283">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-284">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-284">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-285">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-287">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-287">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-288">Clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-288">Class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cc3aa-289">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-289">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="cc3aa-290">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-291">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-291">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-292">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-292">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-294">Valor actual indicado por el sensor.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-294">Current value indicated by the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-295">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-295">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-296">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-298">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-298">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-299">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-299">Textual description of the object.</span></span>

<span data-ttu-id="cc3aa-300">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-300">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-301">**ID**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-301">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-302">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-304">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-304">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-305">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-305">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="cc3aa-306">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-307">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-307">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-308">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-310">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-310">If **TRUE**, the error reported in **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="cc3aa-311">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-312">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-312">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-313">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-315">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-315">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="cc3aa-316">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-318">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-320">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-320">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-321">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-321">Date and time the object was installed.</span></span> <span data-ttu-id="cc3aa-322">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-322">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="cc3aa-323">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-323">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-324">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-324">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-325">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-325">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-327">Si es **true**, el sensor es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-327">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-328">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-328">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-329">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-331">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-331">Last error code reported by the logical device.</span></span>

<span data-ttu-id="cc3aa-332">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-333">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-333">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-334">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-334">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-336">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-336">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="cc3aa-337">Si la propiedad **CurrentReading** está entre **LowerThresholdCritical** y **LowerThresholdFatal**, el estado actual es Critical.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-337">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="cc3aa-338">Esta propiedad se hereda de **CIM \_ NumericSensor**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-338">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-339">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-339">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-340">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-340">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-342">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-342">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="cc3aa-343">Si la propiedad **CurrentReading** está por debajo de **LowerThresholdFatal**, el estado actual es fatal.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-343">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="cc3aa-344">Esta propiedad se hereda de **CIM \_ NumericSensor**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-344">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-345">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-345">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-346">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-348">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-348">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="cc3aa-349">Si la propiedad **CurrentReading** está entre **LowerThresholdNonCritical** y **UpperThresholdNonCritical**, el sensor informa de un valor normal.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-349">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="cc3aa-350">Si la propiedad **CurrentReading** está entre **LowerThresholdNonCritical** y **LowerThresholdCritical**, el estado actual es no crítico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-350">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="cc3aa-351">Esta propiedad se hereda de **CIM \_ NumericSensor**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-351">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-352">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-352">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-353">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-355">Valor mayor de la propiedad medida que puede ser leída por el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-355">Largest value of the measured property that can be read by the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-356">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-356">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-357">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-357">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-358">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-359">Valor menor de la propiedad medida que puede ser leída por el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-359">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-360">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-361">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-363">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-363">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-364">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-364">Label by which the object is known.</span></span> <span data-ttu-id="cc3aa-365">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-365">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="cc3aa-366">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-366">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-367">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-367">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-368">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-370">Valor esperado o "normal" para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-370">Expected or "normal" value for the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-371">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-371">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-372">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-372">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-373">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-374">Intervalo máximo normal para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-374">Normal maximum range for the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-375">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-375">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-376">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-376">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-378">Intervalo mínimo normal para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-378">Normal minimum range for the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-379">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-379">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-380">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-382">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-382">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-383">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-383">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="cc3aa-384">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-384">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="cc3aa-385">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="cc3aa-385">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-386">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-386">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-387">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-387">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-389">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-389">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="cc3aa-390">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-390">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cc3aa-391"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-391"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="cc3aa-392"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-392"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cc3aa-393"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-393"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="cc3aa-394"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-394"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-395">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-395">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="cc3aa-396"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-396"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-397">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-397">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="cc3aa-398"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-398"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-399">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="cc3aa-399">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="cc3aa-400">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-400">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="cc3aa-401">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-401">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="cc3aa-402"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-402"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-403">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-403">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="cc3aa-404"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-404"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="cc3aa-405">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-405">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cc3aa-406">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-406">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-407">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-407">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-408">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-409">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-409">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="cc3aa-410">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="cc3aa-410">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="cc3aa-411">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-411">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="cc3aa-412">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="cc3aa-412">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="cc3aa-413">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-414">**Resolución**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-414">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-415">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-415">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-416">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-417">Capacidad del sensor para resolver las diferencias en la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-417">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="cc3aa-418">Este valor puede variar en función de si el dispositivo es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-418">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-419">**Estado**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-420">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-422">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-422">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-423">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-423">Current status of the object.</span></span>

<span data-ttu-id="cc3aa-424">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-424">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cc3aa-425">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="cc3aa-425">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cc3aa-426">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-426">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cc3aa-427">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-427">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cc3aa-428">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-428">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cc3aa-429">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-429">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cc3aa-430">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-430">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cc3aa-431">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-431">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cc3aa-432">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-432">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cc3aa-433">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-433">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cc3aa-434">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-434">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cc3aa-435">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-435">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cc3aa-436">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-436">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cc3aa-437">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-437">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cc3aa-438">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-438">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-439">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-441">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="cc3aa-441">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-442">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-442">State of the logical device.</span></span> <span data-ttu-id="cc3aa-443">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-443">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="cc3aa-444">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-444">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cc3aa-445">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-445">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cc3aa-446">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-446">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="cc3aa-447">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-447">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cc3aa-448">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-448">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="cc3aa-449">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-449">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cc3aa-450">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-450">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-451">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-452">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-453">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-453">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-454">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-454">Scoping system's creation class name.</span></span>

<span data-ttu-id="cc3aa-455">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-455">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-456">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-456">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-457">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-458">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-459">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cc3aa-459">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-460">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-460">Scoping system's name.</span></span>

<span data-ttu-id="cc3aa-461">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-461">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-462">**Tolerancia**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-462">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-463">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-463">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-464">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-465">Tolerancia del sensor para la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-465">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="cc3aa-466">Esta propiedad, y las propiedades de **resolución** y **precisión** , se usan para calcular el valor real de la propiedad física medida.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-466">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="cc3aa-467">La tolerancia puede variar en función de si el dispositivo es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-467">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-468">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-468">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-469">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-469">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-470">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-471">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-471">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="cc3aa-472">Si la propiedad **CurrentReading** está entre **UpperThresholdCritical** y **UpperThresholdFatal**, el estado actual es Critical.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-472">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="cc3aa-473">Esta propiedad se hereda de **CIM \_ NumericSensor**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-473">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-474">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-474">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-475">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-475">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-476">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-477">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-477">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="cc3aa-478">Si la propiedad **CurrentReading** está por encima de **UpperThresholdFatal**, el estado actual es fatal.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-478">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="cc3aa-479">Esta propiedad se hereda de **CIM \_ NumericSensor**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-479">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="cc3aa-480">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-480">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc3aa-481">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-481">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc3aa-482">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc3aa-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cc3aa-483">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-483">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="cc3aa-484">Si la propiedad **CurrentReading** está entre **LowerThresholdNonCritical** y **UpperThresholdNonCritical**, el sensor informa de un valor normal.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-484">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="cc3aa-485">Si la propiedad **CurrentReading** está entre **UpperThresholdNonCritical** y **UpperThresholdCritical**, el estado actual es no crítico.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-485">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="cc3aa-486">Esta propiedad se hereda de **CIM \_ NumericSensor**.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-486">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc3aa-487">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc3aa-487">Remarks</span></span>

<span data-ttu-id="cc3aa-488">La clase **CIM \_ NumericSensor** se deriva del [**\_ sensor CIM**](cim-sensor.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-488">The **CIM\_NumericSensor** class is derived from [**CIM\_Sensor**](cim-sensor.md).</span></span>

<span data-ttu-id="cc3aa-489">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-489">WMI does not implement this class.</span></span> <span data-ttu-id="cc3aa-490">Para las clases derivadas de **CIM \_ NumericSensor**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cc3aa-490">For classes derived from **CIM\_NumericSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="cc3aa-491">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-491">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cc3aa-492">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="cc3aa-492">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc3aa-493">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc3aa-493">Requirements</span></span>



| <span data-ttu-id="cc3aa-494">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc3aa-494">Requirement</span></span> | <span data-ttu-id="cc3aa-495">Value</span><span class="sxs-lookup"><span data-stu-id="cc3aa-495">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc3aa-496">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc3aa-496">Minimum supported client</span></span><br/> | <span data-ttu-id="cc3aa-497">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc3aa-497">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cc3aa-498">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc3aa-498">Minimum supported server</span></span><br/> | <span data-ttu-id="cc3aa-499">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc3aa-499">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cc3aa-500">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cc3aa-500">Namespace</span></span><br/>                | <span data-ttu-id="cc3aa-501">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cc3aa-501">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cc3aa-502">MOF</span><span class="sxs-lookup"><span data-stu-id="cc3aa-502">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc3aa-503"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc3aa-503"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc3aa-504">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cc3aa-504">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc3aa-505"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc3aa-505"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc3aa-506">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc3aa-506">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc3aa-507">**\_Sensor CIM**</span><span class="sxs-lookup"><span data-stu-id="cc3aa-507">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

