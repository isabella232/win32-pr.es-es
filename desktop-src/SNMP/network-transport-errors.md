---
title: Errores de transporte de red
description: La implementación de Microsoft WinSNMP puede detectar un error de transporte de red después de transmitir un mensaje SNMP.
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cf6b7610fbfe8d19a375bd3e3146263b9e9f0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904761"
---
# <a name="network-transport-errors"></a>Errores de transporte de red

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

La implementación de Microsoft WinSNMP puede detectar un error de transporte de red después de transmitir un mensaje SNMP. Cuando esto ocurre, la implementación envía una notificación de recepción de datos a la sesión WinSNMP que inició la solicitud de comunicación. La implementación también devuelve \_ un error snmpapi en la siguiente llamada a la función [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para la sesión. Se produce un error en la función **SnmpRecvMsg** con un código de error extendido que indica un error de capa de transporte de red.

Para obtener una lista de errores de capa de transporte específicos, vea las páginas de referencia de las funciones [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)y [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .

 

 