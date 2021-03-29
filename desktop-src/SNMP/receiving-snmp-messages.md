---
title: Recepción de mensajes SNMP
description: La aplicación WinSNMP debe llamar a la función SnmpRecvMsg para recuperar la respuesta a una solicitud SnmpSendMsg.
ms.assetid: 323a5565-a8a5-4efd-aa4e-e4623b581d09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529420deaf637cec8598a8e8becc87ab514b40b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778600"
---
# <a name="receiving-snmp-messages"></a>Recepción de mensajes SNMP

La aplicación WinSNMP debe llamar a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para recuperar la respuesta a una solicitud [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .

La función [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) pasa un identificador de ventana de la aplicación y un identificador de mensaje de notificación a la implementación de Microsoft WinSNMP. Cuando la ventana de la aplicación recibe este mensaje, indica a la aplicación que llame a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) con el identificador de sesión devuelto por [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).

La función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) devuelve dos identificadores de entidad, un identificador de contexto y el identificador de una PDU. Se recomienda que la aplicación WinSNMP libere estos recursos mediante las funciones [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)y [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) .

Para obtener más información sobre cómo administrar el tiempo entre una llamada a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) y la recepción de la respuesta correspondiente, vea [acerca de la retransmisión](about-retransmission.md). Para obtener información adicional sobre cómo usar el campo de PDU de **\_ ID. de solicitud** para hacer coincidir una PDU de respuesta con su PDU de solicitud, consulte [respuesta de coincidencia y solicitar PDU](matching-response-and-request-pdus.md).

 

 




