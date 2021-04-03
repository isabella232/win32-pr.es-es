---
title: Abrir y cerrar una aplicación WinSNMP
description: La aplicación WinSNMP debe llamar correctamente a la función SnmpStartup antes de llamar a cualquier otra función WinSNMP.
ms.assetid: ff2b99c9-c2fd-4bb7-8fd5-799e72c4560d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f960a22a6155d3f3eeec770af361fac2c0eb036e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076048"
---
# <a name="opening-and-closing-a-winsnmp-application"></a>Abrir y cerrar una aplicación WinSNMP

La aplicación WinSNMP debe llamar correctamente a la función [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) antes de llamar a cualquier otra función WinSNMP. La función **SnmpStartup** permite que la implementación de Microsoft WinSNMP realice procedimientos de inicialización. La función también devuelve a la aplicación la versión de la API WinSNMP que admite la implementación, el nivel de comunicaciones SNMP que admite y los modos de traducción y retransmisión predeterminados de la implementación.

La aplicación WinSNMP debe llamar a la función [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) cuando la aplicación ya no requiere los servicios de la implementación. Aunque **SnmpCleanup** permite que la implementación Desasigne todos los recursos asignados a la aplicación, se recomienda que la aplicación llame primero a la función [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) una vez por cada sesión WinSNMP abierta para maximizar el rendimiento de la implementación. La aplicación WinSNMP debe llamar a [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) como la última función WinSNMP antes de finalizar.

 

 




