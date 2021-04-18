---
title: Envío de mensajes SNMP
description: Una aplicación WinSNMP inicia una solicitud de transmisión mediante el envío de un mensaje SNMP. Los mensajes SNMP incluyen una unidad de datos de protocolo SNMP. Para obtener más información, vea trabajar con unidades de datos de protocolo.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613ac7079f7dc206280b8d8077d2d5ea8db7151c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357440"
---
# <a name="sending-snmp-messages"></a>Envío de mensajes SNMP

Una aplicación WinSNMP inicia una solicitud de transmisión mediante el envío de un mensaje SNMP. Los mensajes SNMP incluyen una unidad de datos de protocolo SNMP. Para obtener más información, vea [trabajar con unidades de datos de protocolo](working-with-protocol-data-units.md).

Una aplicación WinSNMP debe llamar a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) para solicitar que la implementación de Microsoft WinSNMP transmita la PDU, con los otros elementos de mensaje necesarios definidos por la RFC correspondiente. Además de la entidad de destino, la aplicación debe especificar la entidad de origen y un contexto para la solicitud. La función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) se ejecuta de forma asincrónica.

La aplicación WinSNMP debe llamar a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para recuperar la respuesta a una solicitud **SnmpSendMsg** .

La implementación de comprueba la validez de la PDU y los otros elementos del mensaje cuando una aplicación llama a [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).

 

 




