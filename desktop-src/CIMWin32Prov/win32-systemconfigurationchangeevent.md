---
description: Win32 \_ SystemConfigurationChangeEvent&\# 8194; La clase WMI indica que se ha actualizado la lista de dispositivos del sistema (se ha agregado o quitado un dispositivo o se ha cambiado la configuración).
ms.assetid: dce1e866-e739-4f90-9016-48b20ccfb75b
ms.tgt_platform: multiple
title: Win32_SystemConfigurationChangeEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemConfigurationChangeEvent
- Win32_SystemConfigurationChangeEvent.SECURITY_DESCRIPTOR
- Win32_SystemConfigurationChangeEvent.TIME_CREATED
- Win32_SystemConfigurationChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0bc479d3415906a6536c6df1d163056e94e2af76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153409"
---
# <a name="win32_systemconfigurationchangeevent-class"></a><span data-ttu-id="1394f-103">\_Clase Win32 SystemConfigurationChangeEvent</span><span class="sxs-lookup"><span data-stu-id="1394f-103">Win32\_SystemConfigurationChangeEvent class</span></span>

<span data-ttu-id="1394f-104">La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemConfigurationChangeEvent de Win32** indica que se ha actualizado la lista de dispositivos en el sistema (se ha agregado o quitado un dispositivo o se ha cambiado la configuración).</span><span class="sxs-lookup"><span data-stu-id="1394f-104">The **Win32\_SystemConfigurationChangeEvent** [WMI class](../wmisdk/retrieving-a-class.md) indicates that the device list on the system has been refreshed (a device has been added or removed, or the configuration changed).</span></span> <span data-ttu-id="1394f-105">Se desencadena un evento y se crea una instancia de esta clase cuando se envía el mensaje "DevMgrRefreshOn<*nombredeequipo*>".</span><span class="sxs-lookup"><span data-stu-id="1394f-105">An event is fired and an instance of this is class created when the "DevMgrRefreshOn<*ComputerName*>" message is sent.</span></span> <span data-ttu-id="1394f-106">El cambio exacto en la lista de dispositivos no se incluye en el mensaje, por lo que se requiere una actualización del dispositivo para obtener la configuración actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="1394f-106">The exact change to the device list is not contained in the message, so a device refresh is required to obtain the current system settings.</span></span> <span data-ttu-id="1394f-107">Algunos ejemplos de cambios de configuración afectados son la configuración de IRQ, los puertos COM y las versiones del BIOS.</span><span class="sxs-lookup"><span data-stu-id="1394f-107">Examples of configuration changes affected are IRQ settings, COM ports, and BIOS versions.</span></span>

<span data-ttu-id="1394f-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1394f-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1394f-109">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="1394f-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1394f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1394f-110">Syntax</span></span>

``` syntax
[UUID("76746942-D94B-47E2-BBA4-AFD2FDBA61"), AMENDMENT]
class Win32_SystemConfigurationChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a><span data-ttu-id="1394f-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="1394f-111">Members</span></span>

<span data-ttu-id="1394f-112">La **clase \_ SystemConfigurationChangeEvent de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1394f-112">The **Win32\_SystemConfigurationChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="1394f-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1394f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1394f-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1394f-114">Properties</span></span>

<span data-ttu-id="1394f-115">La **clase \_ SystemConfigurationChangeEvent de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1394f-115">The **Win32\_SystemConfigurationChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1394f-116">**EventType**</span><span class="sxs-lookup"><span data-stu-id="1394f-116">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1394f-117">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1394f-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1394f-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1394f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1394f-119">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management messages \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice Management messages \| WM \_ SETTINGCHANGE")</span><span class="sxs-lookup"><span data-stu-id="1394f-119">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="1394f-120">Tipo de notificación de cambio de evento que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="1394f-120">Type of event change notification that has occurred.</span></span>

<span data-ttu-id="1394f-121">Esta propiedad se hereda de [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="1394f-121">This property is inherited from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="1394f-122">**Configuración modificada** (1)</span><span class="sxs-lookup"><span data-stu-id="1394f-122">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="1394f-123">**Llegada del dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="1394f-123">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="1394f-124">**Eliminación de dispositivos** (3)</span><span class="sxs-lookup"><span data-stu-id="1394f-124">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="1394f-125">**Acoplamiento** (4)</span><span class="sxs-lookup"><span data-stu-id="1394f-125">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1394f-126">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="1394f-126">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1394f-127">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="1394f-127">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="1394f-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1394f-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1394f-129">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="1394f-129">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="1394f-130">Esta propiedad se hereda del [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="1394f-130">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="1394f-131">Para obtener más información sobre las constantes que se usan para establecer este descriptor de seguridad, vea [constantes de seguridad de WMI](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1394f-131">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="1394f-132">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="1394f-132">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1394f-133">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1394f-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1394f-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1394f-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1394f-135">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="1394f-135">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="1394f-136">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="1394f-136">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="1394f-137">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="1394f-137">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="1394f-138">Esta propiedad se hereda del [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="1394f-138">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="1394f-139">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="1394f-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1394f-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1394f-140">Remarks</span></span>

<span data-ttu-id="1394f-141">La **clase \_ SystemConfigurationChangeEvent de Win32** se deriva de [**\_ DeviceChangeEvent de Win32**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="1394f-141">The **Win32\_SystemConfigurationChangeEvent** class is derived from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1394f-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1394f-142">Requirements</span></span>



| <span data-ttu-id="1394f-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="1394f-143">Requirement</span></span> | <span data-ttu-id="1394f-144">Value</span><span class="sxs-lookup"><span data-stu-id="1394f-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1394f-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1394f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1394f-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1394f-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1394f-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1394f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1394f-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1394f-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1394f-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1394f-149">Namespace</span></span><br/>                | <span data-ttu-id="1394f-150">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1394f-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1394f-151">MOF</span><span class="sxs-lookup"><span data-stu-id="1394f-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1394f-152"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1394f-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1394f-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1394f-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1394f-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1394f-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1394f-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="1394f-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1394f-156">**Win32 \_ DeviceChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="1394f-156">**Win32\_DeviceChangeEvent**</span></span>](win32-devicechangeevent.md)
</dt> <dt>

[<span data-ttu-id="1394f-157">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="1394f-157">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
