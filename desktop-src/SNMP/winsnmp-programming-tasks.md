---
title: Tareas de programación de WinSNMP
description: En la tabla siguiente se resumen los procedimientos de programación básicos que debe realizar para codificar una aplicación WinSNMP y los temas que proporcionan información sobre estas tareas.
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb83d6d61311866ddb84d3980f5742f82f51405
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479401"
---
# <a name="winsnmp-programming-tasks"></a>Tareas de programación de WinSNMP

En la tabla siguiente se resumen los procedimientos de programación básicos que debe realizar para codificar una aplicación WinSNMP y los temas que proporcionan información sobre estas tareas.




| Tarea de programación | Temas y funciones relacionados con tareas | 
|------------------|----------------------------------|
| Abra la aplicación WinSNMP. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-application.md">Apertura y cierre de una aplicación WinSNMP.</a><br /> | 
| Abra una o varias sesiones de WinSNMP. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-session.md">Apertura y cierre de una sesión winSNMP.</a><br /> | 
| Regístrese para recibir capturas o notificaciones. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>. Consulte <a href="managing-traps-and-notifications.md">Administración de capturas y notificaciones.</a><br /> | 
| Cree una o varias listas de enlaces de variables para la incorporación en una PDU. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>. Vea <a href="working-with-variable-binding-lists.md">Trabajar con listas de enlaces de variables.</a><br /><blockquote>[!Note]<br />Es posible que la aplicación tenga que llamar a otras <a href="winsnmp-functions.md">funciones de enlace de variables</a> para crear la lista de enlaces de variables.</blockquote><br /> | 
| Cree uno o varios PDU para la transmisión y el procesamiento. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>. Consulte <a href="working-with-protocol-data-units.md">Trabajar con unidades de datos de protocolo.</a><br /><blockquote>[!Note]<br />Es posible que la aplicación tenga que llamar a otras <a href="winsnmp-functions.md">funciones PDU y</a> funciones de utilidad WinSNMP <a href="winsnmp-functions.md"></a> para crear la PDU.</blockquote><br /> | 
| Envíe una o varias solicitudes de operación SNMP. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg.</strong></a> Consulte <a href="sending-snmp-messages.md">Envío de mensajes SNMP.</a><br /> | 
| Recupere la respuesta a la solicitud de operación SNMP. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg.</strong></a> Consulte <a href="receiving-snmp-messages.md">Recepción de mensajes SNMP.</a><br /> | 
| Procese la respuesta de la solicitud. | Use lógica específica de la aplicación. | 
| Cierre cada sesión de WinSNMP. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-session.md">Apertura y cierre de una sesión winSNMP.</a><br /> | 
| Cierre la aplicación WinSNMP. | Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-application.md">Apertura y cierre de una aplicación WinSNMP.</a><br /> | 




 

Los temas siguientes contienen información adicional sobre otros conceptos generales de programación específicos del entorno winSNMP.



| Tema                                                              | Conceptos                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tareas generales de programación](general-winsnmp-programming-tasks.md) | [Administrar identificadores de objeto](managing-object-identifiers.md)[que liberan descriptores winSNMP](freeing-winsnmp-descriptors.md)<br/> [Establecer el modo de traducción de entidades y contexto](setting-the-entity-and-context-translation-mode.md)<br/> [Administración de la directiva de retransmisión](managing-the-retransmission-policy.md)<br/> [Escritura de aplicaciones WinSNMP con varios subprocesos](writing-winsnmp-applications-with-multiple-threads.md)<br/> [Registro de una aplicación de agente SNMP](registering-an-snmp-agent-application.md)<br/> |



 

Además, es posible que la aplicación WinSNMP tenga que incorporar llamadas a las siguientes funciones winSNMP: [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity) [**SnmpFreeDescriptor,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)y [**SnmpFreePdu.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) Esto permite a la implementación de Microsoft WinSNMP liberar objetos de memoria winSNMP. Como regla general, la aplicación WinSNMP debe liberar todos los recursos asignados como resultado de una llamada a una función WinSNMP. Para obtener más información sobre la desasignación de recursos, vea [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).

 

 





