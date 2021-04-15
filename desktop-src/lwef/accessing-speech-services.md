---
title: Acceso a Speech Services (interfaz de Microsoft Agent Server)
description: Acceso a servicios de voz
ms.assetid: 99cf630d-3bd1-403a-833a-9173a84fe3c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda1369fa83c5e8ffaf7f08317f69a2a569620f3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695838"
---
# <a name="accessing-speech-services-microsoft-agent-server-interface"></a>Acceso a Speech Services (interfaz de Microsoft Agent Server)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Aunque los servicios del agente de Microsoft incluyen compatibilidad con la entrada de voz, se debe instalar un motor de reconocimiento de voz de comando y control compatible para tener acceso a los servicios de entrada de voz del agente. Del mismo modo, si desea utilizar los servicios de voz de Microsoft Agent para admitir la salida de voz sintetizada de un carácter, debe instalar un motor de voz de texto a voz (TTS) compatible para su carácter. Dado que los servicios de voz de Microsoft Agent se basan en Microsoft Speech API (SAPI), puede usar cualquier motor compatible con las interfaces de voz necesarias.

Para habilitar la compatibilidad con la entrada de voz en la aplicación, defina un objeto de [**comando**](https://www.bing.com/search?q=**Command**) y establezca su propiedad [**Voice**](https://www.bing.com/search?q=**Voice**) . El agente de Microsoft cargará automáticamente los servicios de voz, de modo que cuando el usuario presione la tecla de escucha o llame a [**Listen**](https://www.bing.com/search?q=**Listen**), se cargará el motor de reconocimiento de voz. De forma predeterminada, el identificador de idioma del carácter determinará qué motor se carga. El agente intenta cargar el primer motor que SAPI devuelve como coincidencia con este idioma. Use [**IAgentCharacterEx:: SetSRModeID**](IAgentCharacterEx::SetSRModeID) si desea cargar un motor específico.

Para habilitar la salida de texto a voz, use el método [**Speak**](https://www.bing.com/search?q=**Speak**) . El agente de Microsoft intentará cargar automáticamente un motor que coincida con el identificador de idioma del carácter. Si la definición del carácter incluye un identificador de modo de motor TTS específico y dicho motor está disponible y coincide con el identificador de idioma del carácter, el agente carga dicho motor para el carácter. Si no es así, el agente carga el primer motor TTS que SAPI devuelve como coincidencia con la configuración de idioma del carácter. También puede usar [**IAgentCharacterEx:: SetTTSModeID**](IAgentCharacterEx::SetTTSModeID) para cargar un motor específico.

Normalmente, el agente de Microsoft carga un motor de reconocimiento de voz cuando se inicia el modo de escucha y carga un motor de texto a voz cuando se llama por primera vez a [**Speak**](https://www.bing.com/search?q=**Speak**) . Sin embargo, si desea cargar previamente el motor de voz, puede hacerlo consultando las propiedades relacionadas con las interfaces de voz. Por ejemplo, si se llama a [**IAgentCharacterEx:: GetSRModeID**](IAgentCharacterEx::GetSRModeID) o [**IAgentCharacterEx:: GetTTSModeID**](IAgentCharacterEx::GetTTSModeID) , se intentará cargar ese tipo de motor.

 

 




