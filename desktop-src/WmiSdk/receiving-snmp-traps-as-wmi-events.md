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
# <a name="receiving-snmp-traps-as-wmi-events"></a>Recepción de capturas de SNMP como eventos WMI

WMI asigna automáticamente capturas de SNMP a eventos de WMI. El sistema coloca los datos contenidos en la captura en las propiedades correspondientes de una instancia de evento WMI para el acceso por parte del equipo host WMI.

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Recibir una captura SNMP es casi idéntico a recibir eventos de cualquier otro proveedor WMI. Sin embargo, el filtro de eventos SNMP tiene varias clases únicas que se deben tener en cuenta antes de registrarse para los eventos. Además, el proveedor de eventos requiere el uso del \\ espacio de nombres Smir exclusivamente.

Las clases más comunes con las que registrarse son [SnmpNotification](snmpnotification.md) y [SnmpExtendedNotification](snmpextendednotification.md). Los consumidores que intentan usar notificaciones de eventos para actualizar valores en dispositivos SNMP supervisados deben registrarse para los eventos SnmpExtendedNotification. La información de los eventos SnmpNotification no se puede volver a usar.

En la tabla siguiente se muestra información acerca de cómo configurar el equipo para recibir capturas SNMP como eventos WMI.



| Tarea                                                                               | Descripción                                                                        |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Elección entre proveedores de eventos SNMP](choosing-between-snmp-event-providers.md) | WMI incluye dos proveedores de eventos SNMP.                                             |
| [Recibir eventos SNMP](receiving-snmp-events.md)                                 | Los proveedores de eventos SNMP admiten tres tipos de capturas de SNMPv1 y notificaciones de SNMPv2. |



 

En el ejemplo siguiente se configura un equipo para supervisar el evento **SnmpLinkUpNotification** desde un concentrador administrado.


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



 

 



