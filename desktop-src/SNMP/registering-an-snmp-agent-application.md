---
title: Registro de una aplicación de agente SNMP
description: Además de las operaciones del administrador SNMP, la versión de API WinSNMP 2,0 también admite operaciones del agente SNMP.
ms.assetid: 473560b5-4611-410e-aeae-764c9c76e765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40922469c52e33e4b5c2f408c1c107b6784529f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994403"
---
# <a name="registering-an-snmp-agent-application"></a>Registro de una aplicación de agente SNMP

Además de las operaciones del administrador SNMP, la versión de API WinSNMP 2,0 también admite operaciones del agente SNMP.

Para registrar una aplicación WinSNMP como agente SNMP, la aplicación puede llamar a la función [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) . Esta función informa a la implementación de Microsoft WinSNMP de que una entidad SNMP actuará en el rol de un agente SNMP. La aplicación también puede llamar a **SnmpListen** para informar a la implementación cuando dejará de actuar como agente.

Si una aplicación llama a la función [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) y pasa el valor snmpapi en \_ el parámetro *lStatus* , se producen las siguientes acciones:

1.  La entidad que funcionará en un rol de agente SNMP se enlaza a su puerto asignado y "escucha" para las solicitudes de mensajes SNMP entrantes.
2.  El agente utiliza la lógica específica de la aplicación para procesar cada solicitud SNMP.
3.  El agente forma las respuestas adecuadas a cada solicitud.
4.  El agente transmite la respuesta a la entidad que realiza la solicitud mediante una llamada a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) . Cuando el agente llama a **SnmpSendMsg**, especifica la dirección del agente en el parámetro *srcEntity* y la dirección de la entidad del administrador remoto en el parámetro *dstEntity* . (Estos valores son los valores inversos de la entidad agente recibida en estos parámetros cuando llamó a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para recuperar una solicitud SNMP).

Para obtener más información acerca de las aplicaciones de administración de SNMP y del agente, consulte [About SNMP](about-snmp.md).

 

 




