---
description: La \_ clase WMI abstracta DeviceChangeEvent de Win32 representa los eventos de cambio de dispositivo que se derivan de la adición, eliminación o modificación de dispositivos en el sistema del equipo.
ms.assetid: 78155357-4231-4ded-980e-89feeb864ef2
ms.tgt_platform: multiple
title: Win32_DeviceChangeEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceChangeEvent
- Win32_DeviceChangeEvent.SECURITY_DESCRIPTOR
- Win32_DeviceChangeEvent.TIME_CREATED
- Win32_DeviceChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f97ab262d95b70a69b06e15202a78d5c1364f90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807922"
---
# <a name="win32_devicechangeevent-class"></a><span data-ttu-id="17ecf-103">\_Clase Win32 DeviceChangeEvent</span><span class="sxs-lookup"><span data-stu-id="17ecf-103">Win32\_DeviceChangeEvent class</span></span>

<span data-ttu-id="17ecf-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) abstracta **\_ DeviceChangeEvent de Win32** representa los eventos de cambio de dispositivo que se derivan de la adición, eliminación o modificación de dispositivos en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="17ecf-104">The **Win32\_DeviceChangeEvent** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents device change events that result from the addition, removal, or modification of devices on the computer system.</span></span> <span data-ttu-id="17ecf-105">Esto incluye los cambios en la configuración de hardware (acoplamiento y desacoplamiento), el estado del hardware o los dispositivos recién asignados (asignación de una unidad de red).</span><span class="sxs-lookup"><span data-stu-id="17ecf-105">This includes changes in the hardware configuration (docking and undocking), the hardware state, or newly mapped devices (mapping of a network drive).</span></span> <span data-ttu-id="17ecf-106">Por ejemplo, un dispositivo ha cambiado cuando \_ se envía un mensaje de DEVICECHANGE de WM.</span><span class="sxs-lookup"><span data-stu-id="17ecf-106">For example, a device has changed when a WM\_DEVICECHANGE message is sent.</span></span>

<span data-ttu-id="17ecf-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="17ecf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="17ecf-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="17ecf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="17ecf-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17ecf-109">Syntax</span></span>

``` syntax
[UUID("0DE6AAF8-49F1-4868-B3D4-61CB69BA4322"), AMENDMENT]
class Win32_DeviceChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a><span data-ttu-id="17ecf-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="17ecf-110">Members</span></span>

<span data-ttu-id="17ecf-111">La **clase \_ DeviceChangeEvent de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="17ecf-111">The **Win32\_DeviceChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="17ecf-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17ecf-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17ecf-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17ecf-113">Properties</span></span>

<span data-ttu-id="17ecf-114">La **clase \_ DeviceChangeEvent de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="17ecf-114">The **Win32\_DeviceChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17ecf-115">**EventType**</span><span class="sxs-lookup"><span data-stu-id="17ecf-115">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17ecf-116">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="17ecf-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="17ecf-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17ecf-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17ecf-118">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIDevice Management messages \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice Management messages \| WM \_ SETTINGCHANGE")</span><span class="sxs-lookup"><span data-stu-id="17ecf-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="17ecf-119">Tipo de notificación de cambio de evento que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="17ecf-119">Type of event change notification that has occurred.</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="17ecf-120">**Configuración modificada** (1)</span><span class="sxs-lookup"><span data-stu-id="17ecf-120">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="17ecf-121">**Llegada del dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="17ecf-121">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="17ecf-122">**Eliminación de dispositivos** (3)</span><span class="sxs-lookup"><span data-stu-id="17ecf-122">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="17ecf-123">**Acoplamiento** (4)</span><span class="sxs-lookup"><span data-stu-id="17ecf-123">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="17ecf-124">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="17ecf-124">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17ecf-125">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="17ecf-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="17ecf-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17ecf-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17ecf-127">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="17ecf-127">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="17ecf-128">Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="17ecf-128">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="17ecf-129">Para obtener más información sobre las constantes que se usan para establecer este descriptor de seguridad, vea [constantes de seguridad de WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="17ecf-129">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="17ecf-130">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="17ecf-130">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17ecf-131">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="17ecf-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="17ecf-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17ecf-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17ecf-133">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="17ecf-133">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="17ecf-134">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="17ecf-134">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="17ecf-135">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="17ecf-135">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="17ecf-136">Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="17ecf-136">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="17ecf-137">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="17ecf-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17ecf-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17ecf-138">Remarks</span></span>

<span data-ttu-id="17ecf-139">**Win32 \_ DeviceChangeEvent** es una clase abstracta que se deriva de [**\_ \_ ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span><span class="sxs-lookup"><span data-stu-id="17ecf-139">The **Win32\_DeviceChangeEvent** is an abstract class derived from [**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="17ecf-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17ecf-140">Requirements</span></span>



| <span data-ttu-id="17ecf-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="17ecf-141">Requirement</span></span> | <span data-ttu-id="17ecf-142">Value</span><span class="sxs-lookup"><span data-stu-id="17ecf-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17ecf-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17ecf-143">Minimum supported client</span></span><br/> | <span data-ttu-id="17ecf-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17ecf-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17ecf-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17ecf-145">Minimum supported server</span></span><br/> | <span data-ttu-id="17ecf-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17ecf-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17ecf-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="17ecf-147">Namespace</span></span><br/>                | <span data-ttu-id="17ecf-148">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="17ecf-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17ecf-149">MOF</span><span class="sxs-lookup"><span data-stu-id="17ecf-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17ecf-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17ecf-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17ecf-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="17ecf-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17ecf-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17ecf-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17ecf-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="17ecf-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17ecf-154">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="17ecf-154">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

<span data-ttu-id="17ecf-155">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17ecf-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

