---
description: El \_ VolumeChangeEvent de Win32 representa un evento de unidad local que es el resultado de la adición de una letra de unidad o unidad montada en el sistema del equipo.
ms.assetid: 38595319-d7a1-4dcd-9ad8-a27cc484b699
ms.tgt_platform: multiple
title: Win32_VolumeChangeEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VolumeChangeEvent
- Win32_VolumeChangeEvent.SECURITY_DESCRIPTOR
- Win32_VolumeChangeEvent.TIME_CREATED
- Win32_VolumeChangeEvent.EventType
- Win32_VolumeChangeEvent.DriveName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e7610cae8d0cc746774b99a101e3c6aaf1f8a64d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152854"
---
# <a name="win32_volumechangeevent-class"></a><span data-ttu-id="38155-103">\_Clase Win32 VolumeChangeEvent</span><span class="sxs-lookup"><span data-stu-id="38155-103">Win32\_VolumeChangeEvent class</span></span>

<span data-ttu-id="38155-104">La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ VolumeChangeEvent de Win32** representa un evento de unidad local que es el resultado de la adición de una letra de unidad o unidad montada en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="38155-104">The **Win32\_VolumeChangeEvent** [WMI class](../wmisdk/retrieving-a-class.md) represents a local drive event that results from the addition of a drive letter or mounted drive on the computer system.</span></span> <span data-ttu-id="38155-105">Las unidades de red no se admiten actualmente.</span><span class="sxs-lookup"><span data-stu-id="38155-105">Network drives are not currently supported.</span></span>

<span data-ttu-id="38155-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="38155-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="38155-107">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="38155-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="38155-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38155-108">Syntax</span></span>

``` syntax
[UUID("455CE053-2552-4051-A3E4-C4200DC31B7"), AMENDMENT]
class Win32_VolumeChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  string DriveName;
};
```

## <a name="members"></a><span data-ttu-id="38155-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="38155-109">Members</span></span>

<span data-ttu-id="38155-110">La **clase \_ VolumeChangeEvent de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="38155-110">The **Win32\_VolumeChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="38155-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="38155-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38155-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="38155-112">Properties</span></span>

<span data-ttu-id="38155-113">La **clase \_ VolumeChangeEvent de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="38155-113">The **Win32\_VolumeChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38155-114">**DriveName**</span><span class="sxs-lookup"><span data-stu-id="38155-114">**DriveName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38155-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="38155-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38155-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38155-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38155-117">Nombre de unidad (letra) que se ha agregado o quitado del sistema.</span><span class="sxs-lookup"><span data-stu-id="38155-117">Drive name (letter) that has been added or removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="38155-118">**EventType**</span><span class="sxs-lookup"><span data-stu-id="38155-118">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38155-119">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="38155-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="38155-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38155-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38155-121">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management messages \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice Management messages \| WM \_ SETTINGCHANGE")</span><span class="sxs-lookup"><span data-stu-id="38155-121">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="38155-122">Tipo de notificación de cambio de evento que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="38155-122">Type of event change notification that has occurred.</span></span>

<span data-ttu-id="38155-123">Esta propiedad se hereda de [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="38155-123">This property is inherited from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="38155-124">**Configuración modificada** (1)</span><span class="sxs-lookup"><span data-stu-id="38155-124">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="38155-125">**Llegada del dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="38155-125">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="38155-126">**Eliminación de dispositivos** (3)</span><span class="sxs-lookup"><span data-stu-id="38155-126">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="38155-127">**Acoplamiento** (4)</span><span class="sxs-lookup"><span data-stu-id="38155-127">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="38155-128">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="38155-128">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38155-129">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="38155-129">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="38155-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38155-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38155-131">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="38155-131">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="38155-132">Esta propiedad se hereda del [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="38155-132">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="38155-133">Para obtener más información sobre las constantes que se usan para establecer este descriptor de seguridad, vea [constantes de seguridad de WMI](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="38155-133">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="38155-134">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="38155-134">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38155-135">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="38155-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="38155-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38155-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38155-137">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="38155-137">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="38155-138">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="38155-138">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="38155-139">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="38155-139">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="38155-140">Esta propiedad se hereda del [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="38155-140">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="38155-141">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="38155-141">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38155-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38155-142">Remarks</span></span>

<span data-ttu-id="38155-143">La **clase \_ VolumeChangeEvent de Win32** se deriva de [**\_ DeviceChangeEvent de Win32**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="38155-143">The **Win32\_VolumeChangeEvent** class is derived from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38155-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38155-144">Requirements</span></span>



| <span data-ttu-id="38155-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="38155-145">Requirement</span></span> | <span data-ttu-id="38155-146">Value</span><span class="sxs-lookup"><span data-stu-id="38155-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38155-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38155-147">Minimum supported client</span></span><br/> | <span data-ttu-id="38155-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38155-148">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="38155-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38155-149">Minimum supported server</span></span><br/> | <span data-ttu-id="38155-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38155-150">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="38155-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="38155-151">Namespace</span></span><br/>                | <span data-ttu-id="38155-152">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="38155-152">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="38155-153">MOF</span><span class="sxs-lookup"><span data-stu-id="38155-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38155-154"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38155-154"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="38155-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="38155-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38155-156"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38155-156"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38155-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="38155-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38155-158">**Win32 \_ DeviceChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="38155-158">**Win32\_DeviceChangeEvent**</span></span>](win32-devicechangeevent.md)
</dt> <dt>

[<span data-ttu-id="38155-159">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="38155-159">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
