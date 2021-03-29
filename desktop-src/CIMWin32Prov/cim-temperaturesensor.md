---
description: La \_ clase TemperatureSensor de CIM existe por compatibilidad con versiones anteriores de definiciones de esquema CIM.
ms.assetid: ddef21db-e33a-4e2b-ac31-df3f0acd6fc2
ms.tgt_platform: multiple
title: CIM_TemperatureSensor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TemperatureSensor
- CIM_TemperatureSensor.Accuracy
- CIM_TemperatureSensor.Availability
- CIM_TemperatureSensor.Caption
- CIM_TemperatureSensor.ConfigManagerErrorCode
- CIM_TemperatureSensor.ConfigManagerUserConfig
- CIM_TemperatureSensor.CreationClassName
- CIM_TemperatureSensor.CurrentReading
- CIM_TemperatureSensor.Description
- CIM_TemperatureSensor.DeviceID
- CIM_TemperatureSensor.ErrorCleared
- CIM_TemperatureSensor.ErrorDescription
- CIM_TemperatureSensor.InstallDate
- CIM_TemperatureSensor.IsLinear
- CIM_TemperatureSensor.LastErrorCode
- CIM_TemperatureSensor.LowerThresholdCritical
- CIM_TemperatureSensor.LowerThresholdFatal
- CIM_TemperatureSensor.LowerThresholdNonCritical
- CIM_TemperatureSensor.MaxReadable
- CIM_TemperatureSensor.MinReadable
- CIM_TemperatureSensor.Name
- CIM_TemperatureSensor.NominalReading
- CIM_TemperatureSensor.NormalMax
- CIM_TemperatureSensor.NormalMin
- CIM_TemperatureSensor.PNPDeviceID
- CIM_TemperatureSensor.PowerManagementCapabilities
- CIM_TemperatureSensor.PowerManagementSupported
- CIM_TemperatureSensor.Resolution
- CIM_TemperatureSensor.Status
- CIM_TemperatureSensor.StatusInfo
- CIM_TemperatureSensor.SystemCreationClassName
- CIM_TemperatureSensor.SystemName
- CIM_TemperatureSensor.Tolerance
- CIM_TemperatureSensor.UpperThresholdCritical
- CIM_TemperatureSensor.UpperThresholdFatal
- CIM_TemperatureSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f48988db3cb213c06013b7ebac61095dbc365daa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360071"
---
# <a name="cim_temperaturesensor-class"></a><span data-ttu-id="95374-103">\_Clase TemperatureSensor de CIM</span><span class="sxs-lookup"><span data-stu-id="95374-103">CIM\_TemperatureSensor class</span></span>

<span data-ttu-id="95374-104">La **clase \_ TemperatureSensor de CIM** existe por compatibilidad con versiones anteriores de definiciones de esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="95374-104">The **CIM\_TemperatureSensor** class exists for backward compatibility with earlier CIM schema definitions.</span></span> <span data-ttu-id="95374-105">Con las adiciones al [**\_ sensor CIM**](cim-sensor.md) y las clases de [**CIM \_ NumericSensor**](cim-numericsensor.md) en la versión 2,2, ya no es necesario.</span><span class="sxs-lookup"><span data-stu-id="95374-105">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span> <span data-ttu-id="95374-106">Un sensor de temperatura se puede definir estableciendo la propiedad **SensorType** , heredada **del \_ sensor CIM**, en 2 ("temperatura").</span><span class="sxs-lookup"><span data-stu-id="95374-106">A temperature sensor can be defined by setting the **SensorType** property, inherited from **CIM\_Sensor**, to 2 ("Temperature").</span></span> <span data-ttu-id="95374-107">Otras propiedades de esta clase están codificadas como valores constantes que se corresponden con las definiciones de la jerarquía del sensor.</span><span class="sxs-lookup"><span data-stu-id="95374-107">Other properties of this class are hardcoded as constant values that correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95374-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="95374-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="95374-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="95374-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="95374-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="95374-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="95374-111">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="95374-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="95374-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95374-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979D-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_TemperatureSensor : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="95374-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="95374-113">Members</span></span>

<span data-ttu-id="95374-114">La clase **CIM \_ TemperatureSensor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="95374-114">The **CIM\_TemperatureSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="95374-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="95374-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="95374-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95374-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="95374-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="95374-117">Methods</span></span>

