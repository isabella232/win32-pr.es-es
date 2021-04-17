---
title: Acerca de Administración remota de Windows
description: Administración remota de Windows es un componente de las características de administración de hardware de Windows que administran el hardware de servidor de forma local y remota.
ms.assetid: f58add53-0746-4423-9ab8-02ba05f82fa7
ms.tgt_platform: multiple
keywords:
- Acerca de Administración remota de Windows
- Administración remota de Windows, acerca de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9221676d3a9864e4fc88fc57c5bb6691512c220a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714438"
---
# <a name="about-windows-remote-management"></a>Acerca de Administración remota de Windows

Administración remota de Windows es un componente de las características de [Administración de hardware de Windows](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) que administran el hardware de servidor de forma local y remota. Estas características incluyen un servicio que implementa el protocolo [*WS-Management*](windows-remote-management-glossary.md) , el diagnóstico de hardware y el control a través de los controladores de administración de placa base ([*BMC*](windows-remote-management-glossary.md)), y una API com y [objetos de scripting](winrm-scripting-api.md) que le permiten escribir aplicaciones que se comunican de forma remota a través del Protocolo de WS-Management. Para obtener más información acerca de la especificación pública para WS-Management protocolo, consulte [servicios web para administración (WS-Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).

## <a name="components-of-winrm-and-hardware-management"></a>Componentes de WinRM y administración de hardware

A continuación se muestra una lista de los componentes y las características que proporciona WinRM y la supervisión de hardware:

-   [API de scripting de WinRM](winrm-scripting-api.md)

    Esta API de scripting permite obtener datos de equipos remotos mediante scripts que realizan operaciones de protocolo WS-Management.

-   **WinRM. cmd**

    Esta herramienta de línea de comandos para la administración del sistema se implementa en un archivo Visual Basic Scripting Edition (Winrm.vbs) escrito mediante la API de scripting de WinRM. Esta herramienta permite a un administrador configurar WinRM y obtener datos o administrar recursos. Para obtener más información, vea la ayuda en pantalla proporcionada por la línea de comandos **WinRM** **/?**.

-   **Winrs.exe**

    Esta herramienta de línea de comandos permite a los administradores ejecutar de forma remota la mayoría de los comandos Cmd.exe mediante el protocolo WS-Management. Para obtener más información, vea la ayuda en pantalla que proporciona la línea de comandos **Winrs** **/?**.

-   Controlador de interfaz de administración de plataforma inteligente (IPMI) y proveedor WMI

    La administración de hardware a través del proveedor y el controlador de la [*interfaz de administración de plataforma inteligente (IPMI)*](windows-remote-management-glossary.md) le permite controlar y diagnosticar el hardware de servidor remoto a través de BMC cuando el sistema operativo no se ejecuta ni se implementa.

    Para obtener más información, consulte el [proveedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

-   Servicio WMI

    El servicio WMI continúa ejecutándose en paralelo con WinRM y proporciona los datos o el control solicitados a través del [*complemento WMI*](windows-remote-management-glossary.md). Puede continuar obteniendo datos de clases WMI estándar, como el proceso de [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process), así como los datos proporcionados por IPMI. Para obtener más información sobre la configuración y la instalación necesarias para WinRM, consulte Introducción a la [Administración de hardware](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)).

-   Protocolo WS-Management

    WS-Management protocolo, un protocolo basado en SOAP y compatible con firewall, se ha diseñado para que los sistemas ubiquen e intercambien la información de administración. La intención de la especificación del protocolo WS-Management es proporcionar interoperabilidad y coherencia para los sistemas empresariales que tienen equipos que ejecutan diversos sistemas operativos de distintos proveedores.

    WS-Management Protocolo se basa en las siguientes especificaciones de servicio web estándar: HTTPS, SOAP sobre HTTP (perfil WS-I), SOAP 1,2, WS-Addressing, WS-Transfer, WS-Enumeration y WS-Eventing. Para obtener más información sobre el borrador actual de la especificación, vea la [Página de índice de especificaciones de administración](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

## <a name="working-with-winrm"></a>Trabajar con WinRM

Para obtener más información acerca de la escritura de scripts de WinRM, consulte [uso de administración remota de Windows](using-windows-remote-management.md).

En la tabla siguiente se enumeran los temas que proporcionan información acerca del Protocolo de WS-Management, WinRM y WMI, cómo especificar recursos de administración, como unidades de disco o procesos.



| Tema                                                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Instalación y configuración de Administración remota de Windows](installation-and-configuration-for-windows-remote-management.md) | El [*agente de escucha*](windows-remote-management-glossary.md) de WinRM requiere la configuración en los equipos cliente y servidor.                                                                                                                                                                                                                               |
| [Arquitectura de Administración remota de Windows](windows-remote-management-architecture.md)                                             | Diagrama que muestra los componentes de WinRM y los componentes que se encuentran en los equipos cliente y servidor.                                                                                                                                                                                                                                                               |
| [Protocolo WS-Management](ws-management-protocol.md)                                                                             | Descripción del Protocolo de WS-Management estándar público para enviar y recibir datos de administración de forma remota a cualquier dispositivo de equipo que implemente el protocolo.                                                                                                                                                                                                             |
| [Scripting en Administración remota de Windows](scripting-in-windows-remote-management.md)                                             | La API de scripting de WinRM es similar a las acciones del Protocolo de WS-Management. Los datos recuperados por los scripts tienen el formato XML, no los objetos.                                                                                                                                                                                                                                  |
| [Autenticación para conexiones remotas](authentication-for-remote-connections.md)                                               | WS-Management protocolo mantiene la seguridad de la transferencia de datos entre equipos al admitir varios métodos estándar de autenticación y cifrado de mensajes.                                                                                                                                                                                                                |
| [Administración remota de Windows y WMI](windows-remote-management-and-wmi.md)                                                       | Dado que WinRM se integra con [instrumental de administración de Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page), puede obtener datos de WMI con scripts o aplicaciones que usan la [API de scripting de WinRM](winrm-scripting-api.md) o a través de la herramienta de línea de comandos de WinRM.                                                                                                                     |
| [URI de recursos](resource-uris.md)                                                                                               | Un [*URI de recurso*](windows-remote-management-glossary.md) es un identificador de una operación o valor de administración. Por ejemplo, las unidades de disco representan un tipo de recurso.                                                                                                                                                                              |
| [Administración remota de hardware](remote-hardware-management.md)                                                                     | El [proveedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) proporciona [clases](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) y datos que describen el dominio de administración de hardware del controlador de administración de placa base (BMC), los sistemas de equipos de BMC del dominio y los sensores de BMC. Otros objetos representan el registro de eventos del sistema de BMC (SEL) y los mensajes del registro. |
| [Eventos](events.md)                                                                                                             | No puede obtener eventos a través de scripting de WinRM, pero puede usar la herramienta de línea de comandos Wevtutil.exe para ver eventos del [recopilador de eventos](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) .                                                                                                                                                                                        |



 

 

 