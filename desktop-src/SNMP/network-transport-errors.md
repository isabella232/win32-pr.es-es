---
title: Errores de transporte de red
description: La implementación de Microsoft WinSNMP puede detectar un error de transporte de red después de transmitir un mensaje SNMP.
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15284bba97f2dda8d2fb4224dc2c94bd14050afb9463c73b4d297c1647ec273f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009313"
---
# <a name="network-transport-errors"></a>Errores de transporte de red

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [Windows administración remota](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-Man.\]

La implementación de Microsoft WinSNMP puede detectar un error de transporte de red después de transmitir un mensaje SNMP. Cuando esto sucede, la implementación envía una notificación de recepción de datos a la sesión de WinSNMP que inició la solicitud de comunicación. La implementación también devuelve SNMPAPI \_ FAILURE en la siguiente llamada a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) de la sesión. Se produce un error en la función **SnmpRecvMsg** con un código de error extendido que indica un error de capa de transporte de red.

Para obtener una lista de errores específicos de la capa de transporte, vea las páginas de referencia de las funciones [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)y [**SnmpRecvMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)

 

 