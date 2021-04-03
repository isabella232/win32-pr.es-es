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
# <a name="winsnmp-programming-tasks"></a><span data-ttu-id="de534-103">Tareas de programación WinSNMP</span><span class="sxs-lookup"><span data-stu-id="de534-103">WinSNMP Programming Tasks</span></span>

<span data-ttu-id="de534-104">En la tabla siguiente se resumen los procedimientos de programación básicos que debe realizar para codificar una aplicación WinSNMP y los temas que proporcionan información acerca de estas tareas.</span><span class="sxs-lookup"><span data-stu-id="de534-104">The following table summarizes the basic programming procedures that you must perform to code a WinSNMP application, and the topics that provide information about these tasks.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de534-105">Tarea de programación</span><span class="sxs-lookup"><span data-stu-id="de534-105">Programming task</span></span></th>
<th><span data-ttu-id="de534-106">Temas y funciones relacionadas con tareas</span><span class="sxs-lookup"><span data-stu-id="de534-106">Task-related function and topics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="de534-107">Abra la aplicación WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="de534-107">Open the WinSNMP application.</span></span></td>
<td><span data-ttu-id="de534-108">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de534-108">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>.</span></span> <span data-ttu-id="de534-109">Consulte <a href="opening-and-closing-a-winsnmp-application.md">abrir y cerrar una aplicación WinSNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="de534-109">See <a href="opening-and-closing-a-winsnmp-application.md">Opening and Closing a WinSNMP Application</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de534-110">Abra una o más sesiones de WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="de534-110">Open one or more WinSNMP sessions.</span></span></td>
<td><span data-ttu-id="de534-111">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de534-111">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>.</span></span> <span data-ttu-id="de534-112">Consulte <a href="opening-and-closing-a-winsnmp-session.md">abrir y cerrar una sesión WinSNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="de534-112">See <a href="opening-and-closing-a-winsnmp-session.md">Opening and Closing a WinSNMP Session</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de534-113">Regístrese para recibir capturas o notificaciones.</span><span class="sxs-lookup"><span data-stu-id="de534-113">Register to receive traps or notifications.</span></span></td>
<td><span data-ttu-id="de534-114">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de534-114">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>.</span></span> <span data-ttu-id="de534-115">Consulte <a href="managing-traps-and-notifications.md">Administración de capturas y notificaciones</a>.</span><span class="sxs-lookup"><span data-stu-id="de534-115">See <a href="managing-traps-and-notifications.md">Managing Traps and Notifications</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de534-116">Cree una o varias listas de enlaces variables para incorporarlas en una PDU.</span><span class="sxs-lookup"><span data-stu-id="de534-116">Create one or more variable binding lists for incorporation in a PDU.</span></span></td>
<td><span data-ttu-id="de534-117">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de534-117">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>.</span></span> <span data-ttu-id="de534-118">Vea <a href="working-with-variable-binding-lists.md">trabajar con listas de enlaces variables</a>.</span><span class="sxs-lookup"><span data-stu-id="de534-118">See <a href="working-with-variable-binding-lists.md">Working with Variable Binding Lists</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de534-119">Es posible que la aplicación necesite llamar a otras <a href="winsnmp-functions.md">funciones de enlace de variables</a> para crear la lista de enlaces de variables.</span><span class="sxs-lookup"><span data-stu-id="de534-119">The application may need to call other <a href="winsnmp-functions.md">variable binding functions</a> to create the variable binding list.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de534-120">Cree una o varias PDU para la transmisión y el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="de534-120">Create one or more PDUs for transmission and processing.</span></span></td>
<td><span data-ttu-id="de534-121">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de534-121">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>.</span></span> <span data-ttu-id="de534-122">Consulte <a href="working-with-protocol-data-units.md">trabajar con unidades de datos de protocolo</a>.</span><span class="sxs-lookup"><span data-stu-id="de534-122">See <a href="working-with-protocol-data-units.md">Working with Protocol Data Units</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="de534-123">Es posible que la aplicación necesite llamar a otras <a href="winsnmp-functions.md">funciones de PDU</a> y a <a href="winsnmp-functions.md">las funciones</a> de la utilidad WINSNMP para crear la PDU.</span><span class="sxs-lookup"><span data-stu-id="de534-123">The application may need to call other <a href="winsnmp-functions.md">PDU functions</a> and WinSNMP <a href="winsnmp-functions.md">utility functions</a> to create the PDU.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de534-124">Envíe una o más solicitudes de operación SNMP.</span><span class="sxs-lookup"><span data-stu-id="de534-124">Submit one or more SNMP operation requests.</span></span></td>
<td><span data-ttu-id="de534-125">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de534-125">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>.</span></span> <span data-ttu-id="de534-126">Consulte <a href="sending-snmp-messages.md">envío de mensajes SNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="de534-126">See <a href="sending-snmp-messages.md">Sending SNMP Messages</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de534-127">Recupere la respuesta a la solicitud de operación SNMP.</span><span class="sxs-lookup"><span data-stu-id="de534-127">Retrieve the response to the SNMP operation request.</span></span></td>
<td><span data-ttu-id="de534-128">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de534-128">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>.</span></span> <span data-ttu-id="de534-129">Vea <a href="receiving-snmp-messages.md">recibir mensajes SNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="de534-129">See <a href="receiving-snmp-messages.md">Receiving SNMP Messages</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de534-130">Procesa la respuesta de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="de534-130">Process the request response.</span></span></td>
<td><span data-ttu-id="de534-131">Usar lógica específica de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="de534-131">Use application-specific logic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de534-132">Cierre cada sesión de WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="de534-132">Close each WinSNMP session.</span></span></td>
<td><span data-ttu-id="de534-133">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de534-133">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>.</span></span> <span data-ttu-id="de534-134">Consulte <a href="opening-and-closing-a-winsnmp-session.md">abrir y cerrar una sesión WinSNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="de534-134">See <a href="opening-and-closing-a-winsnmp-session.md">Opening and Closing a WinSNMP Session</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de534-135">Cierre la aplicación WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="de534-135">Close the WinSNMP application.</span></span></td>
<td><span data-ttu-id="de534-136">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="de534-136">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>.</span></span> <span data-ttu-id="de534-137">Consulte <a href="opening-and-closing-a-winsnmp-application.md">abrir y cerrar una aplicación WinSNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="de534-137">See <a href="opening-and-closing-a-winsnmp-application.md">Opening and Closing a WinSNMP Application</a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="de534-138">Los temas siguientes contienen información adicional sobre otros conceptos de programación generales específicos del entorno de WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="de534-138">The following topics contain additional information about other general programming concepts specific to the WinSNMP environment.</span></span>



