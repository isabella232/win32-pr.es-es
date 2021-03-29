---
description: Abstracción o emulación de una entidad de hardware que puede o no basarse en el hardware físico.
ms.assetid: e31c82ed-2da2-4a18-a55e-16931d74f243
title: CIM_LogicalDevice (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice
- CIM_LogicalDevice.SystemCreationClassName
- CIM_LogicalDevice.SystemName
- CIM_LogicalDevice.CreationClassName
- CIM_LogicalDevice.DeviceID
- CIM_LogicalDevice.PowerManagementSupported
- CIM_LogicalDevice.PowerManagementCapabilities
- CIM_LogicalDevice.Availability
- CIM_LogicalDevice.StatusInfo
- CIM_LogicalDevice.LastErrorCode
- CIM_LogicalDevice.ErrorDescription
- CIM_LogicalDevice.ErrorCleared
- CIM_LogicalDevice.OtherIdentifyingInfo
- CIM_LogicalDevice.PowerOnHours
- CIM_LogicalDevice.TotalPowerOnHours
- CIM_LogicalDevice.IdentifyingDescriptions
- CIM_LogicalDevice.AdditionalAvailability
- CIM_LogicalDevice.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 471b10f8d3c8640cfcc4277d0151bdd46d59db86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808390"
---
# <a name="cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="37bfa-103">CIM_LogicalDevice (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="37bfa-103">CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="37bfa-104">Abstracción o emulación de una entidad de hardware que puede o no basarse en el hardware físico.</span><span class="sxs-lookup"><span data-stu-id="37bfa-104">An abstraction or emulation of a hardware entity that may or may not be based on physical hardware.</span></span>

## <a name="syntax"></a><span data-ttu-id="37bfa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37bfa-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_LogicalDevice : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  DeviceID;
  boolean PowerManagementSupported;
  uint16  PowerManagementCapabilities[];
  uint16  Availability;
  uint16  StatusInfo;
  uint32  LastErrorCode;
  string  ErrorDescription;
  boolean ErrorCleared;
  string  OtherIdentifyingInfo[];
  uint64  PowerOnHours;
  uint64  TotalPowerOnHours;
  string  IdentifyingDescriptions[];
  uint16  AdditionalAvailability[];
  uint64  MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="37bfa-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="37bfa-106">Members</span></span>

<span data-ttu-id="37bfa-107">La clase de **\_ LogicalDevice de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="37bfa-107">The **CIM\_LogicalDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="37bfa-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="37bfa-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="37bfa-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="37bfa-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="37bfa-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="37bfa-110">Methods</span></span>

<span data-ttu-id="37bfa-111">La clase de **\_ LogicalDevice de CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="37bfa-111">The **CIM\_LogicalDevice** class has these methods.</span></span>



| <span data-ttu-id="37bfa-112">Método</span><span class="sxs-lookup"><span data-stu-id="37bfa-112">Method</span></span>                                                           | <span data-ttu-id="37bfa-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="37bfa-113">Description</span></span>                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37bfa-114">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="37bfa-114">**EnableDevice**</span></span>](cim-logicaldevice-enabledevice.md)           | <span data-ttu-id="37bfa-115">Este método es desusado.</span><span class="sxs-lookup"><span data-stu-id="37bfa-115">This method is deprecated.</span></span> <span data-ttu-id="37bfa-116">En su lugar, use el método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="37bfa-116">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="37bfa-117">**Descripción desusada:** Habilita o deshabilita el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37bfa-117">**Deprecated description:** Enables or disables the logical device.</span></span><br/>                                                                     |
| [<span data-ttu-id="37bfa-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="37bfa-118">**OnlineDevice**</span></span>](cim-logicaldevice-onlinedevice.md)           | <span data-ttu-id="37bfa-119">Este método es desusado.</span><span class="sxs-lookup"><span data-stu-id="37bfa-119">This method is deprecated.</span></span> <span data-ttu-id="37bfa-120">En su lugar, use el método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="37bfa-120">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="37bfa-121">**Descripción desusada:** Pone en línea el dispositivo lógico para que pueda aceptar solicitudes o sin conexión, por lo que ya no puede aceptar solicitudes.</span><span class="sxs-lookup"><span data-stu-id="37bfa-121">**Deprecated description:** Brings the logical device online so it can accept requests, or offline so it can no longer accept requests.</span></span><br/> |
| [<span data-ttu-id="37bfa-122">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="37bfa-122">**QuiesceDevice**</span></span>](cim-logicaldevice-quiescedevice.md)         | <span data-ttu-id="37bfa-123">Este método es desusado.</span><span class="sxs-lookup"><span data-stu-id="37bfa-123">This method is deprecated.</span></span> <span data-ttu-id="37bfa-124">En su lugar, use el método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="37bfa-124">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="37bfa-125">**Descripción desusada:** Suspende temporalmente la actividad en el dispositivo lógico o vuelve a habilitar la actividad.</span><span class="sxs-lookup"><span data-stu-id="37bfa-125">**Deprecated description:** Temporarily suspends activity on the logical device, or re-enables the activity.</span></span><br/>                            |
| [<span data-ttu-id="37bfa-126">**Reset**</span><span class="sxs-lookup"><span data-stu-id="37bfa-126">**Reset**</span></span>](cim-logicaldevice-reset.md)                         | <span data-ttu-id="37bfa-127">Restablece el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37bfa-127">Resets the logical device.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="37bfa-128">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="37bfa-128">**RestoreProperties**</span></span>](cim-logicaldevice-restoreproperties.md) | <span data-ttu-id="37bfa-129">Restaura una configuración anterior y el estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37bfa-129">Restores a previous configuration and state of the logical device.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="37bfa-130">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="37bfa-130">**SaveProperties**</span></span>](cim-logicaldevice-saveproperties.md)       | <span data-ttu-id="37bfa-131">Guarda la configuración y el estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37bfa-131">Saves the configuration and state of the logical device.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="37bfa-132">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="37bfa-132">**SetPowerState**</span></span>](cim-logicaldevice-setpowerstate.md)         | <span data-ttu-id="37bfa-133">Este método es desusado.</span><span class="sxs-lookup"><span data-stu-id="37bfa-133">This method is deprecated.</span></span> <span data-ttu-id="37bfa-134">En su lugar, use la propiedad **SetPowerState** de la clase **\_ PowerManagementService de CIM** .</span><span class="sxs-lookup"><span data-stu-id="37bfa-134">Instead, use the **SetPowerState** property of the **CIM\_PowerManagementService** class.</span></span><br/> <span data-ttu-id="37bfa-135">**Descripción desusada:** Establece el estado de energía del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37bfa-135">**Deprecated description:** Sets the power state of the logical device.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="37bfa-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="37bfa-136">Properties</span></span>

