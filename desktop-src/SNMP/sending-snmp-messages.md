---
title: Envío de mensajes SNMP
description: Una aplicación WinSNMP inicia una solicitud de transmisión mediante el envío de un mensaje SNMP. Los mensajes SNMP incluyen una unidad de datos del protocolo SNMP. Para obtener más información, vea Trabajar con unidades de datos de protocolo.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4461c5d554444b2a7a5384a0ca79825b27ebe3c3bc489b6152c81ae71d172f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009073"
---
# <a name="sending-snmp-messages"></a>Envío de mensajes SNMP

Una aplicación WinSNMP inicia una solicitud de transmisión mediante el envío de un mensaje SNMP. Los mensajes SNMP incluyen una unidad de datos del protocolo SNMP. Para obtener más información, vea [Trabajar con unidades de datos de protocolo.](working-with-protocol-data-units.md)

Una aplicación WinSNMP debe llamar a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) para solicitar que la implementación de Microsoft WinSNMP transmita la PDU, con los demás elementos de mensaje necesarios definidos por la RFC pertinente. Además de la entidad de destino, la aplicación debe especificar la entidad de origen y un contexto para la solicitud. La [**función SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) se ejecuta de forma asincrónica.

La aplicación WinSNMP debe llamar a [**la función SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para recuperar la respuesta a una **solicitud SnmpSendMsg.**

La implementación comprueba la validez de la PDU y los demás elementos de mensaje cuando una aplicación llama a [**SnmpSendMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)

 

 




