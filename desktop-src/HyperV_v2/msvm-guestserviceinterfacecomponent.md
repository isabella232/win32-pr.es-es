---
description: Representa el estado del componente de la interfaz de servicio invitado, que proporciona un mecanismo para interactuar con la máquina virtual desde las interfaces de administración en el sistema host.
ms.assetid: 9A158B42-052B-42B3-8539-00927056306D
title: Msvm_GuestServiceInterfaceComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent
- Msvm_GuestServiceInterfaceComponent.Availability
- Msvm_GuestServiceInterfaceComponent.Caption
- Msvm_GuestServiceInterfaceComponent.ConfigManagerErrorCode
- Msvm_GuestServiceInterfaceComponent.ConfigManagerUserConfig
- Msvm_GuestServiceInterfaceComponent.CreationClassName
- Msvm_GuestServiceInterfaceComponent.Description
- Msvm_GuestServiceInterfaceComponent.DeviceID
- Msvm_GuestServiceInterfaceComponent.ErrorCleared
- Msvm_GuestServiceInterfaceComponent.ErrorDescription
- Msvm_GuestServiceInterfaceComponent.InstallDate
- Msvm_GuestServiceInterfaceComponent.LastErrorCode
- Msvm_GuestServiceInterfaceComponent.Name
- Msvm_GuestServiceInterfaceComponent.PNPDeviceID
- Msvm_GuestServiceInterfaceComponent.PowerManagementCapabilities
- Msvm_GuestServiceInterfaceComponent.PowerManagementSupported
- Msvm_GuestServiceInterfaceComponent.Status
- Msvm_GuestServiceInterfaceComponent.StatusInfo
- Msvm_GuestServiceInterfaceComponent.SystemCreationClassName
- Msvm_GuestServiceInterfaceComponent.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4c55417edeee6d9a9fb15c474ba4ee9ca2dd93f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686951"
---
# <a name="msvm_guestserviceinterfacecomponent-class"></a><span data-ttu-id="b90c2-103">MSVM \_ GuestServiceInterfaceComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="b90c2-103">Msvm\_GuestServiceInterfaceComponent class</span></span>

<span data-ttu-id="b90c2-104">Representa el estado del componente de la interfaz de servicio invitado, que proporciona un mecanismo para interactuar con la máquina virtual desde las interfaces de administración en el sistema host.</span><span class="sxs-lookup"><span data-stu-id="b90c2-104">Represents the state of the guest service interface component, which provides a mechanism to interact with the virtual machine from the management interfaces on the host system.</span></span> <span data-ttu-id="b90c2-105">Esta clase se deriva de la clase de [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) .</span><span class="sxs-lookup"><span data-stu-id="b90c2-105">This class derives from the [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) class.</span></span>

<span data-ttu-id="b90c2-106">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b90c2-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b90c2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b90c2-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponent : CIM_LogicalDevice
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

## <a name="members"></a><span data-ttu-id="b90c2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b90c2-108">Members</span></span>

<span data-ttu-id="b90c2-109">La clase **MSVM \_ GuestServiceInterfaceComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b90c2-109">The **Msvm\_GuestServiceInterfaceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="b90c2-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b90c2-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b90c2-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b90c2-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b90c2-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b90c2-112">Methods</span></span>

<span data-ttu-id="b90c2-113">La clase **MSVM \_ GuestServiceInterfaceComponent** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b90c2-113">The **Msvm\_GuestServiceInterfaceComponent** class has these methods.</span></span>



