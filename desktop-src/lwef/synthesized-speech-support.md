---
title: Compatibilidad con voz sintetizada
description: Compatibilidad con voz sintetizada
ms.assetid: 38172e04-a5b6-41e4-9d7c-539d9d4117be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a89610a912cf601724bc9a2153cba8343e6feb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075697"
---
# <a name="synthesized-speech-support"></a>Compatibilidad con voz sintetizada

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Si usa voz sintetizada, el carácter tiene la capacidad de decir prácticamente cualquier cosa, lo que proporciona la máxima flexibilidad. Con audio grabado, puede asignar al carácter una voz específica o única. Para especificar la salida, proporcione el texto hablado como parámetro del método [**Speak**](speak-method.md) .

Dado que la arquitectura de Microsoft Agent usa Microsoft SAPI para la salida de voz sintetizada, puede usar cualquier motor que se ajuste a esta especificación y admite la salida del alfabeto fonético internacional (IPA) mediante el método [**Visual**](https://www.bing.com/search?q=**Visual**) de la interfaz [**ITTSNotifySinkW**](ittsnotifysinkw.md) . Para obtener más información sobre el motor que requiere, vea [requisitos de compatibilidad del motor de voz](requirements-for-text-to-speech-engines.md).

El valor de identificador de idioma de un carácter determina su salida de TTS. Si un cliente no especifica un identificador de idioma para el carácter, el identificador de idioma del carácter se establece en el identificador de idioma predeterminado del usuario. Si la definición del carácter incluye un motor específico y dicho motor se puede cargar y coincide con la configuración de idioma del carácter, se usará dicho motor. De lo contrario, el agente de Microsoft enumera los demás motores disponibles y solicita una mejor coincidencia de SAPI según el idioma, el sexo y la edad (en ese orden). Si no hay ningún motor coincidente disponible, no hay ninguna salida de TTS para el uso que hace el cliente del carácter. El agente intenta cargar el motor TTS en la primera llamada de [**voz**](speak-method.md) o cuando se consulta o establece correctamente el identificador de modo.

Una aplicación cliente también puede especificar un motor TTS para su carácter (mediante la propiedad [**TTSModeID**](ttsmodeid-property.md) ). Esto invalida el intento del servidor de buscar automáticamente un motor de coincidencia en función del identificador de modo TTS preferido del carácter o la configuración del identificador de idioma actual del carácter. Sin embargo, si ese motor no está instalado (o no se puede cargar de otro modo), se producirá un error en la llamada (y se producirá un error en el control). A continuación, el servidor intenta cargar otro motor basado en el identificador de idioma, la configuración TTS de carácter compilado y los motores de TTS disponibles. Si todavía no hay ninguna coincidencia, TTS no está disponible para ese cliente, pero el carácter todavía puede hablar en el globo de palabras.

Solo los motores de TTS que usa cualquier cliente permanecen cargados. Por ejemplo, si un carácter tiene una preferencia definida para un motor específico y dicho motor está disponible, pero la aplicación cliente ha especificado un motor diferente (estableciendo el identificador de idioma de un carácter de forma diferente del motor o especificando un identificador de modo diferente), solo el motor especificado por la aplicación permanece cargado. El motor que coincida con la preferencia definida por el carácter para un valor de TTS se descarga (a menos que otro cliente use la configuración del motor compilado del carácter).

 

 




