---
title: Administración remota de Windows
description: Windows Administración remota (Windows Remote Management) es la implementación de Microsoft de WS-Management Protocol, un protocolo estándar basado en SOAP y compatible con el firewall que permite la interoperabilidad de hardware y sistemas operativos, de distintos proveedores.
ms.assetid: 6429e748-e0bf-431a-8989-db5b211665d5
ms.tgt_platform: multiple
keywords:
- Windows Administración remota (WinRM), página de inicio
- WS-Management
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbOrient
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c816e3f7092fc7825407497793ed529df13cf9115426b63e4b535bd019f81df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858765"
---
# <a name="windows-remote-management"></a>Administración remota de Windows

## <a name="purpose"></a>Propósito

La Administración remota de Windows (WinRM) es la implementación de Microsoft del [Protocolo WS-Management](ws-management-protocol.md), un protocolo estándar compatible con firewall y basado en el Protocolo simple de acceso a objetos (SOAP) que permite que interoperen el hardware y los sistemas operativos de diferentes proveedores.

La especificación WS-Management protocolo proporciona una manera común para que los sistemas accedan a la información de administración de una infraestructura de TI e intercamba información de administración a través de ella. WinRM e [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md), junto con el recopilador de eventos son componentes de las características Windows administración de [hardware.](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) [](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10))

## <a name="where-applicable"></a>Donde sea aplicable

Puedes usar objetos de scripting de WinRM, la herramienta de línea de comandos WinRM o la herramienta de línea de comandos winRS de Windows Remote Shell para obtener datos de administración de equipos locales y remotos que pueden tener controladores de administración de placa base [*(BMC).*](windows-remote-management-glossary.md) Si el equipo ejecuta una versión Windows sistema operativo basada en el sistema operativo que incluye WinRM, los datos de administración se proporcionan mediante [Windows Management Instrumentation (WMI).](/windows/desktop/WmiSdk/wmi-start-page)

También puede obtener datos del hardware y del sistema a partir de las implementaciones del protocolo WS-Management que se ejecuten en sistemas operativos diferentes de Windows en su empresa. WinRM establece una sesión con un equipo remoto a través del protocolo WS-Management basado en SOAP, en lugar de una conexión a través de DCOM, como hace WMI. Los datos devueltos por el protocolo WS-Management tienen formato XML, en lugar de formato de objeto.

El proveedor WMI de interfaz de administración de plataforma inteligente [(IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) es un proveedor WMI estándar con clases que obtienen datos del sensor BMC de equipos con el hardware adecuado. Se puede acceder a los datos IPMI mediante la API de scripting de WinRM, el [scripting WMI](/windows/desktop/WmiSdk/scripting-api-for-wmi)o las [API COM.](/windows/desktop/WmiSdk/com-api-for-wmi)

## <a name="developer-audience"></a>Audiencia de desarrolladores

El público desarrollador es el equipo de TI Pro que escribe scripts para automatizar la administración de servidores o el desarrollador de ISV que obtiene datos para aplicaciones de administración.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

WinRM forma parte del sistema operativo. Sin embargo, para obtener datos de equipos remotos, debe configurar un agente de [*escucha*](windows-remote-management-glossary.md#l)de WinRM . Para obtener más información, [vea Instalación y configuración de Windows Administración remota.](installation-and-configuration-for-windows-remote-management.md) Si se detecta un BMC al iniciar el sistema, se carga el proveedor de IPMI; De lo contrario, los objetos de scripting de WinRM y la herramienta de línea de comandos winRM siguen estando disponibles.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Acerca de Windows administración remota](about-windows-remote-management.md)
</dt> <dd>

Vínculo a la especificación WS-Management de protocolo público, la arquitectura winRM, la relación con WMI, la administración de hardware con el proveedor de IPMI, la configuración y la instalación.

</dd> <dt>

[Uso de Windows administración remota](using-windows-remote-management.md)
</dt> <dd>

Introducción al uso de la API de scripting de WinRM y la administración de hardware.

</dd> <dt>

[Windows Referencia de administración remota](windows-remote-management-reference.md)
</dt> <dd>

Lista de interfaces de scripting definidas por automatización de servicios web de Microsoft (WS-Management) y definiciones de clases de las clases WMI creadas por el proveedor de IPMI y las clases que se comunican con el controlador IPMI para obtener datos del controlador de administración de placa [base (BMC).](windows-remote-management-glossary.md)

</dd> </dl>

 

 