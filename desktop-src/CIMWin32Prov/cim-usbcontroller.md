---
description: La \_ clase CIM USBController representa las capacidades y la administración de una controladora USB.
ms.assetid: fa891db5-9995-4532-895f-bded8dd0bdac
ms.tgt_platform: multiple
title: CIM_USBController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBController
- CIM_USBController.Availability
- CIM_USBController.Caption
- CIM_USBController.ConfigManagerErrorCode
- CIM_USBController.ConfigManagerUserConfig
- CIM_USBController.CreationClassName
- CIM_USBController.Description
- CIM_USBController.DeviceID
- CIM_USBController.ErrorCleared
- CIM_USBController.ErrorDescription
- CIM_USBController.InstallDate
- CIM_USBController.LastErrorCode
- CIM_USBController.Manufacturer
- CIM_USBController.MaxNumberControlled
- CIM_USBController.Name
- CIM_USBController.PNPDeviceID
- CIM_USBController.PowerManagementCapabilities
- CIM_USBController.PowerManagementSupported
- CIM_USBController.ProtocolSupported
- CIM_USBController.Status
- CIM_USBController.StatusInfo
- CIM_USBController.SystemCreationClassName
- CIM_USBController.SystemName
- CIM_USBController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4c636ae977dc0145b9e4b243c6903a687a525d15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274833"
---
# <a name="cim_usbcontroller-class"></a><span data-ttu-id="c56db-103">\_Clase USBController de CIM</span><span class="sxs-lookup"><span data-stu-id="c56db-103">CIM\_USBController class</span></span>

<span data-ttu-id="c56db-104">La clase **CIM \_ USBController** representa las capacidades y la administración de una controladora USB.</span><span class="sxs-lookup"><span data-stu-id="c56db-104">The **CIM\_USBController** class represents the capabilities and management of a USB controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c56db-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="c56db-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c56db-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c56db-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c56db-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c56db-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c56db-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c56db-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c56db-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c56db-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B5B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_USBController : CIM_Controller
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
  string   Manufacturer;
  uint32   MaxNumberControlled;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="c56db-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="c56db-110">Members</span></span>

<span data-ttu-id="c56db-111">La clase **CIM \_ USBController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c56db-111">The **CIM\_USBController** class has these types of members:</span></span>

-   [<span data-ttu-id="c56db-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c56db-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c56db-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c56db-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c56db-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="c56db-114">Methods</span></span>

<span data-ttu-id="c56db-115">La clase **CIM \_ USBController** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c56db-115">The **CIM\_USBController** class has these methods.</span></span>



| <span data-ttu-id="c56db-116">Método</span><span class="sxs-lookup"><span data-stu-id="c56db-116">Method</span></span>                                                                   | <span data-ttu-id="c56db-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c56db-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c56db-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="c56db-118">**Reset**</span></span>](reset-method-in-class-cim-usbcontroller.md)                 | <span data-ttu-id="c56db-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c56db-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="c56db-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c56db-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="c56db-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c56db-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-usbcontroller.md) | <span data-ttu-id="c56db-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="c56db-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="c56db-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c56db-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c56db-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c56db-124">Properties</span></span>

<span data-ttu-id="c56db-125">La clase **CIM \_ USBController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c56db-125">The **CIM\_USBController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c56db-126">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="c56db-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c56db-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-129">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="c56db-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c56db-130">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c56db-130">Availability and status of the device.</span></span>

<span data-ttu-id="c56db-131">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c56db-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="c56db-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c56db-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="c56db-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c56db-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="c56db-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-135">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="c56db-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c56db-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="c56db-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c56db-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="c56db-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c56db-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="c56db-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c56db-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="c56db-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c56db-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="c56db-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c56db-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="c56db-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c56db-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="c56db-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c56db-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="c56db-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c56db-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="c56db-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c56db-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="c56db-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-146">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="c56db-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c56db-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="c56db-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-148">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="c56db-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c56db-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="c56db-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-150">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="c56db-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c56db-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="c56db-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c56db-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="c56db-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-153">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="c56db-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c56db-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="c56db-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-155">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="c56db-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c56db-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="c56db-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-157">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="c56db-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c56db-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="c56db-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-159">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="c56db-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c56db-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="c56db-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-161">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="c56db-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c56db-162">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c56db-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c56db-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-165">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c56db-165">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c56db-166">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c56db-166">Short textual description of the object.</span></span>

