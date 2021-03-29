---
title: Nombres de host y direcciones IP
description: Las redes TCP/IP requieren que los nombres de host se resuelvan en direcciones IP antes de que se pueda usar la información de la dirección para crear una conexión.
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- Nombres de host y direcciones IP SNMP
- Nombres de host, resolver SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426f711be9e1fda5dc936db6628cccc21093aa09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775115"
---
# <a name="host-names-and-ip-addresses"></a>Nombres de host y direcciones IP

Las redes TCP/IP requieren que los nombres de host se resuelvan en direcciones IP antes de que se pueda usar la información de la dirección para crear una conexión. Los equipos que se ejecutan en el sistema operativo Windows usan un archivo host que, para este propósito, asigna los nombres de host a las direcciones IP.

El archivo host es un archivo de texto que muestra los nombres de host y las direcciones IP explícitos. El archivo host se carga automáticamente en la memoria en el inicio y se consulta cuando un nombre de host requiere resolución. Si el archivo host no contiene la información de asignación necesaria para resolver un nombre de host específico en su dirección IP, se realiza una consulta de resolución en un servidor DNS.

SNMP utiliza el Naming Service de Internet de Windows (WINS) para la resolución de nombres de host. WINS hace posible asignar nombres NetBIOS o nombres de equipo a direcciones IP en redes TCP/IP. Si el equipo no puede tener acceso a un servidor WINS, el servicio SNMP utiliza el archivo host para resolver nombres de host en direcciones IP.

El servicio SNMP admite el uso de los nombres de host y las direcciones IP. Sin embargo, si tiene la opción de usar nombres de host o direcciones IP para identificar ubicaciones de red, las aplicaciones de administración SNMP deben usar nombres de host. Si usa nombres de host, agregue todas las asignaciones de nombre de host y dirección IP de los sistemas participantes al archivo host.

 

 




