---
title: Traducción de capturas de SNMPv1 a SNMPv2C
description: Cuando la implementación de Microsoft WinSNMP recibe capturas de una entidad que funciona en el marco SNMPv1, traduce las capturas al formato SNMPv2C.
ms.assetid: 472f67ba-05d5-46f7-a2f1-1cef6182574e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f70ddbdfb779f6b06f8ed26490c6fabd2421ae96f0006b4af5b7f1ab18f7d5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885865"
---
# <a name="translating-traps-from-snmpv1-to-snmpv2c"></a>Traducción de capturas de SNMPv1 a SNMPv2C

Cuando la implementación de Microsoft WinSNMP recibe capturas de una entidad que funciona en el marco SNMPv1, traduce las capturas al formato SNMPv2C. Por lo tanto, [**cuando SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) entrega una captura, siempre está en el formato SNMPv2C. RFC 1908, "Coexistencia entre la versión 1 y la versión 2 del marco de administración de redes estándar de Internet", especifica las reglas para traducir de SNMPv1 al formato de captura SNMPv2C.

Una aplicación WinSNMP puede comprobar la última entrada de enlace de variables en una lista de enlaces de variables para determinar si la entrada es una captura traducida de SNMPv1 al formato SNMPv2C. Si es así, el último enlace de variable siempre será igual al valor "snmpTrapEnterpriseOID.0".

Para obtener más información, vea [Administración de capturas y notificaciones.](managing-traps-and-notifications.md)

 

 




