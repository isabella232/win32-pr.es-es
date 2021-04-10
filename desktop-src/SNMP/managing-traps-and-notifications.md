---
title: Administración de capturas y notificaciones
description: La aplicación WinSNMP debe registrarse para recibir capturas y notificaciones mediante una llamada a la función SnmpRegister con SNMPAPI \_ en. La aplicación puede anular el registro y deshabilitar las capturas y notificaciones mediante una llamada a la función con SNMPAPI \_ OFF.
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e3a2d9fed1f7c34dd8191550d1dbc68ed984e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903718"
---
# <a name="managing-traps-and-notifications"></a>Administración de capturas y notificaciones

La aplicación WinSNMP debe registrarse para recibir capturas y notificaciones mediante una llamada a la función [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) con snmpapi \_ en. La aplicación puede anular el registro y deshabilitar las capturas y notificaciones mediante una llamada a la función con SNMPAPI \_ OFF.

Hay varias opciones disponibles cuando la aplicación llama a **SnmpRegister**. La aplicación se puede registrar o anular el registro para las siguientes capturas y notificaciones:

-   Un tipo de captura o notificación
-   Todas las capturas y notificaciones
-   Todos los orígenes de solicitudes de captura y notificación
-   Capturas y notificaciones de todas las entidades de administración
-   Capturas y notificaciones para todos los contextos

Para registrar y recibir un tipo de notificación o de captura predefinido, la aplicación debe definir un identificador de objeto (una estructura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ) para cada tipo predefinido. La estructura debe contener una secuencia de coincidencia de patrones para el tipo de captura o notificación. RFC 1907, "base de información de administración para la versión 2 del Protocolo simple de administración de redes (SNMPv2)", define los identificadores de objetos de captura y notificación.

Para recuperar los datos de captura pendientes y las notificaciones de una sesión WinSNMP, una aplicación WinSNMP debe llamar a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) con el identificador de sesión devuelto por la función [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) .

Para obtener más información, consulte [envío de mensajes SNMP](sending-snmp-messages.md) y [recepción de mensajes SNMP](receiving-snmp-messages.md). Para obtener información adicional acerca de la asignación y desasignación de recursos para capturas y notificaciones, consulte [asignación de objetos de memoria WinSNMP](allocating-winsnmp-memory-objects.md).

 

 




