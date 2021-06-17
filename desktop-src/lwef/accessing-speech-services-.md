---
title: Acceso a servicios de Voz (Control de Microsoft Agent)
description: Obtenga información sobre el acceso a los servicios de voz con Microsoft Agent Control. Microsoft Agent está en desuso a partir de Windows 7.
ms.assetid: c6c10f2a-a433-4a8e-a069-48e3c2032fb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035bde03d18b77ce43c47375f2075bba02416c39
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262717"
---
# <a name="accessing-speech-services-microsoft-agent-control"></a>Acceso a servicios de Voz (Control de Microsoft Agent)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Aunque los servicios de Microsoft Agent incluyen compatibilidad con la entrada de voz, se debe instalar un motor de reconocimiento de voz compatible con comandos y controles para acceder a los servicios de entrada de voz del Agente. Del mismo modo, si desea usar los servicios de voz de Microsoft Agent para admitir la salida de voz sintetizada para un carácter, debe instalar un motor de voz de texto a voz (TTS) compatible para el carácter.

Para habilitar la compatibilidad con la entrada de voz en la aplicación, defina un [**objeto Command**](https://www.bing.com/search?q=**Command**) y establezca su [**propiedad Voice.**](https://www.bing.com/search?q=**Voice**) El agente cargará automáticamente los servicios de voz, de modo que cuando el usuario presione la tecla Escuchando o llame a [**Escucha,**](https://www.bing.com/search?q=**Listen**)se cargará el motor de reconocimiento de voz. De forma predeterminada, [**languageID**](https://www.bing.com/search?q=**LanguageID**) del carácter determinará qué motor se carga. El agente intenta cargar el primer motor que Microsoft Speech API (SAPI) devuelve como que coincide con este lenguaje. Use [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) si desea cargar un motor específico.

Para habilitar la salida de texto a voz, use el [**método Speak.**](https://www.bing.com/search?q=**Speak**) El Agente intentará cargar automáticamente un motor que coincida con el [**LanguageID del carácter.**](https://www.bing.com/search?q=**LanguageID**) Si la definición del carácter incluye un identificador de modo de motor TTS específico y ese motor está disponible y coincide con el **LanguageID** del carácter, el Agente carga ese motor para el carácter. Si no es así, carga el primer motor de TTS que devuelve SAPI como que coincide con la configuración de idioma del carácter. También puede usar [**TTSModeID para**](https://www.bing.com/search?q=**TTSModeID**) cargar un motor específico.

Normalmente, el Agente carga el reconocimiento de voz cuando se inicia el modo de escucha y un motor de texto a voz cuando se llama por primera vez a [**Speak.**](https://www.bing.com/search?q=**Speak**) Sin embargo, si desea cargar previamente el motor de voz, consulte las propiedades relacionadas con las interfaces de voz. Por ejemplo, al consultar [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) o [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) se intentará cargar ese tipo de motor.

Dado que los servicios de voz de Microsoft Agent se basan en microsoft Speech API, puede usar cualquier motor que admita las interfaces de voz necesarias.

 

 




