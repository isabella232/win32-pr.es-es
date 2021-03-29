---
title: Acerca de la implementación de Microsoft WinSNMP
description: La implementación de Microsoft WinSNMP cumple con la versión WinSNMP 2,0.
ms.assetid: 99e11d30-d159-4d9b-94d0-baa6e49d82cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbf142ba85458374105af5b80ca5af30a6c5082
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993821"
---
# <a name="about-the-microsoft-winsnmp-implementation"></a>Acerca de la implementación de Microsoft WinSNMP

La implementación de Microsoft WinSNMP cumple con la versión WinSNMP 2,0. Admite todas las funciones y operaciones definidas en la especificación de la versión 1.1 de WinSNMP y en el anexo de la versión WinSNMP 2,0. La implementación de proporciona los siguientes servicios para las aplicaciones WinSNMP:

-   Administra las comunicaciones hacia y desde las entidades de administración. La entidad puede residir en el equipo local o conectarse a través de una red local o de área extensa, o Internet. Para obtener más información, consulte [niveles de compatibilidad con SNMP](levels-of-snmp-support.md).
-   Oculta los detalles del protocolo SNMP, la notación de sintaxis abstracta uno (ASN. 1) y las reglas de codificación básicas (BER) para describir la sintaxis de transferencia.
-   Comprueba la exactitud de las PDU y rechaza las PDU no válidas. Para obtener más información, vea [trabajar con unidades de datos de protocolo](working-with-protocol-data-units.md).
-   Transforma los tipos de PDU de SNMPv2C cuando sea necesario de acuerdo con las RFC pertinentes.
-   Convierte las capturas de SNMPv1 de un agente SNMPv1 en capturas de SNMPv2C de acuerdo con RFC 1908, "coexistencia entre la versión 1 y la versión 2 del marco de administración de redes estándar de Internet". Para obtener más información, consulte [trasladar capturas de SNMPv1 a SNMPv2c](translating-traps-from-snmpv1-to-snmpv2c.md).
-   Admite la Directiva de retransmisión de la aplicación y proporciona compatibilidad con la ejecución de la retransmisión. Para obtener más información, consulte [la base de datos WinSNMP](the-winsnmp-database.md) y [acerca de la retransmisión](about-retransmission.md).
-   Proporciona compatibilidad con la traducción de entidades y contextos para la aplicación. Para obtener más información, consulte [la base de datos WinSNMP](the-winsnmp-database.md) y [establezca la entidad y el modo de traducción de contexto](setting-the-entity-and-context-translation-mode.md).

Para obtener más información sobre la relación entre una aplicación WinSNMP y la implementación de, consulte los [conceptos de administración de datos WinSNMP](winsnmp-data-management-concepts.md) y las [sesiones de WinSNMP](winsnmp-sessions.md).

 

 




