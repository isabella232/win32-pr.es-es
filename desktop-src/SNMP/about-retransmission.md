---
title: Acerca de la retransmisión
description: Una aplicación WinSNMP puede realizar solicitudes de operación SNMP de varias maneras.
ms.assetid: 71150a66-74a3-4957-bc70-3dd25c3b9c71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade0b2d58f371de87be5da855f26686a18518454c787c6a09e9701afbb731757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009963"
---
# <a name="about-retransmission"></a>Acerca de la retransmisión

Una aplicación WinSNMP puede realizar solicitudes de operación SNMP de varias maneras. La aplicación puede emitir varias solicitudes a un agente SNMP, sin esperar una respuesta, o puede emitir una única solicitud y esperar la respuesta. Puesto que SNMP se puede implementar en varios protocolos de transporte, los mecanismos de entrega y las características de confiabilidad pueden variar.

Al codificar la aplicación WinSNMP, debe determinar el nivel de confiabilidad que necesita para las operaciones de comunicaciones, en función de la forma en que la aplicación emite solicitudes de operación. A continuación, debe seleccionar una estrategia de retransmisión e implementar una directiva de retransmisión.

Una directiva de retransmisión incluye un período de tiempo de espera y un recuento de reintentos. Un período de tiempo de espera es el tiempo transcurrido, en centésimas de segundo, entre la emisión de una aplicación de una solicitud [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) y su recepción del mensaje correspondiente. La aplicación recibe el mensaje como resultado de una llamada a la [**función SnmpRecvMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) El valor de tiempo de espera es el período de tiempo que la implementación de WinSNMP de Microsoft espera a que una entidad responda a una solicitud de comunicación. Si no hay ninguna respuesta dentro del período de tiempo de espera, la implementación retransmite la solicitud si el valor de recuento de reintentos especifica intentos de retransmisión o produce un error en la llamada a [**SnmpSendMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) Un número de reintentos es el número máximo de intentos de retransmisión que realiza la implementación si se produce un error en una solicitud de transmisión SNMP.

La implementación almacena valores de tiempo de espera y recuentos de reintentos en su base de datos para la aplicación. La implementación almacena valores individuales para cada entidad de destino.

Las aplicaciones deben establecer sus propias frecuencias de sondeo y deben administrar variables de temporizador. Para obtener más información, vea [Administración de la directiva de retransmisión.](managing-the-retransmission-policy.md)

 

 




