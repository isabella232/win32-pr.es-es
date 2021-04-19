---
title: Acceso a servicios de voz (interfaz del servidor de Microsoft Agent)
description: Acceso a servicios de voz
ms.assetid: 99cf630d-3bd1-403a-833a-9173a84fe3c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eeb4afb2b05ca13c52d49508c3c25b7e02da676
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380809"
---
# <a name="accessing-speech-services-microsoft-agent-server-interface"></a>Acceso a servicios de voz (interfaz del servidor de Microsoft Agent)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Aunque los servicios de Microsoft Agent incluyen compatibilidad con la entrada de voz, se debe instalar un motor de reconocimiento de voz compatible con comandos y controles para acceder a los servicios de entrada de voz del Agente. Del mismo modo, si desea usar los servicios de voz de Microsoft Agent para admitir la salida de voz sintetizada para un carácter, debe instalar un motor de voz de texto a voz (TTS) compatible para el carácter. Dado que los servicios de voz de Microsoft Agent se basan en Microsoft Speech API (SAPI), puede usar cualquier motor que admita las interfaces de voz necesarias.

Para habilitar la compatibilidad con la entrada de voz en la aplicación, defina un [**objeto Command**](https://www.bing.com/search?q=**Command**) y establezca su [**propiedad Voice.**](https://www.bing.com/search?q=**Voice**) Microsoft Agent cargará automáticamente los servicios de voz, de modo que cuando el usuario presione la tecla Listening o llame a [**Listen**](https://www.bing.com/search?q=**Listen**), se cargará el motor de reconocimiento de voz. De forma predeterminada, el identificador de idioma del carácter determinará qué motor se carga. El agente intenta cargar el primer motor que devuelve SAPI como que coincide con este lenguaje. Use **IAgentCharacterEx::SetSRModeID** si desea cargar un motor específico.

Para habilitar la salida de texto a voz, use el [**método Speak.**](https://www.bing.com/search?q=**Speak**) Microsoft Agent intentará cargar automáticamente un motor que coincida con el identificador de idioma del carácter. Si la definición del carácter incluye un identificador de modo de motor TTS específico y ese motor está disponible y coincide con el identificador de idioma del carácter, el Agente carga ese motor para el carácter. Si no es así, el Agente carga el primer motor de TTS que SAPI devuelve como que coincide con la configuración de idioma del carácter. También puede usar **IAgentCharacterEx::SetTTSModeID para** cargar un motor específico.

Normalmente, Microsoft Agent carga un motor de reconocimiento de voz cuando se inicia el modo de escucha y carga un motor de texto a voz cuando se llama por primera vez a [**Speak.**](https://www.bing.com/search?q=**Speak**) Sin embargo, si desea cargar previamente el motor de voz, puede hacerlo consultando las propiedades relacionadas con las interfaces de voz. Por ejemplo, si se **llama a IAgentCharacterEx::GetSRModeID** o **IAgentCharacterEx::GetTTSModeID,** se intentará cargar ese tipo de motor.

 

 




