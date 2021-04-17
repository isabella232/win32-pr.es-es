---
description: La \_ clase CIM BinarySensor proporciona una salida booleana.
ms.assetid: 51396a51-78ea-4c49-8dcc-7fb815f334ae
ms.tgt_platform: multiple
title: CIM_BinarySensor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BinarySensor
- CIM_BinarySensor.Caption
- CIM_BinarySensor.Description
- CIM_BinarySensor.InstallDate
- CIM_BinarySensor.Name
- CIM_BinarySensor.Status
- CIM_BinarySensor.Availability
- CIM_BinarySensor.ConfigManagerErrorCode
- CIM_BinarySensor.ConfigManagerUserConfig
- CIM_BinarySensor.CreationClassName
- CIM_BinarySensor.DeviceID
- CIM_BinarySensor.PowerManagementCapabilities
- CIM_BinarySensor.ErrorCleared
- CIM_BinarySensor.ErrorDescription
- CIM_BinarySensor.LastErrorCode
- CIM_BinarySensor.PNPDeviceID
- CIM_BinarySensor.PowerManagementSupported
- CIM_BinarySensor.StatusInfo
- CIM_BinarySensor.SystemCreationClassName
- CIM_BinarySensor.SystemName
- CIM_BinarySensor.CurrentReading
- CIM_BinarySensor.ExpectedReading
- CIM_BinarySensor.InterpretationOfFalse
- CIM_BinarySensor.InterpretationOfTrue
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f0d795f98473c09937571d415e34cf6fcb7f3486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659653"
---
# <a name="cim_binarysensor-class"></a><span data-ttu-id="d1855-103">\_Clase BinarySensor de CIM</span><span class="sxs-lookup"><span data-stu-id="d1855-103">CIM\_BinarySensor class</span></span>

