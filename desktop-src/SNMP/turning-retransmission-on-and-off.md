---
title: Activación y desactivación de la retransmisión
description: Una aplicación puede establecer el modo de retransmisión con una llamada a la función SnmpSetRetransmitMode. El nuevo modo de retransmisión se aplica a las llamadas subsiguientes a la función SnmpSendMsg.
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24936bcc90ed0debf66eb9040334fff3bceee2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685492"
---
# <a name="turning-retransmission-on-and-off"></a>Activación y desactivación de la retransmisión

Una aplicación puede establecer el modo de retransmisión con una llamada a la función [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) . El nuevo modo de retransmisión se aplica a las llamadas subsiguientes a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .

Cuando la aplicación llama a **SnmpSetRetransmitMode** con el valor de modo de retransmisión snmpapi \_ en, la implementación de Microsoft WinSNMP comienza a ejecutar la Directiva de retransmisión de la aplicación. El nuevo modo de retransmisión no afecta a los mensajes SNMP pendientes. Un mensaje pendiente es aquél que no tiene respuesta en el momento en que la aplicación cambia el modo de retransmisión.

Cuando la aplicación WinSNMP llama a la función [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) con el valor de modo de REtransmisión snmpapi \_ desactivado, la implementación deja de ejecutar la Directiva de retransmisión. La implementación cancela los intentos de retransmisión para los mensajes SNMP pendientes. Esto se debe a que es posible que la implementación de controle todas las solicitudes y operaciones SNMP pendientes y las nuevas solicitudes, antes de que el tiempo de espera de la aplicación o el contador de reintentos señale un evento.

 

 




