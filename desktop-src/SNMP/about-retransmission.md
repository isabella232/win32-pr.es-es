---
title: Acerca de la retransmisión
description: Una aplicación WinSNMP puede hacer solicitudes de operación SNMP de varias maneras.
ms.assetid: 71150a66-74a3-4957-bc70-3dd25c3b9c71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a26ba632cec096300927911c2277cbcf5911e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356882"
---
# <a name="about-retransmission"></a>Acerca de la retransmisión

Una aplicación WinSNMP puede hacer solicitudes de operación SNMP de varias maneras. La aplicación puede emitir varias solicitudes a un agente SNMP, sin tener que esperar una respuesta, o puede emitir una solicitud única y esperar la respuesta. Dado que SNMP se puede implementar en varios protocolos de transporte, los mecanismos de entrega y las características de confiabilidad pueden variar.

Cuando codifique la aplicación WinSNMP, debe determinar el nivel de confiabilidad que necesita para las operaciones de comunicaciones, en función de la manera en que la aplicación emite solicitudes de operación. A continuación, debe seleccionar una estrategia de retransmisión e implementar una directiva de retransmisión.

Una directiva de retransmisión incluye un período de tiempo de espera y un número de reintentos. Un período de tiempo de espera es el tiempo transcurrido, en centésimas de segundo, entre la emisión de una aplicación de una solicitud de [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) y su recepción del mensaje correspondiente. La aplicación recibe el mensaje como resultado de una llamada a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) . El valor de tiempo de espera es el período de tiempo que la implementación de Microsoft WinSNMP espera a que una entidad responda a una solicitud de comunicación. Si no hay ninguna respuesta dentro del período de tiempo de espera, la implementación retransmite la solicitud si el valor de número de reintentos especifica intentos de retransmisión o si se produce un error en la llamada a [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg). Un número de reintentos es el número máximo de intentos de retransmisión que realiza la implementación si se produce un error en una solicitud de transmisión SNMP.

La implementación almacena los valores de tiempo de espera y los recuentos de reintentos en su base de datos para la aplicación. La implementación almacena valores individuales para cada entidad de destino.

Las aplicaciones deben establecer sus propias frecuencias de sondeo y deben administrar las variables de temporizador. Para obtener más información, consulte [Administración de la Directiva de retransmisión](managing-the-retransmission-policy.md).

 

 




