---
title: Ventana Opciones avanzadas de caracteres (ventana Comandos de voz)
description: Obtenga información sobre la ventana Opciones avanzadas de caracteres, que proporciona opciones para que los usuarios ajusten su interacción con todos los caracteres.
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1b5ce1bc7cb42dc03fd35edbbaa6626f19389b0fd72bd507590ad1989d111c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715865"
---
# <a name="advanced-character-options-window-voice-commands-window"></a>Ventana Opciones avanzadas de caracteres (ventana Comandos de voz)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

La ventana Opciones avanzadas de caracteres proporciona opciones para que los usuarios ajusten su interacción con todos los caracteres. Por ejemplo, los usuarios pueden deshabilitar la entrada de voz o cambiar los parámetros de entrada. Los usuarios también pueden cambiar la configuración de salida del globo de palabras. Esta configuración invalida cualquier conjunto de una aplicación cliente o un conjunto como parte de la definición de caracteres. La aplicación no puede cambiar ni deshabilitar estas opciones, ya que se aplican a las preferencias generales del usuario para el funcionamiento de todos los caracteres. Sin embargo, el servidor notificará a la aplicación ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) cuando el usuario cambie y aplique una opción. También puede mostrar o cerrar la ventana mediante la propiedad [**Visible**](visible-property.md) de la ventana y acceder a su ubicación a través de sus [**propiedades Superior**](top-property.md) [**e**](left-property.md) Izquierda.

Además de admitir la animación de un carácter, Microsoft Agent admite la salida de audio del carácter. Esto incluye la salida hablada y los efectos de sonido. En el caso de la salida hablada, el servidor sincroniza automáticamente las imágenes definidas del carácter con la salida. Puede elegir la síntesis de texto a voz (TTS), el audio grabado o solo la salida de texto de globo de palabras.

 

 




