---
title: Tareas de programación de WinSNMP
description: En la tabla siguiente se resumen los procedimientos de programación básicos que debe realizar para codificar una aplicación WinSNMP y los temas que proporcionan información sobre estas tareas.
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7543a0fef8fff3f2ef1672ee29d72b0f82b75af7
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436630"
---
# <a name="winsnmp-programming-tasks"></a>Tareas de programación de WinSNMP

En la tabla siguiente se resumen los procedimientos de programación básicos que debe realizar para codificar una aplicación WinSNMP y los temas que proporcionan información sobre estas tareas.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tarea de programación</th>
<th>Temas y funciones relacionados con tareas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Abra la aplicación WinSNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-application.md">Apertura y cierre de una aplicación WinSNMP.</a><br/></td>
</tr>
<tr class="even">
<td>Abra una o varias sesiones de WinSNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-session.md">Apertura y cierre de una sesión winSNMP.</a><br/></td>
</tr>
<tr class="odd">
<td>Regístrese para recibir capturas o notificaciones.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>. Consulte <a href="managing-traps-and-notifications.md">Administración de capturas y notificaciones.</a><br/></td>
</tr>
<tr class="even">
<td>Cree una o varias listas de enlaces de variables para la incorporación en una PDU.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>. Vea <a href="working-with-variable-binding-lists.md">Trabajar con listas de enlaces de variables</a>.<br/>
<blockquote>
[!Note]<br />
Es posible que la aplicación tenga que llamar a otras <a href="winsnmp-functions.md">funciones de enlace de variables</a> para crear la lista de enlaces de variables.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Cree uno o varios PDU para la transmisión y el procesamiento.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU,</strong></a> <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData,</strong></a> <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>. Vea <a href="working-with-protocol-data-units.md">Trabajar con unidades de datos de protocolo.</a><br/>
<blockquote>
[!Note]<br />
Es posible que la aplicación tenga que llamar a otras <a href="winsnmp-functions.md">funciones de PDU y</a> funciones de utilidad WinSNMP para crear la PDU. <a href="winsnmp-functions.md"></a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Envíe una o varias solicitudes de operación SNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg.</strong></a> Consulte <a href="sending-snmp-messages.md">Envío de mensajes SNMP.</a><br/></td>
</tr>
<tr class="odd">
<td>Recupere la respuesta a la solicitud de operación SNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg.</strong></a> Consulte <a href="receiving-snmp-messages.md">Recepción de mensajes SNMP.</a><br/></td>
</tr>
<tr class="even">
<td>Procese la respuesta de la solicitud.</td>
<td>Use lógica específica de la aplicación.</td>
</tr>
<tr class="odd">
<td>Cierre cada sesión de WinSNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-session.md">Apertura y cierre de una sesión winSNMP.</a><br/></td>
</tr>
<tr class="even">
<td>Cierre la aplicación WinSNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup.</strong></a> Consulte <a href="opening-and-closing-a-winsnmp-application.md">Apertura y cierre de una aplicación WinSNMP.</a><br/></td>
</tr>
</tbody>
</table>



 

Los temas siguientes contienen información adicional sobre otros conceptos generales de programación específicos del entorno winSNMP.



| Tema                                                              | Conceptos                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tareas generales de programación](general-winsnmp-programming-tasks.md) | [Administrar identificadores de objeto](managing-object-identifiers.md)[que liberan descriptores winSNMP](freeing-winsnmp-descriptors.md)<br/> [Establecimiento del modo de traducción de entidades y contexto](setting-the-entity-and-context-translation-mode.md)<br/> [Administración de la directiva de retransmisión](managing-the-retransmission-policy.md)<br/> [Escritura de aplicaciones WinSNMP con varios subprocesos](writing-winsnmp-applications-with-multiple-threads.md)<br/> [Registro de una aplicación del agente SNMP](registering-an-snmp-agent-application.md)<br/> |



 

Además, es posible que la aplicación WinSNMP tenga que incorporar llamadas a las siguientes funciones de WinSNMP: [**SnmpFreeVbl,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) [**SnmpFreeEntity,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity) [**SnmpFreeDescriptor,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)y [**SnmpFreePdu.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) Esto permite a la implementación de Microsoft WinSNMP liberar objetos de memoria winSNMP. Como regla general, la aplicación WinSNMP debe liberar todos los recursos asignados como resultado de una llamada a una función WinSNMP. Para obtener más información sobre la desasignación de recursos, vea [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).

 

 