<span data-ttu-id="95374-118">La clase **CIM \_ TemperatureSensor** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="95374-118">The **CIM\_TemperatureSensor** class has these methods.</span></span>



| <span data-ttu-id="95374-119">Método</span><span class="sxs-lookup"><span data-stu-id="95374-119">Method</span></span>                                                                       | <span data-ttu-id="95374-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="95374-120">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95374-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="95374-121">**Reset**</span></span>](reset-method-in-class-cim-temperaturesensor.md)                 | <span data-ttu-id="95374-122">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="95374-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="95374-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="95374-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="95374-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="95374-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-temperaturesensor.md) | <span data-ttu-id="95374-125">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="95374-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="95374-126">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="95374-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="95374-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95374-127">Properties</span></span>

<span data-ttu-id="95374-128">La clase **CIM \_ TemperatureSensor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="95374-128">The **CIM\_TemperatureSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95374-129">**Precisión**</span><span class="sxs-lookup"><span data-stu-id="95374-129">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-130">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="95374-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-132">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de temperatura DMTF \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="95374-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="95374-133">Precisión del sensor para la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="95374-133">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="95374-134">Su valor se registra como más o menos centésimas de un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="95374-134">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="95374-135">Esta propiedad, y las propiedades de **resolución** y **tolerancia** , se usan para calcular el valor real de la propiedad física medida.</span><span class="sxs-lookup"><span data-stu-id="95374-135">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="95374-136">La precisión puede variar en función de si el dispositivo es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="95374-136">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="95374-137">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-137">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-138">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="95374-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-139">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95374-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95374-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-141">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="95374-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="95374-142">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95374-142">Availability and status of the device.</span></span>

<span data-ttu-id="95374-143">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="95374-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="95374-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="95374-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95374-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="95374-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="95374-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="95374-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="95374-147">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="95374-147">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="95374-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="95374-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="95374-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="95374-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="95374-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="95374-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="95374-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="95374-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="95374-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="95374-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="95374-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="95374-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="95374-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="95374-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="95374-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="95374-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="95374-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="95374-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="95374-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="95374-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="95374-158">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="95374-158">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="95374-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="95374-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="95374-160">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="95374-160">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="95374-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="95374-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="95374-162">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="95374-162">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="95374-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="95374-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="95374-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="95374-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="95374-165">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="95374-165">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="95374-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="95374-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="95374-167">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="95374-167">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="95374-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="95374-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="95374-169">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="95374-169">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="95374-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="95374-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="95374-171">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="95374-171">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="95374-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="95374-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="95374-173">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="95374-173">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="95374-174">**Caption**</span><span class="sxs-lookup"><span data-stu-id="95374-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95374-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95374-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-177">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="95374-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="95374-178">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="95374-178">Short textual description of the object.</span></span>

<span data-ttu-id="95374-179">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95374-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-180">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="95374-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-181">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95374-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-183">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="95374-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="95374-184">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="95374-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="95374-185">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="95374-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="95374-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="95374-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="95374-187"> (0)</span><span class="sxs-lookup"><span data-stu-id="95374-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="95374-188">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="95374-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="95374-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="95374-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="95374-190">(1)</span><span class="sxs-lookup"><span data-stu-id="95374-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="95374-191">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="95374-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="95374-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="95374-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="95374-193">(2)</span><span class="sxs-lookup"><span data-stu-id="95374-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="95374-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="95374-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="95374-195">(3)</span><span class="sxs-lookup"><span data-stu-id="95374-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="95374-196">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="95374-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="95374-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="95374-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="95374-198">(4)</span><span class="sxs-lookup"><span data-stu-id="95374-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="95374-199">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="95374-199">Device is not working properly.</span></span> <span data-ttu-id="95374-200">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="95374-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="95374-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="95374-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="95374-202">(5)</span><span class="sxs-lookup"><span data-stu-id="95374-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="95374-203">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="95374-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="95374-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="95374-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="95374-205"> (6)</span><span class="sxs-lookup"><span data-stu-id="95374-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="95374-206">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="95374-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="95374-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="95374-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="95374-208">(7)</span><span class="sxs-lookup"><span data-stu-id="95374-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="95374-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="95374-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="95374-210">(8)</span><span class="sxs-lookup"><span data-stu-id="95374-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="95374-211">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95374-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="95374-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="95374-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="95374-213">(9)</span><span class="sxs-lookup"><span data-stu-id="95374-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="95374-214">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="95374-214">Device is not working properly.</span></span> <span data-ttu-id="95374-215">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95374-215">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="95374-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="95374-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="95374-217">(10)</span><span class="sxs-lookup"><span data-stu-id="95374-217">(10)</span></span>


