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
# <a name="registering-an-snmp-agent-application"></a><span data-ttu-id="a84d0-103">Registro de una aplicación de agente SNMP</span><span class="sxs-lookup"><span data-stu-id="a84d0-103">Registering an SNMP Agent Application</span></span>

<span data-ttu-id="a84d0-104">Además de las operaciones del administrador SNMP, la versión de API WinSNMP 2,0 también admite operaciones del agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="a84d0-104">In addition to SNMP manager operations, the WinSNMP API version 2.0 also supports SNMP agent operations.</span></span>

<span data-ttu-id="a84d0-105">Para registrar una aplicación WinSNMP como agente SNMP, la aplicación puede llamar a la función [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) .</span><span class="sxs-lookup"><span data-stu-id="a84d0-105">To register a WinSNMP application as an SNMP agent, the application can call the [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) function.</span></span> <span data-ttu-id="a84d0-106">Esta función informa a la implementación de Microsoft WinSNMP de que una entidad SNMP actuará en el rol de un agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="a84d0-106">This function informs the Microsoft WinSNMP implementation that an SNMP entity will be acting in the role of an SNMP agent.</span></span> <span data-ttu-id="a84d0-107">La aplicación también puede llamar a **SnmpListen** para informar a la implementación cuando dejará de actuar como agente.</span><span class="sxs-lookup"><span data-stu-id="a84d0-107">The application can also call **SnmpListen** to inform the implementation when it will no longer be acting as an agent.</span></span>

<span data-ttu-id="a84d0-108">Si una aplicación llama a la función [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) y pasa el valor snmpapi en \_ el parámetro *lStatus* , se producen las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="a84d0-108">If an application calls the [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) function and passes the value SNMPAPI\_ON in the *lStatus* parameter, the following actions occur:</span></span>

1.  <span data-ttu-id="a84d0-109">La entidad que funcionará en un rol de agente SNMP se enlaza a su puerto asignado y "escucha" para las solicitudes de mensajes SNMP entrantes.</span><span class="sxs-lookup"><span data-stu-id="a84d0-109">The entity that will be functioning in an SNMP agent role binds to its assigned port, and "listens" for incoming SNMP message requests.</span></span>
2.  <span data-ttu-id="a84d0-110">El agente utiliza la lógica específica de la aplicación para procesar cada solicitud SNMP.</span><span class="sxs-lookup"><span data-stu-id="a84d0-110">The agent uses application-specific logic to process each SNMP request.</span></span>
3.  <span data-ttu-id="a84d0-111">El agente forma las respuestas adecuadas a cada solicitud.</span><span class="sxs-lookup"><span data-stu-id="a84d0-111">The agent forms appropriate responses to each request.</span></span>
4.  <span data-ttu-id="a84d0-112">El agente transmite la respuesta a la entidad que realiza la solicitud mediante una llamada a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .</span><span class="sxs-lookup"><span data-stu-id="a84d0-112">The agent transmits the response to the requesting entity by calling the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function.</span></span> <span data-ttu-id="a84d0-113">Cuando el agente llama a **SnmpSendMsg**, especifica la dirección del agente en el parámetro *srcEntity* y la dirección de la entidad del administrador remoto en el parámetro *dstEntity* .</span><span class="sxs-lookup"><span data-stu-id="a84d0-113">When the agent calls **SnmpSendMsg**, it specifies the address of the agent in the *srcEntity* parameter, and the address of the remote manager entity in the *dstEntity* parameter.</span></span> <span data-ttu-id="a84d0-114">(Estos valores son los valores inversos de la entidad agente recibida en estos parámetros cuando llamó a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para recuperar una solicitud SNMP).</span><span class="sxs-lookup"><span data-stu-id="a84d0-114">(These values are the reverse of the values the agent entity received in these parameters when it called the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve an SNMP request.)</span></span>

<span data-ttu-id="a84d0-115">Para obtener más información acerca de las aplicaciones de administración de SNMP y del agente, consulte [About SNMP](about-snmp.md).</span><span class="sxs-lookup"><span data-stu-id="a84d0-115">For more information about SNMP management applications and agent applications, see [About SNMP](about-snmp.md).</span></span>

 

 




