---
title: Compatibilidad con voz sintetizada
description: Compatibilidad con voz sintetizada
ms.assetid: 38172e04-a5b6-41e4-9d7c-539d9d4117be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c31fcb655ccb5a8fbb2ffbbb8d01d1da317209fbfa3e270a76d92208c06777df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475327"
---
# <a name="synthesized-speech-support"></a>Compatibilidad con voz sintetizada

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Si usa voz sintetizada, el carácter tiene la capacidad de decir casi cualquier cosa, lo que proporciona la máxima flexibilidad. Con el audio grabado, puede dar al carácter una voz específica o única. Para especificar la salida, proporcione el texto hablado como parámetro del [**método Speak.**](speak-method.md)

Dado que la arquitectura de Microsoft Agent usa Microsoft SAPI para la salida de voz sintetizada, puede usar cualquier motor que se ajuste a esta especificación y admita la salida del alfabeto fonético internacional (IPA) mediante el método [**Visual**](https://www.bing.com/search?q=**Visual**) de la interfaz [**ITTSNotifySinkW.**](ittsnotifysinkw.md) Para obtener más información sobre los requisitos del motor, consulte [Requisitos de compatibilidad del motor de voz.](requirements-for-text-to-speech-engines.md)

La configuración del identificador de idioma de un carácter determina su salida de TTS. Si un cliente no especifica un identificador de idioma para el carácter, el identificador de idioma del carácter se establece en el identificador de idioma predeterminado del usuario. Si la definición del carácter incluye un motor específico y ese motor se puede cargar y coincide con la configuración de idioma del carácter, se usará ese motor. De lo contrario, Microsoft Agent enumera los demás motores disponibles y solicita la mejor coincidencia de SAPI en función del idioma, el sexo y la edad (en ese orden). Si no hay ningún motor de coincidencia disponible, no hay ninguna salida de TTS para el uso del carácter por parte de ese cliente. El agente intenta cargar el motor de TTS en la primera llamada [**a Speak**](speak-method.md) o cuando consulta o establece correctamente su identificador de modo.

Una aplicación cliente también puede especificar un motor de TTS para su carácter (mediante la [**propiedad TTSModeID).**](ttsmodeid-property.md) Esto invalida el intento del servidor de encontrar automáticamente un motor de coincidencia en función del identificador de modo TTS preferido del carácter o de la configuración del identificador de idioma actual del carácter. Sin embargo, si ese motor no está instalado (o no se puede cargar de otro modo), se producirá un error en la llamada (y se producirá un error en el control ). A continuación, el servidor intenta cargar otro motor en función del identificador de idioma, la configuración de TTS de caracteres compilados y los motores de TTS disponibles. Si todavía no hay ninguna coincidencia, TTS no está disponible para ese cliente, pero el carácter todavía puede hablar en su globo de palabras.

Solo los motores de TTS que usa cualquier cliente permanecen cargados. Por ejemplo, si un carácter tiene una preferencia definida para un motor específico y ese motor está disponible, pero la aplicación cliente ha especificado un motor diferente (estableciendo el identificador de idioma de un carácter de forma diferente al motor o especificando un identificador de modo diferente), solo el motor especificado por la aplicación permanece cargado. Se descarga el motor que coincide con la preferencia definida del carácter para una configuración de TTS (a menos que otro cliente use la configuración del motor compilado del carácter).

 

 