<span data-ttu-id="37bfa-137">La clase de **\_ LogicalDevice de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="37bfa-137">The **CIM\_LogicalDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37bfa-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="37bfa-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-139">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37bfa-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-141">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ lógico CIM**.**Disponibilidad**")</span><span class="sxs-lookup"><span data-stu-id="37bfa-141">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**Availability**")</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-142">Una matriz que contiene información de disponibilidad sobre el dispositivo lógico, además del que de la propiedad **Availability** .</span><span class="sxs-lookup"><span data-stu-id="37bfa-142">An array that contains availability information about of the logical device, in addition to the that of the **Availability** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="37bfa-143">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="37bfa-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37bfa-144">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="37bfa-144">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="37bfa-145">En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="37bfa-145">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="37bfa-146">**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="37bfa-146">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="37bfa-147">**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="37bfa-147">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="37bfa-148">**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="37bfa-148">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="37bfa-149">**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="37bfa-149">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="37bfa-150">Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="37bfa-150">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="37bfa-151">**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="37bfa-151">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="37bfa-152">**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="37bfa-152">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="37bfa-153">**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="37bfa-153">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="37bfa-154">**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="37bfa-154">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="37bfa-155">Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="37bfa-155">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="37bfa-156">Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="37bfa-156">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="37bfa-157">Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="37bfa-157">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="37bfa-158">**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="37bfa-158">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="37bfa-159">Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="37bfa-159">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="37bfa-160">En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="37bfa-160">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="37bfa-161">**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="37bfa-161">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="37bfa-162">**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="37bfa-162">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="37bfa-163">**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="37bfa-163">**Quiesced** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37bfa-164">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="37bfa-164">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-165">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37bfa-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-167">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 006,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus "," MIF. \|Dispositivo host DMTF \| 001,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ LogicalDevice de CIM**.**AdditionalAvailability**")</span><span class="sxs-lookup"><span data-stu-id="37bfa-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|006.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus", "MIF.DMTF\|Host Device\|001.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**AdditionalAvailability**")</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-168">Contiene la disponibilidad del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37bfa-168">Contains the availability of the logical device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="37bfa-169">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="37bfa-169">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37bfa-170">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="37bfa-170">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="37bfa-171">En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="37bfa-171">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="37bfa-172">**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="37bfa-172">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="37bfa-173">**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="37bfa-173">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="37bfa-174">**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="37bfa-174">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="37bfa-175">**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="37bfa-175">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="37bfa-176">Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="37bfa-176">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="37bfa-177">**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="37bfa-177">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="37bfa-178">**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="37bfa-178">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="37bfa-179">**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="37bfa-179">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="37bfa-180">**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="37bfa-180">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="37bfa-181">Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="37bfa-181">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="37bfa-182">Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="37bfa-182">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="37bfa-183">Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="37bfa-183">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="37bfa-184">**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="37bfa-184">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="37bfa-185">Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="37bfa-185">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="37bfa-186">En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="37bfa-186">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="37bfa-187">**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="37bfa-187">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="37bfa-188">**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="37bfa-188">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="37bfa-189">**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="37bfa-189">**Quiesced** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37bfa-190">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="37bfa-190">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37bfa-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-193">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="37bfa-193">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-194">Nombre de clase que se usa para crear una instancia del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37bfa-194">The class name used to create an instance of the logical device.</span></span> <span data-ttu-id="37bfa-195">**CreationClassName** se combina con otras propiedades de clave de esta clase para identificar de forma única las instancias de esta clase y sus subclases.</span><span class="sxs-lookup"><span data-stu-id="37bfa-195">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="37bfa-196">**ID**</span><span class="sxs-lookup"><span data-stu-id="37bfa-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37bfa-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-199">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="37bfa-199">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-200">Un identificador único del dispositivo lógico, como la dirección.</span><span class="sxs-lookup"><span data-stu-id="37bfa-200">A unique identifier of the logical device, such as the address.</span></span>

