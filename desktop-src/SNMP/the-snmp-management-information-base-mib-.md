---
title: La base de información de administración (MIB) de SNMP
description: Una base de datos de información de administración (MIB) describe un conjunto de objetos administrados. Una aplicación de consola de administración de SNMP puede manipular los objetos en un equipo específico si el servicio SNMP tiene una DLL de agente de extensión que admite la MIB.
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba4612c026aa5a3a1a1574556f58207bad08e06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774364"
---
# <a name="the-snmp-management-information-base-mib"></a>La base de información de administración (MIB) de SNMP

Una base de datos de información de administración (MIB) describe un conjunto de objetos administrados. Una aplicación de consola de administración de SNMP puede manipular los objetos en un equipo específico si el servicio SNMP tiene una DLL de agente de extensión que admite la MIB.

Cada objeto administrado en una MIB tiene un identificador único. El identificador incluye el tipo del objeto (como contador, cadena, medidor o dirección), el nivel de acceso del objeto (como lectura o lectura/escritura), restricciones de tamaño e información de intervalo.

La tabla siguiente contiene una lista parcial de las MIB que se incluyen con el sistema. Se instalan con el servicio SNMP en el directorio% SystemRoot% \\ system32. Para obtener una lista completa de las MIB, consulte el kit de recursos de Windows.



| MIB         | Descripción                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| DHCP. MIB    | MIB definida por Microsoft que contiene tipos de objeto para supervisar el tráfico de red entre los hosts remotos y los servidores DHCP                        |
| HOSTMIB. MIB | Contiene tipos de objeto para la supervisión y administración de recursos de host                                                                                 |
| LMMIB2. MIB  | Trata los servicios de estación de trabajo y servidor                                                                                                           |
| MIB \_ II. MIB | Contiene la base de información de administración (MIB-II), que proporciona una arquitectura y un sistema sencillos y factibles para administrar Internet basados en TCP/IP. |
| DNS. MIB    | MIB definida por Microsoft para el servicio de nombres Internet de Windows (WINS)                                                                               |



 

**Windows NT:** Normalmente, puede copiar una MIB del agente de extensión SNMP que admita la MIB concreta. En el kit de recursos de Windows NT 4,0 hay disponibles algunas MIB adicionales.

Los archivos DLL del agente de extensión para MIB-II, LAN Manager MIB-II y la MIB de recursos de host se instalan con el servicio SNMP. Los archivos DLL del agente de extensión para las demás MIB se instalan cuando se instalan sus servicios respectivos. En el momento de inicio del servicio, el servicio SNMP carga todos los archivos DLL del agente de extensión que se enumeran en el registro.

Los usuarios pueden agregar otros archivos DLL del agente de extensión que implementen MIB adicionales. Para ello, deben agregar una entrada del registro para el nuevo archivo DLL en el servicio SNMP. También deben registrar la nueva MIB con la aplicación de consola de administración de SNMP. Para obtener más información, consulte la documentación que se incluye con la aplicación de consola de administración.

Para obtener más información, vea [árbol de nombres de MIB](mib-name-tree.md).

 

 




