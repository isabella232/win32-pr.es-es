---
description: WMI asigna automáticamente capturas de SNMP a eventos de WMI. El sistema coloca los datos contenidos en la captura en las propiedades correspondientes de una instancia de evento WMI para el acceso por parte del equipo host WMI.
ms.assetid: 549f58a9-9d3b-41b9-a374-ab83877f63a7
ms.tgt_platform: multiple
title: Recepción de capturas de SNMP como eventos WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da24be8ea9a4882af0b961b1d0f6f0c3d442c70c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544702"
---
# <a name="receiving-snmp-traps-as-wmi-events"></a><span data-ttu-id="e3038-104">Recepción de capturas de SNMP como eventos WMI</span><span class="sxs-lookup"><span data-stu-id="e3038-104">Receiving SNMP Traps as WMI Events</span></span>

<span data-ttu-id="e3038-105">WMI asigna automáticamente capturas de SNMP a eventos de WMI.</span><span class="sxs-lookup"><span data-stu-id="e3038-105">WMI automatically maps SNMP traps to WMI events.</span></span> <span data-ttu-id="e3038-106">El sistema coloca los datos contenidos en la captura en las propiedades correspondientes de una instancia de evento WMI para el acceso por parte del equipo host WMI.</span><span class="sxs-lookup"><span data-stu-id="e3038-106">The system places the data contained in the trap in the corresponding properties of a WMI event instance for access by the WMI host machine.</span></span>

> [!Note]  
> <span data-ttu-id="e3038-107">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="e3038-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="e3038-108">Recibir una captura SNMP es casi idéntico a recibir eventos de cualquier otro proveedor WMI.</span><span class="sxs-lookup"><span data-stu-id="e3038-108">Receiving an SNMP trap is nearly identical to receiving events from any other WMI provider.</span></span> <span data-ttu-id="e3038-109">Sin embargo, el filtro de eventos SNMP tiene varias clases únicas que se deben tener en cuenta antes de registrarse para los eventos.</span><span class="sxs-lookup"><span data-stu-id="e3038-109">However, the SNMP event filter has several unique classes to be aware of before registering for events.</span></span> <span data-ttu-id="e3038-110">Además, el proveedor de eventos requiere el uso del \\ espacio de nombres Smir exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="e3038-110">Also, the event provider requires the use of the \\smir namespace exclusively.</span></span>

<span data-ttu-id="e3038-111">Las clases más comunes con las que registrarse son [SnmpNotification](snmpnotification.md) y [SnmpExtendedNotification](snmpextendednotification.md).</span><span class="sxs-lookup"><span data-stu-id="e3038-111">The most common classes to register with are [SnmpNotification](snmpnotification.md) and [SnmpExtendedNotification](snmpextendednotification.md).</span></span> <span data-ttu-id="e3038-112">Los consumidores que intentan usar notificaciones de eventos para actualizar valores en dispositivos SNMP supervisados deben registrarse para los eventos SnmpExtendedNotification.</span><span class="sxs-lookup"><span data-stu-id="e3038-112">Consumers intent on using event notifications to update values in monitored SNMP devices must register for SnmpExtendedNotification events.</span></span> <span data-ttu-id="e3038-113">La información de los eventos SnmpNotification no se puede volver a usar.</span><span class="sxs-lookup"><span data-stu-id="e3038-113">The information from SnmpNotification events is not reusable.</span></span>

<span data-ttu-id="e3038-114">En la tabla siguiente se muestra información acerca de cómo configurar el equipo para recibir capturas SNMP como eventos WMI.</span><span class="sxs-lookup"><span data-stu-id="e3038-114">The following table lists information about setting up your computer to receive SNMP traps as WMI events.</span></span>



| <span data-ttu-id="e3038-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="e3038-115">Task</span></span>                                                                               | <span data-ttu-id="e3038-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3038-116">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3038-117">Elección entre proveedores de eventos SNMP</span><span class="sxs-lookup"><span data-stu-id="e3038-117">Choosing Between SNMP Event Providers</span></span>](choosing-between-snmp-event-providers.md) | <span data-ttu-id="e3038-118">WMI incluye dos proveedores de eventos SNMP.</span><span class="sxs-lookup"><span data-stu-id="e3038-118">WMI includes two SNMP event providers.</span></span>                                             |
| [<span data-ttu-id="e3038-119">Recibir eventos SNMP</span><span class="sxs-lookup"><span data-stu-id="e3038-119">Receiving SNMP Events</span></span>](receiving-snmp-events.md)                                 | <span data-ttu-id="e3038-120">Los proveedores de eventos SNMP admiten tres tipos de capturas de SNMPv1 y notificaciones de SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="e3038-120">SNMP event providers support three types of SNMPv1 traps and SNMPv2 notifications.</span></span> |



 

<span data-ttu-id="e3038-121">En el ejemplo siguiente se configura un equipo para supervisar el evento **SnmpLinkUpNotification** desde un concentrador administrado.</span><span class="sxs-lookup"><span data-stu-id="e3038-121">The following example sets up a computer to monitor for the **SnmpLinkUpNotification** event from a managed hub.</span></span>


```VB
Set objLocator = CreateObject("wbemscripting.swbemlocator")
Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")

set objwbemEventsource = _ 
    objServices.ExecNotificationQuery _
   ("SELECT * FROM SnmpLinkUpNotification")

set objWbemObject = objwbemEventsource.NextEvent()

wscript.echo "Received " & objWbemObject.path_.class

for each prop in objWbemObject.properties_
    wscript.echo prop.name & " -- " & prop.value
next
```



 

 



