---
description: Los proveedores de eventos SNMP reciben paquetes de eventos SNMP de la pila WINSNMP y traducen la información incluida en los paquetes en eventos de WMI.
ms.assetid: 4ae0a734-39b0-4418-b55c-6d8f093806a8
ms.tgt_platform: multiple
title: Elección entre proveedores de eventos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dabd8f6d432025406a5faecc3ace423cd6671e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716623"
---
# <a name="choosing-between-snmp-event-providers"></a>Elección entre proveedores de eventos SNMP

Los proveedores de eventos SNMP reciben paquetes de eventos SNMP de la pila WINSNMP y traducen la información incluida en los paquetes en eventos de WMI.

WMI incluye los dos proveedores de eventos SNMP siguientes:

-   Proveedor de eventos encapsulados SNMP (SEEP)

    La aprovisionamiento encapsulado significa que la instancia de evento tiene propiedades simples que describen la información asignada directamente desde la captura de SNMP.

-   Proveedor de eventos de SNMP referente (SREP)

    El aprovisionamiento referente abstrae la información presente dentro de la captura de SNMP para que las propiedades que comparten la misma clase e instancia se presenten como objetos incrustados. Esto permite que la instancia única, a la que está asociada la captura, se recupere después de la recepción del evento, mediante SNMP \_ \_ RELPATH.

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Independientemente de si el evento SNMP es una captura de SNMPv1 o una notificación de SNMPv2C, la pila lo notifica como una notificación de SNMPv2. Por lo tanto, los proveedores de eventos procesan todos los eventos SNMP como notificaciones de SNMPv2.

Para describir los eventos SNMP a los consumidores de WMI, cada proveedor de eventos admite una jerarquía de clases que deriva de la clase del sistema [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) . La clase [SNMPNotification](snmpnotification.md) es la clase principal de la jerarquía SEEP; la clase [SNMPExtendedNotification](snmpextendednotification.md) es la clase principal de la jerarquía SREP.

 

 



