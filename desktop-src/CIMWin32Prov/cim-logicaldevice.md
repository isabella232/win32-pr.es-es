---
description: La \_ clase de LogicalDevice de CIM representa una entidad de hardware que puede o no ser realizada en el hardware físico.
ms.assetid: 4f3d38ff-8080-4b53-ae29-82b68558c550
ms.tgt_platform: multiple
title: CIM_LogicalDevice (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice
- CIM_LogicalDevice.Caption
- CIM_LogicalDevice.Description
- CIM_LogicalDevice.InstallDate
- CIM_LogicalDevice.Name
- CIM_LogicalDevice.Status
- CIM_LogicalDevice.Availability
- CIM_LogicalDevice.ConfigManagerErrorCode
- CIM_LogicalDevice.ConfigManagerUserConfig
- CIM_LogicalDevice.CreationClassName
- CIM_LogicalDevice.DeviceID
- CIM_LogicalDevice.PowerManagementCapabilities
- CIM_LogicalDevice.ErrorCleared
- CIM_LogicalDevice.ErrorDescription
- CIM_LogicalDevice.LastErrorCode
- CIM_LogicalDevice.PNPDeviceID
- CIM_LogicalDevice.PowerManagementSupported
- CIM_LogicalDevice.StatusInfo
- CIM_LogicalDevice.SystemCreationClassName
- CIM_LogicalDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 49974b966e1378350e8e5475ef14bb092b3aaea1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153162"
---
# <a name="cim_logicaldevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="16f16-103">CIM_LogicalDevice (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="16f16-103">CIM_LogicalDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="16f16-104">La clase de **\_ LogicalDevice de CIM** representa una entidad de hardware que puede o no ser realizada en el hardware físico.</span><span class="sxs-lookup"><span data-stu-id="16f16-104">The **CIM\_LogicalDevice** class represents a hardware entity that may or may not be realized in physical hardware.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="16f16-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="16f16-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="16f16-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="16f16-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="16f16-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="16f16-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="16f16-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="16f16-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="16f16-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16f16-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C529-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDevice : CIM_LogicalElement
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
};
```

## <a name="members"></a><span data-ttu-id="16f16-110">Members</span><span class="sxs-lookup"><span data-stu-id="16f16-110">Members</span></span>

<span data-ttu-id="16f16-111">La clase de **\_ LogicalDevice de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="16f16-111">The **CIM\_LogicalDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="16f16-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="16f16-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="16f16-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="16f16-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="16f16-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="16f16-114">Methods</span></span>

<span data-ttu-id="16f16-115">La clase de **\_ LogicalDevice de CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="16f16-115">The **CIM\_LogicalDevice** class has these methods.</span></span>



| <span data-ttu-id="16f16-116">Método</span><span class="sxs-lookup"><span data-stu-id="16f16-116">Method</span></span>                                                                   | <span data-ttu-id="16f16-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="16f16-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16f16-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="16f16-118">**Reset**</span></span>](reset-method-in-class-cim-logicaldevice.md)                 | <span data-ttu-id="16f16-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="16f16-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="16f16-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="16f16-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="16f16-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="16f16-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-logicaldevice.md) | <span data-ttu-id="16f16-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="16f16-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="16f16-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="16f16-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="16f16-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="16f16-124">Properties</span></span>

<span data-ttu-id="16f16-125">La clase de **\_ LogicalDevice de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="16f16-125">The **CIM\_LogicalDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16f16-126">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="16f16-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16f16-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16f16-129">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="16f16-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="16f16-130">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16f16-130">Availability and status of the device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="16f16-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="16f16-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="16f16-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="16f16-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="16f16-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="16f16-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="16f16-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="16f16-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="16f16-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="16f16-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="16f16-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="16f16-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="16f16-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="16f16-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="16f16-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="16f16-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="16f16-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="16f16-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="16f16-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="16f16-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="16f16-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="16f16-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="16f16-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="16f16-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="16f16-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="16f16-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="16f16-144">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="16f16-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="16f16-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="16f16-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="16f16-146">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="16f16-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="16f16-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="16f16-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="16f16-148">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="16f16-148">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="16f16-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="16f16-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="16f16-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="16f16-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="16f16-151">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="16f16-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="16f16-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="16f16-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="16f16-153">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="16f16-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="16f16-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="16f16-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="16f16-155">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="16f16-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="16f16-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="16f16-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="16f16-157">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="16f16-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="16f16-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="16f16-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="16f16-159">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="16f16-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="16f16-160">**Caption**</span><span class="sxs-lookup"><span data-stu-id="16f16-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="16f16-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16f16-163">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="16f16-163">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="16f16-164">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="16f16-164">A short textual description of the object.</span></span>

<span data-ttu-id="16f16-165">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="16f16-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="16f16-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="16f16-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-167">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16f16-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16f16-169">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="16f16-169">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="16f16-170">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="16f16-170">Win32 Configuration Manager error code.</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="16f16-171">**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="16f16-171">**This device is working properly.**</span></span> <span data-ttu-id="16f16-172"> (0)</span><span class="sxs-lookup"><span data-stu-id="16f16-172">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="16f16-173">**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="16f16-173">**This device is not configured correctly.**</span></span> <span data-ttu-id="16f16-174">(1)</span><span class="sxs-lookup"><span data-stu-id="16f16-174">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="16f16-175">**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16f16-175">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="16f16-176">(2)</span><span class="sxs-lookup"><span data-stu-id="16f16-176">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="16f16-177">**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="16f16-177">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="16f16-178">(3)</span><span class="sxs-lookup"><span data-stu-id="16f16-178">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="16f16-179">**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="16f16-179">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="16f16-180">(4)</span><span class="sxs-lookup"><span data-stu-id="16f16-180">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="16f16-181">**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="16f16-181">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="16f16-182">(5)</span><span class="sxs-lookup"><span data-stu-id="16f16-182">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="16f16-183">**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="16f16-183">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="16f16-184"> (6)</span><span class="sxs-lookup"><span data-stu-id="16f16-184">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="16f16-185">**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="16f16-185">**Cannot filter.**</span></span> <span data-ttu-id="16f16-186">(7)</span><span class="sxs-lookup"><span data-stu-id="16f16-186">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="16f16-187">**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16f16-187">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="16f16-188">(8)</span><span class="sxs-lookup"><span data-stu-id="16f16-188">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="16f16-189">**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="16f16-189">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="16f16-190">(9)</span><span class="sxs-lookup"><span data-stu-id="16f16-190">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="16f16-191">**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="16f16-191">**This device cannot start.**</span></span> <span data-ttu-id="16f16-192">(10)</span><span class="sxs-lookup"><span data-stu-id="16f16-192">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="16f16-193">**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16f16-193">**This device failed.**</span></span> <span data-ttu-id="16f16-194">(11)</span><span class="sxs-lookup"><span data-stu-id="16f16-194">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="16f16-195">**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="16f16-195">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="16f16-196">(12)</span><span class="sxs-lookup"><span data-stu-id="16f16-196">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="16f16-197">**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16f16-197">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="16f16-198">(13)</span><span class="sxs-lookup"><span data-stu-id="16f16-198">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="16f16-199">**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="16f16-199">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="16f16-200">(14)</span><span class="sxs-lookup"><span data-stu-id="16f16-200">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="16f16-201">**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="16f16-201">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="16f16-202">(15)</span><span class="sxs-lookup"><span data-stu-id="16f16-202">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="16f16-203">**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16f16-203">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="16f16-204">(16)</span><span class="sxs-lookup"><span data-stu-id="16f16-204">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="16f16-205">**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="16f16-205">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="16f16-206">(17)</span><span class="sxs-lookup"><span data-stu-id="16f16-206">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="16f16-207">**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16f16-207">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="16f16-208">(18)</span><span class="sxs-lookup"><span data-stu-id="16f16-208">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="16f16-209">**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="16f16-209">**Failure using the VxD loader.**</span></span> <span data-ttu-id="16f16-210">(19)</span><span class="sxs-lookup"><span data-stu-id="16f16-210">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="16f16-211">**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="16f16-211">**Your registry might be corrupted.**</span></span> <span data-ttu-id="16f16-212">(20)</span><span class="sxs-lookup"><span data-stu-id="16f16-212">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="16f16-213">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16f16-213">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="16f16-214">(21)</span><span class="sxs-lookup"><span data-stu-id="16f16-214">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="16f16-215">**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="16f16-215">**This device is disabled.**</span></span> <span data-ttu-id="16f16-216">(22)</span><span class="sxs-lookup"><span data-stu-id="16f16-216">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="16f16-217">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="16f16-217">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="16f16-218">(23)</span><span class="sxs-lookup"><span data-stu-id="16f16-218">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="16f16-219">**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="16f16-219">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="16f16-220">(24)</span><span class="sxs-lookup"><span data-stu-id="16f16-220">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="16f16-221">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16f16-221">**Windows is still setting up this device.**</span></span> <span data-ttu-id="16f16-222">(25)</span><span class="sxs-lookup"><span data-stu-id="16f16-222">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="16f16-223">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16f16-223">**Windows is still setting up this device.**</span></span> <span data-ttu-id="16f16-224">(26)</span><span class="sxs-lookup"><span data-stu-id="16f16-224">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="16f16-225">**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="16f16-225">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="16f16-226">(27)</span><span class="sxs-lookup"><span data-stu-id="16f16-226">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="16f16-227">**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="16f16-227">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="16f16-228">(28)</span><span class="sxs-lookup"><span data-stu-id="16f16-228">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="16f16-229">**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="16f16-229">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="16f16-230">(29)</span><span class="sxs-lookup"><span data-stu-id="16f16-230">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="16f16-231">**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="16f16-231">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="16f16-232">(30)</span><span class="sxs-lookup"><span data-stu-id="16f16-232">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="16f16-233">**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="16f16-233">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="16f16-234">(31)</span><span class="sxs-lookup"><span data-stu-id="16f16-234">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="16f16-235">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="16f16-235">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-236">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="16f16-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16f16-238">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="16f16-238">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="16f16-239">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="16f16-239">If **TRUE**, the device is using a user-defined configuration.</span></span>

</dd> <dt>

<span data-ttu-id="16f16-240">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="16f16-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-241">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="16f16-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16f16-243">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="16f16-243">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="16f16-244">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="16f16-244">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="16f16-245">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="16f16-245">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="16f16-246">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="16f16-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-247">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="16f16-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16f16-249">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="16f16-249">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="16f16-250">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="16f16-250">A textual description of the object.</span></span>

<span data-ttu-id="16f16-251">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="16f16-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="16f16-252">**ID**</span><span class="sxs-lookup"><span data-stu-id="16f16-252">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-253">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="16f16-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16f16-255">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="16f16-255">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="16f16-256">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="16f16-256">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="16f16-257">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="16f16-257">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-258">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="16f16-258">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16f16-260">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="16f16-260">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

</dd> <dt>

<span data-ttu-id="16f16-261">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="16f16-261">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-262">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="16f16-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16f16-264">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="16f16-264">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

</dd> <dt>

<span data-ttu-id="16f16-265">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="16f16-265">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-266">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="16f16-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-267">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16f16-268">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="16f16-268">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="16f16-269">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="16f16-269">Indicates when the object was installed.</span></span> <span data-ttu-id="16f16-270">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="16f16-270">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="16f16-271">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="16f16-271">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="16f16-272">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="16f16-272">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-273">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16f16-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16f16-275">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="16f16-275">Last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="16f16-276">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="16f16-276">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-277">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="16f16-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16f16-279">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="16f16-279">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="16f16-280">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="16f16-280">Label by which the object is known.</span></span> <span data-ttu-id="16f16-281">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="16f16-281">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="16f16-282">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="16f16-282">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="16f16-283">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="16f16-283">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-284">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="16f16-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16f16-286">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="16f16-286">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="16f16-287">Indica el identificador de dispositivo Plug and Play Win32 del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="16f16-287">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="16f16-288">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="16f16-288">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="16f16-289">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="16f16-289">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-290">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16f16-290">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="16f16-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16f16-292">Indica las capacidades de energía específicas relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="16f16-292">Indicates the specific power-related capabilities of the logical device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="16f16-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="16f16-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="16f16-294">Las capacidades relacionadas con la energía son desconocidas.</span><span class="sxs-lookup"><span data-stu-id="16f16-294">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="16f16-295"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="16f16-295"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="16f16-296">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16f16-296">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="16f16-297"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="16f16-297"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="16f16-298">Se han deshabilitado las capacidades relacionadas con la energía.</span><span class="sxs-lookup"><span data-stu-id="16f16-298">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="16f16-299"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="16f16-299"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="16f16-300">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="16f16-300">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="16f16-301"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="16f16-301"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="16f16-302">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="16f16-302">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="16f16-303"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="16f16-303"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="16f16-304">Se admite el método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="16f16-304">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="16f16-305">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="16f16-305">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="16f16-306">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="16f16-306">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="16f16-307"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="16f16-307"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="16f16-308">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="16f16-308">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="16f16-309"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="16f16-309"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="16f16-310">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o Interval, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="16f16-310">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="16f16-311">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="16f16-311">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-312">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="16f16-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16f16-314">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="16f16-314">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="16f16-315">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="16f16-315">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="16f16-316">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="16f16-316">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="16f16-317">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="16f16-317">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="16f16-318">**Estado**</span><span class="sxs-lookup"><span data-stu-id="16f16-318">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-319">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="16f16-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16f16-321">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="16f16-321">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="16f16-322">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="16f16-322">String that indicates the current status of the object.</span></span> <span data-ttu-id="16f16-323">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="16f16-323">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="16f16-324">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="16f16-324">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="16f16-325">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="16f16-325">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="16f16-326">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="16f16-326">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="16f16-327">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="16f16-327">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="16f16-328">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="16f16-328">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="16f16-329">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="16f16-329">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="16f16-330">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="16f16-330">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="16f16-331">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="16f16-331">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="16f16-332">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="16f16-332">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="16f16-333">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="16f16-333">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="16f16-334">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="16f16-334">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="16f16-335">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="16f16-335">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="16f16-336">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="16f16-336">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="16f16-337">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="16f16-337">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="16f16-338">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="16f16-338">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="16f16-339">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="16f16-339">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="16f16-340">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="16f16-340">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="16f16-341">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="16f16-341">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="16f16-342">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="16f16-342">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="16f16-343">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="16f16-343">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-344">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16f16-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16f16-346">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="16f16-346">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="16f16-347">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="16f16-347">State of the logical device.</span></span> <span data-ttu-id="16f16-348">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="16f16-348">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="16f16-349">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="16f16-349">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="16f16-350">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="16f16-350">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="16f16-351">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="16f16-351">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="16f16-352">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="16f16-352">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="16f16-353">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="16f16-353">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="16f16-354">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="16f16-354">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-355">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="16f16-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16f16-357">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="16f16-357">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="16f16-358">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="16f16-358">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="16f16-359">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="16f16-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16f16-360">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="16f16-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16f16-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="16f16-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16f16-362">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="16f16-362">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="16f16-363">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="16f16-363">The scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16f16-364">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16f16-364">Remarks</span></span>

<span data-ttu-id="16f16-365">Las características de los dispositivos lógicos que administran la operación o la configuración están contenidas en el objeto **\_ LogicalDevice de CIM** , o asociados con él.</span><span class="sxs-lookup"><span data-stu-id="16f16-365">Logical device characteristics that manage operation or configuration are contained in, or associated with, the **CIM\_LogicalDevice** object.</span></span> <span data-ttu-id="16f16-366">Las propiedades operativas de la impresora, por ejemplo, son tamaños de papel compatibles o errores detectados.</span><span class="sxs-lookup"><span data-stu-id="16f16-366">Printer operational properties, for example, are supported paper sizes or detected errors.</span></span> <span data-ttu-id="16f16-367">Las propiedades de configuración de dispositivo de sensor, por ejemplo, son valores de umbral.</span><span class="sxs-lookup"><span data-stu-id="16f16-367">Sensor device configuration properties, for example, are threshold settings.</span></span> <span data-ttu-id="16f16-368">Pueden existir varias configuraciones para un dispositivo lógico y se encuentran en los objetos de [**\_ configuración de CIM**](cim-setting.md) , que están asociados con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="16f16-368">Various configurations can exist for a logical device and are contained in the [**CIM\_Setting**](cim-setting.md) objects, which are associated with the logical device.</span></span>

<span data-ttu-id="16f16-369">La clase de **\_ LogicalDevice de CIM** se deriva de [**\_ LogicalElement CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="16f16-369">The **CIM\_LogicalDevice** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="16f16-370">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="16f16-370">WMI does not implement this class.</span></span> <span data-ttu-id="16f16-371">Para las clases derivadas de un **\_ LogicalDevice de CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="16f16-371">For classes derived from **CIM\_LogicalDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="16f16-372">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="16f16-372">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="16f16-373">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="16f16-373">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="16f16-374">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16f16-374">Requirements</span></span>



| <span data-ttu-id="16f16-375">Requisito</span><span class="sxs-lookup"><span data-stu-id="16f16-375">Requirement</span></span> | <span data-ttu-id="16f16-376">Value</span><span class="sxs-lookup"><span data-stu-id="16f16-376">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16f16-377">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16f16-377">Minimum supported client</span></span><br/> | <span data-ttu-id="16f16-378">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16f16-378">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="16f16-379">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16f16-379">Minimum supported server</span></span><br/> | <span data-ttu-id="16f16-380">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16f16-380">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="16f16-381">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="16f16-381">Namespace</span></span><br/>                | <span data-ttu-id="16f16-382">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="16f16-382">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="16f16-383">MOF</span><span class="sxs-lookup"><span data-stu-id="16f16-383">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16f16-384"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16f16-384"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="16f16-385">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="16f16-385">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16f16-386"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16f16-386"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16f16-387">Consulte también</span><span class="sxs-lookup"><span data-stu-id="16f16-387">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16f16-388">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="16f16-388">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

