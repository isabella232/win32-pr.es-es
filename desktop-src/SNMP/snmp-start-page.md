---
title: Servicio SNMP
description: 'La implementación de Microsoft Windows del Protocolo simple de administración de redes (SNMP) se usa para configurar dispositivos remotos, supervisar el rendimiento de la red, auditar el uso de la red y detectar errores de red o acceso inadecuado. Importante: la API SNMP de Microsoft Windows solo es compatible con las versiones de protocolo hasta SNMPv2C. No es compatible con las versiones posteriores del protocolo.'
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP SNMP
- SNMP SNMP, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71df55c79244c0f74ef685271834adc01ca7e981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078249"
---
# <a name="snmp-service"></a>Servicio SNMP

\[SNMP está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, use [administración remota de Windows](/windows/desktop/WinRM/portal), que es la implementación de Microsoft de WS-MAN.\]

## <a name="purpose"></a>Propósito

La implementación de Microsoft Windows del Protocolo simple de administración de redes (SNMP) se usa para configurar dispositivos remotos, supervisar el rendimiento de la red, auditar el uso de la red y detectar errores de red o acceso inadecuado.

> [!IMPORTANT]
> La API SNMP de Microsoft Windows solo admite versiones de protocolo de hasta SNMPv2C. No es compatible con las versiones posteriores del protocolo.

 

## <a name="where-applicable"></a>Donde sea aplicable

SNMP utiliza una arquitectura distribuida que consta de aplicaciones de administración y aplicaciones de agente. El servicio SNMP implementa un agente SNMP. Para usar la información que proporciona el servicio SNMP, debe tener al menos un host que ejecute una aplicación de administración SNMP. Puede usar software de administración SNMP de terceros o puede desarrollar su propia aplicación de software de administración SNMP. Las siguientes API están disponibles para este propósito:

-   API de administración de SNMP, un conjunto de funciones que se pueden usar para desarrollar rápidamente sistemas de administración SNMP básicos
-   WinSNMP API, versión 2,0, un conjunto de funciones para codificar, descodificar, enviar y recibir mensajes SNMP

Además, la API del agente de extensión SNMP define la interfaz entre el servicio SNMP y los archivos DLL del agente de extensión SNMP de terceros. Las funciones de la API de la utilidad SNMP se pueden usar para simplificar el procesamiento de mensajes SNMP.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Las API enumeradas en la sección anterior están diseñadas para que las usen los programadores de C/C++. Es necesario estar familiarizado con SNMP y SNMPv2C, así como tener conocimientos prácticos de los conceptos de administración de redes y redes.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Para obtener más información sobre el sistema operativo necesario para usar una función determinada, vea la sección requisitos de la página de referencia de esa función.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                | Descripción                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novedades de SNMP](new-in-snmp.md)<br/>                                                            | Información sobre las actualizaciones de SNMP.<br/>                                                                                                      |
| [Protocolo simple de administración de redes (SNMP)](simple-network-management-protocol-snmp-.md):<br/> | Información y referencia de API para SNMP, incluida la API de administración de SNMP, la API del agente de extensión SNMP y las funciones de API de la utilidad SNMP.<br/> |
| [API WinSNMP](snmp-reference.md)<br/>                                                         | Información y referencia de la API para la interfaz de programación de aplicaciones (API WinSNMP) de Microsoft Windows SNMP. <br/>                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Protocolo de configuración dinámica de host (DHCP)](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[Administración de red](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[Servicio de acceso remoto y enrutamiento](/windows/desktop/RRAS/portal)
</dt> </dl>

 

