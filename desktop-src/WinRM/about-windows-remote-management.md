---
title: Acerca Windows administración remota
description: Windows Administración remota es un componente de las características de administración Windows hardware que administran el hardware del servidor de forma local y remota.
ms.assetid: f58add53-0746-4423-9ab8-02ba05f82fa7
ms.tgt_platform: multiple
keywords:
- Acerca Windows administración remota
- Windows Administración remota, acerca de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a83df38de4af354f826b9bbba59ddab76e1b656c72e1c3dc74301da883f875cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858915"
---
# <a name="about-windows-remote-management"></a>Acerca Windows administración remota

Windows Administración remota es un componente de las características de administración Windows [hardware](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) que administran el hardware del servidor de forma local y remota. Estas características incluyen un servicio que implementa el protocolo [*WS-Management,*](windows-remote-management-glossary.md) el diagnóstico y el control de hardware a través de controladores de administración de placa base [*(BMC)*](windows-remote-management-glossary.md)y una API COM y objetos de [scripting](winrm-scripting-api.md) que permiten escribir aplicaciones que se comunican de forma remota a través del protocolo WS-Management. Para obtener más información sobre la especificación pública para WS-Management, vea [Web Services for Management (WS–Management).](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf)

## <a name="components-of-winrm-and-hardware-management"></a>Componentes de WinRM y administración de hardware

A continuación se muestra una lista de componentes y características proporcionados por WinRM y la supervisión de hardware:

-   [WinRM Scripting API](winrm-scripting-api.md)

    Esta API de scripting le permite obtener datos de equipos remotos mediante scripts que realizan WS-Management de protocolo.

-   **Winrm.cmd**

    Esta herramienta de línea de comandos para la administración del sistema se implementa en un archivo Visual Basic Scripting Edition (Winrm.vbs) escrito mediante la API de scripting de WinRM. Esta herramienta permite a un administrador configurar WinRM y obtener datos o administrar recursos. Para más información, consulte la ayuda en línea proporcionada por la línea de **comandos Winrm** **/?**.

-   **Winrs.exe**

    Esta herramienta de línea de comandos permite a los administradores ejecutar de forma remota la mayoría Cmd.exe comandos mediante WS-Management protocolo. Para obtener más información, consulte la ayuda en línea proporcionada por la línea de **comandos Winrs** **/?**.

-   Controlador de interfaz de administración de plataforma inteligente (IPMI) y proveedor WMI

    La administración de hardware a través del proveedor y el controlador de [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md) le permite controlar y diagnosticar hardware de servidor remoto a través de BMC cuando el sistema operativo no se está ejecutando ni implementado.

    Para obtener más información, vea el [proveedor de IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

-   Servicio WMI

    El servicio WMI continúa en ejecución en paralelo con WinRM y proporciona los datos solicitados o el control a través del [*complemento WMI*](windows-remote-management-glossary.md). Puede seguir obteniendo datos de clases WMI estándar, como [**Proceso de \_ Win32,**](/windows/desktop/CIMWin32Prov/win32-process)así como datos proporcionados por IPMI. Para obtener más información sobre la configuración y la instalación necesarias para WinRM, consulte [Introducción a la administración de hardware.](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10))

-   WS-Management protocolo

    WS-Management protocolo, un protocolo basado en SOAP y que admite firewalls, se diseñó para que los sistemas buscara e intercambiara información de administración. La intención de la especificación WS-Management protocolo es proporcionar interoperabilidad y coherencia para los sistemas empresariales que tienen equipos que se ejecutan en una variedad de sistemas operativos de distintos proveedores.

    WS-Management protocolo se basa en las siguientes especificaciones de servicio web estándar: HTTPS, SOAP sobre HTTP (perfil WS-I), SOAP 1.2, WS-Addressing, WS-Transfer, WS-Enumeration y WS-Eventing. Para obtener más información sobre el borrador actual de la especificación, vea la página índice de [especificaciones de administración](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

## <a name="working-with-winrm"></a>Trabajar con WinRM

Para obtener más información sobre cómo escribir scripts de WinRM, [consulte Uso de Windows administración remota.](using-windows-remote-management.md)

En la tabla siguiente se enumeran los temas que proporcionan información sobre el protocolo WS-Management, WinRM y WMI, cómo especificar recursos de administración como unidades de disco o procesos.



| Tema                                                                                                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Instalación y configuración para la Windows remota](installation-and-configuration-for-windows-remote-management.md) | El agente de escucha [*de*](windows-remote-management-glossary.md) WinRM requiere configuración en los equipos cliente y servidor.                                                                                                                                                                                                                               |
| [Windows Arquitectura de administración remota](windows-remote-management-architecture.md)                                             | Diagrama que muestra los componentes de WinRM y qué componentes se encuentran en los equipos cliente y servidor.                                                                                                                                                                                                                                                               |
| [Protocolo WS-Management](ws-management-protocol.md)                                                                             | Descripción del protocolo de WS-Management estándar público para enviar y recibir datos de administración de forma remota a cualquier dispositivo informático que implemente el protocolo.                                                                                                                                                                                                             |
| [Scripting en Windows remota](scripting-in-windows-remote-management.md)                                             | La API de scripting de WinRM es similar a las acciones del WS-Management protocolo. Los datos recuperados por scripts tienen formato XML, no objetos.                                                                                                                                                                                                                                  |
| [Autenticación para conexiones remotas](authentication-for-remote-connections.md)                                               | WS-Management protocolo mantiene la seguridad para la transferencia de datos entre equipos al admitir varios métodos estándar de autenticación y cifrado de mensajes.                                                                                                                                                                                                                |
| [Windows Administración remota y WMI](windows-remote-management-and-wmi.md)                                                       | Dado que WinRM está integrado con [Windows Management Instrumentation (WMI),](/windows/desktop/WmiSdk/wmi-start-page)puede obtener datos WMI con scripts o aplicaciones que usan [WinRM Scripting API](winrm-scripting-api.md) o a través de la herramienta de línea de comandos Winrm.                                                                                                                     |
| [URI de recursos](resource-uris.md)                                                                                               | Un [*URI de*](windows-remote-management-glossary.md) recurso es un identificador para una operación o un valor de administración. Por ejemplo, las unidades de disco representan un tipo de recurso.                                                                                                                                                                              |
| [Administración remota de hardware](remote-hardware-management.md)                                                                     | El proveedor de [](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) [IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) proporciona clases y datos que describen el dominio de administración de hardware del controlador de administración de placa base (BMC), los sistemas de equipos BMC del dominio y los sensores de BMC. Otros objetos representan el registro de eventos del sistema BMC (SEL) y los mensajes del registro. |
| [Eventos](events.md)                                                                                                             | No puede obtener eventos a través de scripting de WinRM, pero puede usar la herramienta Wevtutil.exe línea de comandos para ver los eventos [del recopilador de](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) eventos.                                                                                                                                                                                        |



 

 

 