</dd> <dt>

<span data-ttu-id="37bfa-201">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="37bfa-201">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-202">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="37bfa-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-204">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("el [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).**OperationalStatus**")</span><span class="sxs-lookup"><span data-stu-id="37bfa-204">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-205">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="37bfa-205">This property is deprecated.</span></span> <span data-ttu-id="37bfa-206">En su lugar, use la propiedad **OperationalStatus** de la clase del **\_ ManagedSystemElement de CIM** .</span><span class="sxs-lookup"><span data-stu-id="37bfa-206">Instead, use the **OperationalStatus** property from the **CIM\_ManagedSystemElement** class.</span></span>

<span data-ttu-id="37bfa-207">**Descripción desusada:** Indica si se ha borrado un error de la propiedad **LastErrorCode** .</span><span class="sxs-lookup"><span data-stu-id="37bfa-207">**Deprecated description:** Indicates whether an error reported by the **LastErrorCode** property is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="37bfa-208">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="37bfa-208">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-209">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37bfa-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-211">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ DeviceErrorData. ErrorDescription")</span><span class="sxs-lookup"><span data-stu-id="37bfa-211">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_DeviceErrorData.ErrorDescription")</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-212">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="37bfa-212">This property is deprecated.</span></span> <span data-ttu-id="37bfa-213">En su lugar, use la propiedad **ErrorDescription** de la clase **\_ DeviceErrorData de CIM** .</span><span class="sxs-lookup"><span data-stu-id="37bfa-213">Instead, use the **ErrorDescription** property from the **CIM\_DeviceErrorData** class.</span></span>

<span data-ttu-id="37bfa-214">**Descripción desusada:** Información adicional sobre el error indicado por la propiedad **LastErrorCode** .</span><span class="sxs-lookup"><span data-stu-id="37bfa-214">**Deprecated description:** Additional information about the error reported by the **LastErrorCode** property.</span></span>

