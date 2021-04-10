---
description: Win32 \_ PowerManagementEvent &\# 32; La clase WMI representa los eventos de administración de energía resultantes de los cambios de estado de energía.
ms.assetid: b5781805-87c7-4eaf-afbb-a1770fcff41c
ms.tgt_platform: multiple
title: Win32_PowerManagementEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PowerManagementEvent
- Win32_PowerManagementEvent.SECURITY_DESCRIPTOR
- Win32_PowerManagementEvent.TIME_CREATED
- Win32_PowerManagementEvent.EventType
- Win32_PowerManagementEvent.OEMEventCode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0e7dfa68646dbefb6d6b70218fe99830b44a0c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153109"
---
# <a name="win32_powermanagementevent-class"></a><span data-ttu-id="b909e-103">\_Clase Win32 PowerManagementEvent</span><span class="sxs-lookup"><span data-stu-id="b909e-103">Win32\_PowerManagementEvent class</span></span>

<span data-ttu-id="b909e-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PowerManagementEvent de Win32** representa los eventos de administración de energía resultantes de los cambios de estado de energía.</span><span class="sxs-lookup"><span data-stu-id="b909e-104">The **Win32\_PowerManagementEvent** [WMI class](../wmisdk/retrieving-a-class.md) represents power management events resulting from power state changes.</span></span> <span data-ttu-id="b909e-105">Estos cambios de estado están asociados a los protocolos de administración avanzada de energía (APM) o configuración avanzada y de interfaz de energía (ACPI).</span><span class="sxs-lookup"><span data-stu-id="b909e-105">These state changes are associated with either the Advanced Power Management (APM) or the Advanced Configuration and Power Interface (ACPI) system management protocols.</span></span>

<span data-ttu-id="b909e-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b909e-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b909e-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b909e-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b909e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b909e-108">Syntax</span></span>

``` syntax
[UUID("{86460B6B-E709-11d2-B139-00105A1F77A1}"), AMENDMENT]
class Win32_PowerManagementEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  uint16 OEMEventCode;
};
```

## <a name="members"></a><span data-ttu-id="b909e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b909e-109">Members</span></span>

<span data-ttu-id="b909e-110">La **clase \_ PowerManagementEvent de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b909e-110">The **Win32\_PowerManagementEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="b909e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b909e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b909e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b909e-112">Properties</span></span>

<span data-ttu-id="b909e-113">La **clase \_ PowerManagementEvent de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b909e-113">The **Win32\_PowerManagementEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b909e-114">**EventType**</span><span class="sxs-lookup"><span data-stu-id="b909e-114">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b909e-115">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b909e-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b909e-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b909e-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b909e-117">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("eventos de administración de energía de inesperados win32api \| ")</span><span class="sxs-lookup"><span data-stu-id="b909e-117">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Power Management Events")</span></span>
</dt> </dl>

<span data-ttu-id="b909e-118">Tipo de cambio en el estado de energía del sistema.</span><span class="sxs-lookup"><span data-stu-id="b909e-118">Type of change in the system power state.</span></span>

<dt>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>

<span data-ttu-id="b909e-119"><span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Entrar en suspensión** (4)</span><span class="sxs-lookup"><span data-stu-id="b909e-119"><span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Entering Suspend** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b909e-120">Mientras está suspendido, el equipo parece estar desactivado; sin embargo, se puede "activar" en respuesta a varios eventos, incluidos los datos proporcionados por el usuario (por ejemplo, al mover el mouse o al presionar una tecla en el teclado).</span><span class="sxs-lookup"><span data-stu-id="b909e-120">While suspended, the computer appears to be off; however, it can be "awakened" in response to various events, including user input (such as moving the mouse or pressing a key on the keyboard).</span></span> <span data-ttu-id="b909e-121">Mientras el equipo está suspendido, el consumo de energía se reduce a uno de varios niveles, en función de cómo se use el sistema.</span><span class="sxs-lookup"><span data-stu-id="b909e-121">While the computer is suspended, power consumption is reduced to one of several levels depending on how the system is to be used.</span></span> <span data-ttu-id="b909e-122">Cuanto menor sea el nivel de consumo de energía, más tiempo tardará el sistema en volver al estado de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="b909e-122">The lower the level of power consumption, the more time it takes the system to return to the working state.</span></span> <span data-ttu-id="b909e-123">Cuando el equipo entra en estado de suspensión, el escritorio está bloqueado y debe presionar CTRL + ALT + Supr y proporcionar un nombre de usuario y una contraseña válidos para reanudar las operaciones.</span><span class="sxs-lookup"><span data-stu-id="b909e-123">When the computer enters the suspend state, the desktop is locked, and you must press CTRL+ALT+DELETE and provide a valid user name and password to resume operations</span></span>

