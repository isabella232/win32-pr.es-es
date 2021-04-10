---
title: Administración remota de Windows
description: Administración remota de Windows (Administración remota de Windows) es la implementación de Microsoft de WS-Management protocolo, un protocolo estándar basado en SOAP y compatible con firewall que permite que interoperen el hardware y los sistemas operativos de diferentes proveedores.
ms.assetid: 6429e748-e0bf-431a-8989-db5b211665d5
ms.tgt_platform: multiple
keywords:
- Administración remota de Windows (WinRM), página de inicio
- WS-Management
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbOrient
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27311699fe0321eddc1d3117b17acf3e49e9d518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995286"
---
# <a name="windows-remote-management"></a>Administración remota de Windows

## <a name="purpose"></a>Propósito

La Administración remota de Windows (WinRM) es la implementación de Microsoft del [Protocolo WS-Management](ws-management-protocol.md), un protocolo estándar compatible con firewall y basado en el Protocolo simple de acceso a objetos (SOAP) que permite que interoperen el hardware y los sistemas operativos de diferentes proveedores.

La especificación del protocolo WS-Management proporciona una manera común de que los sistemas tengan acceso a la información de administración de una infraestructura de ti y la intercambie. WinRM y la [*interfaz de administración de plataforma inteligente (IPMI)*](windows-remote-management-glossary.md), junto con el [recopilador de eventos](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) , son componentes de las características de administración de hardware de [Windows](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) .

## <a name="where-applicable"></a>Donde sea aplicable

Puede usar objetos de scripting de WinRM, la herramienta de línea de comandos de WinRM o la herramienta de línea de comandos de shell remoto de Windows WinRS para obtener datos de administración de equipos locales y remotos que pueden tener [*controladores de administración de placa base (BMC)*](windows-remote-management-glossary.md). Si el equipo ejecuta una versión de sistema operativo basada en Windows que incluye WinRM, [instrumental de administración de Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page)proporciona los datos de administración.

También puede obtener datos del hardware y del sistema a partir de las implementaciones del protocolo WS-Management que se ejecuten en sistemas operativos diferentes de Windows en su empresa. WinRM establece una sesión con un equipo remoto a través del protocolo WS-Management basado en SOAP, en lugar de una conexión a través de DCOM, como hace WMI. Los datos devueltos por el protocolo WS-Management tienen formato XML, en lugar de formato de objeto.

El proveedor WMI de [interfaz de administración de plataforma inteligente (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) es un proveedor de WMI estándar con clases que obtienen datos del sensor de BMC de equipos con el hardware adecuado. Se puede tener acceso a los datos de IPMI mediante la API de scripting de WinRM, el [scripting](/windows/desktop/WmiSdk/scripting-api-for-wmi)de WMI o las API de [com](/windows/desktop/WmiSdk/com-api-for-wmi) .

## <a name="developer-audience"></a>Audiencia de desarrolladores

El público del desarrollador es el profesional de ti que escribe scripts para automatizar la administración de servidores o el desarrollador de ISV que obtiene los datos para las aplicaciones de administración.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

WinRM forma parte del sistema operativo. Sin embargo, para obtener datos de equipos remotos, debe configurar un [*agente de escucha*](windows-remote-management-glossary.md#l)de WinRM. Para obtener más información, vea [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md). Si se detecta un BMC al iniciar el sistema, se carga el proveedor IPMI; de lo contrario, los objetos de scripting de WinRM y la herramienta de línea de comandos de WinRM seguirán estando disponibles.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Acerca de Administración remota de Windows](about-windows-remote-management.md)
</dt> <dd>

Vínculo a la especificación del protocolo público WS-Management, la arquitectura de WinRM, la relación con WMI, la administración de hardware con el proveedor IPMI, la configuración y la instalación.

</dd> <dt>

[Usar Administración remota de Windows](using-windows-remote-management.md)
</dt> <dd>

Introducción al uso de la API de scripting de WinRM y la administración de hardware.

</dd> <dt>

[Referencia de Administración remota de Windows](windows-remote-management-reference.md)
</dt> <dd>

Lista de interfaces de scripting definidas por los servicios Web de Microsoft para la automatización de administración (WS-Management) y las definiciones de clase de las clases WMI creadas por el proveedor IPMI y las clases que se comunican con el controlador IPMI para obtener los datos del [controlador de administración de placa base (BMC)](windows-remote-management-glossary.md) .

</dd> </dl>

 

 