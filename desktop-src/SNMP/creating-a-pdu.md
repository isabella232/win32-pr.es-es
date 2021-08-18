---
title: Creación de una PDU
description: Para crear e inicializar una PDU, una aplicación WinSNMP llama a la función SnmpCreatePdu.
ms.assetid: 7f02a2c6-19bc-456f-bf04-3297d19000f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ef0598c08c27d988825b3f0db3d8172362e9e6daf2ed4dbad049e2808b01034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009603"
---
# <a name="creating-a-pdu"></a>Creación de una PDU

Para crear e inicializar una PDU, una aplicación WinSNMP llama a [**la función SnmpCreatePdu.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) La aplicación debe llamar a **SnmpCreatePdu** antes de llamar a la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) para solicitar que la implementación de WinSNMP de Microsoft transmita una PDU. La aplicación también debe llamar a [**SnmpCreatePdu antes**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) de llamar a la [**función SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) para solicitar la codificación de un mensaje SNMP.

La aplicación debe llamar a [**la función SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) para liberar los recursos que [**la función SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) asigna para las nuevas PDU.

 

 