<span data-ttu-id="c56db-167">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c56db-168">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c56db-168">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-169">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c56db-169">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-171">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c56db-171">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c56db-172">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="c56db-172">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c56db-173">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-173">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c56db-174"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="c56db-174"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c56db-175"> (0)</span><span class="sxs-lookup"><span data-stu-id="c56db-175">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-176">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="c56db-176">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c56db-177"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="c56db-177"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c56db-178">(1)</span><span class="sxs-lookup"><span data-stu-id="c56db-178">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-179">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c56db-179">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c56db-180"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c56db-180"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c56db-181">(2)</span><span class="sxs-lookup"><span data-stu-id="c56db-181">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c56db-182"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="c56db-182"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c56db-183">(3)</span><span class="sxs-lookup"><span data-stu-id="c56db-183">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-184">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="c56db-184">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c56db-185"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="c56db-185"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c56db-186">(4)</span><span class="sxs-lookup"><span data-stu-id="c56db-186">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-187">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="c56db-187">Device is not working properly.</span></span> <span data-ttu-id="c56db-188">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="c56db-188">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c56db-189"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="c56db-189"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c56db-190">(5)</span><span class="sxs-lookup"><span data-stu-id="c56db-190">(5)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-191">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="c56db-191">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c56db-192"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="c56db-192"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c56db-193"> (6)</span><span class="sxs-lookup"><span data-stu-id="c56db-193">(6)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-194">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c56db-194">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c56db-195"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="c56db-195"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c56db-196">(7)</span><span class="sxs-lookup"><span data-stu-id="c56db-196">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c56db-197"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c56db-197"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c56db-198">(8)</span><span class="sxs-lookup"><span data-stu-id="c56db-198">(8)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-199">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c56db-199">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c56db-200"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="c56db-200"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c56db-201">(9)</span><span class="sxs-lookup"><span data-stu-id="c56db-201">(9)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-202">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="c56db-202">Device is not working properly.</span></span> <span data-ttu-id="c56db-203">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c56db-203">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c56db-204"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="c56db-204"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c56db-205">(10)</span><span class="sxs-lookup"><span data-stu-id="c56db-205">(10)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-206">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="c56db-206">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c56db-207"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c56db-207"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c56db-208">(11)</span><span class="sxs-lookup"><span data-stu-id="c56db-208">(11)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-209">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c56db-209">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c56db-210"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="c56db-210"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c56db-211">(12)</span><span class="sxs-lookup"><span data-stu-id="c56db-211">(12)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-212">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="c56db-212">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c56db-213"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c56db-213"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c56db-214">(13)</span><span class="sxs-lookup"><span data-stu-id="c56db-214">(13)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-215">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c56db-215">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c56db-216"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="c56db-216"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c56db-217">(14)</span><span class="sxs-lookup"><span data-stu-id="c56db-217">(14)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-218">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="c56db-218">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c56db-219"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="c56db-219"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c56db-220">(15)</span><span class="sxs-lookup"><span data-stu-id="c56db-220">(15)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-221">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="c56db-221">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c56db-222"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c56db-222"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c56db-223">(16)</span><span class="sxs-lookup"><span data-stu-id="c56db-223">(16)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-224">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c56db-224">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c56db-225"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="c56db-225"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c56db-226">(17)</span><span class="sxs-lookup"><span data-stu-id="c56db-226">(17)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-227">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="c56db-227">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c56db-228"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c56db-228"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c56db-229">(18)</span><span class="sxs-lookup"><span data-stu-id="c56db-229">(18)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-230">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c56db-230">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c56db-231"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="c56db-231"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c56db-232">(19)</span><span class="sxs-lookup"><span data-stu-id="c56db-232">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c56db-233"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="c56db-233"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c56db-234">(20)</span><span class="sxs-lookup"><span data-stu-id="c56db-234">(20)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-235">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="c56db-235">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c56db-236"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c56db-236"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c56db-237">(21)</span><span class="sxs-lookup"><span data-stu-id="c56db-237">(21)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-238">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="c56db-238">System failure.</span></span> <span data-ttu-id="c56db-239">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="c56db-239">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="c56db-240">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c56db-240">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c56db-241"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="c56db-241"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c56db-242">(22)</span><span class="sxs-lookup"><span data-stu-id="c56db-242">(22)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-243">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="c56db-243">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c56db-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="c56db-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c56db-245">(23)</span><span class="sxs-lookup"><span data-stu-id="c56db-245">(23)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-246">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="c56db-246">System failure.</span></span> <span data-ttu-id="c56db-247">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="c56db-247">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c56db-248"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="c56db-248"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c56db-249">(24)</span><span class="sxs-lookup"><span data-stu-id="c56db-249">(24)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-250">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="c56db-250">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c56db-251"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c56db-251"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c56db-252">(25)</span><span class="sxs-lookup"><span data-stu-id="c56db-252">(25)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-253">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c56db-253">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c56db-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c56db-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c56db-255">(26)</span><span class="sxs-lookup"><span data-stu-id="c56db-255">(26)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-256">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c56db-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c56db-257"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="c56db-257"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c56db-258">(27)</span><span class="sxs-lookup"><span data-stu-id="c56db-258">(27)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-259">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="c56db-259">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c56db-260"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="c56db-260"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c56db-261">(28)</span><span class="sxs-lookup"><span data-stu-id="c56db-261">(28)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-262">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="c56db-262">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c56db-263"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="c56db-263"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c56db-264">(29)</span><span class="sxs-lookup"><span data-stu-id="c56db-264">(29)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-265">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="c56db-265">Device is disabled.</span></span> <span data-ttu-id="c56db-266">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="c56db-266">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c56db-267"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="c56db-267"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c56db-268">(30)</span><span class="sxs-lookup"><span data-stu-id="c56db-268">(30)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-269">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="c56db-269">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c56db-270"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c56db-270"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c56db-271">31</span><span class="sxs-lookup"><span data-stu-id="c56db-271">(31)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-272">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="c56db-272">Device is not working properly.</span></span> <span data-ttu-id="c56db-273">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="c56db-273">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c56db-274">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="c56db-274">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-275">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c56db-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-277">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c56db-277">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c56db-278">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="c56db-278">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c56db-279">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-279">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c56db-280">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c56db-280">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-281">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c56db-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-283">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c56db-283">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c56db-284">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="c56db-284">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c56db-285">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="c56db-285">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c56db-286">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c56db-287">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c56db-287">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-288">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c56db-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-290">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="c56db-290">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c56db-291">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c56db-291">Textual description of the object.</span></span>