<span data-ttu-id="d1855-104">La clase **CIM \_ BinarySensor** proporciona una salida booleana.</span><span class="sxs-lookup"><span data-stu-id="d1855-104">The **CIM\_BinarySensor** class provides a Boolean output.</span></span> <span data-ttu-id="d1855-105">Las propiedades **CurrentState** y **PossibleStates** se agregaron para el sensor, por lo que la subclase **CIM \_ BinarySensor** ya no es necesaria, aunque se conserva por compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="d1855-105">The **CurrentState** and **PossibleStates** properties were added for sensoring, thus making the **CIM\_BinarySensor** subclass no longer necessary, although, it is retained for backward compatibility.</span></span> <span data-ttu-id="d1855-106">Se puede crear un sensor binario creando una instancia de un sensor con dos Estados posibles.</span><span class="sxs-lookup"><span data-stu-id="d1855-106">A binary sensor can be created by instantiating a sensor with two possible states.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1855-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="d1855-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d1855-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d1855-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d1855-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d1855-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d1855-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d1855-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1855-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1855-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{11140D44-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_BinarySensor : CIM_Sensor
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
  boolean  CurrentReading;
  boolean  ExpectedReading;
  string   InterpretationOfFalse;
  string   InterpretationOfTrue;
};
```

## <a name="members"></a><span data-ttu-id="d1855-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1855-112">Members</span></span>

<span data-ttu-id="d1855-113">La clase **CIM \_ BinarySensor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d1855-113">The **CIM\_BinarySensor** class has these types of members:</span></span>

-   [<span data-ttu-id="d1855-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="d1855-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="d1855-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1855-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d1855-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="d1855-116">Methods</span></span>

<span data-ttu-id="d1855-117">La clase **CIM \_ BinarySensor** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d1855-117">The **CIM\_BinarySensor** class has these methods.</span></span>



| <span data-ttu-id="d1855-118">Método</span><span class="sxs-lookup"><span data-stu-id="d1855-118">Method</span></span>                                                                  | <span data-ttu-id="d1855-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1855-119">Description</span></span>                                                                                                                                |
|:------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1855-120">**Reset**</span><span class="sxs-lookup"><span data-stu-id="d1855-120">**Reset**</span></span>](reset-method-in-class-cim-binarysensor.md)                 | <span data-ttu-id="d1855-121">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d1855-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="d1855-122">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="d1855-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="d1855-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d1855-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-binarysensor.md) | <span data-ttu-id="d1855-124">Define el estado de energía deseado para un dispositivo lógico y el momento en que el dispositivo debe ponerse en ese estado.</span><span class="sxs-lookup"><span data-stu-id="d1855-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="d1855-125">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="d1855-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d1855-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1855-126">Properties</span></span>

<span data-ttu-id="d1855-127">La clase **CIM \_ BinarySensor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d1855-127">The **CIM\_BinarySensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1855-128">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="d1855-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1855-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1855-131">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="d1855-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d1855-132">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1855-132">Availability and status of the device.</span></span>

<span data-ttu-id="d1855-133">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d1855-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d1855-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1855-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="d1855-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d1855-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="d1855-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d1855-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="d1855-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d1855-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="d1855-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d1855-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="d1855-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d1855-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="d1855-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d1855-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="d1855-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d1855-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="d1855-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d1855-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="d1855-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d1855-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="d1855-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d1855-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="d1855-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d1855-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="d1855-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d1855-147">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="d1855-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d1855-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="d1855-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d1855-149">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="d1855-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d1855-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="d1855-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d1855-151">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="d1855-151">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d1855-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="d1855-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d1855-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="d1855-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d1855-154">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="d1855-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d1855-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="d1855-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d1855-156">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="d1855-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d1855-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="d1855-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d1855-158">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="d1855-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d1855-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="d1855-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d1855-160">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="d1855-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d1855-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="d1855-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d1855-162">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="d1855-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1855-163">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d1855-163">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1855-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1855-166">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d1855-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d1855-167">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="d1855-167">A short textual description of the object.</span></span>

<span data-ttu-id="d1855-168">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1855-169">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d1855-169">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-170">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1855-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1855-172">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d1855-172">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d1855-173">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="d1855-173">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="d1855-174">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-174">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d1855-175">**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="d1855-175">**This device is working properly.**</span></span> <span data-ttu-id="d1855-176"> (0)</span><span class="sxs-lookup"><span data-stu-id="d1855-176">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d1855-177">**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="d1855-177">**This device is not configured correctly.**</span></span> <span data-ttu-id="d1855-178">(1)</span><span class="sxs-lookup"><span data-stu-id="d1855-178">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d1855-179">**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1855-179">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d1855-180">(2)</span><span class="sxs-lookup"><span data-stu-id="d1855-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d1855-181">**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="d1855-181">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d1855-182">(3)</span><span class="sxs-lookup"><span data-stu-id="d1855-182">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d1855-183">**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="d1855-183">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d1855-184">(4)</span><span class="sxs-lookup"><span data-stu-id="d1855-184">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d1855-185">**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="d1855-185">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d1855-186">(5)</span><span class="sxs-lookup"><span data-stu-id="d1855-186">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d1855-187">**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="d1855-187">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d1855-188"> (6)</span><span class="sxs-lookup"><span data-stu-id="d1855-188">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d1855-189">**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="d1855-189">**Cannot filter.**</span></span> <span data-ttu-id="d1855-190">(7)</span><span class="sxs-lookup"><span data-stu-id="d1855-190">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d1855-191">**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1855-191">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d1855-192">(8)</span><span class="sxs-lookup"><span data-stu-id="d1855-192">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d1855-193">**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="d1855-193">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d1855-194">(9)</span><span class="sxs-lookup"><span data-stu-id="d1855-194">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d1855-195">**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="d1855-195">**This device cannot start.**</span></span> <span data-ttu-id="d1855-196">(10)</span><span class="sxs-lookup"><span data-stu-id="d1855-196">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d1855-197">**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1855-197">**This device failed.**</span></span> <span data-ttu-id="d1855-198">(11)</span><span class="sxs-lookup"><span data-stu-id="d1855-198">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d1855-199">**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="d1855-199">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d1855-200">(12)</span><span class="sxs-lookup"><span data-stu-id="d1855-200">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d1855-201">**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1855-201">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d1855-202">(13)</span><span class="sxs-lookup"><span data-stu-id="d1855-202">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d1855-203">**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="d1855-203">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d1855-204">(14)</span><span class="sxs-lookup"><span data-stu-id="d1855-204">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d1855-205">**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="d1855-205">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d1855-206">(15)</span><span class="sxs-lookup"><span data-stu-id="d1855-206">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d1855-207">**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1855-207">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d1855-208">(16)</span><span class="sxs-lookup"><span data-stu-id="d1855-208">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d1855-209">**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="d1855-209">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d1855-210">(17)</span><span class="sxs-lookup"><span data-stu-id="d1855-210">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d1855-211">**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1855-211">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d1855-212">(18)</span><span class="sxs-lookup"><span data-stu-id="d1855-212">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d1855-213">**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="d1855-213">**Failure using the VxD loader.**</span></span> <span data-ttu-id="d1855-214">(19)</span><span class="sxs-lookup"><span data-stu-id="d1855-214">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d1855-215">**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="d1855-215">**Your registry might be corrupted.**</span></span> <span data-ttu-id="d1855-216">(20)</span><span class="sxs-lookup"><span data-stu-id="d1855-216">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d1855-217">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1855-217">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d1855-218">(21)</span><span class="sxs-lookup"><span data-stu-id="d1855-218">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d1855-219">**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="d1855-219">**This device is disabled.**</span></span> <span data-ttu-id="d1855-220">(22)</span><span class="sxs-lookup"><span data-stu-id="d1855-220">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d1855-221">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="d1855-221">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d1855-222">(23)</span><span class="sxs-lookup"><span data-stu-id="d1855-222">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d1855-223">**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="d1855-223">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d1855-224">(24)</span><span class="sxs-lookup"><span data-stu-id="d1855-224">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d1855-225">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1855-225">**Windows is still setting up this device.**</span></span> <span data-ttu-id="d1855-226">(25)</span><span class="sxs-lookup"><span data-stu-id="d1855-226">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d1855-227">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1855-227">**Windows is still setting up this device.**</span></span> <span data-ttu-id="d1855-228">(26)</span><span class="sxs-lookup"><span data-stu-id="d1855-228">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d1855-229">**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="d1855-229">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d1855-230">(27)</span><span class="sxs-lookup"><span data-stu-id="d1855-230">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d1855-231">**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="d1855-231">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d1855-232">(28)</span><span class="sxs-lookup"><span data-stu-id="d1855-232">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d1855-233">**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="d1855-233">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d1855-234">(29)</span><span class="sxs-lookup"><span data-stu-id="d1855-234">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d1855-235">**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="d1855-235">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d1855-236">(30)</span><span class="sxs-lookup"><span data-stu-id="d1855-236">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d1855-237">**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d1855-237">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d1855-238">31</span><span class="sxs-lookup"><span data-stu-id="d1855-238">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1855-239">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="d1855-239">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-240">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d1855-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1855-242">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d1855-242">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d1855-243">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d1855-243">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d1855-244">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-244">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1855-245">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d1855-245">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-246">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1855-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1855-248">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d1855-248">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d1855-249">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="d1855-249">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d1855-250">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="d1855-250">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d1855-251">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-251">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1855-252">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="d1855-252">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-253">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d1855-253">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1855-255">Valor actual indicado por el sensor.</span><span class="sxs-lookup"><span data-stu-id="d1855-255">Current value indicated by the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="d1855-256">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d1855-256">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1855-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1855-259">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="d1855-259">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d1855-260">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="d1855-260">A textual description of the object.</span></span>

<span data-ttu-id="d1855-261">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-261">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1855-262">**ID**</span><span class="sxs-lookup"><span data-stu-id="d1855-262">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-263">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1855-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1855-265">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d1855-265">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d1855-266">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d1855-266">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="d1855-267">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-267">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1855-268">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d1855-268">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-269">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d1855-269">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1855-271">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="d1855-271">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="d1855-272">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-272">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1855-273">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d1855-273">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-274">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1855-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1855-276">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="d1855-276">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="d1855-277">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1855-278">**ExpectedReading**</span><span class="sxs-lookup"><span data-stu-id="d1855-278">**ExpectedReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-279">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d1855-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1855-281">Valor ' normal ' del sensor.</span><span class="sxs-lookup"><span data-stu-id="d1855-281">'Normal' value for the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="d1855-282">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d1855-282">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-283">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1855-283">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1855-285">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="d1855-285">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d1855-286">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="d1855-286">Indicates when the object was installed.</span></span> <span data-ttu-id="d1855-287">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="d1855-287">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d1855-288">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1855-289">**InterpretationOfFalse**</span><span class="sxs-lookup"><span data-stu-id="d1855-289">**InterpretationOfFalse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-290">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1855-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1855-292">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d1855-292">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d1855-293">Descripción de un valor "false" del sensor binario.</span><span class="sxs-lookup"><span data-stu-id="d1855-293">Description of a 'False' value from the binary sensor.</span></span> <span data-ttu-id="d1855-294">Esta información puede mostrarse a un usuario.</span><span class="sxs-lookup"><span data-stu-id="d1855-294">This information can be displayed to a user.</span></span>

</dd> <dt>

<span data-ttu-id="d1855-295">**InterpretationOfTrue**</span><span class="sxs-lookup"><span data-stu-id="d1855-295">**InterpretationOfTrue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-296">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1855-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1855-298">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d1855-298">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d1855-299">Descripción de un valor "true" del sensor binario.</span><span class="sxs-lookup"><span data-stu-id="d1855-299">Description of a 'True' value from the binary sensor.</span></span> <span data-ttu-id="d1855-300">Esta información puede mostrarse a un usuario.</span><span class="sxs-lookup"><span data-stu-id="d1855-300">This information can be displayed to a user.</span></span>

</dd> <dt>

<span data-ttu-id="d1855-301">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d1855-301">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-302">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1855-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1855-304">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d1855-304">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d1855-305">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1855-306">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d1855-306">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1855-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1855-309">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d1855-309">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d1855-310">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="d1855-310">Label by which the object is known.</span></span> <span data-ttu-id="d1855-311">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="d1855-311">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d1855-312">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1855-313">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d1855-313">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-314">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1855-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1855-316">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d1855-316">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d1855-317">Indica el identificador de dispositivo Plug and Play Win32 del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d1855-317">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="d1855-318">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="d1855-318">Example: "\*PNP030b"</span></span>

<span data-ttu-id="d1855-319">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1855-320">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d1855-320">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-321">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1855-321">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d1855-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1855-323">Indica las capacidades de energía específicas relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d1855-323">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="d1855-324">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1855-325"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="d1855-325"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d1855-326">Las capacidades relacionadas con la energía son desconocidas.</span><span class="sxs-lookup"><span data-stu-id="d1855-326">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d1855-327"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="d1855-327"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d1855-328">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1855-328">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d1855-329"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="d1855-329"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d1855-330">Se han deshabilitado las capacidades relacionadas con la energía.</span><span class="sxs-lookup"><span data-stu-id="d1855-330">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d1855-331"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d1855-331"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d1855-332">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="d1855-332">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d1855-333"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="d1855-333"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d1855-334">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="d1855-334">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d1855-335"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="d1855-335"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d1855-336">Se admite el método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="d1855-336">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="d1855-337">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="d1855-337">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="d1855-338">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="d1855-338">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d1855-339"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="d1855-339"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d1855-340">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="d1855-340">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d1855-341"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="d1855-341"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d1855-342">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o Interval, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="d1855-342">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1855-343">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d1855-343">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-344">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d1855-344">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1855-346">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="d1855-346">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="d1855-347">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="d1855-347">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="d1855-348">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="d1855-348">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="d1855-349">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="d1855-349">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="d1855-350">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1855-351">**Estado**</span><span class="sxs-lookup"><span data-stu-id="d1855-351">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1855-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1855-354">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="d1855-354">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d1855-355">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="d1855-355">String that indicates the current status of the object.</span></span> <span data-ttu-id="d1855-356">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="d1855-356">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d1855-357">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="d1855-357">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d1855-358">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="d1855-358">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d1855-359">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="d1855-359">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d1855-360">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="d1855-360">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d1855-361">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="d1855-361">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d1855-362">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-362">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d1855-363">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d1855-363">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d1855-364">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="d1855-364">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d1855-365">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="d1855-365">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d1855-366">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="d1855-366">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1855-367">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="d1855-367">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d1855-368">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="d1855-368">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d1855-369">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="d1855-369">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d1855-370">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="d1855-370">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d1855-371">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="d1855-371">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d1855-372">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="d1855-372">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d1855-373">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="d1855-373">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d1855-374">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="d1855-374">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d1855-375">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="d1855-375">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1855-376">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d1855-376">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-377">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1855-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-378">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1855-379">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d1855-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d1855-380">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d1855-380">State of the logical device.</span></span> <span data-ttu-id="d1855-381">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="d1855-381">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="d1855-382">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-382">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d1855-383">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d1855-383">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1855-384">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="d1855-384">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d1855-385">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d1855-385">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d1855-386">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="d1855-386">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d1855-387">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="d1855-387">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1855-388">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d1855-388">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-389">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1855-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1855-391">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d1855-391">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d1855-392">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d1855-392">The scoping system's creation class name.</span></span>

<span data-ttu-id="d1855-393">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-393">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1855-394">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d1855-394">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1855-395">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d1855-395">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1855-396">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1855-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1855-397">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d1855-397">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d1855-398">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d1855-398">The scoping system's name.</span></span>

<span data-ttu-id="d1855-399">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1855-400">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1855-400">Remarks</span></span>

<span data-ttu-id="d1855-401">La clase **CIM \_ BinarySensor** se deriva del [**\_ sensor CIM**](cim-sensor.md).</span><span class="sxs-lookup"><span data-stu-id="d1855-401">The **CIM\_BinarySensor** class is derived from [**CIM\_Sensor**](cim-sensor.md).</span></span>

<span data-ttu-id="d1855-402">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="d1855-402">WMI does not implement this class.</span></span>

<span data-ttu-id="d1855-403">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="d1855-403">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d1855-404">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="d1855-404">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1855-405">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1855-405">Requirements</span></span>



| <span data-ttu-id="d1855-406">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1855-406">Requirement</span></span> | <span data-ttu-id="d1855-407">Value</span><span class="sxs-lookup"><span data-stu-id="d1855-407">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1855-408">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1855-408">Minimum supported client</span></span><br/> | <span data-ttu-id="d1855-409">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1855-409">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1855-410">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1855-410">Minimum supported server</span></span><br/> | <span data-ttu-id="d1855-411">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1855-411">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1855-412">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d1855-412">Namespace</span></span><br/>                | <span data-ttu-id="d1855-413">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d1855-413">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1855-414">MOF</span><span class="sxs-lookup"><span data-stu-id="d1855-414">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1855-415"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1855-415"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1855-416">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d1855-416">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1855-417"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1855-417"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1855-418">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1855-418">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1855-419">**\_Sensor CIM**</span><span class="sxs-lookup"><span data-stu-id="d1855-419">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