</dd> <dt>

<span data-ttu-id="37bfa-215">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="37bfa-215">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-216">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="37bfa-216">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-218">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ LogicalDevice de CIM**.**OtherIdentifyingInfo**")</span><span class="sxs-lookup"><span data-stu-id="37bfa-218">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**OtherIdentifyingInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-219">Matriz de cadenas que describen los elementos de la matriz **OtherIdentifyingInfo** del mismo índice.</span><span class="sxs-lookup"><span data-stu-id="37bfa-219">An array of strings that describe the **OtherIdentifyingInfo** array items of the same index.</span></span>

</dd> <dt>

<span data-ttu-id="37bfa-220">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="37bfa-220">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-221">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="37bfa-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-223">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ DeviceErrorData. LastErrorCode")</span><span class="sxs-lookup"><span data-stu-id="37bfa-223">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_DeviceErrorData.LastErrorCode")</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-224">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="37bfa-224">This property is deprecated.</span></span> <span data-ttu-id="37bfa-225">En su lugar, usamos la propiedad **LastErrorCode** de la **clase \_ DeviceErrorData de CIM** .</span><span class="sxs-lookup"><span data-stu-id="37bfa-225">Instead, we use the **LastErrorCode** property from the **CIM\_DeviceErrorData** class.</span></span>

<span data-ttu-id="37bfa-226">**Descripción desusada:** Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37bfa-226">**Deprecated description:** The last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="37bfa-227">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="37bfa-227">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-228">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37bfa-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-230">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sin valor"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos")</span><span class="sxs-lookup"><span data-stu-id="37bfa-230">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-231">Esta propiedad está en desuso y no debe utilizarse.</span><span class="sxs-lookup"><span data-stu-id="37bfa-231">This property is deprecated and should not be used.</span></span>

<span data-ttu-id="37bfa-232">**Descripción desusada:** El tiempo máximo, en milisegundos, que un dispositivo puede permanecer en un Estado deshabilitado temporalmente (las propiedades **Availability** y **AdditionalAvailability** se establecen en "21" inactiva).</span><span class="sxs-lookup"><span data-stu-id="37bfa-232">**Deprecated description:** The maximum time in milliseconds, that a device can remain in a temporarily disabled state (**Availability** and **AdditionalAvailability** properties set to "21"   quiescent ).</span></span> <span data-ttu-id="37bfa-233">Un valor de "0" indica que el dispositivo lógico puede permanecer indefinidamente en un Estado deshabilitado temporalmente.</span><span class="sxs-lookup"><span data-stu-id="37bfa-233">A value of "0" indicates that the logical device can remain in a temporarily disabled state indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="37bfa-234">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="37bfa-234">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-235">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="37bfa-235">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-237">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ LogicalDevice de CIM**.**IdentifyingDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="37bfa-237">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**IdentifyingDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-238">Información que identifica el dispositivo lógico, que no sea **DeviceID**.</span><span class="sxs-lookup"><span data-stu-id="37bfa-238">Information that identifies the logical device, other than **DeviceID**.</span></span>

</dd> <dt>

