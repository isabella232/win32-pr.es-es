---
title: Nombres de host y direcciones IP
description: Las redes TCP/IP requieren que los nombres de host se resuelvan en direcciones IP antes de que se pueda usar la información de dirección para crear una conexión.
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- SNMP de direcciones IP y nombres de host
- Nombres de host, resolver SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f884f8ed681a5fc4864665f4c2a97ef8ed9fc0d81756d51848428b76163f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009513"
---
# <a name="host-names-and-ip-addresses"></a>Nombres de host y direcciones IP

Las redes TCP/IP requieren que los nombres de host se resuelvan en direcciones IP antes de que se pueda usar la información de dirección para crear una conexión. Los equipos que se ejecutan Windows sistema operativo usan un archivo host que, para este fin, asigna nombres de host a direcciones IP.

El archivo host es un archivo de texto que enumera nombres de host explícitos y direcciones IP. El archivo host se carga automáticamente en la memoria durante el inicio y se consulta cuando un nombre de host requiere resolución. Si el archivo host no contiene la información de asignación necesaria para resolver un nombre de host específico en su dirección IP, se realiza una consulta de resolución a un servidor DNS.

SNMP usa el Windows Internet Naming Service (WINS) para la resolución de nombres de host. WINS permite asignar nombres NetBIOS, o nombres de equipo, a direcciones IP en redes TCP/IP. Si el equipo no puede acceder a un servidor WINS, el servicio SNMP usa el archivo host para resolver los nombres de host en direcciones IP.

El servicio SNMP admite el uso de nombres de host y direcciones IP. Sin embargo, si tiene la opción de usar nombres de host o direcciones IP para identificar ubicaciones de red, las aplicaciones de administración SNMP deben usar nombres de host. Si usa nombres de host, agregue todas las asignaciones de nombre de host y dirección IP de los sistemas participantes al archivo host.

 

 