| <span data-ttu-id="b90c2-114">Método</span><span class="sxs-lookup"><span data-stu-id="b90c2-114">Method</span></span>                                                                               | <span data-ttu-id="b90c2-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b90c2-115">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b90c2-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="b90c2-116">**RequestStateChange**</span></span>](requeststatechange-msvm-guestserviceinterfacecomponent.md) | <span data-ttu-id="b90c2-117">Solicita que el estado del componente de la interfaz de servicio invitado cambie al valor especificado.</span><span class="sxs-lookup"><span data-stu-id="b90c2-117">Requests that the state of the guest service interface component be changed to the specified value.</span></span><br/>                           |
| [<span data-ttu-id="b90c2-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="b90c2-118">**Reset**</span></span>](/windows/desktop/CIMWin32Prov/reset-method-in-class-cim-logicaldevice)                        | <span data-ttu-id="b90c2-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b90c2-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="b90c2-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b90c2-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="b90c2-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b90c2-121">**SetPowerState**</span></span>](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-logicaldevice)        | <span data-ttu-id="b90c2-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="b90c2-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b90c2-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="b90c2-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b90c2-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b90c2-124">Properties</span></span>

<span data-ttu-id="b90c2-125">La clase **MSVM \_ GuestServiceInterfaceComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b90c2-125">The **Msvm\_GuestServiceInterfaceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b90c2-126">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="b90c2-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b90c2-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-129">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b90c2-129">Availability and status of the device.</span></span>



| <span data-ttu-id="b90c2-130">Value</span><span class="sxs-lookup"><span data-stu-id="b90c2-130">Value</span></span>                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="b90c2-131">Significado</span><span class="sxs-lookup"><span data-stu-id="b90c2-131">Meaning</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="b90c2-132"><dt>**Otros**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-132"><dt>**Other**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                                                                          |                                                                                                             |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="b90c2-133"><dt>**Desconocido**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-133"><dt>**Unknown**</dt> <dt>2 (0x2)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span><dl> <span data-ttu-id="b90c2-134">En <dt>**ejecución o completada**</dt> <dt>3 (0X3)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-134"><dt>**Running/Full Power**</dt> <dt>3 (0x3)</dt></span></span> </dl>                                      |                                                                                                             |
| <span id="Warning"></span><span id="warning"></span><span id="WARNING"></span><dl> <span data-ttu-id="b90c2-135"><dt>**ADVERTENCIA**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-135"><dt>**Warning**</dt> <dt>4 (0x4)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="b90c2-136"><dt>**En la prueba**</dt> <dt>5 (0X5)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-136"><dt>**In Test**</dt> <dt>5 (0x5)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="b90c2-137"><dt>**No aplicable**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-137"><dt>**Not Applicable**</dt> <dt>6 (0x6)</dt></span></span> </dl>                                                      |                                                                                                             |
| <span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span><dl> <span data-ttu-id="b90c2-138"><dt>**Desconectar**</dt> <dt>7 (0X7)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-138"><dt>**Power Off**</dt> <dt>7 (0x7)</dt></span></span> </dl>                                                                          |                                                                                                             |
| <span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span><dl> <span data-ttu-id="b90c2-139"><dt>**Off line**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-139"><dt>**Off Line**</dt> <dt>8 (0x8)</dt></span></span> </dl>                                                                              |                                                                                                             |
| <span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span><dl> <span data-ttu-id="b90c2-140"><dt>**Desactivado el arancel**</dt> <dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-140"><dt>**Off Duty**</dt> <dt>9 (0x9)</dt></span></span> </dl>                                                                              |                                                                                                             |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="b90c2-141"><dt>**Degradado**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-141"><dt>**Degraded**</dt> <dt>10 (0xA)</dt></span></span> </dl>                                                                             |                                                                                                             |
| <span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span><dl> <span data-ttu-id="b90c2-142"><dt>**No instalado**</dt> <dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-142"><dt>**Not Installed**</dt> <dt>11 (0xB)</dt></span></span> </dl>                                                         |                                                                                                             |
| <span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span><dl> <span data-ttu-id="b90c2-143"><dt>**Error de instalación**</dt> <dt>12 (0xc)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-143"><dt>**Install Error**</dt> <dt>12 (0xC)</dt></span></span> </dl>                                                         |                                                                                                             |
| <span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span><dl> <span data-ttu-id="b90c2-144">Ahorro <dt>**de energía: 13 desconocido**</dt> <dt>(0xd)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-144"><dt>**Power Save - Unknown**</dt> <dt>13 (0xD)</dt></span></span> </dl>                             | <span data-ttu-id="b90c2-145">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="b90c2-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span><br/>                 |
| <span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span><dl> <span data-ttu-id="b90c2-146">Ahorro <dt>**de energía: modo de baja energía**</dt> <dt>14 (0xE)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-146"><dt>**Power Save - Low Power Mode**</dt> <dt>14 (0xE)</dt></span></span> </dl> | <span data-ttu-id="b90c2-147">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="b90c2-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span><br/> |
| <span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span><dl> <span data-ttu-id="b90c2-148"><dt>**Ahorro de energía: 15 en espera**</dt> <dt>(0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-148"><dt>**Power Save - Standby**</dt> <dt>15 (0xF)</dt></span></span> </dl>                             | <span data-ttu-id="b90c2-149">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="b90c2-149">The device is not functioning but could be brought to full power quickly.</span></span><br/>                        |
| <span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span><dl> <span data-ttu-id="b90c2-150"><dt>**Ciclo de alimentación**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-150"><dt>**Power Cycle**</dt> <dt>16 (0x10)</dt></span></span> </dl>                                                                |                                                                                                             |
| <span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span><dl> <span data-ttu-id="b90c2-151">Ahorro <dt>**de energía: ADVERTENCIA**</dt> <dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-151"><dt>**Power Save - Warning**</dt> <dt>17 (0x11)</dt></span></span> </dl>                            | <span data-ttu-id="b90c2-152">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="b90c2-152">The device is in a warning state, though also in a power save mode.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="b90c2-153">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b90c2-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b90c2-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-156">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b90c2-156">Short textual description of the object.</span></span> <span data-ttu-id="b90c2-157">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b90c2-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b90c2-158">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b90c2-158">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-159">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b90c2-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-161">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="b90c2-161">Win32 Configuration Manager error code.</span></span>



| <span data-ttu-id="b90c2-162">Value</span><span class="sxs-lookup"><span data-stu-id="b90c2-162">Value</span></span>                                                                                | <span data-ttu-id="b90c2-163">Significado</span><span class="sxs-lookup"><span data-stu-id="b90c2-163">Meaning</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b90c2-164"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-164"><dt>0 (0x0)</dt></span></span> </dl>   | <span data-ttu-id="b90c2-165">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="b90c2-165">Device is working properly.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="b90c2-166"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-166"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="b90c2-167">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b90c2-167">Device is not configured correctly.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="b90c2-168"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-168"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="b90c2-169">Windows no puede cargar el controlador para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b90c2-169">Windows cannot load the driver for this device.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="b90c2-170"><dt>3 (0X3)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-170"><dt>3 (0x3)</dt></span></span> </dl>   | <span data-ttu-id="b90c2-171">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="b90c2-171">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span><br/>                             |
| <dl> <span data-ttu-id="b90c2-172"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-172"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="b90c2-173">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="b90c2-173">Device is not working properly.</span></span> <span data-ttu-id="b90c2-174">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="b90c2-174">One of its drivers or the registry might be corrupted.</span></span><br/>                                        |
| <dl> <span data-ttu-id="b90c2-175"><dt>5 (0X5)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-175"><dt>5 (0x5)</dt></span></span> </dl>   | <span data-ttu-id="b90c2-176">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="b90c2-176">Driver for the device requires a resource that Windows cannot manage.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="b90c2-177"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-177"><dt>6 (0x6)</dt></span></span> </dl>   | <span data-ttu-id="b90c2-178">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b90c2-178">Boot configuration for the device conflicts with other devices.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="b90c2-179"><dt>7 (0X7)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-179"><dt>7 (0x7)</dt></span></span> </dl>   | <span data-ttu-id="b90c2-180">No se puede filtrar.</span><span class="sxs-lookup"><span data-stu-id="b90c2-180">Cannot filter.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="b90c2-181"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-181"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="b90c2-182">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b90c2-182">Driver loader for the device is missing.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="b90c2-183"><dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-183"><dt>9 (0x9)</dt></span></span> </dl>   | <span data-ttu-id="b90c2-184">El dispositivo no funciona correctamente. el firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b90c2-184">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span><br/>               |
| <dl> <span data-ttu-id="b90c2-185"><dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-185"><dt>10 (0xA)</dt></span></span> </dl>  | <span data-ttu-id="b90c2-186">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="b90c2-186">Device cannot start.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="b90c2-187"><dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-187"><dt>11 (0xB)</dt></span></span> </dl>  | <span data-ttu-id="b90c2-188">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b90c2-188">Device failed.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="b90c2-189"><dt>12 (0xC)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-189"><dt>12 (0xC)</dt></span></span> </dl>  | <span data-ttu-id="b90c2-190">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="b90c2-190">Device cannot find enough free resources to use.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="b90c2-191"><dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-191"><dt>13 (0xD)</dt></span></span> </dl>  | <span data-ttu-id="b90c2-192">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b90c2-192">Windows cannot verify the device's resources.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b90c2-193"><dt>14 (0xE)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-193"><dt>14 (0xE)</dt></span></span> </dl>  | <span data-ttu-id="b90c2-194">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="b90c2-194">Device cannot work properly until the computer is restarted.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="b90c2-195"><dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-195"><dt>15 (0xF)</dt></span></span> </dl>  | <span data-ttu-id="b90c2-196">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="b90c2-196">Device is not working properly due to a possible re-enumeration problem.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="b90c2-197"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-197"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="b90c2-198">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b90c2-198">Windows cannot identify all of the resources that the device uses.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="b90c2-199"><dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-199"><dt>17 (0x11)</dt></span></span> </dl> | <span data-ttu-id="b90c2-200">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="b90c2-200">Device is requesting an unknown resource type.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="b90c2-201"><dt>18 (0X12)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-201"><dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="b90c2-202">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b90c2-202">Device drivers must be reinstalled.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="b90c2-203"><dt>19 (0x13)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-203"><dt>19 (0x13)</dt></span></span> </dl> | <span data-ttu-id="b90c2-204">Error al usar el cargador de VxD.</span><span class="sxs-lookup"><span data-stu-id="b90c2-204">Failure using the VxD loader.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="b90c2-205"><dt>20 (0x14)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-205"><dt>20 (0x14)</dt></span></span> </dl> | <span data-ttu-id="b90c2-206">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="b90c2-206">Registry might be corrupted.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="b90c2-207"><dt>21 (0x15)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-207"><dt>21 (0x15)</dt></span></span> </dl> | <span data-ttu-id="b90c2-208">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="b90c2-208">System failure.</span></span> <span data-ttu-id="b90c2-209">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="b90c2-209">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b90c2-210">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b90c2-210">Windows is removing the device.</span></span><br/> |
| <dl> <span data-ttu-id="b90c2-211"><dt>22 (0x16)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-211"><dt>22 (0x16)</dt></span></span> </dl> | <span data-ttu-id="b90c2-212">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b90c2-212">Device is disabled.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="b90c2-213"><dt>23 (0x17)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-213"><dt>23 (0x17)</dt></span></span> </dl> | <span data-ttu-id="b90c2-214">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="b90c2-214">System failure.</span></span> <span data-ttu-id="b90c2-215">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="b90c2-215">If changing the device driver is ineffective, see the hardware documentation.</span></span><br/>                                 |
| <dl> <span data-ttu-id="b90c2-216"><dt>24 (0x18)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-216"><dt>24 (0x18)</dt></span></span> </dl> | <span data-ttu-id="b90c2-217">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="b90c2-217">Device is not present, not working properly, or does not have all of its drivers installed.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b90c2-218"><dt>25 (0x19)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-218"><dt>25 (0x19)</dt></span></span> </dl> | <span data-ttu-id="b90c2-219">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b90c2-219">Windows is still setting up the device.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="b90c2-220"><dt>26 (0x1A)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-220"><dt>26 (0x1A)</dt></span></span> </dl> | <span data-ttu-id="b90c2-221">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b90c2-221">Windows is still setting up the device.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="b90c2-222"><dt>27 (0x1B)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-222"><dt>27 (0x1B)</dt></span></span> </dl> | <span data-ttu-id="b90c2-223">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="b90c2-223">Device does not have valid log configuration.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b90c2-224"><dt>28 (0x1C)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-224"><dt>28 (0x1C)</dt></span></span> </dl> | <span data-ttu-id="b90c2-225">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="b90c2-225">Device drivers are not installed.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="b90c2-226"><dt>29 (0x1D)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-226"><dt>29 (0x1D)</dt></span></span> </dl> | <span data-ttu-id="b90c2-227">El dispositivo está deshabilitado; el firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="b90c2-227">Device is disabled; the device firmware did not provide the required resources.</span></span><br/>                                               |
| <dl> <span data-ttu-id="b90c2-228"><dt>30 (0x1E)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-228"><dt>30 (0x1E)</dt></span></span> </dl> | <span data-ttu-id="b90c2-229">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="b90c2-229">Device is using an IRQ resource that another device is using.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="b90c2-230"><dt>31 (0x1F)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-230"><dt>31 (0x1F)</dt></span></span> </dl> | <span data-ttu-id="b90c2-231">El dispositivo no funciona correctamente. Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="b90c2-231">Device is not working properly; Windows cannot load the required device drivers.</span></span><br/>                                              |



 

</dd> <dt>

<span data-ttu-id="b90c2-232">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="b90c2-232">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-233">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b90c2-233">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-235">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b90c2-235">If **TRUE**, the device is using a user-defined configuration.</span></span>

</dd> <dt>

<span data-ttu-id="b90c2-236">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b90c2-236">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-237">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b90c2-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-239">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="b90c2-239">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b90c2-240">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="b90c2-240">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="b90c2-241">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b90c2-241">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-242">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b90c2-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-244">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b90c2-244">Textual description of the object.</span></span> <span data-ttu-id="b90c2-245">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b90c2-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b90c2-246">**ID**</span><span class="sxs-lookup"><span data-stu-id="b90c2-246">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-247">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b90c2-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-249">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b90c2-249">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="b90c2-250">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b90c2-250">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-251">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b90c2-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-253">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="b90c2-253">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

</dd> <dt>

<span data-ttu-id="b90c2-254">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b90c2-254">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-255">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b90c2-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-257">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="b90c2-257">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

</dd> <dt>

<span data-ttu-id="b90c2-258">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b90c2-258">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-259">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b90c2-259">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-260">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-261">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="b90c2-261">Date and time the object was installed.</span></span> <span data-ttu-id="b90c2-262">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="b90c2-262">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="b90c2-263">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b90c2-263">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b90c2-264">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b90c2-264">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-265">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b90c2-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-266">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-267">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b90c2-267">Last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="b90c2-268">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b90c2-268">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-269">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b90c2-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-271">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="b90c2-271">Label by which the object is known.</span></span> <span data-ttu-id="b90c2-272">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="b90c2-272">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="b90c2-273">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b90c2-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b90c2-274">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b90c2-274">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-275">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b90c2-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-277">Indica el identificador de dispositivo Plug and Play Win32 del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b90c2-277">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="b90c2-278">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b90c2-278">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b90c2-279">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b90c2-279">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-280">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b90c2-280">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-282">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b90c2-282">Array of the specific power-related capabilities of a logical device.</span></span> <span data-ttu-id="b90c2-283">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="b90c2-283">This property is inherited from **CIM\_LogicalDevice**.</span></span>



| <span data-ttu-id="b90c2-284">Value</span><span class="sxs-lookup"><span data-stu-id="b90c2-284">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="b90c2-285">Significado</span><span class="sxs-lookup"><span data-stu-id="b90c2-285">Meaning</span></span>                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="b90c2-286"><dt>**Desconocido**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-286"><dt>**Unknown**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <span data-ttu-id="b90c2-287"><dt>**No se admite**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-287"><dt>**Not Supported**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                                                                                             |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="b90c2-288"><dt>**Deshabilitado**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-288"><dt>**Disabled**</dt> <dt>2 (0x2)</dt></span></span> </dl>                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="b90c2-289"><dt>**Habilitado**</dt> <dt>3 (0X3)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-289"><dt>**Enabled**</dt> <dt>3 (0x3)</dt></span></span> </dl>                                                                                                                                     | <span data-ttu-id="b90c2-290">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="b90c2-290">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span><br/>                                                                                                                                                                                               |
| <span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span><dl> <span data-ttu-id="b90c2-291"><dt>**Modos de ahorro de energía introducidos automáticamente**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-291"><dt>**Power Saving Modes Entered Automatically**</dt> <dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="b90c2-292">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="b90c2-292">The device can change its power state based on usage or other criteria.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span><dl> <span data-ttu-id="b90c2-293"><dt>**Estado de energía configurable**</dt> <dt>5 (0X5)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-293"><dt>**Power State Settable**</dt> <dt>5 (0x5)</dt></span></span> </dl>                                                                                 | <span data-ttu-id="b90c2-294">Se admite el método [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) .</span><span class="sxs-lookup"><span data-stu-id="b90c2-294">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method is supported.</span></span> <span data-ttu-id="b90c2-295">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="b90c2-295">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b90c2-296">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b90c2-296">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span><br/> |
| <span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span><dl> <span data-ttu-id="b90c2-297"><dt>**Ciclo de energía admitido**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-297"><dt>**Power Cycling Supported**</dt> <dt>6 (0x6)</dt></span></span> </dl>                                                                     | <span data-ttu-id="b90c2-298">El método [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="b90c2-298">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span><br/>                                                                                                                                                            |
| <span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span><dl> <span data-ttu-id="b90c2-299"><dt>**Potencia de tiempo admitida**</dt> <dt>7 (0X7)</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-299"><dt>**Timed Power On Supported**</dt> <dt>7 (0x7)</dt></span></span> </dl>                                                                 | <span data-ttu-id="b90c2-300">El método [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="b90c2-300">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and *Time* set to a specific date and time, or interval, for power-on.</span></span><br/>                                                                                       |



 

</dd> <dt>

<span data-ttu-id="b90c2-301">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b90c2-301">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-302">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b90c2-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-304">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="b90c2-304">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b90c2-305">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="b90c2-305">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b90c2-306">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="b90c2-306">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b90c2-307">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="b90c2-307">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="b90c2-308">**Estado**</span><span class="sxs-lookup"><span data-stu-id="b90c2-308">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-309">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b90c2-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-311">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b90c2-311">Current status of the object.</span></span> <span data-ttu-id="b90c2-312">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="b90c2-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="b90c2-313">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b90c2-313">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="b90c2-314">**ACEPTAR**</span><span class="sxs-lookup"><span data-stu-id="b90c2-314">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="b90c2-315">**Error**</span><span class="sxs-lookup"><span data-stu-id="b90c2-315">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="b90c2-316">**Degradado**</span><span class="sxs-lookup"><span data-stu-id="b90c2-316">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="b90c2-317">**Unknown**</span><span class="sxs-lookup"><span data-stu-id="b90c2-317">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="b90c2-318">**"Pred FAIL"**</span><span class="sxs-lookup"><span data-stu-id="b90c2-318">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="b90c2-319">**Comenzar**</span><span class="sxs-lookup"><span data-stu-id="b90c2-319">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="b90c2-320">**Bloqueo**</span><span class="sxs-lookup"><span data-stu-id="b90c2-320">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="b90c2-321">**Servicio**</span><span class="sxs-lookup"><span data-stu-id="b90c2-321">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="b90c2-322">**Calca**</span><span class="sxs-lookup"><span data-stu-id="b90c2-322">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="b90c2-323">**"Recover"**</span><span class="sxs-lookup"><span data-stu-id="b90c2-323">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="b90c2-324">**"Sin contacto"**</span><span class="sxs-lookup"><span data-stu-id="b90c2-324">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="b90c2-325">**"Pérdida de comunicación"**</span><span class="sxs-lookup"><span data-stu-id="b90c2-325">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b90c2-326">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b90c2-326">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-327">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b90c2-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-329">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b90c2-329">State of the logical device.</span></span> <span data-ttu-id="b90c2-330">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="b90c2-330">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span> <span data-ttu-id="b90c2-331">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="b90c2-331">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

<dl> <dt>

<span data-ttu-id="b90c2-332"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="b90c2-332"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1 (0x1))</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-333"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="b90c2-333"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2 (0x2))</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-334"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3 (0X3))</span><span class="sxs-lookup"><span data-stu-id="b90c2-334"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3 (0x3))</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-335"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="b90c2-335"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (4 (0x4))</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (5 (0X5))</span><span class="sxs-lookup"><span data-stu-id="b90c2-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5 (0x5))</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b90c2-337">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b90c2-337">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-338">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b90c2-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-340">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b90c2-340">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="b90c2-341">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b90c2-341">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b90c2-342">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b90c2-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b90c2-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b90c2-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b90c2-344">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b90c2-344">Scoping system's name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b90c2-345">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b90c2-345">Requirements</span></span>



| <span data-ttu-id="b90c2-346">Requisito</span><span class="sxs-lookup"><span data-stu-id="b90c2-346">Requirement</span></span> | <span data-ttu-id="b90c2-347">Value</span><span class="sxs-lookup"><span data-stu-id="b90c2-347">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b90c2-348">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b90c2-348">Minimum supported client</span></span><br/> | <span data-ttu-id="b90c2-349">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="b90c2-349">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b90c2-350">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b90c2-350">Minimum supported server</span></span><br/> | <span data-ttu-id="b90c2-351">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b90c2-351">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b90c2-352">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b90c2-352">Namespace</span></span><br/>                | <span data-ttu-id="b90c2-353">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b90c2-353">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b90c2-354">MOF</span><span class="sxs-lookup"><span data-stu-id="b90c2-354">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b90c2-355"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-355"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b90c2-356">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b90c2-356">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b90c2-357"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b90c2-357"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b90c2-358">Vea también</span><span class="sxs-lookup"><span data-stu-id="b90c2-358">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b90c2-359">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b90c2-359">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="b90c2-360">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b90c2-360">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

