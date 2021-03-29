---
title: Asignar identificadores de solicitud
description: Una aplicación WinSNMP puede llamar a la función SnmpCreatePdu o a la función SnmpSetPduData para asignar un identificador de solicitud generado por la aplicación a una PDU. La aplicación debe pasar el valor en el \_ parámetro de ID. de solicitud.
ms.assetid: 72559054-982f-4c2b-83d2-268f130f6ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753f0ec1f5f3ca4347b6344aa111b91e735f06ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772853"
---
# <a name="assigning-request-identifiers"></a>Asignar identificadores de solicitud

Una aplicación WinSNMP puede llamar a la función [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) o a la función [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) para asignar un identificador de solicitud generado por la aplicación a una PDU. La aplicación debe pasar el valor en el parámetro de *\_ ID* . de solicitud.

Una aplicación puede solicitar que la implementación de Microsoft WinSNMP genere y asigne un identificador de solicitud a una PDU pasando cero en el parámetro de *\_ identificador de solicitud* de la función [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) . La aplicación puede recuperar el identificador de solicitud asignado con una llamada a la función [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) .

Para asignar un identificador de solicitud igual a un valor específico, incluido cero, la aplicación debe pasar ese valor en el parámetro de *\_ identificador de solicitud* de la función [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .

Cuando la implementación ejecuta la Directiva de retransmisión de la aplicación, incluye el **campo \_ ID. de solicitud** de la PDU original en cada mensaje SNMP retransmitido. Para obtener más información, vea [acerca de la retransmisión](about-retransmission.md) y [Administración de la Directiva de retransmisión](managing-the-retransmission-policy.md).

> [!Note]  
> Cuando la implementación recibe capturas de una entidad SNMPv1, asigna un valor distinto de cero al campo **\_ ID. de solicitud** de la PDU. Este valor puede duplicar un identificador de solicitud usado por la aplicación en una PDU de solicitud. Las aplicaciones deben comprobar la duplicación.

 

 

 




