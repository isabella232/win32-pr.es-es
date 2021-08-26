---
title: Archivos del sistema para SNMP
description: En la tabla siguiente se describen los archivos de entidad de seguridad relacionados con el servicio SNMP.
ms.assetid: 513d7c75-2f68-4d7d-897f-493089f045cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 139b83a2d2117af693bcd7ae624ff18d7a18ab5618c9a9597c1e142f62aba07d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886055"
---
# <a name="system-files-for-snmp"></a>Archivos del sistema para SNMP

En la tabla siguiente se describen los archivos de entidad de seguridad relacionados con el servicio SNMP.



| Nombre de archivo     | Descripción                                                                                                                                                                                                                         |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DHCPMIB.DLL  | DLL del agente de extensión que implementa la MIB DHCP definida por Microsoft. Solo se instala en servidores DHCP.                                                                                                                                 |
| EVNTAGNT.DLL | DLL de SNMP que traduce los registros de eventos en capturas de SNMP; también conocido como traductor de eventos SNMP.                                                                                                                                       |
| HOSTMIB.DLL  | DLL del agente de extensión que implementa la MIB de recursos de host.                                                                                                                                                                         |
| LMMIB2.DLL   | DLL del agente de extensión que implementa LAN Manager MIB-II.                                                                                                                                                                             |
| MGMTAPI.DLL  | Biblioteca de API de Administración SNMP de Microsoft. Esta API permite a las aplicaciones del administrador SNMP "escuchar" las solicitudes del administrador SNMP y enviar solicitudes a agentes SNMP y recibir respuestas de estos.                                                |
| Mib. Bin      | Información de MIB compilada usada por MGMTAPI.DLL.                                                                                                                                                                                       |
| SNMP.EXE     | Servicio SNMP. Este es el agente maestro que recibe las solicitudes SNMP y las entrega al archivo DLL del agente de extensión adecuado.                                                                                                        |
| SNMPAPI.DLL  | DLL de utilidades SNMP que usan los archivos DLL del agente de extensión SNMP y las aplicaciones de administrador. Este archivo DLL contiene un marco para desarrollar archivos DLL del agente de extensión.                                                                                   |
| SNMPSNAP.DLL | Aplicación de configuración SNMP que es un Microsoft Management Console de complemento (MMC). El complemento agrega varias páginas a la hoja Propiedades del servicio SNMP. Para obtener más información, consulte la ayuda en línea para el servicio SNMP. |
| SNMPTRAP.EXE | Servicio de captura de SNMP. Recibe capturas snmp y las reenvía a las aplicaciones del administrador SNMP.                                                                                                                                              |
| WINSMIB.DLL  | DLL del agente de extensión que implementa la MIB WINS definida por Microsoft. Solo se instala en servidores WINS.                                                                                                                                 |
| WSNMP32.DLL  | Biblioteca [de API WinSNMP de](winsnmp-api.md) Microsoft. Esta API permite a las aplicaciones del administrador SNMP "escuchar" las solicitudes del administrador SNMP y enviar solicitudes a agentes SNMP y recibir respuestas de estos.                                     |



 

Para obtener más información, vea [La base de información de administración de SNMP (MIB).](the-snmp-management-information-base-mib-.md) (También puede hacer referencia al kit de recursos Windows 2000).

 

 




