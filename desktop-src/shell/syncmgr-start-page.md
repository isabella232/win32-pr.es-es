---
description: El administrador de sincronización proporciona una tecnología centralizada y estándar para sincronizar archivos para su uso sin conexión en un equipo móvil o en un equipo conectado a una red de área local.
title: administrador de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6cdac7e5-8985-407a-98bb-936bb20ed069
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbOrient
ms.openlocfilehash: 2fc56b2afec4fdedf98fe213437a27f2592ce72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997760"
---
# <a name="synchronization-manager"></a>administrador de sincronización

## <a name="purpose"></a>Propósito

El administrador de sincronización proporciona una tecnología centralizada y estándar para sincronizar archivos para su uso sin conexión en un equipo móvil o en un equipo conectado a una red de área local. Junto con las funciones de conectividad, las notificaciones (servicio de notificación de eventos del sistema) y el almacenamiento en caché del lado cliente, el administrador de sincronización proporciona una infraestructura para admitir la informática móvil. En lugar de cada aplicación que implementa su propia tecnología para almacenar en caché y sincronizar los recursos de red para uso local, el sistema operativo proporciona un modelo integrado que todas las aplicaciones pueden usar. Los archivos se sincronizan independientemente del protocolo. Por ejemplo, un programa de correo electrónico puede transferir sus mensajes mediante SMTP, NMTP o POP3, mientras que un explorador puede utilizar HTTP y una base de datos puede usar la llamada a procedimiento remoto (RPC). Los desarrolladores pueden usar la interfaz común para el administrador de sincronización en sus aplicaciones para sincronizar archivos entre el equipo local del usuario y el almacenamiento de red.

## <a name="where-applicable"></a>Donde sea aplicable

El administrador de sincronización está diseñado para aplicaciones que se ejecutan principalmente en equipos móviles. Las aplicaciones que se ejecutan en equipos conectados a redes de área local de latencia alta también pueden beneficiarse del uso del administrador de sincronización.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Este documento está destinado a los desarrolladores de software que desarrollan aplicaciones para la informática móvil y redes de área local de latencia alta. En este documento se proporciona una referencia completa de todas las partes del administrador de sincronización, incluidos los métodos e interfaces para el administrador de sincronización.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Requiere Windows Server 2003, Windows XP, Windows 2000 o Windows Millennium Edition (Windows me). También está disponible como paquete redistribuible para Microsoft Windows NT 4,0, Windows 98 y Windows 95.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                                                                                                         |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca del administrador de sincronización](syncmgr-about.md)<br/>                               | El administrador de sincronización proporciona una tecnología centralizada y estándar para sincronizar archivos para su uso sin conexión en un equipo local.<br/>     |
| [Configuraciones de informática móvil](syncmgr-mobile-computing-configs.md)<br/>          | Las aplicaciones pueden usar sincronización Manager para mantener los archivos y los recursos almacenados en caché localmente y sincronizados en equipos de escritorio y móviles.<br/> |
| [Escenarios de aplicación](syncmgr-app-scenarios.md)<br/>                               | Aplicaciones y servicios que pueden usar el administrador de sincronización.<br/>                                                                          |
| [Arquitectura del administrador de sincronización](syncmgr-architecture.md)<br/>                 |                                                                                                                                                     |
| [Usar el administrador de sincronización desde un programa](syncmgr-using-from-a-program.md)<br/> |                                                                                                                                                     |
| [Referencia del administrador de sincronización](syncmgr-reference.md)<br/>                       | Los siguientes elementos de programación componen la API para el administrador de sincronización.<br/>                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del servicio de notificación de eventos del sistema](../sens/about-system-event-notification-service.md)
</dt> </dl>

 

 
