---
title: Introducción a la interfaz de programación de Microsoft Agent
description: Introducción a la interfaz de programación de Microsoft Agent
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4dc087064afb0e3beaaf97d987e496239d3fd378461acaf5601927ac6d929
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887925"
---
# <a name="microsoft-agent-programming-interface-overview"></a>Introducción a la interfaz de programación de Microsoft Agent

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Microsoft Agent API proporciona servicios que admiten la presentación y animación de caracteres animados. Implementado como un servidor DE AUTOMATIZACIÓN OLE (Modelo de objetos componentes COM), Microsoft Agent permite que varias aplicaciones, denominadas aplicaciones cliente o clientes, aloen y accedan a sus servicios de animación, entrada y salida \[ \] al mismo tiempo. Un cliente puede ser cualquier aplicación que se conecte a las interfaces COM de Microsoft Agent.

Como servidor COM, Microsoft Agent se inicia automáticamente solo cuando una aplicación cliente usa las interfaces COM y las solicitudes para conectarse a él. Permanece en ejecución hasta que todos los clientes cierran sus conexiones. Cuando no quedan clientes conectados, Microsoft Agent se cierra automáticamente.

Aunque puede llamar directamente a las interfaces COM de Microsoft Agent, Microsoft Agent también incluye un control de ActiveX Microsoft. Este control facilita el acceso a los servicios de Microsoft Agent desde lenguajes de programación que admiten ActiveX interfaz de control.

Además de admitir programas independientes escritos para Windows, el Agente se puede incluir en scripts para admitir páginas web, siempre que el explorador admita la interfaz ActiveX usuario. Microsoft Internet Explorer compatibilidad con ActiveX, así como lenguajes de scripting que puede usar para programar el Agente. Si no usa Internet Explorer, consulte con su proveedor o proveedor la compatibilidad del explorador con ActiveX.

La siguiente información proporciona una breve introducción a las interfaces de programación para el software de Microsoft Agent.

-   [Servicios de animación](animation-services.md)
-   [Servicios de entrada](input-services.md)
-   [Ventana Comandos de voz](the-voice-commands-window.md)
-   [Servicios de salida](output-services.md)

 

 