</dd> <dt>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>

<span data-ttu-id="b909e-124"><span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Reanudar desde suspensión** (7)</span><span class="sxs-lookup"><span data-stu-id="b909e-124"><span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Resume from Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b909e-125">Indica que se ha enviado un mensaje de reanudación a partir de la suspensión, lo que permite al equipo volver a su estado de energía normal.</span><span class="sxs-lookup"><span data-stu-id="b909e-125">Indicates that a Resume from Suspend message has been sent, enabling the computer to return to its regular power state.</span></span>

</dd> <dt>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>

<span data-ttu-id="b909e-126"><span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Cambio de estado de energía** (10)</span><span class="sxs-lookup"><span data-stu-id="b909e-126"><span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Power Status Change** (10)</span></span>


</dt> <dd>

<span data-ttu-id="b909e-127">Indica un cambio en el estado de energía del equipo, por ejemplo, un conmutador de alimentación de la batería a AC o de CA a una fuente de alimentación ininterrumpida.</span><span class="sxs-lookup"><span data-stu-id="b909e-127">Indicates a change in the power status of the computer, such as a switch from battery power to AC, or from AC to an uninterruptible power supply.</span></span> <span data-ttu-id="b909e-128">El sistema difunde también este evento cuando la energía de la batería restante queda por debajo del umbral especificado por el usuario o cuando la energía de la batería cambia en un porcentaje especificado.</span><span class="sxs-lookup"><span data-stu-id="b909e-128">The system also broadcasts this event when remaining battery power slips below the threshold specified by the user or if the battery power changes by a specified percentage.</span></span>

</dd> <dt>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>

<span data-ttu-id="b909e-129"><span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**Evento OEM** (11)</span><span class="sxs-lookup"><span data-stu-id="b909e-129"><span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**OEM Event** (11)</span></span>


</dt> <dd>

<span data-ttu-id="b909e-130">Indica que un BIOS de administración avanzada de energía (APM) ha enviado un evento OEM.</span><span class="sxs-lookup"><span data-stu-id="b909e-130">Indicates that an Advanced Power Management (APM) BIOS has sent an OEM event.</span></span> <span data-ttu-id="b909e-131">El valor del evento se capturará en la propiedad **OEMEventCode** .</span><span class="sxs-lookup"><span data-stu-id="b909e-131">The value of the event will be captured in the **OEMEventCode** property.</span></span> <span data-ttu-id="b909e-132">Dado que algunas implementaciones de BIOS de APM no proporcionan notificaciones de eventos de OEM, este evento nunca se puede difundir en algunos equipos.</span><span class="sxs-lookup"><span data-stu-id="b909e-132">Because some APM BIOS implementations do not provide OEM event notifications, this event might never be broadcast on some computers.</span></span> <span data-ttu-id="b909e-133">APM es un esquema de administración de energía heredado.</span><span class="sxs-lookup"><span data-stu-id="b909e-133">APM is a legacy power management scheme.</span></span> <span data-ttu-id="b909e-134">Aunque todavía se admite, el APM se ha sustituido en gran medida por ACPI (Advanced Configuration and Power Interface).</span><span class="sxs-lookup"><span data-stu-id="b909e-134">Although still supported, APM has been largely superseded by ACPI (Advanced Configuration and Power Interface).</span></span>

</dd> <dt>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>

