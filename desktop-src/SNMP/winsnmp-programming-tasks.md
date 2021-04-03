---
title: Tareas de programación WinSNMP
description: En la tabla siguiente se resumen los procedimientos de programación básicos que debe realizar para codificar una aplicación WinSNMP y los temas que proporcionan información acerca de estas tareas.
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75fa8d2ad223fbd8f71eff78c7cd232ddc492a9
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "103904391"
---
# <a name="winsnmp-programming-tasks"></a>Tareas de programación WinSNMP

En la tabla siguiente se resumen los procedimientos de programación básicos que debe realizar para codificar una aplicación WinSNMP y los temas que proporcionan información acerca de estas tareas.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tarea de programación</th>
<th>Temas y funciones relacionadas con tareas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Abra la aplicación WinSNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-application.md">abrir y cerrar una aplicación WinSNMP</a>.<br/></td>
</tr>
<tr class="even">
<td>Abra una o más sesiones de WinSNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-session.md">abrir y cerrar una sesión WinSNMP</a>.<br/></td>
</tr>
<tr class="odd">
<td>Regístrese para recibir capturas o notificaciones.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>. Consulte <a href="managing-traps-and-notifications.md">Administración de capturas y notificaciones</a>.<br/></td>
</tr>
<tr class="even">
<td>Cree una o varias listas de enlaces variables para incorporarlas en una PDU.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>. Vea <a href="working-with-variable-binding-lists.md">trabajar con listas de enlaces variables</a>.<br/>
<blockquote>
[!Note]<br />
Es posible que la aplicación necesite llamar a otras <a href="winsnmp-functions.md">funciones de enlace de variables</a> para crear la lista de enlaces de variables.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Cree una o varias PDU para la transmisión y el procesamiento.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>. Consulte <a href="working-with-protocol-data-units.md">trabajar con unidades de datos de protocolo</a>.<br/>
<blockquote>
[!Note]<br />
Es posible que la aplicación necesite llamar a otras <a href="winsnmp-functions.md">funciones de PDU</a> y a <a href="winsnmp-functions.md">las funciones</a> de la utilidad WINSNMP para crear la PDU.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Envíe una o más solicitudes de operación SNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>. Consulte <a href="sending-snmp-messages.md">envío de mensajes SNMP</a>.<br/></td>
</tr>
<tr class="odd">
<td>Recupere la respuesta a la solicitud de operación SNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>. Vea <a href="receiving-snmp-messages.md">recibir mensajes SNMP</a>.<br/></td>
</tr>
<tr class="even">
<td>Procesa la respuesta de la solicitud.</td>
<td>Usar lógica específica de la aplicación.</td>
</tr>
<tr class="odd">
<td>Cierre cada sesión de WinSNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-session.md">abrir y cerrar una sesión WinSNMP</a>.<br/></td>
</tr>
<tr class="even">
<td>Cierre la aplicación WinSNMP.</td>
<td>Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>. Consulte <a href="opening-and-closing-a-winsnmp-application.md">abrir y cerrar una aplicación WinSNMP</a>.<br/></td>
</tr>
</tbody>
</table>



 

Los temas siguientes contienen información adicional sobre otros conceptos de programación generales específicos del entorno de WinSNMP.



|                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tareas de programación generales](general-winsnmp-programming-tasks.md) | [Administrar identificadores de objeto](managing-object-identifiers.md)[liberación de descriptores WinSNMP](freeing-winsnmp-descriptors.md)<br/> [Establecer el modo de traducción de entidad y contexto](setting-the-entity-and-context-translation-mode.md)<br/> [Administrar la Directiva de retransmisión](managing-the-retransmission-policy.md)<br/> [Escribir aplicaciones WinSNMP con varios subprocesos](writing-winsnmp-applications-with-multiple-threads.md)<br/> [Registro de una aplicación de agente SNMP](registering-an-snmp-agent-application.md)<br/> |



 

Además, la aplicación WinSNMP puede necesitar incorporar llamadas a las funciones WinSNMP siguientes: [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)y [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu). Esto permite que la implementación de Microsoft WinSNMP libere objetos de memoria WinSNMP. Como norma general, la aplicación WinSNMP debe liberar todos los recursos asignados como resultado de una llamada a una función WinSNMP. Para obtener más información acerca de la desasignación de recursos, consulte [asignación de objetos de memoria WinSNMP](allocating-winsnmp-memory-objects.md).

 

 





