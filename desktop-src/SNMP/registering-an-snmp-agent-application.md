---
title: Registro de una aplicación del agente SNMP
description: Además de las operaciones del administrador de SNMP, la API de WinSNMP versión 2.0 también admite operaciones de agente SNMP.
ms.assetid: 473560b5-4611-410e-aeae-764c9c76e765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3415e511639c7cbbc18455ed93be74e11414c1f442797c8b72f7456092757c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009133"
---
# <a name="registering-an-snmp-agent-application"></a>Registro de una aplicación del agente SNMP

Además de las operaciones del administrador de SNMP, la API de WinSNMP versión 2.0 también admite operaciones de agente SNMP.

Para registrar una aplicación WinSNMP como agente SNMP, la aplicación puede llamar a la [**función SnmpListen.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) Esta función informa a la implementación de Microsoft WinSNMP de que una entidad SNMP actuará en el rol de un agente SNMP. La aplicación también puede llamar **a SnmpListen** para informar a la implementación cuando ya no actuará como agente.

Si una aplicación llama a [**la función SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) y pasa el valor SNMPAPI ON en el parámetro \_ *lStatus,* se producen las siguientes acciones:

1.  La entidad que va a funcionar en un rol de agente SNMP se enlaza a su puerto asignado y "escucha" las solicitudes entrantes de mensajes SNMP.
2.  El agente usa lógica específica de la aplicación para procesar cada solicitud SNMP.
3.  El agente forma las respuestas adecuadas a cada solicitud.
4.  El agente transmite la respuesta a la entidad solicitante llamando a la [**función SnmpSendMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) Cuando el agente llama a **SnmpSendMsg,** especifica la dirección del agente en el parámetro *srcEntity* y la dirección de la entidad de administrador remoto en el parámetro *dstEntity.* (Estos valores son el inverso de los valores que la entidad del agente recibió en estos parámetros cuando llamó a la [**función SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para recuperar una solicitud SNMP).

Para obtener más información sobre las aplicaciones de administración SNMP y las aplicaciones de agente, vea [Acerca de SNMP.](about-snmp.md)

 

 




