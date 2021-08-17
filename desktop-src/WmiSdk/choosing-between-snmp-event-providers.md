---
description: Los proveedores de eventos SNMP reciben paquetes de eventos SNMP de la pila WINSNMP y traducen la información incluida en los paquetes en eventos WMI.
ms.assetid: 4ae0a734-39b0-4418-b55c-6d8f093806a8
ms.tgt_platform: multiple
title: Elegir entre proveedores de eventos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0902c463ee0fc51505e125a329f592ebced6df20ec7f63296ba7248cd8dade98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131878"
---
# <a name="choosing-between-snmp-event-providers"></a>Elegir entre proveedores de eventos SNMP

Los proveedores de eventos SNMP reciben paquetes de eventos SNMP de la pila WINSNMP y traducen la información incluida en los paquetes en eventos WMI.

WMI incluye los dos proveedores de eventos SNMP siguientes:

-   Proveedor de eventos encapsulados SNMP (SEEP)

    El aprovisionamiento encapsulado significa que la instancia de evento tiene propiedades sencillas que describen la información asignada directamente desde la captura de SNMP.

-   Proveedor de eventos de referencia snmp (SREP)

    El aprovisionamiento de referencia abstrae la información presente dentro de la captura de SNMP para que las propiedades que comparten la misma clase e instancia se presenten como objetos incrustados. Esto permite que la instancia única, a la que está asociada la captura, se recupere después de la recepción del evento, mediante SNMP \_ \_ RELPATH.

> [!Note]  
> Para obtener más información sobre cómo instalar el proveedor, vea [Configuración del entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

 

Independientemente de si el evento SNMP es una captura SNMPv1 o una notificación SNMPv2C, la pila lo notifica como una notificación SNMPv2. Por lo tanto, los proveedores de eventos procesan todos los eventos SNMP como notificaciones SNMPv2.

Para describir los eventos SNMP a los consumidores WMI, cada proveedor de eventos admite una jerarquía de clases que deriva de la clase del sistema [**\_ \_ ExtrinsicEvent.**](--extrinsicevent.md) La [clase SNMPNotification](snmpnotification.md) es la clase primaria para la jerarquía SEEP; la [clase SNMPExtendedNotification](snmpextendednotification.md) es la clase primaria de la jerarquía SREP.

 

 