<span data-ttu-id="b909e-135"><span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Reanudar automáticamente** (18)</span><span class="sxs-lookup"><span data-stu-id="b909e-135"><span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Resume Automatic** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b909e-136">Indica que el equipo se ha activado en respuesta a un evento.</span><span class="sxs-lookup"><span data-stu-id="b909e-136">Indicates that the computer has awakened in response to an event.</span></span> <span data-ttu-id="b909e-137">Si el sistema detecta actividad del usuario (por ejemplo, un clic del mouse), se difundirá el mensaje ResumeSuspend, lo que permite a las aplicaciones saber que pueden reanudar la interactividad completa con el usuario.</span><span class="sxs-lookup"><span data-stu-id="b909e-137">If the system detects user activity (such as a mouse click), the ResumeSuspend message will be broadcast, letting applications know that they can resume full interactivity with the user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b909e-138">**OEMEventCode**</span><span class="sxs-lookup"><span data-stu-id="b909e-138">**OEMEventCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b909e-139">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b909e-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b909e-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b909e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b909e-141">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("eventos de administración de energía de inesperados win32api \| ")</span><span class="sxs-lookup"><span data-stu-id="b909e-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Power Management Events")</span></span>
</dt> </dl>

<span data-ttu-id="b909e-142">Estado de alimentación del sistema definido por el fabricante de equipos originales (OEM) cuando la propiedad **EventType** de esta clase está establecida en 11 (evento OEM); de lo contrario, esta propiedad se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="b909e-142">System power state defined by the original equipment manufacturer (OEM) when the **EventType** property of this class is set to 11 (OEM Event); otherwise, this property is set to **NULL**.</span></span> <span data-ttu-id="b909e-143">Los eventos OEM se generan cuando un BIOS APM señala un evento de OEM de APM.</span><span class="sxs-lookup"><span data-stu-id="b909e-143">OEM events are generated when an APM BIOS signals an APM OEM event.</span></span> <span data-ttu-id="b909e-144">Los códigos de evento de OEM están en el intervalo 0x0200h-0x02FFh.</span><span class="sxs-lookup"><span data-stu-id="b909e-144">OEM event codes are in the range 0x0200h - 0x02FFh.</span></span>

</dd> <dt>

