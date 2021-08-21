---
title: Apertura y cierre de una aplicación WinSNMP
description: La aplicación WinSNMP debe llamar correctamente a la función SnmpStartup antes de llamar a cualquier otra función winSNMP.
ms.assetid: ff2b99c9-c2fd-4bb7-8fd5-799e72c4560d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4aa18f437f8b1a430ad27b40b838859d2e00641bcb4532602715548b370acce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009253"
---
# <a name="opening-and-closing-a-winsnmp-application"></a>Apertura y cierre de una aplicación WinSNMP

La aplicación WinSNMP debe llamar correctamente a la [**función SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) antes de llamar a cualquier otra función winSNMP. La **función SnmpStartup** permite que la implementación de Microsoft WinSNMP realice procedimientos de inicialización. La función también devuelve a la aplicación la versión de la API winSNMP que admite la implementación, el nivel de comunicaciones SNMP que admite y los modos predeterminados de traducción y retransmisión de la implementación.

La aplicación WinSNMP debe llamar a [**la función SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) cuando la aplicación ya no requiera los servicios de la implementación. Aunque **SnmpCleanup** permite que la implementación desasigne todos los recursos asignados a la aplicación, se recomienda que la aplicación llame primero a la función [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) una vez para cada sesión winSNMP abierta, para maximizar el rendimiento de la implementación. La aplicación WinSNMP debe llamar a [**SnmpCleanup como**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) la última función winSNMP antes de finalizar.

 

 