<span data-ttu-id="37bfa-239">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="37bfa-239">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-240">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37bfa-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-242">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities. PowerCapabilities")</span><span class="sxs-lookup"><span data-stu-id="37bfa-242">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities.PowerCapabilities")</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-243">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="37bfa-243">This property is deprecated.</span></span> <span data-ttu-id="37bfa-244">En su lugar, utilice la clase **\_ PowerManagementCapabilities de CIM** .</span><span class="sxs-lookup"><span data-stu-id="37bfa-244">Instead, use the **CIM\_PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="37bfa-245">**Descripción desusada:** Una matriz que contiene las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37bfa-245">**Deprecated description:** An array that contains the power management capabilities of the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37bfa-246">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="37bfa-246">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="37bfa-247">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="37bfa-247">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="37bfa-248">**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="37bfa-248">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="37bfa-249">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="37bfa-249">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="37bfa-250">**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="37bfa-250">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="37bfa-251">**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="37bfa-251">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="37bfa-252">**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="37bfa-252">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="37bfa-253">Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="37bfa-253">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37bfa-254">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="37bfa-254">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-255">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="37bfa-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-257">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities")</span><span class="sxs-lookup"><span data-stu-id="37bfa-257">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities")</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-258">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="37bfa-258">This property is deprecated.</span></span> <span data-ttu-id="37bfa-259">En su lugar, use la clase **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="37bfa-259">Instead, use the **PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="37bfa-260">**Descripción desusada: true** si el dispositivo lógico se puede administrar con energía; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="37bfa-260">**Deprecated description:  true** if the logical device can be power managed; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="37bfa-261">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="37bfa-261">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-262">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37bfa-262">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-264">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("horas"), **contador**</span><span class="sxs-lookup"><span data-stu-id="37bfa-264">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hours"), **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-265">El número de horas consecutivas que se ha alimentado el dispositivo lógico desde su último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="37bfa-265">The number of consecutive hours the logical device has been powered, since its last power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="37bfa-266">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="37bfa-266">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-267">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="37bfa-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-269">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Estado operativo DMTF \| 006,4 ")</span><span class="sxs-lookup"><span data-stu-id="37bfa-269">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|006.4")</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-270">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="37bfa-270">This property is deprecated.</span></span> <span data-ttu-id="37bfa-271">En su lugar, utilice la clase **\_ PowerManagementCapabilities de CIM** .</span><span class="sxs-lookup"><span data-stu-id="37bfa-271">Instead, use the **CIM\_PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="37bfa-272">**Descripción desusada:** Indica si el dispositivo lógico está habilitado o en un estado relacionado.</span><span class="sxs-lookup"><span data-stu-id="37bfa-272">**Deprecated description:** Indicates whether the logical device is enabled or in a related state.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="37bfa-273">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="37bfa-273">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="37bfa-274">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="37bfa-274">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="37bfa-275">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="37bfa-275">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="37bfa-276">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="37bfa-276">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="37bfa-277">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="37bfa-277">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="37bfa-278">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="37bfa-278">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-279">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37bfa-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-281">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="37bfa-281">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-282">Nombre de clase que se usa para crear una instancia del sistema que contiene el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37bfa-282">The class name used to create an instance of the system that contains the logical device.</span></span> <span data-ttu-id="37bfa-283">**SystemCreationClassName** se combina con otras propiedades clave de esta clase para identificar de forma única las instancias de esta clase y sus subclases.</span><span class="sxs-lookup"><span data-stu-id="37bfa-283">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="37bfa-284">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="37bfa-284">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-285">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="37bfa-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-287">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**")</span><span class="sxs-lookup"><span data-stu-id="37bfa-287">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-288">Nombre del sistema que contiene el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37bfa-288">The name of the system that contains the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="37bfa-289">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="37bfa-289">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37bfa-290">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="37bfa-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="37bfa-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37bfa-292">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("horas"), **contador**</span><span class="sxs-lookup"><span data-stu-id="37bfa-292">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hours"), **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="37bfa-293">Número total de horas que se ha encendido el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="37bfa-293">The total number of hours the logical device has been powered.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37bfa-294">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37bfa-294">Requirements</span></span>



| <span data-ttu-id="37bfa-295">Requisito</span><span class="sxs-lookup"><span data-stu-id="37bfa-295">Requirement</span></span> | <span data-ttu-id="37bfa-296">Value</span><span class="sxs-lookup"><span data-stu-id="37bfa-296">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37bfa-297">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37bfa-297">Minimum supported client</span></span><br/> | <span data-ttu-id="37bfa-298">Windows 8</span><span class="sxs-lookup"><span data-stu-id="37bfa-298">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="37bfa-299">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37bfa-299">Minimum supported server</span></span><br/> | <span data-ttu-id="37bfa-300">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37bfa-300">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="37bfa-301">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="37bfa-301">Namespace</span></span><br/>                | <span data-ttu-id="37bfa-302">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="37bfa-302">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="37bfa-303">MOF</span><span class="sxs-lookup"><span data-stu-id="37bfa-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37bfa-304"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37bfa-304"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37bfa-305">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="37bfa-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37bfa-306"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37bfa-306"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="37bfa-307">Vea también</span><span class="sxs-lookup"><span data-stu-id="37bfa-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37bfa-308">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="37bfa-308">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

