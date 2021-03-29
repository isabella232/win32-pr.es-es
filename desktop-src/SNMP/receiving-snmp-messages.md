---
title: Recepción de mensajes SNMP
description: La aplicación WinSNMP debe llamar a la función SnmpRecvMsg para recuperar la respuesta a una solicitud SnmpSendMsg.
ms.assetid: 323a5565-a8a5-4efd-aa4e-e4623b581d09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529420deaf637cec8598a8e8becc87ab514b40b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778600"
---
# <a name="receiving-snmp-messages"></a><span data-ttu-id="7366e-103">Recepción de mensajes SNMP</span><span class="sxs-lookup"><span data-stu-id="7366e-103">Receiving SNMP Messages</span></span>

<span data-ttu-id="7366e-104">La aplicación WinSNMP debe llamar a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para recuperar la respuesta a una solicitud [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .</span><span class="sxs-lookup"><span data-stu-id="7366e-104">The WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve the response to an [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) request.</span></span>

<span data-ttu-id="7366e-105">La función [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) pasa un identificador de ventana de la aplicación y un identificador de mensaje de notificación a la implementación de Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="7366e-105">The [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function passes an application window handle and a notification message identifier to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="7366e-106">Cuando la ventana de la aplicación recibe este mensaje, indica a la aplicación que llame a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) con el identificador de sesión devuelto por [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span><span class="sxs-lookup"><span data-stu-id="7366e-106">When the application window receives this message, it signals the application to call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function using the session handle returned by [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span></span>

<span data-ttu-id="7366e-107">La función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) devuelve dos identificadores de entidad, un identificador de contexto y el identificador de una PDU.</span><span class="sxs-lookup"><span data-stu-id="7366e-107">The [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function returns two entity handles, a context handle, and the handle to a PDU.</span></span> <span data-ttu-id="7366e-108">Se recomienda que la aplicación WinSNMP libere estos recursos mediante las funciones [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)y [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) .</span><span class="sxs-lookup"><span data-stu-id="7366e-108">It is recommended that the WinSNMP application free these resources using the [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext), and [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) functions.</span></span>

<span data-ttu-id="7366e-109">Para obtener más información sobre cómo administrar el tiempo entre una llamada a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) y la recepción de la respuesta correspondiente, vea [acerca de la retransmisión](about-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="7366e-109">For additional information about managing the time between a call to the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function and the receipt of the corresponding response, see [About Retransmission](about-retransmission.md).</span></span> <span data-ttu-id="7366e-110">Para obtener información adicional sobre cómo usar el campo de PDU de **\_ ID. de solicitud** para hacer coincidir una PDU de respuesta con su PDU de solicitud, consulte [respuesta de coincidencia y solicitar PDU](matching-response-and-request-pdus.md).</span><span class="sxs-lookup"><span data-stu-id="7366e-110">For additional information about using the **request\_id** PDU field to match a response PDU with its request PDU, see [Matching Response and Request PDUs](matching-response-and-request-pdus.md).</span></span>

 

 




