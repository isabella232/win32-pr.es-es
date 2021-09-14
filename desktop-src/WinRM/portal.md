---
title: Administración remota de Windows
description: Windows Administración remota (Windows Remote Management) es la implementación de Microsoft del protocolo WS-Management, un protocolo estándar basado en SOAP y compatible con el firewall que permite interoperar el hardware y los sistemas operativos, de distintos proveedores.
ms.assetid: 6429e748-e0bf-431a-8989-db5b211665d5
ms.tgt_platform: multiple
keywords:
- Windows Administración remota (WinRM), página de inicio
- WS-Management
ms.topic: article
ms.date: 09/10/2021
topic_type:
- kbOrient
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b0744e5ad50ac602071a946dab76a864684d7b60
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974803"
---
# <a name="windows-remote-management"></a>Administración remota de Windows

## <a name="what-is-winrm"></a>¿Qué es WinRM?

La Administración remota de Windows (WinRM) es la implementación de Microsoft del [Protocolo WS-Management](ws-management-protocol.md), un protocolo estándar compatible con firewall y basado en el Protocolo simple de acceso a objetos (SOAP) que permite que interoperen el hardware y los sistemas operativos de diferentes proveedores.

La WS-Management de protocolo proporciona una manera común para que los sistemas accedan a la información de administración e intercedánea a través de una infraestructura de TI. WinRM e [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md#i), junto con [el](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)#event-collector) recopilador de eventos son componentes de las características de administración [Windows hardware.](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10))

## <a name="where-can-i-use-winrm"></a>¿Dónde puedo usar WinRM?

Puedes usar objetos de scripting de WinRM, la herramienta de línea de comandos WinRM o la herramienta de línea de comandos winRS de Windows Remote Shell para obtener datos de administración de equipos locales y remotos que pueden tener controladores de administración de placa base [*(BMC).*](windows-remote-management-glossary.md) Si el equipo ejecuta una versión Windows sistema operativo basada en Windows que incluye WinRM, los datos de administración se proporcionan mediante [Windows Management Instrumentation (WMI).](/windows/desktop/WmiSdk/wmi-start-page)

También puede obtener datos del hardware y del sistema a partir de las implementaciones del protocolo WS-Management que se ejecuten en sistemas operativos diferentes de Windows en su empresa. WinRM establece una sesión con un equipo remoto a través del protocolo WS-Management basado en SOAP, en lugar de una conexión a través de DCOM, como hace WMI. Los datos devueltos por el protocolo WS-Management tienen formato XML, en lugar de formato de objeto.

El proveedor WMI de interfaz de administración de plataforma inteligente [(IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) es un proveedor WMI estándar con clases que obtienen datos del sensor BMC de equipos con el hardware adecuado. Se puede acceder a los datos IPMI mediante la API de scripting de WinRM, el [scripting WMI](/windows/desktop/WmiSdk/scripting-api-for-wmi)o las [API COM.](/windows/desktop/WmiSdk/com-api-for-wmi)

## <a name="who-is-this-for"></a>Quién es esto?

El público previsto para Windows Remote Management son los profesionales de TI, que escriben scripts para automatizar la administración de servidores, y los desarrolladores de ISV (proveedor de software independiente), que desean obtener datos para las aplicaciones de administración.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

WinRM forma parte del sistema operativo. Sin embargo, para obtener datos de equipos remotos, debe configurar un agente de [*escucha*](windows-remote-management-glossary.md#l)de WinRM . Para obtener más información, [vea Instalación y configuración de Windows Administración remota.](installation-and-configuration-for-windows-remote-management.md) Si se detecta un BMC al iniciar el sistema, se carga el proveedor de IPMI; De lo contrario, los objetos de scripting de WinRM y la herramienta de línea de comandos winRM siguen estando disponibles.

## <a name="learn-more"></a>Más información

[Acerca Windows administración remota](about-windows-remote-management.md)

Vínculo a la especificación WS-Management protocolo público, la arquitectura winRM, la relación con WMI, la administración de hardware con el proveedor IPMI, la configuración y la instalación.

[Uso de Windows administración remota](using-windows-remote-management.md)

Introducción al uso de la API de scripting de WinRM y la administración de hardware.

[Windows Referencia de administración remota](windows-remote-management-reference.md)

Lista de interfaces de scripting definidas por automatización de Servicios web de Microsoft para administración (WS-Management) y definiciones de clases de las clases WMI creadas por el proveedor de IPMI y las clases que se comunican con el controlador IPMI para obtener datos del controlador de administración de placa [base (BMC).](windows-remote-management-glossary.md)