|                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de534-139">Tareas de programación generales</span><span class="sxs-lookup"><span data-stu-id="de534-139">General programming tasks</span></span>](general-winsnmp-programming-tasks.md) | <span data-ttu-id="de534-140">[Administrar identificadores de objeto](managing-object-identifiers.md)[liberación de descriptores WinSNMP](freeing-winsnmp-descriptors.md)</span><span class="sxs-lookup"><span data-stu-id="de534-140">[Managing Object Identifiers](managing-object-identifiers.md)[Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md)</span></span><br/> [<span data-ttu-id="de534-141">Establecer el modo de traducción de entidad y contexto</span><span class="sxs-lookup"><span data-stu-id="de534-141">Setting the Entity and Context Translation Mode</span></span>](setting-the-entity-and-context-translation-mode.md)<br/> [<span data-ttu-id="de534-142">Administrar la Directiva de retransmisión</span><span class="sxs-lookup"><span data-stu-id="de534-142">Managing the Retransmission Policy</span></span>](managing-the-retransmission-policy.md)<br/> [<span data-ttu-id="de534-143">Escribir aplicaciones WinSNMP con varios subprocesos</span><span class="sxs-lookup"><span data-stu-id="de534-143">Writing WinSNMP Applications with Multiple Threads</span></span>](writing-winsnmp-applications-with-multiple-threads.md)<br/> [<span data-ttu-id="de534-144">Registro de una aplicación de agente SNMP</span><span class="sxs-lookup"><span data-stu-id="de534-144">Registering an SNMP Agent Application</span></span>](registering-an-snmp-agent-application.md)<br/> |



 

<span data-ttu-id="de534-145">Además, la aplicación WinSNMP puede necesitar incorporar llamadas a las funciones WinSNMP siguientes: [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)y [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu).</span><span class="sxs-lookup"><span data-stu-id="de534-145">In addition, the WinSNMP application may need to incorporate calls to the following WinSNMP functions: [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext), and [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu).</span></span> <span data-ttu-id="de534-146">Esto permite que la implementación de Microsoft WinSNMP libere objetos de memoria WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="de534-146">This enables the Microsoft WinSNMP implementation to free WinSNMP memory objects.</span></span> <span data-ttu-id="de534-147">Como norma general, la aplicación WinSNMP debe liberar todos los recursos asignados como resultado de una llamada a una función WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="de534-147">As a general rule, the WinSNMP application should free all resources allocated as the result of a call to a WinSNMP function.</span></span> <span data-ttu-id="de534-148">Para obtener más información acerca de la desasignación de recursos, consulte [asignación de objetos de memoria WinSNMP](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="de534-148">For additional information about deallocating resources, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 