<span data-ttu-id="c56db-292">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-292">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c56db-293">**ID**</span><span class="sxs-lookup"><span data-stu-id="c56db-293">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-294">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c56db-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-296">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c56db-296">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c56db-297">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c56db-297">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="c56db-298">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c56db-299">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c56db-299">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-300">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c56db-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c56db-302">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="c56db-302">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="c56db-303">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c56db-304">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c56db-304">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-305">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c56db-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c56db-307">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="c56db-307">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="c56db-308">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c56db-309">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c56db-309">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-310">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c56db-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-312">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="c56db-312">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c56db-313">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="c56db-313">Date and time the object was installed.</span></span> <span data-ttu-id="c56db-314">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="c56db-314">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c56db-315">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-315">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c56db-316">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c56db-316">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-317">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c56db-317">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c56db-319">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c56db-319">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c56db-320">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c56db-321">**Le**</span><span class="sxs-lookup"><span data-stu-id="c56db-321">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-322">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c56db-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-324">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c56db-324">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c56db-325">Nombre del fabricante del controlador USB.</span><span class="sxs-lookup"><span data-stu-id="c56db-325">Name of the USB controller manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="c56db-326">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="c56db-326">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-327">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c56db-327">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-329">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puerto de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="c56db-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="c56db-330">Número máximo de entidades directamente direccionables admitidas por el controlador.</span><span class="sxs-lookup"><span data-stu-id="c56db-330">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="c56db-331">Se debe utilizar un valor de 0 si el número es desconocido o ilimitado.</span><span class="sxs-lookup"><span data-stu-id="c56db-331">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="c56db-332">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-332">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="c56db-333">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c56db-333">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-334">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c56db-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-336">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c56db-336">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c56db-337">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="c56db-337">Label by which the object is known.</span></span> <span data-ttu-id="c56db-338">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="c56db-338">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c56db-339">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c56db-340">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c56db-340">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-341">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c56db-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-343">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c56db-343">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c56db-344">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c56db-344">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="c56db-345">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c56db-346">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c56db-346">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="c56db-347">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c56db-347">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-348">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c56db-348">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c56db-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c56db-350">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c56db-350">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="c56db-351">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="c56db-351">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c56db-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="c56db-352"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c56db-353"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="c56db-353"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c56db-354"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="c56db-354"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c56db-355"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c56db-355"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-356">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="c56db-356">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c56db-357"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="c56db-357"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-358">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="c56db-358">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c56db-359"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="c56db-359"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-360">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="c56db-360">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="c56db-361">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="c56db-361">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="c56db-362">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="c56db-362">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c56db-363"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="c56db-363"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-364">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="c56db-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c56db-365"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="c56db-365"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c56db-366">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="c56db-366">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c56db-367">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c56db-367">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-368">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c56db-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c56db-370">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="c56db-370">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="c56db-371">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="c56db-371">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c56db-372">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="c56db-372">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="c56db-373">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="c56db-373">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="c56db-374">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c56db-375">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="c56db-375">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-376">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c56db-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-378">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puerto de bus DMTF \| 001,2 "," MIF. \|Discos DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="c56db-378">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c56db-379">Protocolo usado por el controlador para tener acceso a dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="c56db-379">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="c56db-380">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-380">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="c56db-381">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="c56db-381">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c56db-382">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="c56db-382">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c56db-383">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="c56db-383">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="c56db-384">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="c56db-384">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="c56db-385">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="c56db-385">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="c56db-386">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="c56db-386">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="c56db-387">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="c56db-387">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="c56db-388">**Disco flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="c56db-388">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="c56db-389">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="c56db-389">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="c56db-390">**Interfaz paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="c56db-390">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="c56db-391">**Protocolo SCSI canal de fibra** (10)</span><span class="sxs-lookup"><span data-stu-id="c56db-391">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="c56db-392">**Protocolo de bus serie SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="c56db-392">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="c56db-393">**Protocolo de bus serie SCSI: 2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="c56db-393">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="c56db-394">**Arquitectura de almacenamiento en serie SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="c56db-394">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="c56db-395">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="c56db-395">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="c56db-396">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="c56db-396">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="c56db-397">**Bus serie universal** (16)</span><span class="sxs-lookup"><span data-stu-id="c56db-397">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="c56db-398">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="c56db-398">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="c56db-399">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="c56db-399">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="c56db-400">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="c56db-400">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="c56db-401">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="c56db-401">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="c56db-402">**Potencia** (21)</span><span class="sxs-lookup"><span data-stu-id="c56db-402">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="c56db-403">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="c56db-403">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="c56db-404">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="c56db-404">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="c56db-405">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="c56db-405">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="c56db-406">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="c56db-406">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="c56db-407">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="c56db-407">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="c56db-408">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="c56db-408">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="c56db-409">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="c56db-409">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="c56db-410">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="c56db-410">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="c56db-411">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="c56db-411">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="c56db-412">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="c56db-412">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="c56db-413">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="c56db-413">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="c56db-414">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="c56db-414">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="c56db-415">**FDDI ANSI x3t 9.5** (34)</span><span class="sxs-lookup"><span data-stu-id="c56db-415">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="c56db-416">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="c56db-416">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="c56db-417">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="c56db-417">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="c56db-418">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="c56db-418">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="c56db-419">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="c56db-419">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="c56db-420">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="c56db-420">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="c56db-421">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="c56db-421">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="c56db-422">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="c56db-422">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="c56db-423">**ATA/IDE mejorado** (42)</span><span class="sxs-lookup"><span data-stu-id="c56db-423">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="c56db-424">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="c56db-424">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="c56db-425">**TWIRP (infrarrojo bidireccional)** (44)</span><span class="sxs-lookup"><span data-stu-id="c56db-425">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="c56db-426">**FIR (infrarrojo rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="c56db-426">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="c56db-427">**Sir (infrarrojos serie)** (46)</span><span class="sxs-lookup"><span data-stu-id="c56db-427">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="c56db-428">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="c56db-428">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c56db-429">**Estado**</span><span class="sxs-lookup"><span data-stu-id="c56db-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-430">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c56db-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-431">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-432">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c56db-432">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c56db-433">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c56db-433">Current status of the object.</span></span> <span data-ttu-id="c56db-434">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-434">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c56db-435">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c56db-435">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c56db-436">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="c56db-436">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c56db-437">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="c56db-437">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c56db-438">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c56db-438">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c56db-439">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="c56db-439">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c56db-440">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="c56db-440">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c56db-441">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="c56db-441">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c56db-442">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="c56db-442">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c56db-443">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="c56db-443">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c56db-444">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="c56db-444">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c56db-445">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c56db-445">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c56db-446">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="c56db-446">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c56db-447">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="c56db-447">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c56db-448">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c56db-448">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-449">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c56db-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-450">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-451">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="c56db-451">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c56db-452">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c56db-452">State of the logical device.</span></span> <span data-ttu-id="c56db-453">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="c56db-453">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="c56db-454">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-454">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c56db-455">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="c56db-455">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c56db-456">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="c56db-456">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c56db-457">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c56db-457">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c56db-458">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="c56db-458">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c56db-459">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="c56db-459">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c56db-460">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c56db-460">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-461">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c56db-461">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-462">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-463">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c56db-463">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c56db-464">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="c56db-464">Scoping system's creation class name.</span></span>

