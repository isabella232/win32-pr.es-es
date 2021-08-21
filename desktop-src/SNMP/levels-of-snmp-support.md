---
title: Niveles de compatibilidad con SNMP
description: La implementación de Microsoft WinSNMP proporciona compatibilidad con comunicaciones SNMP de nivel 2.
ms.assetid: 9874ad9b-4eb9-4d63-816b-fe444c5b4d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa76a475ed266a7a4928a79f809b7011a537c777c89ea0a97d06983d6656a9ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009463"
---
# <a name="levels-of-snmp-support"></a>Niveles de compatibilidad con SNMP

La implementación de Microsoft WinSNMP proporciona compatibilidad con comunicaciones SNMP de nivel 2. El nivel 2 admite el protocolo SNMPv2 estándar del Grupo de tareas de ingeniería de Internet (IETF), tal como se define en las RFC 1902-1908. También admite el contenedor de mensajes basado en la comunidad tal como se define en RFC 1901 (SNMPv2C).

La compatibilidad con comunicaciones de nivel 2 incluye servicios de codificación y codificación de mensajes, anteriormente denominados compatibilidad con comunicaciones de nivel 0 en WinSNMP versión 1.1a. El nivel 2 también admite todas las operaciones del protocolo SNMPv1, anteriormente denominadas compatibilidad con comunicaciones de nivel 1 en WinSNMP versión 1.1a.

La implementación devuelve el nivel máximo de comunicaciones SNMP que admite en respuesta a una llamada de la aplicación WinSNMP a la [**función SnmpStartup.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)

Si la aplicación WinSNMP usa la implementación solo para codificación y codificación de mensajes SNMP, la aplicación debe realizar las transformaciones necesarias que la implementación habría realizado. Esto incluye la traducción de capturas de SNMPv1 devueltas por una llamada a la función [**SnmpRecvMsg,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) a capturas SNMPv2C. También incluye la traducción de tipos PDU definidos por SNMPv1 al tipo PDU correspondiente definido por SNMPv2C, de acuerdo con RFC 1908.

 

 




