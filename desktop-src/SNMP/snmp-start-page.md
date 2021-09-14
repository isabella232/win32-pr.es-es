---
title: Servicio SNMP
description: Microsoft Windows implementación del Protocolo simple de administración de redes (SNMP) se usa para configurar dispositivos remotos, supervisar el rendimiento de la red, auditar el uso de la red y detectar errores de red o acceso inadecuado. Importante La API snmp Windows Microsoft solo admite versiones de protocolo hasta SNMPv2C. No admite ninguna versión posterior del protocolo.
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP SNMP
- SNMP SNMP, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71df55c79244c0f74ef685271834adc01ca7e981
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071359"
---
# <a name="snmp-service"></a>Servicio SNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, [Windows administración remota](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-Man.\]

## <a name="purpose"></a>Propósito

Microsoft Windows implementación del Protocolo simple de administración de redes (SNMP) se usa para configurar dispositivos remotos, supervisar el rendimiento de la red, auditar el uso de la red y detectar errores de red o acceso inadecuado.

> [!IMPORTANT]
> Microsoft Windows SNMP API solo admite versiones de protocolo hasta SNMPv2C. No admite ninguna versión posterior del protocolo.

 

## <a name="where-applicable"></a>Donde sea aplicable

SNMP usa una arquitectura distribuida que consta de aplicaciones de administración y aplicaciones de agente. El servicio SNMP implementa un agente SNMP. Para usar la información que proporciona el servicio SNMP, debe tener al menos un host que ejecute una aplicación de administración SNMP. Puede usar software de administración SNMP de terceros o puede desarrollar su propia aplicación de software de administración SNMP. Las siguientes API están disponibles para este propósito:

-   Snmp API de Administración, un conjunto de funciones que se pueden usar para desarrollar rápidamente sistemas de administración SNMP básicos
-   Api WinSNMP, versión 2.0, un conjunto de funciones para codificar, codificar, codificar, enviar y recibir mensajes SNMP

Además, la API del agente de extensión SNMP define la interfaz entre el servicio SNMP y los archivos DLL del agente de extensión SNMP de terceros. Las funciones de la API de la utilidad SNMP se pueden usar para simplificar el procesamiento de mensajes SNMP.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Las API enumeradas en la sección anterior están diseñadas para su uso por los programadores de C/C++. Es necesario estar familiarizado con SNMP y SNMPv2C, así como tener conocimientos prácticos de los conceptos de administración de redes y redes.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Para obtener más información sobre el sistema operativo necesario para usar una función determinada, vea la sección Requisitos de la página de referencia de esa función.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                | Descripción                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novedades de SNMP](new-in-snmp.md)<br/>                                                            | Información sobre las actualizaciones de SNMP.<br/>                                                                                                      |
| [Protocolo simple de administración de redes (SNMP)](simple-network-management-protocol-snmp-.md):<br/> | Información y referencia de API para SNMP, incluidas las funciones SNMP API de Administración, SNMP Extension Agent API y SNMP Utility API.<br/> |
| [WinSNMP API](snmp-reference.md)<br/>                                                         | Información y referencia de API para microsoft Windows interfaz de programación de aplicaciones SNMP (API winSNMP). <br/>                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Protocolo de configuración dinámica de host (DHCP)](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[Administración de red](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[Servicio de acceso remoto y enrutamiento](/windows/desktop/RRAS/portal)
</dt> </dl>

 

