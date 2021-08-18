---
title: Respuesta de coincidencia y PDU de solicitud
description: Es posible que el orden en que la aplicación WinSNMP reciba respuestas SNMP no coincida con el orden en que la aplicación envía solicitudes de operación SNMP.
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e669b3e15652b8df68cb8fc27437106e644909e99bf0b7aee21a128194cf7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009332"
---
# <a name="matching-response-and-request-pdus"></a>Respuesta de coincidencia y PDU de solicitud

Es posible que el orden en que la aplicación WinSNMP reciba respuestas SNMP no coincida con el orden en que la aplicación envía solicitudes de operación SNMP. Para hacer coincidir la respuesta con la solicitud, la aplicación debe usar el campo identificador de solicitud **(el identificador \_** de solicitud) de la respuesta.

El **campo \_ id.** de solicitud es un valor numérico único que identifica la PDU. Las aplicaciones pueden asignar identificadores de solicitud llamando a [**la función SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) o [**a la función SnmpSetPduData.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) Llame a [**la función SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) para recuperar el identificador de solicitud de una PDU. **\_**

 

 




