---
title: Activar y desactivar la retransmisión
description: Una aplicación puede establecer el modo de retransmisión con una llamada a la función SnmpSetRetransmitMode. El nuevo modo de retransmisión se aplica a las llamadas posteriores a la función SnmpSendMsg.
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc7624977b4959911cc4128c9a75ac70fac7031bfb853c4b31db34d0987b4d4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885675"
---
# <a name="turning-retransmission-on-and-off"></a>Activar y desactivar la retransmisión

Una aplicación puede establecer el modo de retransmisión con una llamada a la [**función SnmpSetRetransmitMode.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) El nuevo modo de retransmisión se aplica a las llamadas posteriores a la [**función SnmpSendMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)

Cuando la aplicación llama a **SnmpSetRetransmitMode con** el valor de modo de retransmisión SNMPAPI ON, la implementación de Microsoft WinSNMP comienza la ejecución de la directiva de retransmisión de \_ la aplicación. El nuevo modo de retransmisión no afecta a los mensajes SNMP pendientes. Un mensaje pendiente es aquel que no tiene respuesta en el momento en que la aplicación cambia el modo de retransmisión.

Cuando la aplicación WinSNMP llama a la función [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) con el valor de modo de retransmisión SNMPAPI OFF, la implementación deja de ejecutar la directiva \_ de retransmisión. La implementación cancela los intentos de retransmisión de los mensajes SNMP pendientes. Esto se debe a que es posible que la implementación no pueda controlar todas las solicitudes y operaciones SNMP pendientes más las nuevas solicitudes, antes de que un contador de tiempo de espera o reintento de la aplicación señale un evento.

 

 




