---
title: Creación de una PDU
description: Para crear e inicializar una PDU, una aplicación WinSNMP llama a la función SnmpCreatePdu.
ms.assetid: 7f02a2c6-19bc-456f-bf04-3297d19000f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aba7a4ca42e2a5d63169d2521410773ca018c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903495"
---
# <a name="creating-a-pdu"></a>Creación de una PDU

Para crear e inicializar una PDU, una aplicación WinSNMP llama a la función [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) . La aplicación debe llamar a **SnmpCreatePdu** antes de llamar a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) para solicitar que la implementación de Microsoft WINSNMP transmita una PDU. La aplicación también debe llamar a [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) antes de llamar a la función [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) para solicitar la codificación de un mensaje SNMP.

La aplicación debe llamar a la función [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) para liberar los recursos que la función [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) asigna para las PDU nuevas.

 

 