<span data-ttu-id="b909e-145">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="b909e-145">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b909e-146">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="b909e-146">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b909e-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b909e-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b909e-148">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="b909e-148">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="b909e-149">Esta propiedad se hereda del [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="b909e-149">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="b909e-150">Para obtener más información sobre las constantes que se usan para establecer este descriptor de seguridad, vea [constantes de seguridad de WMI](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b909e-150">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b909e-151">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="b909e-151">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b909e-152">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b909e-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b909e-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b909e-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b909e-154">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="b909e-154">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="b909e-155">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="b909e-155">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="b909e-156">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="b909e-156">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="b909e-157">Esta propiedad se hereda del [**\_ \_ evento**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="b909e-157">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="b909e-158">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="b909e-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b909e-159">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b909e-159">Remarks</span></span>

<span data-ttu-id="b909e-160">La **clase \_ PowerManagementEvent de Win32** se deriva de [**\_ \_ ExtrinsicEvent**](../wmisdk/--extrinsicevent.md).</span><span class="sxs-lookup"><span data-stu-id="b909e-160">The **Win32\_PowerManagementEvent** class is derived from [**\_\_ExtrinsicEvent**](../wmisdk/--extrinsicevent.md).</span></span>

<span data-ttu-id="b909e-161">Los cambios en el estado de energía suelen indicar que se ha producido un problema con un equipo o con otro dispositivo administrado.</span><span class="sxs-lookup"><span data-stu-id="b909e-161">Changes in power status often indicate that a problem has occurred with a computer or with another managed device.</span></span> <span data-ttu-id="b909e-162">Si un servidor cambia repentinamente de corriente alterna a una fuente de alimentación ininterrumpida, este cambio puede indicar que se ha producido un problema eléctrico de algún tipo, ya sea con el equipo o con el sistema eléctrico en el salón en el que se mantiene el equipo.</span><span class="sxs-lookup"><span data-stu-id="b909e-162">If a server suddenly switches from AC power to an uninterruptible power supply, this change can indicate that an electrical problem of some kind has occurred, either with the computer itself or with the electrical system in the room in which the computer is kept.</span></span>

<span data-ttu-id="b909e-163">Los administradores necesitan supervisar estos cambios en el estado de energía y recibir notificaciones de dichos cambios inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="b909e-163">Administrators need to monitor these changes in power status and be notified of such changes immediately.</span></span> <span data-ttu-id="b909e-164">Esto les permite tomar medidas antes de que el dispositivo pierda energía completamente.</span><span class="sxs-lookup"><span data-stu-id="b909e-164">This enables them to take action before the device loses power entirely.</span></span> <span data-ttu-id="b909e-165">(Por ejemplo, los sistemas de suministro de energía ininterrumpidos podrían ejecutarse durante solo 15 minutos o antes de cerrarse).</span><span class="sxs-lookup"><span data-stu-id="b909e-165">(Uninterruptible power supply systems, for example, might run for only 15 minutes or so before shutting down.)</span></span>

<span data-ttu-id="b909e-166">La clase **Win32 \_ PowerManagementEvent** se puede usar para supervisar los cambios de estado de energía en un equipo.</span><span class="sxs-lookup"><span data-stu-id="b909e-166">The **Win32\_PowerManagementEvent** class can be used to monitor changes in power status on a computer.</span></span> <span data-ttu-id="b909e-167">Estos cambios pueden incluir un cambio de una fuente de alimentación a otra, así como un cambio en el estado de la alimentación del equipo (por ejemplo, al entrar o salir del modo de suspensión).</span><span class="sxs-lookup"><span data-stu-id="b909e-167">These changes can include a switch from one power source to another as well as a change in computer power state (for example, entering or exiting Suspend mode).</span></span>

<span data-ttu-id="b909e-168">La **clase \_ PowerManagementEvent de Win32** solo tiene dos propiedades: EventType, que se usan para indicar el tipo de evento de cambio de energía que se ha producido, y OEMEventType, que usan algunos fabricantes de equipos originales para definir eventos de cambio de energía adicionales.</span><span class="sxs-lookup"><span data-stu-id="b909e-168">The **Win32\_PowerManagementEvent** class has only two properties: EventType, used to indicate the type of power change event that occurred, and OEMEventType, which is used by some original equipment manufacturers to define additional power change events.</span></span>

<span data-ttu-id="b909e-169">Para obtener más información sobre cómo responder a los eventos de energía de Windows, consulte el artículo [supervisión y respuesta a Windows Power Events con PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) en la sesión de ¡ Hola!</span><span class="sxs-lookup"><span data-stu-id="b909e-169">For more information on responding to Windows power events, see the [Monitor and Respond to Windows Power Events with PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) article on the Hey!</span></span> <span data-ttu-id="b909e-170">Scripting Guy!</span><span class="sxs-lookup"><span data-stu-id="b909e-170">Scripting Guy!</span></span> <span data-ttu-id="b909e-171">.</span><span class="sxs-lookup"><span data-stu-id="b909e-171">blog.</span></span>

## <a name="examples"></a><span data-ttu-id="b909e-172">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b909e-172">Examples</span></span>

<span data-ttu-id="b909e-173">El siguiente VBScript supervisa los cambios de estado de energía en un equipo.</span><span class="sxs-lookup"><span data-stu-id="b909e-173">The following VBScript monitors changes in power status on a computer.</span></span>


```VB
Set colMonitoredEvents = GetObject("winmgmts:")._
 ExecNotificationQuery("SELECT * FROM Win32_PowerManagementEvent")
Do
 Set strLatestEvent = colMonitoredEvents.NextEvent
 Wscript.Echo strLatestEvent.EventType
Loop
```



## <a name="requirements"></a><span data-ttu-id="b909e-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b909e-174">Requirements</span></span>



| <span data-ttu-id="b909e-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="b909e-175">Requirement</span></span> | <span data-ttu-id="b909e-176">Value</span><span class="sxs-lookup"><span data-stu-id="b909e-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b909e-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b909e-177">Minimum supported client</span></span><br/> | <span data-ttu-id="b909e-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b909e-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b909e-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b909e-179">Minimum supported server</span></span><br/> | <span data-ttu-id="b909e-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b909e-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b909e-181">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b909e-181">Namespace</span></span><br/>                | <span data-ttu-id="b909e-182">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b909e-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b909e-183">MOF</span><span class="sxs-lookup"><span data-stu-id="b909e-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b909e-184"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b909e-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b909e-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b909e-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b909e-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b909e-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b909e-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="b909e-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b909e-188">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="b909e-188">**\_\_ExtrinsicEvent**</span></span>](../wmisdk/--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="b909e-189">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="b909e-189">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

<span data-ttu-id="b909e-190">[Supervisión de los cambios en el estado de energía del equipo](/previous-versions/tn-archive/ee176537(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="b909e-190">[Monitoring Changes in Computer Power Status](/previous-versions/tn-archive/ee176537(v=technet.10))</span></span>
</dt> </dl>

 

 
