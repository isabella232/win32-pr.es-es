---
title: Asignación de identificadores de solicitud
description: Una aplicación WinSNMP puede llamar a la función SnmpCreatePdu o a la función SnmpSetPduData para asignar un identificador de solicitud generado por la aplicación a una PDU. La aplicación debe pasar el valor en el parámetro de identificador \_ de solicitud.
ms.assetid: 72559054-982f-4c2b-83d2-268f130f6ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9914256a071d93ebebd932e6771758c4c76e2c419f8f9cf13a0323ca44ea7715
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009803"
---
# <a name="assigning-request-identifiers"></a>Asignación de identificadores de solicitud

Una aplicación WinSNMP puede llamar a la función [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) o a la función [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) para asignar un identificador de solicitud generado por la aplicación a una PDU. La aplicación debe pasar el valor en el parámetro *de identificador \_ de* solicitud.

Una aplicación puede solicitar que la implementación de Microsoft WinSNMP genere y asigne un identificador de solicitud a una PDU pasando cero en el parámetro *de \_* identificador de solicitud de la [**función SnmpCreatePdu.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) La aplicación puede recuperar el identificador de solicitud asignado con una llamada a la [**función SnmpGetPduData.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)

Para asignar un identificador de solicitud igual a un valor específico, incluido cero, la aplicación debe pasar ese valor en el parámetro *request \_ id* de la [**función SnmpSetPduData.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)

Cuando la implementación ejecuta la directiva de retransmisión **de \_** la aplicación, incluye el campo de identificador de solicitud de la PDU original en cada mensaje SNMP retransmitido. Para obtener más información, vea [Acerca de la retransmisión](about-retransmission.md) y [Administración de la directiva de retransmisión.](managing-the-retransmission-policy.md)

> [!Note]  
> Cuando la implementación recibe capturas de una entidad SNMPv1, asigna **un \_** valor distinto de cero al campo id. de solicitud de la PDU. Este valor puede duplicar un identificador de solicitud utilizado por la aplicación en una PDU de solicitud. Las aplicaciones deben comprobar si hay duplicación.

 

 

 