</dt> <dd>

<span data-ttu-id="95374-218">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="95374-218">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="95374-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="95374-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="95374-220">(11)</span><span class="sxs-lookup"><span data-stu-id="95374-220">(11)</span></span>


</dt> <dd>

<span data-ttu-id="95374-221">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95374-221">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="95374-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="95374-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="95374-223">(12)</span><span class="sxs-lookup"><span data-stu-id="95374-223">(12)</span></span>


</dt> <dd>

<span data-ttu-id="95374-224">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="95374-224">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="95374-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="95374-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="95374-226">(13)</span><span class="sxs-lookup"><span data-stu-id="95374-226">(13)</span></span>


</dt> <dd>

<span data-ttu-id="95374-227">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95374-227">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="95374-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="95374-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="95374-229">(14)</span><span class="sxs-lookup"><span data-stu-id="95374-229">(14)</span></span>


</dt> <dd>

<span data-ttu-id="95374-230">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="95374-230">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="95374-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="95374-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="95374-232">(15)</span><span class="sxs-lookup"><span data-stu-id="95374-232">(15)</span></span>


</dt> <dd>

<span data-ttu-id="95374-233">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="95374-233">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="95374-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="95374-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="95374-235">(16)</span><span class="sxs-lookup"><span data-stu-id="95374-235">(16)</span></span>


</dt> <dd>

<span data-ttu-id="95374-236">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95374-236">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="95374-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="95374-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="95374-238">(17)</span><span class="sxs-lookup"><span data-stu-id="95374-238">(17)</span></span>


</dt> <dd>

<span data-ttu-id="95374-239">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="95374-239">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="95374-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="95374-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="95374-241">(18)</span><span class="sxs-lookup"><span data-stu-id="95374-241">(18)</span></span>


</dt> <dd>

<span data-ttu-id="95374-242">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="95374-242">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="95374-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="95374-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="95374-244">(19)</span><span class="sxs-lookup"><span data-stu-id="95374-244">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="95374-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="95374-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="95374-246">(20)</span><span class="sxs-lookup"><span data-stu-id="95374-246">(20)</span></span>


</dt> <dd>

<span data-ttu-id="95374-247">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="95374-247">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="95374-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="95374-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="95374-249">(21)</span><span class="sxs-lookup"><span data-stu-id="95374-249">(21)</span></span>


</dt> <dd>

<span data-ttu-id="95374-250">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="95374-250">System failure.</span></span> <span data-ttu-id="95374-251">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="95374-251">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="95374-252">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95374-252">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="95374-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="95374-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="95374-254">(22)</span><span class="sxs-lookup"><span data-stu-id="95374-254">(22)</span></span>


</dt> <dd>

<span data-ttu-id="95374-255">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="95374-255">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="95374-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="95374-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="95374-257">(23)</span><span class="sxs-lookup"><span data-stu-id="95374-257">(23)</span></span>


</dt> <dd>

<span data-ttu-id="95374-258">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="95374-258">System failure.</span></span> <span data-ttu-id="95374-259">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="95374-259">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="95374-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="95374-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="95374-261">(24)</span><span class="sxs-lookup"><span data-stu-id="95374-261">(24)</span></span>


</dt> <dd>

<span data-ttu-id="95374-262">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="95374-262">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="95374-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="95374-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="95374-264">(25)</span><span class="sxs-lookup"><span data-stu-id="95374-264">(25)</span></span>


</dt> <dd>

<span data-ttu-id="95374-265">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95374-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="95374-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="95374-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="95374-267">(26)</span><span class="sxs-lookup"><span data-stu-id="95374-267">(26)</span></span>


</dt> <dd>

