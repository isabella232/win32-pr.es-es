---
title: Recepción de mensajes SNMP
description: La aplicación WinSNMP debe llamar a la función SnmpRecvMsg para recuperar la respuesta a una solicitud SnmpSendMsg.
ms.assetid: 323a5565-a8a5-4efd-aa4e-e4623b581d09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bd341e71aa6b8387b82f6576599fb6cb7d3545f34e01f80267f19a73edb7cba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009183"
---
# <a name="receiving-snmp-messages"></a>Recepción de mensajes SNMP

La aplicación WinSNMP debe llamar a [**la función SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para recuperar la respuesta a una [**solicitud SnmpSendMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)

La [**función SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) pasa un identificador de ventana de aplicación y un identificador de mensaje de notificación a la implementación de Microsoft WinSNMP. Cuando la ventana de la aplicación recibe este mensaje, indica a la aplicación que llame a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) mediante el identificador de sesión devuelto [**por SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).

La [**función SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) devuelve dos identificadores de entidad, un identificador de contexto y el identificador a una PDU. Se recomienda que la aplicación WinSNMP libre estos recursos mediante las funciones [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)y [**SnmpFreePdu.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)

Para obtener información adicional sobre cómo administrar el tiempo entre una llamada a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) y la recepción de la respuesta correspondiente, vea Acerca de [la retransmisión.](about-retransmission.md) Para obtener información adicional sobre cómo usar el campo PDU de identificador de solicitud para hacer coincidir una PDU de respuesta con su PDU de solicitud, vea [Matching Response and Request PDUs](matching-response-and-request-pdus.md)(PDU de solicitud y respuesta de coincidencia). **\_**

 

 




