---
title: Traducción de solicitudes de mensajes
description: En este tema se describe el proceso de traducción de solicitudes SNMPv1 a solicitudes de SNMPv2.
ms.assetid: 7671ae36-99b1-47b1-930a-f376021d56a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2a67ecb78b16f818ea50158faf827e19d4eba5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531965"
---
# <a name="translating-message-requests"></a>Traducción de solicitudes de mensajes

En este tema se describe el proceso de traducción de solicitudes SNMPv1 a solicitudes de SNMPv2.

Si una aplicación WinSNMP solicita funcionalidad que está disponible en el marco de trabajo de la versión 2C de SNMP (SNMPv2C), pero la entidad de destino solo admite el marco de SNMP versión 1 (SNMPv1), la implementación de Microsoft WinSNMP intenta traducir la solicitud al formato SNMPv1. Para ello, la implementación usa los procedimientos definidos en RFC 1908, "coexistencia entre la versión 1 y la versión 2 del marco de administración de redes de Internet-Standard". Si no es posible la conversión, se produce un error en la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) con el código de error extendido snmpapi \_ operación \_ no válida.

 

 




