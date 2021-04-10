---
description: La \_ clase CIM PointingDevice representa un dispositivo que apunta a las regiones de la pantalla. Cualquier dispositivo que manipula un puntero, o apunta a regiones de una presentación visual, es un miembro de esta clase. Por ejemplo, un mouse, un lápiz, un teclado táctil o una tableta.
ms.assetid: b093134a-534a-4680-8fce-d96baff26139
ms.tgt_platform: multiple
title: CIM_PointingDevice (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PointingDevice
- CIM_PointingDevice.Availability
- CIM_PointingDevice.Caption
- CIM_PointingDevice.ConfigManagerErrorCode
- CIM_PointingDevice.ConfigManagerUserConfig
- CIM_PointingDevice.CreationClassName
- CIM_PointingDevice.Description
- CIM_PointingDevice.DeviceID
- CIM_PointingDevice.ErrorCleared
- CIM_PointingDevice.ErrorDescription
- CIM_PointingDevice.Handedness
- CIM_PointingDevice.InstallDate
- CIM_PointingDevice.IsLocked
- CIM_PointingDevice.LastErrorCode
- CIM_PointingDevice.Name
- CIM_PointingDevice.NumberOfButtons
- CIM_PointingDevice.PNPDeviceID
- CIM_PointingDevice.PointingType
- CIM_PointingDevice.PowerManagementCapabilities
- CIM_PointingDevice.PowerManagementSupported
- CIM_PointingDevice.Resolution
- CIM_PointingDevice.Status
- CIM_PointingDevice.StatusInfo
- CIM_PointingDevice.SystemCreationClassName
- CIM_PointingDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3f0a52ac11d927f5cabf171f49fee3a5febaa6a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275058"
---
# <a name="cim_pointingdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="7388e-105">CIM_PointingDevice (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="7388e-105">CIM_PointingDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="7388e-106">La clase **CIM \_ PointingDevice** representa un dispositivo que apunta a las regiones de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="7388e-106">The **CIM\_PointingDevice** class represents a device that points to regions on the display.</span></span> <span data-ttu-id="7388e-107">Cualquier dispositivo que manipula un puntero, o apunta a regiones de una presentación visual, es un miembro de esta clase.</span><span class="sxs-lookup"><span data-stu-id="7388e-107">Any device that manipulates a pointer, or points to regions on a visual display, is a member of this class.</span></span> <span data-ttu-id="7388e-108">Por ejemplo, un mouse, un lápiz, un teclado táctil o una tableta.</span><span class="sxs-lookup"><span data-stu-id="7388e-108">For example, a mouse, stylus, touch pad, or tablet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7388e-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="7388e-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7388e-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7388e-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7388e-111">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7388e-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7388e-112">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7388e-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7388e-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7388e-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C535-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_PointingDevice : CIM_UserDevice
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
  uint16   Handedness;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   Name;
  uint8    NumberOfButtons;
  string   PNPDeviceID;
  uint16   PointingType;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Resolution;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="7388e-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="7388e-114">Members</span></span>

<span data-ttu-id="7388e-115">La clase **CIM \_ PointingDevice** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7388e-115">The **CIM\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="7388e-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="7388e-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="7388e-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7388e-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7388e-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="7388e-118">Methods</span></span>

<span data-ttu-id="7388e-119">La clase **CIM \_ PointingDevice** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7388e-119">The **CIM\_PointingDevice** class has these methods.</span></span>



| <span data-ttu-id="7388e-120">Método</span><span class="sxs-lookup"><span data-stu-id="7388e-120">Method</span></span>                                                                    | <span data-ttu-id="7388e-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="7388e-121">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7388e-122">**Reset**</span><span class="sxs-lookup"><span data-stu-id="7388e-122">**Reset**</span></span>](reset-method-in-class-cim-pointingdevice.md)                 | <span data-ttu-id="7388e-123">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7388e-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="7388e-124">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="7388e-124">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="7388e-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7388e-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pointingdevice.md) | <span data-ttu-id="7388e-126">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="7388e-126">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="7388e-127">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="7388e-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7388e-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7388e-128">Properties</span></span>

