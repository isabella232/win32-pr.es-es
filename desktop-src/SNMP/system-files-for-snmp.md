---
title: Archivos del sistema para SNMP
description: En la tabla siguiente se describen los archivos principales relacionados con el servicio SNMP.
ms.assetid: 513d7c75-2f68-4d7d-897f-493089f045cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb917276fd807835fea703ec27cc66a0d493766d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486711"
---
# <a name="system-files-for-snmp"></a>Archivos del sistema para SNMP

En la tabla siguiente se describen los archivos principales relacionados con el servicio SNMP.



| Nombre de archivo     | Descripción                                                                                                                                                                                                                         |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DHCPMIB.DLL  | DLL del agente de extensión que implementa la MIB de DHCP definida por Microsoft. Instalado solo en servidores DHCP.                                                                                                                                 |
| EVNTAGNT.DLL | DLL SNMP que traduce los registros de eventos en capturas SNMP; también se conoce como traductor de eventos SNMP.                                                                                                                                       |
| HOSTMIB.DLL  | DLL del agente de extensión que implementa la MIB de recursos del host.                                                                                                                                                                         |
| LMMIB2.DLL   | DLL del agente de extensión que implementa LAN Manager MIB-II.                                                                                                                                                                             |
| MGMTAPI.DLL  | Biblioteca de API de administración de SNMP de Microsoft. Esta API permite a las aplicaciones de administrador de SNMP "escuchar" las solicitudes del administrador de SNMP y enviar y recibir las respuestas de los agentes SNMP.                                                |
| MIB. BIN      | Información de MIB compilada utilizada por MGMTAPI.DLL.                                                                                                                                                                                       |
| SNMP.EXE     | Servicio SNMP. Este es el agente principal que recibe solicitudes SNMP y las entrega a la DLL del agente de extensión correspondiente.                                                                                                        |
| SNMPAPI.DLL  | DLL de utilidades SNMP que usan las dll y las aplicaciones de administrador del agente de extensión SNMP. Este archivo DLL contiene un marco para desarrollar archivos DLL del agente de extensión.                                                                                   |
| SNMPSNAP.DLL | Aplicación de configuración de SNMP que es un componente de complemento de Microsoft Management Console (MMC). El complemento agrega varias páginas a la hoja de propiedades del servicio SNMP. Para obtener más información, consulte la ayuda en pantalla del servicio SNMP. |
| SNMPTRAP.EXE | Servicio de captura de SNMP. Recibe capturas SNMP y las reenvía a aplicaciones SNMP Manager.                                                                                                                                              |
| WINSMIB.DLL  | DLL del agente de extensión que implementa la MIB de WINS definida por Microsoft. Instalado solo en servidores WINS.                                                                                                                                 |
| WSNMP32.DLL  | Biblioteca de API de Microsoft [WinSNMP](winsnmp-api.md) . Esta API permite a las aplicaciones de administrador de SNMP "escuchar" las solicitudes del administrador de SNMP y enviar y recibir las respuestas de los agentes SNMP.                                     |



 

Para obtener más información, consulte [la base de datos de información de administración (MIB) de SNMP](the-snmp-management-information-base-mib-.md). (También puede hacer referencia al kit de recursos de Windows 2000).

 

 




