---
title: Ventana Opciones de carácter avanzadas (ventana comandos de voz)
description: La ventana Opciones de carácter avanzadas
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f481871d3861da99b54829e5c6e1b34c9137060a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359592"
---
# <a name="advanced-character-options-window-voice-commands-window"></a>Ventana Opciones de carácter avanzadas (ventana comandos de voz)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

La ventana Opciones de carácter avanzadas proporciona opciones para que los usuarios ajusten su interacción con todos los caracteres. Por ejemplo, los usuarios pueden deshabilitar la entrada de voz o cambiar los parámetros de entrada. Los usuarios también pueden cambiar la configuración de salida del globo de palabras. Estas opciones invalidan cualquier conjunto de una aplicación cliente o se establecen como parte de la definición de caracteres. La aplicación no puede cambiar o deshabilitar estas opciones porque se aplican a las preferencias de usuario generales para el funcionamiento de todos los caracteres. Sin embargo, el servidor notificará a la aplicación ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) cuando el usuario cambie y aplique una opción. También puede mostrar o cerrar la ventana con la propiedad [**visible**](visible-property.md) de la ventana y acceder a su ubicación a través de sus propiedades [**superior**](top-property.md) e [**izquierda**](left-property.md) .

Además de admitir la animación de un carácter, Microsoft Agent admite la salida de audio para el carácter. Esto incluye la salida hablada y los efectos sonoros. En el caso de la salida de voz, el servidor automáticamente sincroniza las imágenes de la boca definidas del carácter con la salida. Puede seleccionar síntesis de texto a voz (TTS), audio grabado o solo texto de globo de palabras.

 

 