<span data-ttu-id="7388e-129">La clase **CIM \_ PointingDevice** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7388e-129">The **CIM\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7388e-130">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="7388e-130">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-131">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7388e-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7388e-133">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="7388e-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="7388e-134">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7388e-134">Availability and status of the device.</span></span>

<span data-ttu-id="7388e-135">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-135">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7388e-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="7388e-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7388e-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="7388e-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="7388e-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="7388e-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="7388e-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="7388e-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="7388e-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="7388e-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7388e-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="7388e-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="7388e-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="7388e-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="7388e-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="7388e-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="7388e-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="7388e-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7388e-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="7388e-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="7388e-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="7388e-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="7388e-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="7388e-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="7388e-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="7388e-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-149">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="7388e-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="7388e-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="7388e-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-151">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="7388e-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="7388e-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="7388e-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-153">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="7388e-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="7388e-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="7388e-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="7388e-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="7388e-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-156">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="7388e-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="7388e-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="7388e-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-158">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="7388e-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="7388e-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="7388e-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-160">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="7388e-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="7388e-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="7388e-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-162">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="7388e-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="7388e-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="7388e-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-164">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="7388e-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7388e-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7388e-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7388e-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7388e-168">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7388e-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7388e-169">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7388e-169">Short textual description of the object.</span></span>

