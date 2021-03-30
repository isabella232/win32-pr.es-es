---
title: Niveles de compatibilidad con SNMP
description: La implementación de Microsoft WinSNMP proporciona compatibilidad con las comunicaciones SNMP de nivel 2.
ms.assetid: 9874ad9b-4eb9-4d63-816b-fe444c5b4d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b48c930266073f10e5cb8019a7462317bd798c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148770"
---
# <a name="levels-of-snmp-support"></a><span data-ttu-id="b1184-103">Niveles de compatibilidad con SNMP</span><span class="sxs-lookup"><span data-stu-id="b1184-103">Levels of SNMP Support</span></span>

<span data-ttu-id="b1184-104">La implementación de Microsoft WinSNMP proporciona compatibilidad con las comunicaciones SNMP de nivel 2.</span><span class="sxs-lookup"><span data-stu-id="b1184-104">The Microsoft WinSNMP implementation provides level 2 SNMP communications support.</span></span> <span data-ttu-id="b1184-105">El nivel 2 es compatible con el protocolo SNMPv2 estándar de Internet Engineering Task Force (IETF), tal y como se define en RFC 1902-1908.</span><span class="sxs-lookup"><span data-stu-id="b1184-105">Level 2 supports the Internet Engineering Task Force (IETF) standard SNMPv2 protocol as defined in RFCs 1902-1908.</span></span> <span data-ttu-id="b1184-106">También admite el contenedor de mensajes basado en la comunidad, tal y como se define en RFC 1901 (SNMPv2C).</span><span class="sxs-lookup"><span data-stu-id="b1184-106">It also supports the community-based message wrapper as defined in RFC 1901 (SNMPv2C).</span></span>

<span data-ttu-id="b1184-107">La compatibilidad con las comunicaciones de nivel 2 incluye servicios de codificación y descodificación de mensajes, anteriormente denominado compatibilidad de comunicaciones de nivel 0 en la versión 1.1 de WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="b1184-107">Level 2 communications support includes message encoding and decoding services, previously called Level 0 communications support in WinSNMP version 1.1a.</span></span> <span data-ttu-id="b1184-108">El nivel 2 también es compatible con todas las operaciones de protocolo SNMPv1, anteriormente denominadas compatibilidad de comunicaciones de nivel 1 en la versión 1.1 de WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="b1184-108">Level 2 also supports all SNMPv1 protocol operations, previously called Level 1 communications support in WinSNMP version 1.1a.</span></span>

<span data-ttu-id="b1184-109">La implementación de devuelve el nivel máximo de comunicaciones SNMP que admite en respuesta a una llamada de la aplicación WinSNMP a la función [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) .</span><span class="sxs-lookup"><span data-stu-id="b1184-109">The implementation returns the maximum level of SNMP communications it supports in response to a call by the WinSNMP application to the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function.</span></span>

<span data-ttu-id="b1184-110">Si la aplicación WinSNMP usa la implementación de para la codificación y descodificación de mensajes SNMP, la aplicación debe realizar las transformaciones necesarias que la implementación habría realizado.</span><span class="sxs-lookup"><span data-stu-id="b1184-110">If the WinSNMP application uses the implementation for SNMP message encoding and decoding only, the application must perform required transformations that the implementation would have performed.</span></span> <span data-ttu-id="b1184-111">Esto incluye la traducción de las capturas de SNMPv1 devueltas por una llamada a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) , a las capturas de SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="b1184-111">This includes translating SNMPv1 traps returned by a call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function, to SNMPv2C traps.</span></span> <span data-ttu-id="b1184-112">También incluye la conversión de tipos de PDU definidos por SNMPv1 en el tipo de PDU correspondiente definido por SNMPv2C, de acuerdo con RFC 1908.</span><span class="sxs-lookup"><span data-stu-id="b1184-112">It also includes translating PDU types defined by SNMPv1 to the relevant PDU type defined by SNMPv2C, in accordance with RFC 1908.</span></span>

 

 




