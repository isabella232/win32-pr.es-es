---
description: La \_ clase de controlador CIM es una clase primaria para agrupar dispositivos varios relacionados con el control. Algunos ejemplos de controladores son controladores SCSI, controladores USB y controladores serie.
ms.assetid: 526d58bb-cdf4-42c2-ae89-7b86d99e2017
ms.tgt_platform: multiple
title: CIM_Controller (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Controller
- CIM_Controller.Caption
- CIM_Controller.Description
- CIM_Controller.InstallDate
- CIM_Controller.Name
- CIM_Controller.Status
- CIM_Controller.Availability
- CIM_Controller.ConfigManagerErrorCode
- CIM_Controller.ConfigManagerUserConfig
- CIM_Controller.CreationClassName
- CIM_Controller.DeviceID
- CIM_Controller.PowerManagementCapabilities
- CIM_Controller.ErrorCleared
- CIM_Controller.ErrorDescription
- CIM_Controller.LastErrorCode
- CIM_Controller.PNPDeviceID
- CIM_Controller.PowerManagementSupported
- CIM_Controller.StatusInfo
- CIM_Controller.SystemCreationClassName
- CIM_Controller.SystemName
- CIM_Controller.MaxNumberControlled
- CIM_Controller.ProtocolSupported
- CIM_Controller.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b23ef846c118c8d0698660175e4be700ea892055
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274932"
---
# <a name="cim_controller-class-cimwin32-wmi-providers"></a><span data-ttu-id="14d1a-104">CIM_Controller (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="14d1a-104">CIM_Controller class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="14d1a-105">La clase de **\_ controlador CIM** es una clase primaria para agrupar dispositivos varios relacionados con el control.</span><span class="sxs-lookup"><span data-stu-id="14d1a-105">The **CIM\_Controller** class is a parent class for grouping miscellaneous control-related devices.</span></span> <span data-ttu-id="14d1a-106">Algunos ejemplos de controladores son controladores SCSI, controladores USB y controladores serie.</span><span class="sxs-lookup"><span data-stu-id="14d1a-106">Examples of controllers are SCSI controllers, USB controllers, and serial controllers.</span></span>

<span data-ttu-id="14d1a-107">La clase de **\_ controlador CIM** es una abstracción para dispositivos con una sola pila de protocolos, que existen principalmente para la comunicación y el control o restablecimiento de dispositivos de nivel inferior ([**CIM \_ ControlledBy**](cim-controlledby.md)).</span><span class="sxs-lookup"><span data-stu-id="14d1a-107">The **CIM\_Controller** class is an abstraction for devices with a single protocol stack, which exist primarily for communication to, and control or reset of, downstream ([**CIM\_ControlledBy**](cim-controlledby.md)) devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="14d1a-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="14d1a-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="14d1a-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="14d1a-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="14d1a-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="14d1a-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="14d1a-111">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="14d1a-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="14d1a-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14d1a-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C531-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Controller : CIM_LogicalDevice
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
  uint32   MaxNumberControlled;
  uint16   ProtocolSupported;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="14d1a-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="14d1a-113">Members</span></span>

<span data-ttu-id="14d1a-114">La clase del **\_ controlador CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="14d1a-114">The **CIM\_Controller** class has these types of members:</span></span>

-   [<span data-ttu-id="14d1a-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="14d1a-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="14d1a-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="14d1a-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="14d1a-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="14d1a-117">Methods</span></span>

<span data-ttu-id="14d1a-118">La clase del **\_ controlador CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="14d1a-118">The **CIM\_Controller** class has these methods.</span></span>



| <span data-ttu-id="14d1a-119">Método</span><span class="sxs-lookup"><span data-stu-id="14d1a-119">Method</span></span>                                                                | <span data-ttu-id="14d1a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="14d1a-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14d1a-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="14d1a-121">**Reset**</span></span>](reset-method-in-class-cim-controller.md)                 | <span data-ttu-id="14d1a-122">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="14d1a-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="14d1a-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="14d1a-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="14d1a-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="14d1a-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-controller.md) | <span data-ttu-id="14d1a-125">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="14d1a-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="14d1a-126">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="14d1a-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="14d1a-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="14d1a-127">Properties</span></span>

<span data-ttu-id="14d1a-128">La clase del **\_ controlador CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="14d1a-128">The **CIM\_Controller** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14d1a-129">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="14d1a-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-130">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14d1a-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-132">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="14d1a-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-133">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14d1a-133">Availability and status of the device.</span></span>

<span data-ttu-id="14d1a-134">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="14d1a-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="14d1a-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="14d1a-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="14d1a-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="14d1a-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="14d1a-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="14d1a-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="14d1a-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="14d1a-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="14d1a-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="14d1a-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="14d1a-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="14d1a-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="14d1a-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="14d1a-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="14d1a-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="14d1a-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="14d1a-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="14d1a-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="14d1a-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="14d1a-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="14d1a-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="14d1a-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="14d1a-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="14d1a-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="14d1a-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="14d1a-148">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="14d1a-148">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="14d1a-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="14d1a-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="14d1a-150">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="14d1a-150">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="14d1a-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="14d1a-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="14d1a-152">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="14d1a-152">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="14d1a-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="14d1a-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="14d1a-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="14d1a-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="14d1a-155">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="14d1a-155">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="14d1a-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="14d1a-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="14d1a-157">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="14d1a-157">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="14d1a-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="14d1a-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="14d1a-159">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="14d1a-159">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="14d1a-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="14d1a-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="14d1a-161">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="14d1a-161">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="14d1a-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="14d1a-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="14d1a-163">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="14d1a-163">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="14d1a-164">**Caption**</span><span class="sxs-lookup"><span data-stu-id="14d1a-164">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14d1a-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-167">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="14d1a-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-168">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="14d1a-168">A short textual description of the object.</span></span>

<span data-ttu-id="14d1a-169">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="14d1a-170">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="14d1a-170">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-171">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14d1a-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-173">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="14d1a-173">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-174">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="14d1a-174">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="14d1a-175">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-175">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="14d1a-176">**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-176">**This device is working properly.**</span></span> <span data-ttu-id="14d1a-177"> (0)</span><span class="sxs-lookup"><span data-stu-id="14d1a-177">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="14d1a-178">**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-178">**This device is not configured correctly.**</span></span> <span data-ttu-id="14d1a-179">(1)</span><span class="sxs-lookup"><span data-stu-id="14d1a-179">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="14d1a-180">**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-180">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="14d1a-181">(2)</span><span class="sxs-lookup"><span data-stu-id="14d1a-181">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="14d1a-182">**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-182">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="14d1a-183">(3)</span><span class="sxs-lookup"><span data-stu-id="14d1a-183">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="14d1a-184">**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-184">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="14d1a-185">(4)</span><span class="sxs-lookup"><span data-stu-id="14d1a-185">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="14d1a-186">**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-186">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="14d1a-187">(5)</span><span class="sxs-lookup"><span data-stu-id="14d1a-187">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="14d1a-188">**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-188">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="14d1a-189"> (6)</span><span class="sxs-lookup"><span data-stu-id="14d1a-189">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="14d1a-190">**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-190">**Cannot filter.**</span></span> <span data-ttu-id="14d1a-191">(7)</span><span class="sxs-lookup"><span data-stu-id="14d1a-191">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="14d1a-192">**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-192">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="14d1a-193">(8)</span><span class="sxs-lookup"><span data-stu-id="14d1a-193">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="14d1a-194">**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-194">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="14d1a-195">(9)</span><span class="sxs-lookup"><span data-stu-id="14d1a-195">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="14d1a-196">**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-196">**This device cannot start.**</span></span> <span data-ttu-id="14d1a-197">(10)</span><span class="sxs-lookup"><span data-stu-id="14d1a-197">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="14d1a-198">**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-198">**This device failed.**</span></span> <span data-ttu-id="14d1a-199">(11)</span><span class="sxs-lookup"><span data-stu-id="14d1a-199">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="14d1a-200">**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-200">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="14d1a-201">(12)</span><span class="sxs-lookup"><span data-stu-id="14d1a-201">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="14d1a-202">**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-202">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="14d1a-203">(13)</span><span class="sxs-lookup"><span data-stu-id="14d1a-203">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="14d1a-204">**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-204">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="14d1a-205">(14)</span><span class="sxs-lookup"><span data-stu-id="14d1a-205">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="14d1a-206">**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-206">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="14d1a-207">(15)</span><span class="sxs-lookup"><span data-stu-id="14d1a-207">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="14d1a-208">**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-208">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="14d1a-209">(16)</span><span class="sxs-lookup"><span data-stu-id="14d1a-209">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="14d1a-210">**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-210">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="14d1a-211">(17)</span><span class="sxs-lookup"><span data-stu-id="14d1a-211">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="14d1a-212">**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-212">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="14d1a-213">(18)</span><span class="sxs-lookup"><span data-stu-id="14d1a-213">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="14d1a-214">**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-214">**Failure using the VxD loader.**</span></span> <span data-ttu-id="14d1a-215">(19)</span><span class="sxs-lookup"><span data-stu-id="14d1a-215">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="14d1a-216">**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-216">**Your registry might be corrupted.**</span></span> <span data-ttu-id="14d1a-217">(20)</span><span class="sxs-lookup"><span data-stu-id="14d1a-217">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="14d1a-218">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-218">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="14d1a-219">(21)</span><span class="sxs-lookup"><span data-stu-id="14d1a-219">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="14d1a-220">**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-220">**This device is disabled.**</span></span> <span data-ttu-id="14d1a-221">(22)</span><span class="sxs-lookup"><span data-stu-id="14d1a-221">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="14d1a-222">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-222">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="14d1a-223">(23)</span><span class="sxs-lookup"><span data-stu-id="14d1a-223">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="14d1a-224">**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-224">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="14d1a-225">(24)</span><span class="sxs-lookup"><span data-stu-id="14d1a-225">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="14d1a-226">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-226">**Windows is still setting up this device.**</span></span> <span data-ttu-id="14d1a-227">(25)</span><span class="sxs-lookup"><span data-stu-id="14d1a-227">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="14d1a-228">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-228">**Windows is still setting up this device.**</span></span> <span data-ttu-id="14d1a-229">(26)</span><span class="sxs-lookup"><span data-stu-id="14d1a-229">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="14d1a-230">**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-230">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="14d1a-231">(27)</span><span class="sxs-lookup"><span data-stu-id="14d1a-231">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="14d1a-232">**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-232">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="14d1a-233">(28)</span><span class="sxs-lookup"><span data-stu-id="14d1a-233">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="14d1a-234">**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-234">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="14d1a-235">(29)</span><span class="sxs-lookup"><span data-stu-id="14d1a-235">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="14d1a-236">**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-236">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="14d1a-237">(30)</span><span class="sxs-lookup"><span data-stu-id="14d1a-237">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="14d1a-238">**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="14d1a-238">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="14d1a-239">31</span><span class="sxs-lookup"><span data-stu-id="14d1a-239">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="14d1a-240">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="14d1a-240">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-241">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="14d1a-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-243">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="14d1a-243">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-244">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="14d1a-244">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="14d1a-245">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-245">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="14d1a-246">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="14d1a-246">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-247">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14d1a-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-249">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="14d1a-249">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-250">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="14d1a-250">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="14d1a-251">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="14d1a-251">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="14d1a-252">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-252">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="14d1a-253">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="14d1a-253">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-254">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14d1a-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-255">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-256">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="14d1a-256">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-257">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="14d1a-257">A textual description of the object.</span></span>

<span data-ttu-id="14d1a-258">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-258">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="14d1a-259">**ID**</span><span class="sxs-lookup"><span data-stu-id="14d1a-259">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-260">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14d1a-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-261">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-262">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="14d1a-262">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-263">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="14d1a-263">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="14d1a-264">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-264">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="14d1a-265">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="14d1a-265">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-266">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="14d1a-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-267">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-268">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="14d1a-268">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="14d1a-269">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-269">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="14d1a-270">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="14d1a-270">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-271">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14d1a-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-273">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="14d1a-273">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="14d1a-274">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-274">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="14d1a-275">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="14d1a-275">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-276">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="14d1a-276">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-277">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-278">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="14d1a-278">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-279">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="14d1a-279">Indicates when the object was installed.</span></span> <span data-ttu-id="14d1a-280">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="14d1a-280">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="14d1a-281">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-281">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="14d1a-282">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="14d1a-282">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-283">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14d1a-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-285">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="14d1a-285">Last error code reported by the logical device.</span></span>

<span data-ttu-id="14d1a-286">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="14d1a-287">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="14d1a-287">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-288">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14d1a-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-290">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puerto de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="14d1a-290">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-291">Número máximo de entidades directamente direccionables admitidas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="14d1a-291">Maximum number of directly addressable entities supported by this controller.</span></span> <span data-ttu-id="14d1a-292">Se debe utilizar un valor de 0 si el número es desconocido o ilimitado.</span><span class="sxs-lookup"><span data-stu-id="14d1a-292">A value of 0 should be used if the number is unknown or unlimited.</span></span>

</dd> <dt>

<span data-ttu-id="14d1a-293">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="14d1a-293">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-294">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14d1a-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-296">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="14d1a-296">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-297">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="14d1a-297">Label by which the object is known.</span></span> <span data-ttu-id="14d1a-298">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="14d1a-298">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="14d1a-299">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="14d1a-300">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="14d1a-300">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-301">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14d1a-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-303">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="14d1a-303">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-304">Indica el identificador de dispositivo Plug and Play Win32 del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="14d1a-304">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="14d1a-305">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="14d1a-305">Example: "\*PNP030b"</span></span>

<span data-ttu-id="14d1a-306">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="14d1a-307">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="14d1a-307">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-308">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14d1a-308">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-310">Indica las capacidades de energía específicas relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="14d1a-310">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="14d1a-311">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="14d1a-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="14d1a-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="14d1a-313">Las capacidades relacionadas con la energía son desconocidas.</span><span class="sxs-lookup"><span data-stu-id="14d1a-313">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="14d1a-314"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="14d1a-314"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="14d1a-315">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14d1a-315">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="14d1a-316"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="14d1a-316"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="14d1a-317">Se han deshabilitado las capacidades relacionadas con la energía.</span><span class="sxs-lookup"><span data-stu-id="14d1a-317">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="14d1a-318"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="14d1a-318"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="14d1a-319">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="14d1a-319">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="14d1a-320"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="14d1a-320"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="14d1a-321">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="14d1a-321">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="14d1a-322"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="14d1a-322"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="14d1a-323">Se admite el método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="14d1a-323">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="14d1a-324">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="14d1a-324">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="14d1a-325">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="14d1a-325">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="14d1a-326"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="14d1a-326"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="14d1a-327">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="14d1a-327">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="14d1a-328"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="14d1a-328"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="14d1a-329">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o Interval, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="14d1a-329">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="14d1a-330">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="14d1a-330">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-331">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="14d1a-331">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-333">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="14d1a-333">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="14d1a-334">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="14d1a-334">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="14d1a-335">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="14d1a-335">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="14d1a-336">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="14d1a-336">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="14d1a-337">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="14d1a-338">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="14d1a-338">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-339">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14d1a-339">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-341">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puerto de bus DMTF \| 001,2 "," MIF. \|Discos DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="14d1a-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-342">Protocolo usado por el controlador para tener acceso a los dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="14d1a-342">The protocol used by the controller to access 'controlled' devices.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="14d1a-343">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="14d1a-343">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="14d1a-344">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="14d1a-344">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="14d1a-345">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="14d1a-345">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="14d1a-346">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="14d1a-346">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="14d1a-347">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="14d1a-347">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="14d1a-348">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="14d1a-348">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="14d1a-349">**Disco flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="14d1a-349">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="14d1a-350">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="14d1a-350">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="14d1a-351">**Interfaz paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="14d1a-351">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="14d1a-352">**Protocolo SCSI canal de fibra** (10)</span><span class="sxs-lookup"><span data-stu-id="14d1a-352">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="14d1a-353">**Protocolo de bus serie SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="14d1a-353">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="14d1a-354">**Protocolo de bus serie SCSI: 2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="14d1a-354">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="14d1a-355">**Arquitectura de almacenamiento en serie SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="14d1a-355">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="14d1a-356">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="14d1a-356">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="14d1a-357">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="14d1a-357">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="14d1a-358">**Bus serie universal** (16)</span><span class="sxs-lookup"><span data-stu-id="14d1a-358">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="14d1a-359">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="14d1a-359">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="14d1a-360">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="14d1a-360">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="14d1a-361">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="14d1a-361">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="14d1a-362">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="14d1a-362">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="14d1a-363">**Potencia** (21)</span><span class="sxs-lookup"><span data-stu-id="14d1a-363">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="14d1a-364">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="14d1a-364">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="14d1a-365">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="14d1a-365">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="14d1a-366">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="14d1a-366">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="14d1a-367">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="14d1a-367">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="14d1a-368">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="14d1a-368">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="14d1a-369">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="14d1a-369">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="14d1a-370">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="14d1a-370">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="14d1a-371">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="14d1a-371">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="14d1a-372">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="14d1a-372">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="14d1a-373">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="14d1a-373">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="14d1a-374">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="14d1a-374">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="14d1a-375">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="14d1a-375">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="14d1a-376">**FDDI ANSI x3t 9.5** (34)</span><span class="sxs-lookup"><span data-stu-id="14d1a-376">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="14d1a-377">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="14d1a-377">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="14d1a-378">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="14d1a-378">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="14d1a-379">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="14d1a-379">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="14d1a-380">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="14d1a-380">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="14d1a-381">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="14d1a-381">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="14d1a-382">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="14d1a-382">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="14d1a-383">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="14d1a-383">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="14d1a-384">**ATA/IDE mejorado** (42)</span><span class="sxs-lookup"><span data-stu-id="14d1a-384">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="14d1a-385">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="14d1a-385">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="14d1a-386">**TWIRP (infrarrojo bidireccional)** (44)</span><span class="sxs-lookup"><span data-stu-id="14d1a-386">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="14d1a-387">**FIR (infrarrojo rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="14d1a-387">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="14d1a-388">**Sir (infrarrojos serie)** (46)</span><span class="sxs-lookup"><span data-stu-id="14d1a-388">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="14d1a-389">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="14d1a-389">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="14d1a-390">**Estado**</span><span class="sxs-lookup"><span data-stu-id="14d1a-390">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-391">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14d1a-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-392">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-393">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="14d1a-393">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-394">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="14d1a-394">String that indicates the current status of the object.</span></span> <span data-ttu-id="14d1a-395">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="14d1a-395">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="14d1a-396">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="14d1a-396">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="14d1a-397">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="14d1a-397">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="14d1a-398">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="14d1a-398">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="14d1a-399">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="14d1a-399">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="14d1a-400">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="14d1a-400">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="14d1a-401">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="14d1a-402">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="14d1a-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="14d1a-403">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="14d1a-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="14d1a-404">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="14d1a-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="14d1a-405">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="14d1a-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="14d1a-406">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="14d1a-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="14d1a-407">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="14d1a-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="14d1a-408">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="14d1a-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="14d1a-409">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="14d1a-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="14d1a-410">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="14d1a-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="14d1a-411">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="14d1a-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="14d1a-412">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="14d1a-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="14d1a-413">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="14d1a-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="14d1a-414">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="14d1a-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="14d1a-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="14d1a-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-416">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="14d1a-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-417">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-418">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="14d1a-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-419">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="14d1a-419">State of the logical device.</span></span> <span data-ttu-id="14d1a-420">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="14d1a-420">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="14d1a-421">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="14d1a-422">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="14d1a-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="14d1a-423">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="14d1a-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="14d1a-424">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="14d1a-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="14d1a-425">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="14d1a-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="14d1a-426">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="14d1a-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="14d1a-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="14d1a-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-428">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14d1a-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-429">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-430">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="14d1a-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-431">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="14d1a-431">The scoping system's creation class name.</span></span>

<span data-ttu-id="14d1a-432">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="14d1a-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="14d1a-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-434">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="14d1a-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-436">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="14d1a-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-437">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="14d1a-437">The scoping system's name.</span></span>

<span data-ttu-id="14d1a-438">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="14d1a-439">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="14d1a-439">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14d1a-440">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="14d1a-440">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="14d1a-441">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="14d1a-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="14d1a-442">Fecha y hora de la última vez que se restableció el controlador (apagado o reinicializado).</span><span class="sxs-lookup"><span data-stu-id="14d1a-442">Date and time the controller was last reset (powered down or reinitialized).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14d1a-443">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14d1a-443">Remarks</span></span>

<span data-ttu-id="14d1a-444">La clase del **\_ controlador CIM** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-444">The **CIM\_Controller** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="14d1a-445">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="14d1a-445">WMI does not implement this class.</span></span> <span data-ttu-id="14d1a-446">Para las clases derivadas del **\_ controlador CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="14d1a-446">For classes derived from **CIM\_Controller**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="14d1a-447">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="14d1a-447">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="14d1a-448">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="14d1a-448">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="14d1a-449">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14d1a-449">Requirements</span></span>



| <span data-ttu-id="14d1a-450">Requisito</span><span class="sxs-lookup"><span data-stu-id="14d1a-450">Requirement</span></span> | <span data-ttu-id="14d1a-451">Value</span><span class="sxs-lookup"><span data-stu-id="14d1a-451">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14d1a-452">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14d1a-452">Minimum supported client</span></span><br/> | <span data-ttu-id="14d1a-453">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14d1a-453">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="14d1a-454">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14d1a-454">Minimum supported server</span></span><br/> | <span data-ttu-id="14d1a-455">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14d1a-455">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="14d1a-456">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="14d1a-456">Namespace</span></span><br/>                | <span data-ttu-id="14d1a-457">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="14d1a-457">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="14d1a-458">MOF</span><span class="sxs-lookup"><span data-stu-id="14d1a-458">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14d1a-459"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14d1a-459"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="14d1a-460">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="14d1a-460">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14d1a-461"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14d1a-461"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14d1a-462">Vea también</span><span class="sxs-lookup"><span data-stu-id="14d1a-462">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14d1a-463">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="14d1a-463">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

