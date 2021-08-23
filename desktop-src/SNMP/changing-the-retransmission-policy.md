---
title: Cambio de la directiva de retransmisión
description: La implementación de Microsoft WinSNMP proporciona compatibilidad con directivas de retransmisión almacenando un valor de tiempo de espera y un recuento de reintentos para la aplicación WinSNMP en una base de datos.
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed160de40b300d1b2430304b7a487f4544fee9a13db6049d1d837958276da8e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009773"
---
# <a name="changing-the-retransmission-policy"></a>Cambio de la directiva de retransmisión

La implementación de Microsoft WinSNMP proporciona compatibilidad con directivas de retransmisión almacenando un valor de tiempo de espera y un recuento de reintentos para la aplicación WinSNMP en una base de datos. La implementación almacena valores para entidades de destino individuales. Inicialmente, la implementación proporciona valores predeterminados para estos elementos, pero una aplicación puede agregar o modificar valores para entidades individuales.

Una llamada a las [**funciones SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) y [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) devuelve los valores de tiempo de espera y recuento de reintentos para una entidad de destino específica. Para cambiar el valor de tiempo de espera, una aplicación WinSNMP debe llamar a [**la función SnmpSetTimeout.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) Para cambiar el valor del recuento de reintentos, la aplicación debe llamar a [**la función SnmpSetRetry.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) La configuración actualizada afecta a las nuevas solicitudes de mensajes SNMP a la entidad de destino.

 

 




