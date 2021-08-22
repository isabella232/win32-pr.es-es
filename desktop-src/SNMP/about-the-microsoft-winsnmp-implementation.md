---
title: Acerca de la implementación de Microsoft WinSNMP
description: La implementación de WinSNMP de Microsoft cumple con la versión 2.0 de WinSNMP.
ms.assetid: 99e11d30-d159-4d9b-94d0-baa6e49d82cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693a2fd5c6aa21d684d485f75b04160e72bfe1455c13ef8c320c863b61ab696b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009873"
---
# <a name="about-the-microsoft-winsnmp-implementation"></a>Acerca de la implementación de Microsoft WinSNMP

La implementación de WinSNMP de Microsoft cumple con la versión 2.0 de WinSNMP. Admite todas las funciones y operaciones definidas en la especificación winSNMP versión 1.1a y en el anexo de la versión 2.0 de WinSNMP. La implementación proporciona los siguientes servicios para aplicaciones WinSNMP:

-   Administra las comunicaciones hacia y desde las entidades de administración. La entidad puede residir en el equipo local o estar conectada a través de una red de área extensa o local, o de Internet. Para obtener más información, vea [Niveles de compatibilidad con SNMP.](levels-of-snmp-support.md)
-   Oculta los detalles del protocolo SNMP, la notación de sintaxis abstracta Uno (ASN.1) y las reglas básicas de codificación (BER) para describir la sintaxis de transferencia.
-   Comprueba la corrección de las PDU y rechaza las PDU no válidas. Para obtener más información, vea [Trabajar con unidades de datos de protocolo.](working-with-protocol-data-units.md)
-   Transforma los tipos PDU de SNMPv2C cuando es necesario de acuerdo con las RFC pertinentes.
-   Convierte las capturas de SNMPv1 de un agente SNMPv1 en capturas SNMPv2C de acuerdo con RFC 1908, "Coexistencia entre la versión 1 y la versión 2 del marco de administración de redes estándar de Internet". Para obtener más información, [vea Translateing Traps from SNMPv1 to SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md)( Traducción de capturas de SNMPv1 a SNMPv2C).
-   Admite la directiva de retransmisión de la aplicación y proporciona compatibilidad con la ejecución de retransmisión. Para obtener más información, vea [The WinSNMP Database (La base de datos winSNMP)](the-winsnmp-database.md) y [About Retransmission (Acerca de la retransmisión).](about-retransmission.md)
-   Proporciona compatibilidad con la traducción de entidades y contextos para la aplicación. Para obtener más información, vea [The WinSNMP Database](the-winsnmp-database.md) y [Setting the Entity and Context Translation Mode](setting-the-entity-and-context-translation-mode.md).

Para obtener información adicional sobre la relación entre una aplicación WinSNMP y la implementación, vea Conceptos de [WinSNMP Administración de datos y](winsnmp-data-management-concepts.md) Sesiones de [WinSNMP](winsnmp-sessions.md).

 

 




