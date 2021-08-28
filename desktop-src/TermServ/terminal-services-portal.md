---
title: Servicios de Escritorio remoto (Servicios de Escritorio remoto)
description: Escritorio remoto de Microsoft Los servicios son software de acceso a equipos remotos que admite el acceso a Escritorio remoto. Servicios de Escritorio remoto conecta varios clientes a un Escritorio remoto host de sesión de escritorio remoto.
ms.assetid: 90c40b7a-e324-43fc-a1e6-f29997ed9436
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto
- Servicios de Escritorio remoto Servicios de Escritorio remoto , página principal
- Terminal Services Consulte Servicios de Escritorio remoto Servicios de Escritorio remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525f62433c10c8c4f750a8ae1abbfa9496f2f096139c182a677c9dbf69ce4a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999915"
---
# <a name="remote-desktop-services-remote-desktop-services"></a>Servicios de Escritorio remoto (Servicios de Escritorio remoto)

## <a name="purpose"></a>Propósito

Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008 con Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) permiten a un servidor hospedar varias sesiones de cliente simultáneas. Escritorio remoto usa Servicios de Escritorio remoto tecnología para permitir que una sola sesión se ejecute de forma remota. Un usuario puede conectarse a un servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto) (anteriormente conocido como servidor de terminal) mediante el software cliente Conexión a Escritorio remoto (RDC). El Conexión web a Escritorio remoto extiende Servicios de Escritorio remoto tecnología a la Web.

> [!Note]  
> Este tema está disponible para desarrolladores de software. Si busca información de usuario para las conexiones Escritorio remoto, consulte [Conexión a Escritorio remoto: preguntas más frecuentes](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).

 

## <a name="where-applicable"></a>Donde sea aplicable

Puede Conexión a Escritorio remoto cliente de Conexión a Escritorio remoto (RDC) en una variedad de formas. Los dispositivos de hardware de cliente fino que ejecutan un sistema operativo Windows integrado pueden ejecutar el software cliente RDC para conectarse a un servidor host de sesión de Escritorio remoto. Windows equipos basados en UNIX, Macintosh o Macintosh pueden ejecutar software cliente RDC para conectarse a un servidor host de sesión de Escritorio remoto para mostrar Windows aplicaciones basadas en escritorio remoto. Esta combinación de clientes RDC proporciona acceso a Windows aplicaciones basadas en aplicaciones desde prácticamente cualquier sistema operativo.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Los desarrolladores que usan Servicios de Escritorio remoto deben estar familiarizados con los lenguajes de programación C y C++ y el Windows de programación basado en aplicaciones. Es necesario estar familiarizado con la arquitectura de cliente/servidor. El Conexión web a Escritorio remoto incluye interfaces que pueden incluirse en scripts para crear e implementar canales virtuales que pueden incluirse en scripts Servicios de Escritorio remoto web.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Las aplicaciones que usan Servicios de Escritorio remoto requieren Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 o Windows Vista. Para usar Conexión web a Escritorio remoto funcionalidad, la Servicios de Escritorio remoto cliente requiere Internet Explorer y una conexión a la World Wide Web. Para obtener información sobre los requisitos en tiempo de ejecución para un elemento de programación determinado, vea la sección Requisitos de la página de referencia de ese elemento.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Escritorio remoto ActiveX control](remote-desktop-activex-control.md)
</dt> <dd>

Describe cómo usar el control Escritorio remoto ActiveX control .

</dd> <dt>

[Protocolo de escritorio remoto Provider API](custom-remote-desktop-protocols.md)
</dt> <dd>

Use la API Protocolo de escritorio remoto provider para crear un protocolo que proporcione comunicación entre el servicio Servicios de Escritorio remoto y varios clientes.

</dd> <dt>

[Servicios de Escritorio remoto canales virtuales](terminal-services-virtual-channels.md)
</dt> <dd>

*Los canales* virtuales son extensiones de software que se pueden usar para agregar mejoras funcionales a una Servicios de Escritorio remoto aplicación.

</dd> <dt>

[RemoteFX API de redireccionamiento multimedia](remotefx-api.md)
</dt> <dd>

La REMOTEFX Media Redirection API se usa en una sesión de Escritorio remoto para identificar las áreas del servidor que muestran contenido que cambia rápidamente, como vídeo. A continuación, este contenido se puede codificar en vídeo y enviarse al cliente en formato codificado.

</dd> <dt>

[Conexión a Escritorio remoto API de cliente de Broker](connection-broker-client-api.md)
</dt> <dd>

Describe cómo usar la API de cliente Conexión a Escritorio remoto Broker.

</dd> <dt>

[Referencia de la API del agente de tareas de escritorio personal](task-agent-api-reference.md)
</dt> <dd>

La API del agente de tareas de escritorio personal se usa para controlar las actualizaciones programadas en un escritorio virtual personal.

</dd> <dt>

[Acerca de Servicios de Escritorio remoto](about-terminal-services.md)
</dt> <dd>

Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) proporciona una funcionalidad similar a un entorno basado en terminal, host centralizado o sistema central, en el que varios terminales se conectan a un equipo host.

</dd> <dt>

[Escritorio remoto Management Services Provider](rdms-api-reference.md)
</dt> <dd>

El Escritorio remoto Management Services (RDMS) administra entornos de infraestructura de escritorio virtual (VDI).

</dd> <dt>

[Servicios de Escritorio remoto referencia](terminal-services-reference.md)
</dt> <dd>

Documentación de los métodos de propiedad que puede usar para examinar y configurar Servicios de Escritorio remoto de usuario. Servicios de Escritorio remoto también se documentan las funciones, las estructuras Conexión web a Escritorio remoto las interfaces que pueden incluirse en scripts.

</dd> <dt>

[Servicios de Escritorio remoto teclas de método abreviado](terminal-services-shortcut-keys.md)
</dt> <dd>

Una lista de las teclas Servicios de Escritorio remoto método abreviado de teclado.

</dd> <dt>

[Servicios de Escritorio remoto proveedor WMI](terminal-services-wmi-provider.md)
</dt> <dd>

El Servicios de Escritorio remoto WMI proporciona acceso mediante programación a la información y la configuración expuestas por el complemento Servicios de Escritorio remoto Configuration/Connections Microsoft Management Console (MMC).

</dd> <dt>

[Uso de Servicios de Escritorio remoto](using-terminal-services.md)
</dt> <dd>

Cómo programar en el entorno de Servicios de Escritorio remoto y cómo extender la tecnología Servicios de Escritorio remoto (anteriormente conocida como Terminal Services) a la Web mediante Conexión web a Escritorio remoto.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Terminal Services ya está Servicios de Escritorio remoto](terminal-services-is-now-remote-desktop-services.md)
</dt> </dl>

 

 




