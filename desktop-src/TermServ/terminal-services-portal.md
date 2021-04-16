---
title: Servicios de Escritorio remoto (Servicios de Escritorio remoto)
description: Escritorio remoto de Microsoft Services es un software de acceso de equipo remoto que admite el acceso al escritorio remoto. Servicios de Escritorio remoto conecta varios clientes a un servidor host de sesión Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: 90c40b7a-e324-43fc-a1e6-f29997ed9436
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Servicios de Escritorio remoto, Página principal
- Terminal Services vea Servicios de Escritorio remoto Servicios de Escritorio remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f39e176473c98f1e240d58592463df749a95f939
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105685838"
---
# <a name="remote-desktop-services-remote-desktop-services"></a>Servicios de Escritorio remoto (Servicios de Escritorio remoto)

## <a name="purpose"></a>Propósito

Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008 con Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) permiten a un servidor hospedar varias sesiones de cliente simultáneas. Escritorio remoto usa Servicios de Escritorio remoto tecnología para permitir que una sola sesión se ejecute de forma remota. Un usuario puede conectarse a Escritorio remoto un servidor host de sesión de escritorio remoto (host de sesión de RD) (conocido anteriormente como Terminal Server) mediante el software cliente de Conexión a Escritorio remoto (RDC). La Conexión web a Escritorio remoto extiende Servicios de Escritorio remoto tecnología a la Web.

> [!Note]  
> Este tema está destinado a los desarrolladores de software. Si busca información de usuario para conexiones Escritorio remoto, consulte [conexión a escritorio remoto: preguntas más](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8)frecuentes.

 

## <a name="where-applicable"></a>Donde sea aplicable

Un cliente Conexión a Escritorio remoto (RDC) puede existir en una variedad de formas. Los dispositivos de hardware de cliente ligero que ejecutan un sistema operativo basado en Windows incrustado pueden ejecutar el software cliente de RDC para conectarse a un servidor host de sesión de escritorio remoto. Los equipos basados en Windows, Macintosh o UNIX pueden ejecutar el software cliente de RDC para conectarse a un servidor host de sesión de escritorio remoto con el fin de mostrar aplicaciones basadas en Windows. Esta combinación de clientes de RDC proporciona acceso a las aplicaciones basadas en Windows desde prácticamente cualquier sistema operativo.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Los desarrolladores que usan Servicios de Escritorio remoto deben estar familiarizados con los lenguajes de programación C y C++ y el entorno de programación basado en Windows. Es necesario estar familiarizado con la arquitectura cliente/servidor. El Conexión web a Escritorio remoto incluye interfaces que admiten scripts para crear e implementar canales virtuales con scripts en Servicios de Escritorio remoto aplicaciones Web.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Las aplicaciones que usan Servicios de Escritorio remoto requieren Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 o Windows Vista. Para usar la funcionalidad de Conexión web a Escritorio remoto, la aplicación cliente de Servicios de Escritorio remoto requiere Internet Explorer y una conexión a la World Wide Web. Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, vea la sección de requisitos de la página de referencia de ese elemento.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Escritorio remoto control ActiveX](remote-desktop-activex-control.md)
</dt> <dd>

Describe cómo utilizar el control ActiveX Escritorio remoto.

</dd> <dt>

[API del proveedor de Protocolo de escritorio remoto](custom-remote-desktop-protocols.md)
</dt> <dd>

La API de proveedor de Protocolo de escritorio remoto se usa para crear un protocolo que proporcione comunicación entre el servicio Servicios de Escritorio remoto y varios clientes.

</dd> <dt>

[Servicios de Escritorio remoto canales virtuales](terminal-services-virtual-channels.md)
</dt> <dd>

Los *canales virtuales* son extensiones de software que se pueden usar para agregar mejoras funcionales a una aplicación servicios de escritorio remoto.

</dd> <dt>

[API de redirección de medios RemoteFX](remotefx-api.md)
</dt> <dd>

La API de redirección de medios RemoteFX se usa en una sesión de Escritorio remoto para identificar las áreas del servidor que muestran contenido de cambio rápido, como el vídeo. Este contenido se puede codificar en vídeo y enviarse al cliente en formato codificado.

</dd> <dt>

[API de cliente de Conexión a Escritorio remoto Broker](connection-broker-client-api.md)
</dt> <dd>

Describe cómo usar la API de cliente de Conexión a Escritorio remoto Broker.

</dd> <dt>

[Referencia de API del agente de tareas de escritorio personal](task-agent-api-reference.md)
</dt> <dd>

Personal Desktop Task Agent API se utiliza para controlar las actualizaciones programadas en un escritorio virtual personal.

</dd> <dt>

[Acerca de Servicios de Escritorio remoto](about-terminal-services.md)
</dt> <dd>

Servicios de Escritorio remoto (antes conocido como Terminal Services) proporciona una funcionalidad similar a un entorno de host, centralizado, o de gran sistema (mainframe) en el que varios terminales se conectan a un equipo host.

</dd> <dt>

[Proveedor de servicios de administración de Escritorio remoto](rdms-api-reference.md)
</dt> <dd>

El proveedor de servicios de administración de Escritorio remoto (RDMS) administra los entornos de infraestructura de escritorio virtual (VDI).

</dd> <dt>

[Referencia de Servicios de Escritorio remoto](terminal-services-reference.md)
</dt> <dd>

Documentación de los métodos de propiedad que puede usar para examinar y configurar Servicios de Escritorio remoto propiedades de usuario. También se documentan las funciones, estructuras y Conexión web a Escritorio remoto las interfaces que admiten scripts. Servicios de Escritorio remoto

</dd> <dt>

[Teclas de método abreviado Servicios de Escritorio remoto](terminal-services-shortcut-keys.md)
</dt> <dd>

Una lista de las teclas de método abreviado Servicios de Escritorio remoto.

</dd> <dt>

[Servicios de Escritorio remoto proveedor WMI](terminal-services-wmi-provider.md)
</dt> <dd>

El proveedor WMI de Servicios de Escritorio remoto proporciona acceso mediante programación a la información y la configuración que se exponen en el complemento configuración/conexiones de Microsoft Management Console (MMC) de Servicios de Escritorio remoto.

</dd> <dt>

[Usar Servicios de Escritorio remoto](using-terminal-services.md)
</dt> <dd>

Cómo programar en el entorno de Servicios de Escritorio remoto y cómo extender la tecnología de Servicios de Escritorio remoto (antes conocida como Terminal Services) a la web mediante el uso de Conexión web a Escritorio remoto.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Terminal Services es ahora Servicios de Escritorio remoto](terminal-services-is-now-remote-desktop-services.md)
</dt> </dl>

 

 




