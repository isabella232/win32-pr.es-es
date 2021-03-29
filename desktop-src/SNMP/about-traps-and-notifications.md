---
title: Acerca de las capturas y notificaciones
description: Un tipo de mensaje que una aplicación de agente SNMP puede enviar a una aplicación WinSNMP es un mensaje asincrónico que informa a la aplicación de un evento significativo.
ms.assetid: 5249c5a5-9260-4a67-b00f-a12214012bb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bacc6a92de2cb5a12aaf09f5caa629f28338f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903498"
---
# <a name="about-traps-and-notifications"></a>Acerca de las capturas y notificaciones

Un tipo de mensaje que una aplicación de agente SNMP puede enviar a una aplicación WinSNMP es un mensaje asincrónico que informa a la aplicación de un evento significativo. Un ejemplo de un evento significativo es cuando un vínculo de red se cierra o cuando se produce un error de autenticación.

Estos tipos de mensajes se denominan capturas en SNMPv1 y notificaciones en SNMPv2C. La implementación de Microsoft WinSNMP siempre traduce las capturas de SNMPv1 al formato SNMPv2C, tal como se define en RFC 1908.

Cuando se llama a la función [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) para crear una PDU de captura, solo se puede crear una PDU de captura de SNMPv2c. El único tipo de PDU de captura que se puede actualizar con una llamada a la función [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) es una PDU de captura de SNMPv2c.

Para obtener más información, vea los siguientes temas.



| Tema                                                                                    | Descripción |
|------------------------------------------------------------------------------------------|-------------|
| [Trasladar capturas de SNMPv1 a SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [Formatos de captura](trap-formats.md)                                                         |             |



 

 

 