<span data-ttu-id="95374-268">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95374-268">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="95374-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="95374-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="95374-270">(27)</span><span class="sxs-lookup"><span data-stu-id="95374-270">(27)</span></span>


</dt> <dd>

<span data-ttu-id="95374-271">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="95374-271">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="95374-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="95374-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="95374-273">(28)</span><span class="sxs-lookup"><span data-stu-id="95374-273">(28)</span></span>


</dt> <dd>

<span data-ttu-id="95374-274">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="95374-274">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="95374-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="95374-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="95374-276">(29)</span><span class="sxs-lookup"><span data-stu-id="95374-276">(29)</span></span>


</dt> <dd>

<span data-ttu-id="95374-277">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="95374-277">Device is disabled.</span></span> <span data-ttu-id="95374-278">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="95374-278">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="95374-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="95374-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="95374-280">(30)</span><span class="sxs-lookup"><span data-stu-id="95374-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="95374-281">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="95374-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="95374-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="95374-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="95374-283">31</span><span class="sxs-lookup"><span data-stu-id="95374-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="95374-284">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="95374-284">Device is not working properly.</span></span> <span data-ttu-id="95374-285">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="95374-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="95374-286">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="95374-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-287">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="95374-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95374-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-289">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="95374-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="95374-290">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="95374-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="95374-291">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="95374-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="95374-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-293">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95374-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95374-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-295">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="95374-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="95374-296">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="95374-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="95374-297">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="95374-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="95374-298">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="95374-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-299">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="95374-299">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-300">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="95374-300">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-302">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de temperatura DMTF \| 001,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="95374-302">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="95374-303">Valor actual indicado por el sensor.</span><span class="sxs-lookup"><span data-stu-id="95374-303">Current value indicated by the sensor.</span></span>

<span data-ttu-id="95374-304">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-304">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-305">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95374-305">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-306">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95374-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95374-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-308">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="95374-308">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="95374-309">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="95374-309">Textual description of the object.</span></span>

<span data-ttu-id="95374-310">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95374-310">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-311">**ID**</span><span class="sxs-lookup"><span data-stu-id="95374-311">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-312">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95374-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95374-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-314">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="95374-314">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="95374-315">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="95374-315">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="95374-316">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="95374-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-317">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="95374-317">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-318">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="95374-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95374-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95374-320">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="95374-320">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="95374-321">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="95374-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-322">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="95374-322">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-323">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95374-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95374-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95374-325">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="95374-325">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="95374-326">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="95374-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-327">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="95374-327">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-328">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="95374-328">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="95374-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-330">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="95374-330">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="95374-331">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="95374-331">Date and time the object was installed.</span></span> <span data-ttu-id="95374-332">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="95374-332">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="95374-333">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95374-333">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-334">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="95374-334">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-335">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="95374-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95374-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95374-337">Si es **true**, el sensor es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="95374-337">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="95374-338">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-338">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-339">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="95374-339">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-340">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95374-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95374-342">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="95374-342">Last error code reported by the logical device.</span></span>

<span data-ttu-id="95374-343">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="95374-343">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-344">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="95374-344">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-345">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="95374-345">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-347">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de temperatura DMTF \| 001,13 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="95374-347">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="95374-348">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="95374-348">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="95374-349">Si la propiedad **CurrentReading** está entre **LowerThresholdCritical** y **LowerThresholdFatal**, el estado actual es Critical.</span><span class="sxs-lookup"><span data-stu-id="95374-349">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="95374-350">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-350">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-351">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="95374-351">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-352">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="95374-352">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-354">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de temperatura DMTF \| 001,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="95374-354">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="95374-355">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="95374-355">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="95374-356">Si la propiedad **CurrentReading** está por debajo de **LowerThresholdFatal**, el estado actual es fatal.</span><span class="sxs-lookup"><span data-stu-id="95374-356">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="95374-357">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-357">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-358">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="95374-358">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-359">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="95374-359">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-360">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-361">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de temperatura DMTF \| 001,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="95374-361">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="95374-362">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="95374-362">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="95374-363">Si la propiedad **CurrentReading** está entre **LowerThresholdNonCritical** y **UpperThresholdNonCritical**, el sensor informa de un valor normal.</span><span class="sxs-lookup"><span data-stu-id="95374-363">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="95374-364">Si la propiedad **CurrentReading** está entre **LowerThresholdNonCritical** y **LowerThresholdCritical**, el estado actual es no crítico.</span><span class="sxs-lookup"><span data-stu-id="95374-364">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="95374-365">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-365">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-366">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="95374-366">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-367">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="95374-367">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-369">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de temperatura DMTF \| 001,9 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="95374-369">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="95374-370">Valor mayor de la propiedad medida que puede ser leída por el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="95374-370">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="95374-371">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-371">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-372">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="95374-372">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-373">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="95374-373">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-374">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-375">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de temperatura DMTF \| 001,10 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="95374-375">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="95374-376">Valor menor de la propiedad medida que puede ser leída por el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="95374-376">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="95374-377">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-377">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-378">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="95374-378">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-379">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95374-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95374-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-381">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="95374-381">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="95374-382">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="95374-382">Label by which the object is known.</span></span> <span data-ttu-id="95374-383">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="95374-383">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="95374-384">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95374-384">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-385">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="95374-385">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-386">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="95374-386">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-388">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de temperatura DMTF \| 001,6 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="95374-388">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="95374-389">Valor esperado o normal para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="95374-389">Expected or normal value for the numeric sensor.</span></span>

