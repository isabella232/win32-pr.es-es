---
title: Acerca de las capturas y notificaciones
description: Un tipo de mensaje que una aplicación de agente SNMP puede enviar a una aplicación WinSNMP es un mensaje asincrónico que informa a la aplicación de un evento significativo.
ms.assetid: 5249c5a5-9260-4a67-b00f-a12214012bb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60739041237dad462e516e43c71d552446357f3ddc188d6609de2eef508b9658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009813"
---
# <a name="about-traps-and-notifications"></a>Acerca de las capturas y notificaciones

Un tipo de mensaje que una aplicación de agente SNMP puede enviar a una aplicación WinSNMP es un mensaje asincrónico que informa a la aplicación de un evento significativo. Un ejemplo de un evento significativo es cuando se cierra un vínculo de red o cuando se produce un error de autenticación.

Estos tipos de mensajes se denominan capturas en SNMPv1 y notificaciones en SNMPv2C. La implementación de Microsoft WinSNMP siempre traduce las capturas de SNMPv1 al formato SNMPv2C, tal como se define en RFC 1908.

Cuando se llama a [**la función SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) para crear una PDU de captura, solo se puede crear una PDU de captura SNMPv2C. El único tipo de PDU de captura que puede actualizar con una llamada a la función [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) es una PDU de captura SNMPv2C.

Para obtener más información, vea los temas siguientes:



| Tema                                                                                    | Descripción |
|------------------------------------------------------------------------------------------|-------------|
| [Traducción de capturas de SNMPv1 a SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [Formatos de captura](trap-formats.md)                                                         |             |



 

 

 




