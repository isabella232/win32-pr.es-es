---
title: Trasladar capturas de SNMPv1 a SNMPv2C
description: Cuando la implementación de Microsoft WinSNMP recibe capturas de una entidad que funciona con el marco de SNMPv1, traduce las capturas al formato SNMPv2C.
ms.assetid: 472f67ba-05d5-46f7-a2f1-1cef6182574e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d36870bda9b434bcc19f42332f2751020689591
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903275"
---
# <a name="translating-traps-from-snmpv1-to-snmpv2c"></a>Trasladar capturas de SNMPv1 a SNMPv2C

Cuando la implementación de Microsoft WinSNMP recibe capturas de una entidad que funciona con el marco de SNMPv1, traduce las capturas al formato SNMPv2C. Por lo tanto, cuando [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) entrega una captura, siempre está en el formato SNMPv2c. RFC 1908, "coexistencia entre la versión 1 y la versión 2 del marco de administración de redes estándar de Internet", especifica las reglas de conversión de SNMPv1 al formato de captura de SNMPv2C.

Una aplicación WinSNMP puede comprobar la entrada de enlace de la última variable en una lista de enlaces de variables para determinar si la entrada es una captura traducida desde SNMPv1 al formato SNMPv2C. Si es así, el último enlace de variables siempre será igual al valor "snmpTrapEnterpriseOID. 0".

Para obtener más información, consulte [Administración de capturas y notificaciones](managing-traps-and-notifications.md).

 

 




