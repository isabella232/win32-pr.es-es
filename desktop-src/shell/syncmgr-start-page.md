---
description: Synchronization Manager proporciona una tecnología centralizada y estándar para sincronizar archivos para su uso sin conexión en un equipo móvil o un equipo conectado a una red de área local.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571480"
---
# <a name="synchronization-manager"></a>administrador de sincronización

## <a name="purpose"></a>Propósito

Synchronization Manager proporciona una tecnología centralizada y estándar para sincronizar archivos para su uso sin conexión en un equipo móvil o un equipo conectado a una red de área local. Junto con las funciones de conectividad, las notificaciones (Servicio de notificación de eventos del sistema) y el almacenamiento en caché del lado cliente, Synchronization Manager proporciona una infraestructura para admitir la informática móvil. En lugar de que cada aplicación implemente su propia tecnología para almacenar en caché y sincronizar recursos de red para su uso local, el sistema operativo proporciona un modelo integrado que todas las aplicaciones pueden usar. Los archivos se sincronizan independientemente del protocolo. Por ejemplo, un programa de correo electrónico puede transferir sus mensajes mediante SMTP, NMTP o POP3, mientras que un explorador puede usar HTTP y una base de datos puede usar la llamada a procedimiento remoto (RPC) (RPC). Los desarrolladores pueden usar la interfaz común del Administrador de sincronización en sus aplicaciones para sincronizar archivos entre el equipo local del usuario y el almacenamiento de red.

## <a name="where-applicable"></a>Donde sea aplicable

Synchronization Manager está pensado para aplicaciones que se ejecutan principalmente en equipos móviles. Las aplicaciones que se ejecutan en equipos conectados a redes de área local de alta latencia también pueden beneficiarse del uso de Synchronization Manager.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Este documento está destinado a desarrolladores de software que desarrollan aplicaciones para la informática móvil y redes de área local de alta latencia. En este documento se proporciona una referencia completa de todas las partes del Administrador de sincronización, incluidos los métodos e interfaces del Administrador de sincronización.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Requiere Windows Server 2003, Windows XP, Windows 2000 o Windows Millennium Edition (Windows Me). También está disponible como redistribuible para Microsoft Windows NT 4.0, Windows 98 y Windows 95.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                                                                                                         |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca del Administrador de sincronización](syncmgr-about.md)<br/>                               | Synchronization Manager proporciona una tecnología centralizada y estándar para sincronizar archivos para su uso sin conexión en un equipo local.<br/>     |
| [Configuraciones de informática móvil](syncmgr-mobile-computing-configs.md)<br/>          | Las aplicaciones pueden usar Sychronization Manager para mantener los archivos y recursos almacenados en caché localmente y sincronizados en equipos móviles y de escritorio.<br/> |
| [Escenarios de aplicación](syncmgr-app-scenarios.md)<br/>                               | Aplicaciones y servicios que pueden usar Synchronization Manager.<br/>                                                                          |
| [Arquitectura de Synchronization Manager](syncmgr-architecture.md)<br/>                 |                                                                                                                                                     |
| [Uso del Administrador de sincronización desde un programa](syncmgr-using-from-a-program.md)<br/> |                                                                                                                                                     |
| [Referencia de Synchronization Manager](syncmgr-reference.md)<br/>                       | Los siguientes elementos de programación son la API de Synchronization Manager.<br/>                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del servicio de notificación de eventos del sistema](../sens/about-system-event-notification-service.md)
</dt> </dl>

 

 
