---
description: La \_ clase CIM FlatPanel representa las capacidades y la administración del dispositivo lógico de panel plano.
ms.assetid: 0c515621-4ff9-42af-a281-ac49af6d96ba
ms.tgt_platform: multiple
title: CIM_FlatPanel (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FlatPanel
- CIM_FlatPanel.Availability
- CIM_FlatPanel.Caption
- CIM_FlatPanel.ConfigManagerErrorCode
- CIM_FlatPanel.ConfigManagerUserConfig
- CIM_FlatPanel.CreationClassName
- CIM_FlatPanel.Description
- CIM_FlatPanel.DeviceID
- CIM_FlatPanel.DisplayType
- CIM_FlatPanel.ErrorCleared
- CIM_FlatPanel.ErrorDescription
- CIM_FlatPanel.HorizontalResolution
- CIM_FlatPanel.InstallDate
- CIM_FlatPanel.IsLocked
- CIM_FlatPanel.LastErrorCode
- CIM_FlatPanel.LightSource
- CIM_FlatPanel.Name
- CIM_FlatPanel.PNPDeviceID
- CIM_FlatPanel.PowerManagementCapabilities
- CIM_FlatPanel.PowerManagementSupported
- CIM_FlatPanel.ScanMode
- CIM_FlatPanel.Status
- CIM_FlatPanel.StatusInfo
- CIM_FlatPanel.SupportsColor
- CIM_FlatPanel.SystemCreationClassName
- CIM_FlatPanel.SystemName
- CIM_FlatPanel.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0c399383223734d2f8ebe68528352c229a74bfbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000619"
---
# <a name="cim_flatpanel-class"></a><span data-ttu-id="9e930-103">\_Clase FlatPanel de CIM</span><span class="sxs-lookup"><span data-stu-id="9e930-103">CIM\_FlatPanel class</span></span>

<span data-ttu-id="9e930-104">La clase **CIM \_ FlatPanel** representa las capacidades y la administración del dispositivo lógico de panel plano.</span><span class="sxs-lookup"><span data-stu-id="9e930-104">The **CIM\_FlatPanel** class represents the capabilities and management of the flat panel logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e930-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="9e930-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9e930-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9e930-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9e930-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9e930-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9e930-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9e930-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e930-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e930-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE9-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_FlatPanel : CIM_Display
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DisplayType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   HorizontalResolution;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  uint16   LightSource;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ScanMode;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsColor;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="9e930-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="9e930-110">Members</span></span>

<span data-ttu-id="9e930-111">La clase **CIM \_ FlatPanel** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9e930-111">The **CIM\_FlatPanel** class has these types of members:</span></span>

-   [<span data-ttu-id="9e930-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9e930-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9e930-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9e930-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9e930-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="9e930-114">Methods</span></span>

<span data-ttu-id="9e930-115">La clase **CIM \_ FlatPanel** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9e930-115">The **CIM\_FlatPanel** class has these methods.</span></span>



| <span data-ttu-id="9e930-116">Método</span><span class="sxs-lookup"><span data-stu-id="9e930-116">Method</span></span>                                                               | <span data-ttu-id="9e930-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e930-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e930-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="9e930-118">**Reset**</span></span>](reset-method-in-class-cim-flatpanel.md)                 | <span data-ttu-id="9e930-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9e930-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="9e930-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="9e930-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="9e930-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9e930-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-flatpanel.md) | <span data-ttu-id="9e930-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="9e930-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="9e930-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="9e930-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9e930-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9e930-124">Properties</span></span>

<span data-ttu-id="9e930-125">La clase **CIM \_ FlatPanel** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9e930-125">The **CIM\_FlatPanel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e930-126">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="9e930-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e930-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e930-129">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="9e930-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="9e930-130">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e930-130">Availability and status of the device.</span></span>

<span data-ttu-id="9e930-131">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9e930-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="9e930-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9e930-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="9e930-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="9e930-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="9e930-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9e930-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="9e930-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="9e930-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="9e930-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9e930-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="9e930-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9e930-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="9e930-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="9e930-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="9e930-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="9e930-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="9e930-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9e930-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="9e930-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="9e930-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="9e930-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="9e930-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="9e930-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="9e930-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="9e930-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-145">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="9e930-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9e930-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="9e930-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-147">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="9e930-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9e930-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="9e930-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-149">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="9e930-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9e930-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="9e930-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="9e930-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="9e930-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-152">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="9e930-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9e930-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="9e930-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-154">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="9e930-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="9e930-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="9e930-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-156">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="9e930-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="9e930-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="9e930-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-158">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="9e930-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="9e930-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="9e930-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-160">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="9e930-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9e930-161">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9e930-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9e930-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e930-164">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9e930-164">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9e930-165">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9e930-165">Short textual description of the object.</span></span>

<span data-ttu-id="9e930-166">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e930-167">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9e930-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-168">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9e930-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e930-170">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9e930-170">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9e930-171">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="9e930-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="9e930-172">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="9e930-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="9e930-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="9e930-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="9e930-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-175">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="9e930-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="9e930-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="9e930-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="9e930-177">(1)</span><span class="sxs-lookup"><span data-stu-id="9e930-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-178">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9e930-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9e930-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e930-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="9e930-180">(2)</span><span class="sxs-lookup"><span data-stu-id="9e930-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="9e930-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="9e930-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="9e930-182">(3)</span><span class="sxs-lookup"><span data-stu-id="9e930-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-183">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="9e930-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9e930-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="9e930-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="9e930-185">(4)</span><span class="sxs-lookup"><span data-stu-id="9e930-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-186">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="9e930-186">Device is not working properly.</span></span> <span data-ttu-id="9e930-187">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="9e930-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="9e930-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="9e930-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="9e930-189">(5)</span><span class="sxs-lookup"><span data-stu-id="9e930-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-190">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="9e930-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="9e930-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="9e930-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="9e930-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="9e930-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-193">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="9e930-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="9e930-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="9e930-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="9e930-195">(7)</span><span class="sxs-lookup"><span data-stu-id="9e930-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="9e930-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e930-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="9e930-197">(8)</span><span class="sxs-lookup"><span data-stu-id="9e930-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-198">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e930-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="9e930-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="9e930-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="9e930-200">(9)</span><span class="sxs-lookup"><span data-stu-id="9e930-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-201">El dispositivo no funciona correctamente. el firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e930-201">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="9e930-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="9e930-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="9e930-203">(10)</span><span class="sxs-lookup"><span data-stu-id="9e930-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-204">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="9e930-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="9e930-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e930-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="9e930-206">(11)</span><span class="sxs-lookup"><span data-stu-id="9e930-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-207">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e930-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="9e930-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="9e930-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="9e930-209">(12)</span><span class="sxs-lookup"><span data-stu-id="9e930-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-210">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="9e930-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="9e930-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e930-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="9e930-212">(13)</span><span class="sxs-lookup"><span data-stu-id="9e930-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-213">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e930-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="9e930-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="9e930-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="9e930-215">(14)</span><span class="sxs-lookup"><span data-stu-id="9e930-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-216">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="9e930-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="9e930-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="9e930-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="9e930-218">(15)</span><span class="sxs-lookup"><span data-stu-id="9e930-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-219">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="9e930-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="9e930-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e930-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="9e930-221">(16)</span><span class="sxs-lookup"><span data-stu-id="9e930-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-222">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e930-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="9e930-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="9e930-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="9e930-224">(17)</span><span class="sxs-lookup"><span data-stu-id="9e930-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-225">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="9e930-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9e930-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e930-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="9e930-227">(18)</span><span class="sxs-lookup"><span data-stu-id="9e930-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-228">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="9e930-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="9e930-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="9e930-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="9e930-230">(19)</span><span class="sxs-lookup"><span data-stu-id="9e930-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9e930-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="9e930-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="9e930-232">(20)</span><span class="sxs-lookup"><span data-stu-id="9e930-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-233">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="9e930-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="9e930-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e930-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="9e930-235">(21)</span><span class="sxs-lookup"><span data-stu-id="9e930-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-236">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="9e930-236">System failure.</span></span> <span data-ttu-id="9e930-237">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="9e930-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="9e930-238">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e930-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="9e930-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="9e930-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="9e930-240">(22)</span><span class="sxs-lookup"><span data-stu-id="9e930-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-241">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="9e930-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="9e930-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="9e930-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="9e930-243">(23)</span><span class="sxs-lookup"><span data-stu-id="9e930-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-244">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="9e930-244">System failure.</span></span> <span data-ttu-id="9e930-245">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="9e930-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="9e930-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="9e930-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="9e930-247">(24)</span><span class="sxs-lookup"><span data-stu-id="9e930-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-248">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="9e930-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9e930-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e930-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9e930-250">(25)</span><span class="sxs-lookup"><span data-stu-id="9e930-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-251">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e930-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9e930-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e930-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9e930-253">(26)</span><span class="sxs-lookup"><span data-stu-id="9e930-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-254">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e930-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="9e930-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="9e930-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="9e930-256">(27)</span><span class="sxs-lookup"><span data-stu-id="9e930-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-257">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="9e930-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="9e930-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="9e930-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="9e930-259">(28)</span><span class="sxs-lookup"><span data-stu-id="9e930-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-260">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="9e930-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="9e930-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="9e930-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="9e930-262">(29)</span><span class="sxs-lookup"><span data-stu-id="9e930-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-263">El dispositivo está deshabilitado; el firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="9e930-263">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="9e930-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="9e930-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="9e930-265">(30)</span><span class="sxs-lookup"><span data-stu-id="9e930-265">(30)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-266">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="9e930-266">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9e930-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="9e930-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="9e930-268">31</span><span class="sxs-lookup"><span data-stu-id="9e930-268">(31)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-269">El dispositivo no funciona correctamente. Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="9e930-269">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9e930-270">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="9e930-270">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-271">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9e930-271">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e930-273">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9e930-273">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9e930-274">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="9e930-274">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="9e930-275">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-275">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e930-276">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9e930-276">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-277">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9e930-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e930-279">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9e930-279">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9e930-280">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="9e930-280">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9e930-281">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="9e930-281">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9e930-282">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e930-283">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9e930-283">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-284">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9e930-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e930-286">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="9e930-286">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9e930-287">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9e930-287">Textual description of the object.</span></span>

<span data-ttu-id="9e930-288">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e930-289">**ID**</span><span class="sxs-lookup"><span data-stu-id="9e930-289">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-290">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9e930-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e930-292">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9e930-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9e930-293">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9e930-293">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="9e930-294">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e930-295">**TipoDePresentación**</span><span class="sxs-lookup"><span data-stu-id="9e930-295">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-296">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e930-296">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e930-298">Enumeración que describe el tipo de presentación de paneles planos.</span><span class="sxs-lookup"><span data-stu-id="9e930-298">Enumeration that describes the type of flat panel display.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9e930-299"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9e930-299"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9e930-300"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="9e930-300"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Passive_Matrix_LCD"></span><span id="passive_matrix_lcd"></span><span id="PASSIVE_MATRIX_LCD"></span>

<span data-ttu-id="9e930-301"><span id="Passive_Matrix_LCD"></span><span id="passive_matrix_lcd"></span><span id="PASSIVE_MATRIX_LCD"></span>**LCD de matriz pasiva** (2)</span><span class="sxs-lookup"><span data-stu-id="9e930-301"><span id="Passive_Matrix_LCD"></span><span id="passive_matrix_lcd"></span><span id="PASSIVE_MATRIX_LCD"></span>**Passive Matrix LCD** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Matrix_LCD"></span><span id="active_matrix_lcd"></span><span id="ACTIVE_MATRIX_LCD"></span>

<span data-ttu-id="9e930-302"><span id="Active_Matrix_LCD"></span><span id="active_matrix_lcd"></span><span id="ACTIVE_MATRIX_LCD"></span>**LCD de matriz activa** (3)</span><span class="sxs-lookup"><span data-stu-id="9e930-302"><span id="Active_Matrix_LCD"></span><span id="active_matrix_lcd"></span><span id="ACTIVE_MATRIX_LCD"></span>**Active Matrix LCD** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cholesteric_LCD"></span><span id="cholesteric_lcd"></span><span id="CHOLESTERIC_LCD"></span>

<span data-ttu-id="9e930-303"><span id="Cholesteric_LCD"></span><span id="cholesteric_lcd"></span><span id="CHOLESTERIC_LCD"></span>**CHOLESTERIC LCD** (4)</span><span class="sxs-lookup"><span data-stu-id="9e930-303"><span id="Cholesteric_LCD"></span><span id="cholesteric_lcd"></span><span id="CHOLESTERIC_LCD"></span>**Cholesteric LCD** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Field_Emission_Display"></span><span id="field_emission_display"></span><span id="FIELD_EMISSION_DISPLAY"></span>

<span data-ttu-id="9e930-304"><span id="Field_Emission_Display"></span><span id="field_emission_display"></span><span id="FIELD_EMISSION_DISPLAY"></span>**Presentación** de la emisión de campo (5)</span><span class="sxs-lookup"><span data-stu-id="9e930-304"><span id="Field_Emission_Display"></span><span id="field_emission_display"></span><span id="FIELD_EMISSION_DISPLAY"></span>**Field Emission Display** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-305">Emisión de campo</span><span class="sxs-lookup"><span data-stu-id="9e930-305">Field emission</span></span>

</dd> <dt>

<span id="Electro_Luminescent_Display"></span><span id="electro_luminescent_display"></span><span id="ELECTRO_LUMINESCENT_DISPLAY"></span>

<span data-ttu-id="9e930-306"><span id="Electro_Luminescent_Display"></span><span id="electro_luminescent_display"></span><span id="ELECTRO_LUMINESCENT_DISPLAY"></span>**Presentación de Luminescent** (6)</span><span class="sxs-lookup"><span data-stu-id="9e930-306"><span id="Electro_Luminescent_Display"></span><span id="electro_luminescent_display"></span><span id="ELECTRO_LUMINESCENT_DISPLAY"></span>**Electro Luminescent Display** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-307">Electroluminescent</span><span class="sxs-lookup"><span data-stu-id="9e930-307">Electro luminescent</span></span>

</dd> <dt>

<span id="Gas_Plasma"></span><span id="gas_plasma"></span><span id="GAS_PLASMA"></span>

<span data-ttu-id="9e930-308"><span id="Gas_Plasma"></span><span id="gas_plasma"></span><span id="GAS_PLASMA"></span>**Plasma de gas** (7)</span><span class="sxs-lookup"><span data-stu-id="9e930-308"><span id="Gas_Plasma"></span><span id="gas_plasma"></span><span id="GAS_PLASMA"></span>**Gas Plasma** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="LED"></span><span id="led"></span>

<span data-ttu-id="9e930-309"><span id="LED"></span><span id="led"></span>**LED** (8)</span><span class="sxs-lookup"><span data-stu-id="9e930-309"><span id="LED"></span><span id="led"></span>**LED** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9e930-310">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="9e930-310">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-311">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9e930-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e930-313">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="9e930-313">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="9e930-314">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e930-315">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9e930-315">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-316">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9e930-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e930-318">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="9e930-318">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="9e930-319">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e930-320">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="9e930-320">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-321">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9e930-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e930-323">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("píxeles")</span><span class="sxs-lookup"><span data-stu-id="9e930-323">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="9e930-324">Resolución horizontal, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="9e930-324">Horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="9e930-325">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9e930-325">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-326">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9e930-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e930-328">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="9e930-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9e930-329">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="9e930-329">Date and time the object was installed.</span></span> <span data-ttu-id="9e930-330">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="9e930-330">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9e930-331">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-331">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e930-332">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="9e930-332">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-333">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9e930-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e930-335">Si es **true**, el dispositivo está bloqueado, lo que impide la entrada o salida del usuario.</span><span class="sxs-lookup"><span data-stu-id="9e930-335">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="9e930-336">Esta propiedad se hereda de [**\_ UserDevice CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-336">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e930-337">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9e930-337">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-338">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9e930-338">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e930-340">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9e930-340">Last error code reported by the logical device.</span></span>

<span data-ttu-id="9e930-341">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e930-342">**LightSource**</span><span class="sxs-lookup"><span data-stu-id="9e930-342">**LightSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-343">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e930-343">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e930-345">Descripción del tipo de iluminación de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="9e930-345">Description of the display illumination type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9e930-346">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9e930-346">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9e930-347">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="9e930-347">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Backlit"></span><span id="backlit"></span><span id="BACKLIT"></span>

<span data-ttu-id="9e930-348">**Retroiluminación** (2)</span><span class="sxs-lookup"><span data-stu-id="9e930-348">**Backlit** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Edgelit"></span><span id="edgelit"></span><span id="EDGELIT"></span>

<span data-ttu-id="9e930-349">**Edgelit** (3)</span><span class="sxs-lookup"><span data-stu-id="9e930-349">**Edgelit** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reflective"></span><span id="reflective"></span><span id="REFLECTIVE"></span>

<span data-ttu-id="9e930-350">**Reflectante** (4)</span><span class="sxs-lookup"><span data-stu-id="9e930-350">**Reflective** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9e930-351">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="9e930-351">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9e930-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e930-354">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9e930-354">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9e930-355">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="9e930-355">Label by which the object is known.</span></span> <span data-ttu-id="9e930-356">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="9e930-356">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9e930-357">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-357">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e930-358">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="9e930-358">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-359">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9e930-359">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-360">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e930-361">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9e930-361">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9e930-362">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9e930-362">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="9e930-363">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9e930-364">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="9e930-364">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="9e930-365">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="9e930-365">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-366">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e930-366">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9e930-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e930-368">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9e930-368">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="9e930-369">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="9e930-369">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9e930-370"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9e930-370"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9e930-371"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="9e930-371"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9e930-372"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="9e930-372"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9e930-373"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="9e930-373"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-374">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="9e930-374">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="9e930-375"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="9e930-375"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-376">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="9e930-376">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="9e930-377"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="9e930-377"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-378">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="9e930-378">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="9e930-379">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="9e930-379">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="9e930-380">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="9e930-380">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="9e930-381"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="9e930-381"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-382">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="9e930-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="9e930-383"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="9e930-383"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9e930-384">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="9e930-384">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9e930-385">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="9e930-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-386">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9e930-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e930-388">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="9e930-388">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="9e930-389">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9e930-389">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="9e930-390">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="9e930-390">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="9e930-391">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="9e930-391">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="9e930-392">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e930-393">**ScanMode**</span><span class="sxs-lookup"><span data-stu-id="9e930-393">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-394">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e930-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-395">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e930-396">Modo de recorrido que indica un recorrido único o doble, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9e930-396">Scan mode that indicates single or dual scan, for example.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9e930-397">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9e930-397">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9e930-398">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="9e930-398">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Single_Scan"></span><span id="single_scan"></span><span id="SINGLE_SCAN"></span>

<span data-ttu-id="9e930-399">**Examen único** (2)</span><span class="sxs-lookup"><span data-stu-id="9e930-399">**Single Scan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual_Scan"></span><span id="dual_scan"></span><span id="DUAL_SCAN"></span>

<span data-ttu-id="9e930-400">**Examen dual** (3)</span><span class="sxs-lookup"><span data-stu-id="9e930-400">**Dual Scan** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9e930-401">**Estado**</span><span class="sxs-lookup"><span data-stu-id="9e930-401">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-402">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9e930-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e930-404">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="9e930-404">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9e930-405">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9e930-405">Current status of the object.</span></span> <span data-ttu-id="9e930-406">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-406">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9e930-407">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9e930-407">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9e930-408">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="9e930-408">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9e930-409">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="9e930-409">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9e930-410">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="9e930-410">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9e930-411">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="9e930-411">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9e930-412">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="9e930-412">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9e930-413">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="9e930-413">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9e930-414">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="9e930-414">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9e930-415">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="9e930-415">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9e930-416">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="9e930-416">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9e930-417">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="9e930-417">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9e930-418">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="9e930-418">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9e930-419">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="9e930-419">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9e930-420">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9e930-420">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-421">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e930-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-422">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e930-423">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9e930-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9e930-424">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9e930-424">State of the logical device.</span></span> <span data-ttu-id="9e930-425">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="9e930-425">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="9e930-426">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-426">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9e930-427">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="9e930-427">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9e930-428">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="9e930-428">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9e930-429">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="9e930-429">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9e930-430">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="9e930-430">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9e930-431">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="9e930-431">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9e930-432">**SupportsColor**</span><span class="sxs-lookup"><span data-stu-id="9e930-432">**SupportsColor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-433">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="9e930-433">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-434">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e930-435">Si **es true**, el panel plano admite la presentación en color.</span><span class="sxs-lookup"><span data-stu-id="9e930-435">If **TRUE**, the flat panel supports color display.</span></span>

</dd> <dt>

<span data-ttu-id="9e930-436">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9e930-436">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-437">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9e930-437">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-438">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e930-439">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9e930-439">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9e930-440">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="9e930-440">Scoping system's creation class name.</span></span>

<span data-ttu-id="9e930-441">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-441">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e930-442">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9e930-442">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-443">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9e930-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-444">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e930-445">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9e930-445">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9e930-446">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="9e930-446">Scoping system's name.</span></span>

<span data-ttu-id="9e930-447">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e930-448">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="9e930-448">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e930-449">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9e930-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9e930-450">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e930-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e930-451">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("píxeles")</span><span class="sxs-lookup"><span data-stu-id="9e930-451">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="9e930-452">Resolución vertical, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="9e930-452">Vertical resolution, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e930-453">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e930-453">Remarks</span></span>

<span data-ttu-id="9e930-454">La clase **CIM \_ FlatPanel** se deriva de la [**\_ presentación de CIM**](cim-display.md).</span><span class="sxs-lookup"><span data-stu-id="9e930-454">The **CIM\_FlatPanel** class is derived from [**CIM\_Display**](cim-display.md).</span></span>

<span data-ttu-id="9e930-455">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="9e930-455">WMI does not implement this class.</span></span>

<span data-ttu-id="9e930-456">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="9e930-456">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9e930-457">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="9e930-457">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e930-458">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e930-458">Requirements</span></span>



| <span data-ttu-id="9e930-459">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e930-459">Requirement</span></span> | <span data-ttu-id="9e930-460">Value</span><span class="sxs-lookup"><span data-stu-id="9e930-460">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e930-461">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e930-461">Minimum supported client</span></span><br/> | <span data-ttu-id="9e930-462">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e930-462">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e930-463">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e930-463">Minimum supported server</span></span><br/> | <span data-ttu-id="9e930-464">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e930-464">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e930-465">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9e930-465">Namespace</span></span><br/>                | <span data-ttu-id="9e930-466">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9e930-466">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9e930-467">MOF</span><span class="sxs-lookup"><span data-stu-id="9e930-467">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e930-468"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e930-468"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e930-469">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9e930-469">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e930-470"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e930-470"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e930-471">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e930-471">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e930-472">**Presentación de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="9e930-472">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