<span data-ttu-id="95374-390">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-390">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-391">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="95374-391">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-392">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="95374-392">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-394">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de temperatura DMTF \| 001,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="95374-394">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="95374-395">Intervalo máximo normal para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="95374-395">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="95374-396">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-396">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-397">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="95374-397">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-398">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="95374-398">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-400">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de temperatura DMTF \| 001,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="95374-400">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="95374-401">Intervalo mínimo normal para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="95374-401">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="95374-402">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-402">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-403">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="95374-403">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-404">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95374-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95374-405">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-406">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="95374-406">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="95374-407">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="95374-407">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="95374-408">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="95374-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="95374-409">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="95374-409">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="95374-410">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="95374-410">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-411">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95374-411">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="95374-412">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95374-413">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="95374-413">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="95374-414">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="95374-414">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95374-415"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="95374-415"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="95374-416"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="95374-416"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="95374-417"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="95374-417"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="95374-418"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="95374-418"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="95374-419">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="95374-419">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="95374-420"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="95374-420"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="95374-421">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="95374-421">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="95374-422"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="95374-422"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="95374-423">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="95374-423">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="95374-424">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="95374-424">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="95374-425">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="95374-425">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="95374-426"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="95374-426"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="95374-427">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="95374-427">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="95374-428"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="95374-428"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="95374-429">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="95374-429">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="95374-430">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="95374-430">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-431">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="95374-431">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95374-432">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95374-433">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="95374-433">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="95374-434">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="95374-434">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="95374-435">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="95374-435">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="95374-436">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="95374-436">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="95374-437">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="95374-437">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-438">**Resolución**</span><span class="sxs-lookup"><span data-stu-id="95374-438">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-439">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95374-439">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-441">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de temperatura DMTF \| 001,17 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" centésimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="95374-441">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hundredths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="95374-442">Capacidad del sensor para resolver las diferencias en la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="95374-442">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="95374-443">Este valor puede variar en función de si el dispositivo es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="95374-443">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="95374-444">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-444">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-445">**Estado**</span><span class="sxs-lookup"><span data-stu-id="95374-445">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-446">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95374-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95374-447">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-448">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="95374-448">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="95374-449">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="95374-449">Current status of the object.</span></span> <span data-ttu-id="95374-450">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95374-450">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="95374-451">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="95374-451">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="95374-452">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="95374-452">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="95374-453">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="95374-453">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="95374-454">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="95374-454">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95374-455">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="95374-455">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="95374-456">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="95374-456">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="95374-457">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="95374-457">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="95374-458">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="95374-458">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="95374-459">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="95374-459">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="95374-460">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="95374-460">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="95374-461">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="95374-461">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="95374-462">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="95374-462">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="95374-463">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="95374-463">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="95374-464">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="95374-464">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-465">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95374-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95374-466">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-467">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="95374-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="95374-468">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="95374-468">State of the logical device.</span></span> <span data-ttu-id="95374-469">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="95374-469">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="95374-470">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="95374-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="95374-471">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="95374-471">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95374-472">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="95374-472">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="95374-473">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="95374-473">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="95374-474">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="95374-474">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="95374-475">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="95374-475">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="95374-476">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="95374-476">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-477">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95374-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95374-478">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-479">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="95374-479">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="95374-480">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="95374-480">Scoping system's creation class name.</span></span>

