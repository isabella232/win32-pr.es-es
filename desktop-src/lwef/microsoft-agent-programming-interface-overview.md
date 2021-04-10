---
title: Introducción a la interfaz de programación de Microsoft Agent
description: Introducción a la interfaz de programación de Microsoft Agent
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89249e064eb89d37f497fb79cb8982c79cb83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903509"
---
# <a name="microsoft-agent-programming-interface-overview"></a>Introducción a la interfaz de programación de Microsoft Agent

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

La API del agente de Microsoft proporciona servicios que admiten la visualización y animación de caracteres animados. Microsoft Agent, que se implementa como un servidor de automatización OLE (modelo de objetos componentes \[ com \] ), permite que varias aplicaciones, denominadas clientes o aplicaciones cliente, hospeden y accedan a sus servicios de animación, entrada y salida al mismo tiempo. Un cliente puede ser cualquier aplicación que se conecte a las interfaces COM de Microsoft Agent.

Como servidor COM, el agente de Microsoft se inicia automáticamente solo cuando una aplicación cliente usa las interfaces COM y las solicitudes para conectarse a él. Sigue ejecutándose hasta que todos los clientes cierren sus conexiones. Cuando no quedan clientes conectados, el agente de Microsoft se cierra automáticamente.

Aunque puede llamar directamente a las interfaces COM de Microsoft Agent, el agente de Microsoft también incluye un control ActiveX de Microsoft. Este control facilita el acceso a los servicios de Microsoft Agent desde lenguajes de programación que admiten la interfaz de control ActiveX.

Además de admitir programas independientes escritos para Windows, el agente puede incluirse en scripts para admitir páginas web, siempre que el explorador admita la interfaz ActiveX. Microsoft Internet Explorer incluye compatibilidad con ActiveX, así como con lenguajes de scripting que puede usar para programar el agente. Si no está usando Internet Explorer, consulte con su proveedor o proveedor la compatibilidad del explorador con ActiveX.

La siguiente información proporciona una breve introducción a las interfaces de programación para el software de agente de Microsoft.

-   [Servicios de animación](animation-services.md)
-   [Servicios de entrada](input-services.md)
-   [Ventana comandos de voz](the-voice-commands-window.md)
-   [Servicios de salida](output-services.md)

 

 




