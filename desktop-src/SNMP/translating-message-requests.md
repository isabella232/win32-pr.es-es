---
title: Traducción de solicitudes de mensaje
description: En este tema se describe el proceso de traducción de solicitudes SNMPv1 en solicitudes SNMPv2.
ms.assetid: 7671ae36-99b1-47b1-930a-f376021d56a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1775d59a8de0bd0473570f3028018a1a25cad2ebd4ee004025ad11a38e37e69c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885895"
---
# <a name="translating-message-requests"></a>Traducción de solicitudes de mensaje

En este tema se describe el proceso de traducción de solicitudes SNMPv1 en solicitudes SNMPv2.

Si una aplicación WinSNMP solicita funcionalidad que está disponible en el marco de la versión 2C de SNMP (SNMPv2C), pero la entidad de destino solo admite el marco de snmp versión 1 (SNMPv1), la implementación de Microsoft WinSNMP intenta traducir la solicitud al formato SNMPv1. Para ello, la implementación usa los procedimientos definidos en RFC 1908, "Coexistencia entre la versión 1 y la versión 2 de Internet-Standard Network Management Framework". Si la traducción no es posible, se produce un error en la función [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) con el código de error extendido SNMPAPI \_ OPERATION \_ INVALID.

 

 