<span data-ttu-id="c56db-465">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-465">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c56db-466">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c56db-466">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-467">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c56db-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-468">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c56db-469">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c56db-469">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c56db-470">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="c56db-470">Scoping system's name.</span></span>

<span data-ttu-id="c56db-471">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-471">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c56db-472">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="c56db-472">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c56db-473">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c56db-473">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c56db-474">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c56db-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c56db-475">Fecha y hora de la última vez que se restableció el controlador, lo que significa que el controlador se apagó o reinicializó.</span><span class="sxs-lookup"><span data-stu-id="c56db-475">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="c56db-476">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-476">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c56db-477">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c56db-477">Remarks</span></span>

<span data-ttu-id="c56db-478">La clase **CIM \_ USBController** se deriva del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-478">The **CIM\_USBController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="c56db-479">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="c56db-479">WMI does not implement this class.</span></span> <span data-ttu-id="c56db-480">Para las clases WMI derivadas de **CIM \_ USBController**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c56db-480">For WMI classes derived from **CIM\_USBController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c56db-481">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="c56db-481">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c56db-482">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c56db-482">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c56db-483">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c56db-483">Requirements</span></span>



| <span data-ttu-id="c56db-484">Requisito</span><span class="sxs-lookup"><span data-stu-id="c56db-484">Requirement</span></span> | <span data-ttu-id="c56db-485">Value</span><span class="sxs-lookup"><span data-stu-id="c56db-485">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c56db-486">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c56db-486">Minimum supported client</span></span><br/> | <span data-ttu-id="c56db-487">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c56db-487">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c56db-488">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c56db-488">Minimum supported server</span></span><br/> | <span data-ttu-id="c56db-489">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c56db-489">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c56db-490">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c56db-490">Namespace</span></span><br/>                | <span data-ttu-id="c56db-491">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c56db-491">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c56db-492">MOF</span><span class="sxs-lookup"><span data-stu-id="c56db-492">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c56db-493"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c56db-493"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c56db-494">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c56db-494">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c56db-495"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c56db-495"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c56db-496">Vea también</span><span class="sxs-lookup"><span data-stu-id="c56db-496">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c56db-497">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="c56db-497">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

