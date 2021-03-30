---
title: Acceso a Speech Services (control de Microsoft Agent)
description: Acceso a servicios de voz
ms.assetid: c6c10f2a-a433-4a8e-a069-48e3c2032fb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83459cfd7ee478fca7d2cf2d25c4c1d590d8ed54
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800895"
---
# <a name="accessing-speech-services-microsoft-agent-control"></a>Acceso a Speech Services (control de Microsoft Agent)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Aunque los servicios del agente de Microsoft incluyen compatibilidad con la entrada de voz, se debe instalar un motor de reconocimiento de voz de comando y control compatible para tener acceso a los servicios de entrada de voz del agente. Del mismo modo, si desea utilizar los servicios de voz de Microsoft Agent para admitir la salida de voz sintetizada de un carácter, debe instalar un motor de voz de texto a voz (TTS) compatible para su carácter.

Para habilitar la compatibilidad con la entrada de voz en la aplicación, defina un objeto de [**comando**](https://www.bing.com/search?q=**Command**) y establezca su propiedad [**Voice**](https://www.bing.com/search?q=**Voice**) . El agente cargará automáticamente Speech Services, de modo que cuando el usuario presione la tecla de escucha o llame a [**Listen**](https://www.bing.com/search?q=**Listen**), se cargará el motor de reconocimiento de voz. De forma predeterminada, el [**iddeidioma**](https://www.bing.com/search?q=**LanguageID**) del carácter determinará qué motor se ha cargado. El agente intenta cargar el primer motor que Microsoft Speech API (SAPI) devuelve como coincidencia con este idioma. Use [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) si desea cargar un motor específico.

Para habilitar la salida de texto a voz, use el método [**Speak**](https://www.bing.com/search?q=**Speak**) . El agente intentará cargar automáticamente un motor que coincida con el [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)del carácter. Si la definición del carácter incluye un identificador de modo de motor TTS específico y dicho motor está disponible y coincide con el **LanguageID** del carácter, el agente carga dicho motor para el carácter. Si no es así, carga el primer motor TTS que SAPI devuelve como coincidencia con la configuración de idioma del carácter. También puede usar [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) para cargar un motor específico.

Normalmente, el agente carga el reconocimiento de voz cuando se inicia el modo de escucha [**y se llama**](https://www.bing.com/search?q=**Speak**) por primera vez a un motor de conversión de texto a voz. Sin embargo, si desea cargar previamente el motor de voz, consulte las propiedades relacionadas con las interfaces de voz. Por ejemplo, si se consulta [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) o [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) , se intentará cargar ese tipo de motor.

Dado que los servicios de voz de Microsoft Agent se basan en Microsoft Speech API, puede usar los motores que admitan las interfaces de voz necesarias.

 

 




