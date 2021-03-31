---
title: Cambio de la Directiva de retransmisión
description: La implementación de Microsoft WinSNMP proporciona compatibilidad con la Directiva de retransmisión mediante el almacenamiento de un valor de tiempo de espera y un número de reintentos para la aplicación WinSNMP en una base de datos.
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f21fc479517b8844e9c1db75834b5b1c02edc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903496"
---
# <a name="changing-the-retransmission-policy"></a>Cambio de la Directiva de retransmisión

La implementación de Microsoft WinSNMP proporciona compatibilidad con la Directiva de retransmisión mediante el almacenamiento de un valor de tiempo de espera y un número de reintentos para la aplicación WinSNMP en una base de datos. La implementación de almacena valores para entidades de destino individuales. La implementación proporciona inicialmente valores predeterminados para estos elementos, pero una aplicación puede Agregar o modificar valores para entidades individuales.

Una llamada a las funciones [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) y [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) devuelve los valores de tiempo de espera y número de reintentos para una entidad de destino específica. Para cambiar el valor de tiempo de espera, una aplicación WinSNMP debe llamar a la función [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) . Para cambiar el valor de número de reintentos, la aplicación debe llamar a la función [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) . La configuración actualizada afecta a las nuevas solicitudes de mensajes SNMP a la entidad de destino.

 

 




