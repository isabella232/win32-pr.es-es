---
title: Base de información de administración de SNMP (MIB)
description: Una base de información de administración (MIB) describe un conjunto de objetos administrados. Una aplicación de consola de administración de SNMP puede manipular los objetos en un equipo específico si el servicio SNMP tiene un archivo DLL del agente de extensión que admite miB.
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf3fac2e24b79da3ea7277010da5a3f96e3664416809bc440097f4ec0b1384e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127605"
---
# <a name="the-snmp-management-information-base-mib"></a>Base de información de administración de SNMP (MIB)

Una base de información de administración (MIB) describe un conjunto de objetos administrados. Una aplicación de consola de administración de SNMP puede manipular los objetos en un equipo específico si el servicio SNMP tiene un archivo DLL del agente de extensión que admite miB.

Cada objeto administrado de una MIB tiene un identificador único. El identificador incluye el tipo del objeto (como contador, cadena, medidor o dirección), el nivel de acceso del objeto (como lectura o lectura/escritura), restricciones de tamaño e información de intervalo.

La tabla siguiente contiene una lista parcial de los MIB que se envían con el sistema. Se instalan con el servicio SNMP en el directorio %systemroot% \\ system32. Para obtener una lista completa de los MIB, consulte el Windows Resource Kit.



| MIB         | Descripción                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Dhcp. Mib    | MIB definido por Microsoft que contiene tipos de objeto para supervisar el tráfico de red entre hosts remotos y servidores DHCP                        |
| HOSTMIB. Mib | Contiene tipos de objeto para supervisar y administrar recursos de host                                                                                 |
| LMMIB2. Mib  | Abarca los servicios de estación de trabajo y servidor                                                                                                           |
| MIB \_ II.MIB | Contiene la base de información de administración (MIB-II), que proporciona una arquitectura y un sistema sencillos y fáciles de trabajar para administrar internetes basados en TCP/IP. |
| Gana. Mib    | MIB definido por Microsoft para Windows Internet Name Service (WINS)                                                                               |



 

**Windows NT:** Normalmente, puede copiar un MIB desde el agente de extensión SNMP que admita la MIB determinada. Hay algunas MIB adicionales disponibles con el kit de recursos Windows NT 4.0.

Los archivos DLL del agente de extensión para MIB-II, LAN Manager MIB-II y la MIB de recursos de host se instalan con el servicio SNMP. Los archivos DLL del agente de extensión para las otras MIB se instalan cuando se instalan sus respectivos servicios. En el momento de inicio del servicio, el servicio SNMP carga todos los archivos DLL del agente de extensión que aparecen en el Registro.

Los usuarios pueden agregar otros archivos DLL del agente de extensión que implementen MIB adicionales. Para ello, deben agregar una entrada del Registro para el nuevo archivo DLL en el servicio SNMP. También deben registrar el nuevo MIB con la aplicación de consola de administración de SNMP. Para obtener más información, consulte la documentación incluida con la aplicación de consola de administración.

Para obtener más información, vea [Árbol de nombres de MIB.](mib-name-tree.md)

 

 




