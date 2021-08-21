---
title: Administración de capturas y notificaciones
description: La aplicación WinSNMP debe registrarse para recibir capturas y notificaciones llamando a la función SnmpRegister con SNMPAPI \_ ON. La aplicación puede anular el registro y deshabilitar las capturas y las notificaciones llamando a la función con SNMPAPI \_ OFF.
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402a768aa28efb6f2fdc18994d749cfca2f2c412f748f853fb76fcd7fe3e41d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009383"
---
# <a name="managing-traps-and-notifications"></a>Administración de capturas y notificaciones

La aplicación WinSNMP debe registrarse para recibir capturas y notificaciones llamando a la [**función SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) con SNMPAPI \_ ON. La aplicación puede anular el registro y deshabilitar las capturas y las notificaciones llamando a la función con SNMPAPI \_ OFF.

Hay varias opciones disponibles cuando la aplicación llama **a SnmpRegister**. La aplicación puede registrar o anular el registro de las siguientes capturas y notificaciones:

-   Un tipo de captura o notificación
-   Todas las capturas y notificaciones
-   Todos los orígenes de solicitudes de captura y notificación
-   Capturas y notificaciones de todas las entidades de administración
-   Capturas y notificaciones para cada contexto

Para registrar y recibir un tipo de captura o notificación predefinido, la aplicación debe definir un identificador de objeto (una estructura [**smiOID)**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) para cada tipo predefinido. La estructura debe contener una secuencia de coincidencia de patrones para el tipo de captura o notificación. RFC 1907, "Management Information Base for Version 2 of the Simple Network Management Protocol (SNMPv2)", define identificadores de objetos de captura y notificación.

Para recuperar las notificaciones y los datos de captura pendientes de una sesión de WinSNMP, una aplicación WinSNMP debe llamar a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) con el identificador de sesión devuelto por la [**función SnmpCreateSession.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)

Para obtener más información, vea [Envío de mensajes SNMP](sending-snmp-messages.md) y Recepción de mensajes [SNMP.](receiving-snmp-messages.md) Para obtener información adicional sobre la asignación y desasignación de recursos para capturas y notificaciones, vea [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).

 

 