<span data-ttu-id="7388e-170">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7388e-171">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7388e-171">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-172">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7388e-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7388e-174">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7388e-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7388e-175">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="7388e-175">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="7388e-176">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-176">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="7388e-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="7388e-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="7388e-178"> (0)</span><span class="sxs-lookup"><span data-stu-id="7388e-178">(0)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-179">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="7388e-179">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="7388e-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="7388e-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="7388e-181">(1)</span><span class="sxs-lookup"><span data-stu-id="7388e-181">(1)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-182">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7388e-182">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7388e-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7388e-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="7388e-184">(2)</span><span class="sxs-lookup"><span data-stu-id="7388e-184">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="7388e-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="7388e-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="7388e-186">(3)</span><span class="sxs-lookup"><span data-stu-id="7388e-186">(3)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-187">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="7388e-187">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7388e-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="7388e-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="7388e-189">(4)</span><span class="sxs-lookup"><span data-stu-id="7388e-189">(4)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-190">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="7388e-190">Device is not working properly.</span></span> <span data-ttu-id="7388e-191">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="7388e-191">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="7388e-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="7388e-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="7388e-193">(5)</span><span class="sxs-lookup"><span data-stu-id="7388e-193">(5)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-194">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="7388e-194">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="7388e-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="7388e-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="7388e-196"> (6)</span><span class="sxs-lookup"><span data-stu-id="7388e-196">(6)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-197">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7388e-197">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="7388e-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="7388e-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="7388e-199">(7)</span><span class="sxs-lookup"><span data-stu-id="7388e-199">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="7388e-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7388e-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="7388e-201">(8)</span><span class="sxs-lookup"><span data-stu-id="7388e-201">(8)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-202">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7388e-202">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="7388e-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="7388e-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="7388e-204">(9)</span><span class="sxs-lookup"><span data-stu-id="7388e-204">(9)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-205">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="7388e-205">Device is not working properly.</span></span> <span data-ttu-id="7388e-206">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7388e-206">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="7388e-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="7388e-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="7388e-208">(10)</span><span class="sxs-lookup"><span data-stu-id="7388e-208">(10)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-209">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="7388e-209">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="7388e-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7388e-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="7388e-211">(11)</span><span class="sxs-lookup"><span data-stu-id="7388e-211">(11)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-212">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7388e-212">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="7388e-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="7388e-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="7388e-214">(12)</span><span class="sxs-lookup"><span data-stu-id="7388e-214">(12)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-215">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="7388e-215">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="7388e-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7388e-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="7388e-217">(13)</span><span class="sxs-lookup"><span data-stu-id="7388e-217">(13)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-218">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7388e-218">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="7388e-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="7388e-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="7388e-220">(14)</span><span class="sxs-lookup"><span data-stu-id="7388e-220">(14)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-221">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="7388e-221">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="7388e-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="7388e-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="7388e-223">(15)</span><span class="sxs-lookup"><span data-stu-id="7388e-223">(15)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-224">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="7388e-224">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="7388e-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7388e-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="7388e-226">(16)</span><span class="sxs-lookup"><span data-stu-id="7388e-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-227">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7388e-227">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="7388e-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="7388e-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="7388e-229">(17)</span><span class="sxs-lookup"><span data-stu-id="7388e-229">(17)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-230">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="7388e-230">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7388e-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7388e-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="7388e-232">(18)</span><span class="sxs-lookup"><span data-stu-id="7388e-232">(18)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-233">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7388e-233">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="7388e-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="7388e-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="7388e-235">(19)</span><span class="sxs-lookup"><span data-stu-id="7388e-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7388e-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="7388e-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="7388e-237">(20)</span><span class="sxs-lookup"><span data-stu-id="7388e-237">(20)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-238">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="7388e-238">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="7388e-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7388e-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="7388e-240">(21)</span><span class="sxs-lookup"><span data-stu-id="7388e-240">(21)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-241">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="7388e-241">System failure.</span></span> <span data-ttu-id="7388e-242">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="7388e-242">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="7388e-243">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7388e-243">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="7388e-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="7388e-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="7388e-245">(22)</span><span class="sxs-lookup"><span data-stu-id="7388e-245">(22)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-246">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="7388e-246">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="7388e-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="7388e-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="7388e-248">(23)</span><span class="sxs-lookup"><span data-stu-id="7388e-248">(23)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-249">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="7388e-249">System failure.</span></span> <span data-ttu-id="7388e-250">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="7388e-250">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="7388e-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="7388e-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="7388e-252">(24)</span><span class="sxs-lookup"><span data-stu-id="7388e-252">(24)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-253">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="7388e-253">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7388e-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7388e-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7388e-255">(25)</span><span class="sxs-lookup"><span data-stu-id="7388e-255">(25)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-256">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7388e-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7388e-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7388e-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7388e-258">(26)</span><span class="sxs-lookup"><span data-stu-id="7388e-258">(26)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-259">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7388e-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="7388e-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="7388e-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="7388e-261">(27)</span><span class="sxs-lookup"><span data-stu-id="7388e-261">(27)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-262">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="7388e-262">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="7388e-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="7388e-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="7388e-264">(28)</span><span class="sxs-lookup"><span data-stu-id="7388e-264">(28)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-265">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="7388e-265">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="7388e-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="7388e-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="7388e-267">(29)</span><span class="sxs-lookup"><span data-stu-id="7388e-267">(29)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-268">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="7388e-268">Device is disabled.</span></span> <span data-ttu-id="7388e-269">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="7388e-269">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="7388e-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="7388e-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="7388e-271">(30)</span><span class="sxs-lookup"><span data-stu-id="7388e-271">(30)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-272">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="7388e-272">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7388e-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7388e-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="7388e-274">31</span><span class="sxs-lookup"><span data-stu-id="7388e-274">(31)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-275">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="7388e-275">Device is not working properly.</span></span> <span data-ttu-id="7388e-276">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="7388e-276">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7388e-277">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="7388e-277">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-278">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7388e-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7388e-280">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7388e-280">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7388e-281">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="7388e-281">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="7388e-282">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7388e-283">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7388e-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-284">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7388e-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7388e-286">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7388e-286">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7388e-287">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="7388e-287">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7388e-288">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="7388e-288">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7388e-289">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7388e-290">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7388e-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-291">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7388e-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7388e-293">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="7388e-293">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7388e-294">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7388e-294">Textual description of the object.</span></span>

<span data-ttu-id="7388e-295">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7388e-296">**ID**</span><span class="sxs-lookup"><span data-stu-id="7388e-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-297">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7388e-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7388e-299">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7388e-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7388e-300">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7388e-300">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="7388e-301">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7388e-302">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="7388e-302">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-303">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7388e-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7388e-305">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="7388e-305">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="7388e-306">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7388e-307">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7388e-307">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-308">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7388e-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7388e-310">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="7388e-310">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="7388e-311">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7388e-312">**Situación**</span><span class="sxs-lookup"><span data-stu-id="7388e-312">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-313">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7388e-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7388e-315">Configuración del dispositivo señalador para el funcionamiento del lado derecho o izquierdo.</span><span class="sxs-lookup"><span data-stu-id="7388e-315">Configuration of the pointing device for right-hand or left-hand operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7388e-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="7388e-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7388e-317"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (1)</span><span class="sxs-lookup"><span data-stu-id="7388e-317"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="7388e-318"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Operación de mano derecha** (2)</span><span class="sxs-lookup"><span data-stu-id="7388e-318"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Right Handed Operation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-319">Operación derecha</span><span class="sxs-lookup"><span data-stu-id="7388e-319">Right-hand operation</span></span>

</dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="7388e-320"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Operación de mano izquierda** (3)</span><span class="sxs-lookup"><span data-stu-id="7388e-320"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Left Handed Operation** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-321">Operación de la izquierda</span><span class="sxs-lookup"><span data-stu-id="7388e-321">Left-hand operation</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7388e-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7388e-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-323">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7388e-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7388e-325">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="7388e-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7388e-326">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="7388e-326">Date and time the object was installed.</span></span> <span data-ttu-id="7388e-327">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="7388e-327">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="7388e-328">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7388e-329">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="7388e-329">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-330">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7388e-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7388e-332">Si es **true**, el dispositivo está bloqueado, lo que impide la entrada o salida del usuario.</span><span class="sxs-lookup"><span data-stu-id="7388e-332">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="7388e-333">Esta propiedad se hereda de [**\_ UserDevice CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-333">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7388e-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7388e-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-335">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7388e-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7388e-337">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7388e-337">Last error code reported by the logical device.</span></span>

<span data-ttu-id="7388e-338">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7388e-339">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="7388e-339">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-340">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7388e-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7388e-342">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7388e-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7388e-343">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="7388e-343">Label by which the object is known.</span></span> <span data-ttu-id="7388e-344">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="7388e-344">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7388e-345">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-345">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7388e-346">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="7388e-346">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-347">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7388e-347">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7388e-349">Número de botones del dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="7388e-349">Number of buttons on the pointing device.</span></span>

<span data-ttu-id="7388e-350">Ejemplo: "2"</span><span class="sxs-lookup"><span data-stu-id="7388e-350">Example: "2"</span></span>

</dd> <dt>

<span data-ttu-id="7388e-351">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7388e-351">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7388e-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7388e-354">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7388e-354">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7388e-355">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7388e-355">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="7388e-356">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7388e-357">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="7388e-357">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="7388e-358">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="7388e-358">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-359">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7388e-359">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-360">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7388e-361">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo señalador DMTF \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="7388e-361">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Pointing Device\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="7388e-362">Tipo del dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="7388e-362">Type of the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7388e-363"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="7388e-363"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7388e-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="7388e-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="7388e-365"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span><span class="sxs-lookup"><span data-stu-id="7388e-365"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="7388e-366"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Bola de seguimiento** (4)</span><span class="sxs-lookup"><span data-stu-id="7388e-366"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Track Ball** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-367">Trackball</span><span class="sxs-lookup"><span data-stu-id="7388e-367">Trackball</span></span>

</dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="7388e-368"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Punto de seguimiento** (5)</span><span class="sxs-lookup"><span data-stu-id="7388e-368"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="7388e-369"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Punto de deslizamiento** (6)</span><span class="sxs-lookup"><span data-stu-id="7388e-369"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="7388e-370"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Teclado táctil** (7)</span><span class="sxs-lookup"><span data-stu-id="7388e-370"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="7388e-371"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Pantalla táctil** (8)</span><span class="sxs-lookup"><span data-stu-id="7388e-371"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="7388e-372"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Mouse-sensor óptico** (9)</span><span class="sxs-lookup"><span data-stu-id="7388e-372"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-373">Sensor óptico del mouse</span><span class="sxs-lookup"><span data-stu-id="7388e-373">Mouse   optical sensor</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7388e-374">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7388e-374">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-375">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7388e-375">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7388e-376">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7388e-377">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7388e-377">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="7388e-378">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="7388e-378">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7388e-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="7388e-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7388e-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="7388e-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7388e-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="7388e-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7388e-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="7388e-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-383">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="7388e-383">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="7388e-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="7388e-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-385">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="7388e-385">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="7388e-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="7388e-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-387">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="7388e-387">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="7388e-388">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="7388e-388">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="7388e-389">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="7388e-389">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="7388e-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="7388e-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-391">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="7388e-391">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="7388e-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="7388e-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7388e-393">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="7388e-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7388e-394">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="7388e-394">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-395">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7388e-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-396">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7388e-397">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="7388e-397">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="7388e-398">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="7388e-398">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="7388e-399">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="7388e-399">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="7388e-400">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="7388e-400">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="7388e-401">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-401">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7388e-402">**Resolución**</span><span class="sxs-lookup"><span data-stu-id="7388e-402">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-403">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7388e-403">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7388e-405">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("recuentos por pulgada")</span><span class="sxs-lookup"><span data-stu-id="7388e-405">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("counts per inch")</span></span>
</dt> </dl>

<span data-ttu-id="7388e-406">Resolución de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="7388e-406">Tracking resolution.</span></span>

<span data-ttu-id="7388e-407">Ejemplo: "0"</span><span class="sxs-lookup"><span data-stu-id="7388e-407">Example: "0"</span></span>

</dd> <dt>

<span data-ttu-id="7388e-408">**Estado**</span><span class="sxs-lookup"><span data-stu-id="7388e-408">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-409">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7388e-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7388e-411">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="7388e-411">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7388e-412">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7388e-412">Current status of the object.</span></span> <span data-ttu-id="7388e-413">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-413">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7388e-414">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7388e-414">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7388e-415">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="7388e-415">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7388e-416">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="7388e-416">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7388e-417">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="7388e-417">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7388e-418">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="7388e-418">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7388e-419">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="7388e-419">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7388e-420">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="7388e-420">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7388e-421">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="7388e-421">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7388e-422">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="7388e-422">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7388e-423">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="7388e-423">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7388e-424">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="7388e-424">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7388e-425">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="7388e-425">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7388e-426">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="7388e-426">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7388e-427">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7388e-427">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-428">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7388e-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-429">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7388e-430">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7388e-430">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7388e-431">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7388e-431">State of the logical device.</span></span> <span data-ttu-id="7388e-432">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="7388e-432">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="7388e-433">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-433">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7388e-434">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="7388e-434">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7388e-435">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="7388e-435">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7388e-436">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="7388e-436">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7388e-437">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="7388e-437">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7388e-438">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="7388e-438">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7388e-439">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7388e-439">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-440">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7388e-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-441">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7388e-442">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7388e-442">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7388e-443">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="7388e-443">Scoping system's creation class name.</span></span>

<span data-ttu-id="7388e-444">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-444">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7388e-445">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7388e-445">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7388e-446">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7388e-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7388e-447">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7388e-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7388e-448">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7388e-448">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7388e-449">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="7388e-449">Scoping system's name.</span></span>

<span data-ttu-id="7388e-450">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-450">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7388e-451">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7388e-451">Remarks</span></span>

<span data-ttu-id="7388e-452">La clase **CIM \_ PointingDevice** se deriva de [**\_ UserDevice de CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-452">The **CIM\_PointingDevice** class is derived from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

<span data-ttu-id="7388e-453">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="7388e-453">WMI does not implement this class.</span></span> <span data-ttu-id="7388e-454">Para las clases WMI derivadas de **CIM \_ PointingDevice**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7388e-454">For WMI classes derived from **CIM\_PointingDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="7388e-455">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="7388e-455">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7388e-456">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="7388e-456">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7388e-457">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7388e-457">Requirements</span></span>



| <span data-ttu-id="7388e-458">Requisito</span><span class="sxs-lookup"><span data-stu-id="7388e-458">Requirement</span></span> | <span data-ttu-id="7388e-459">Value</span><span class="sxs-lookup"><span data-stu-id="7388e-459">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7388e-460">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7388e-460">Minimum supported client</span></span><br/> | <span data-ttu-id="7388e-461">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7388e-461">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7388e-462">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7388e-462">Minimum supported server</span></span><br/> | <span data-ttu-id="7388e-463">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7388e-463">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7388e-464">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7388e-464">Namespace</span></span><br/>                | <span data-ttu-id="7388e-465">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7388e-465">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7388e-466">MOF</span><span class="sxs-lookup"><span data-stu-id="7388e-466">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7388e-467"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7388e-467"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7388e-468">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7388e-468">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7388e-469"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7388e-469"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7388e-470">Vea también</span><span class="sxs-lookup"><span data-stu-id="7388e-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7388e-471">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="7388e-471">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