<span data-ttu-id="95374-481">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="95374-481">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-482">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="95374-482">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-483">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95374-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95374-484">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-485">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="95374-485">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="95374-486">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="95374-486">Scoping system's name.</span></span>

<span data-ttu-id="95374-487">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="95374-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-488">**Tolerancia**</span><span class="sxs-lookup"><span data-stu-id="95374-488">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-489">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="95374-489">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-490">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-490">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-491">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de temperatura DMTF \| 001,18 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="95374-491">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="95374-492">Tolerancia del sensor para la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="95374-492">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="95374-493">Esta propiedad, y las propiedades de **resolución** y **precisión** , se usan para calcular el valor real de la propiedad física medida.</span><span class="sxs-lookup"><span data-stu-id="95374-493">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="95374-494">La tolerancia puede variar en función de si el dispositivo es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="95374-494">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="95374-495">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-495">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-496">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="95374-496">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-497">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="95374-497">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-498">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-498">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-499">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de temperatura DMTF \| 001,14 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="95374-499">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="95374-500">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="95374-500">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="95374-501">Si la propiedad **CurrentReading** está entre **UpperThresholdCritical** y **UpperThresholdFatal**, el estado actual es Critical.</span><span class="sxs-lookup"><span data-stu-id="95374-501">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="95374-502">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-502">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-503">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="95374-503">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-504">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="95374-504">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-505">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-506">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de temperatura DMTF \| 001,16 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="95374-506">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="95374-507">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="95374-507">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="95374-508">Si la propiedad **CurrentReading** está por encima de **UpperThresholdFatal**, el estado actual es fatal.</span><span class="sxs-lookup"><span data-stu-id="95374-508">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="95374-509">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-509">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="95374-510">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="95374-510">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95374-511">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="95374-511">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="95374-512">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95374-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95374-513">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de temperatura DMTF \| 001,12 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="95374-513">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="95374-514">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="95374-514">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="95374-515">Si la propiedad **CurrentReading** está entre **LowerThresholdNonCritical** y **UpperThresholdNonCritical**, el sensor informa de un valor normal.</span><span class="sxs-lookup"><span data-stu-id="95374-515">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="95374-516">Si la propiedad **CurrentReading** está entre **UpperThresholdNonCritical** y **UpperThresholdCritical**, el estado actual es no crítico.</span><span class="sxs-lookup"><span data-stu-id="95374-516">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="95374-517">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-517">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95374-518">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95374-518">Remarks</span></span>

<span data-ttu-id="95374-519">La clase **CIM \_ TemperatureSensor** se deriva de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="95374-519">The **CIM\_TemperatureSensor** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="95374-520">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="95374-520">WMI does not implement this class.</span></span> <span data-ttu-id="95374-521">Para las clases WMI derivadas de **CIM \_ TemperatureSensor**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="95374-521">For WMI classes derived from **CIM\_TemperatureSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="95374-522">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="95374-522">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="95374-523">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="95374-523">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="95374-524">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95374-524">Requirements</span></span>



| <span data-ttu-id="95374-525">Requisito</span><span class="sxs-lookup"><span data-stu-id="95374-525">Requirement</span></span> | <span data-ttu-id="95374-526">Value</span><span class="sxs-lookup"><span data-stu-id="95374-526">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95374-527">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95374-527">Minimum supported client</span></span><br/> | <span data-ttu-id="95374-528">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95374-528">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95374-529">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95374-529">Minimum supported server</span></span><br/> | <span data-ttu-id="95374-530">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95374-530">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95374-531">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="95374-531">Namespace</span></span><br/>                | <span data-ttu-id="95374-532">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="95374-532">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="95374-533">MOF</span><span class="sxs-lookup"><span data-stu-id="95374-533">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95374-534"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95374-534"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="95374-535">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95374-535">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95374-536"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95374-536"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95374-537">Vea también</span><span class="sxs-lookup"><span data-stu-id="95374-537">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95374-538">**NumericSensor de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="95374-538">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

