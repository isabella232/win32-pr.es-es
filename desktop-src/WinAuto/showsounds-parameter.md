---
title: Mostrar sonidos (y marca de descripción de audio)
description: En este tema se incluye información sobre un parámetro que indica si una aplicación debe proporcionar una alerta visual o una indicación cuando usa sonido para transmitir información importante.
ms.assetid: 7b316892-76ff-48b3-bf67-34dea2e63936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbf32dfacdf1dc0b8ed3bc51c986ae572e43300263565254ad6b3a48a981beb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734325"
---
# <a name="show-sounds-and-audio-description-flag"></a>Mostrar sonidos (y marca de descripción de audio)

En este tema se incluye información sobre un parámetro que indica si una aplicación debe proporcionar una alerta visual o una indicación cuando usa sonido para transmitir información importante. También proporciona información sobre una marca que indica si una aplicación debe proporcionar una descripción de audio para los elementos visuales.

## <a name="show-sounds-parameter"></a>Mostrar parámetro de sonidos

El parámetro show sounds indica si el usuario quiere que las aplicaciones presenten toda la información importante en formato visual.

El usuario controla la configuración del parámetro show sounds mediante el Centro de accesibilidad en Panel de control u otra aplicación para personalizar el entorno. Las aplicaciones usan las marcas **\_ SPI GETSHOWSOUNDS** y **SPI \_ SETSHOWSOUNDS** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obtener y establecer el parámetro show sounds. Como alternativa, las aplicaciones pueden usar la marca **\_ SHOW SOUNDS** de SM con la función [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) para determinar el estado del parámetro show sounds.

Determinar el estado del parámetro show sounds solo es necesario para las aplicaciones que normalmente presentarían información importante solo por sonido. Las aplicaciones deben proporcionar compatibilidad para mostrar sonidos si usan sonidos de cualquiera de las maneras siguientes:

-   Para transmitir información que es importante para el funcionamiento de la aplicación.
-   Para avisar al usuario de que se presenta información importante visualmente. Si este es el caso, aunque la información se presenta visualmente, el sonido tiene la función adicional de atraer la atención del usuario.

Los formularios de comentarios visuales adecuados pueden hacer que el software sea mucho más funcional para los usuarios que no pueden confiar en el sonido por sí solos. El diseño de los comentarios visuales es específico de la aplicación y depende de la información que se presentará al usuario. Por ejemplo, para atraer la atención del usuario cuando llega un nuevo correo electrónico, la aplicación podría parpadear en su ventana o incluso en toda la pantalla. Si la aplicación suele hacer sonido para indicar que el usuario está intentando realizar una operación no ilegal, también podría mostrar un mensaje adecuado en su línea de estado o usar la función [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) para mostrar un mensaje de error específico. Si la aplicación está diseñada normalmente para reproducir bits de sonido que tienen significado, como la voz digitalizado, también podría mostrar una ventana de título con el mismo texto.

Se ha demostrado que el uso redundante de alertas visuales y acústicas aumenta la facilidad de uso de las aplicaciones de software. El parámetro show sounds es una solicitud de comentarios visuales, pero su uso no restringe una aplicación a la presentación visual de información. Los usuarios deben poder solicitar comentarios visuales, independientemente de si también desean comentarios sonaundos.

## <a name="audio-description-flag"></a>Marca de descripción de audio

Las aplicaciones usan **las \_ marcas SPI GETAUDIODESCRIPTION** y **SPI \_ SETAUDIODESCRIPTION** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para habilitar o deshabilitar las descripciones de audio. Aunque es posible que los usuarios con discapacidades visuales puedan escuchar el audio en el contenido del vídeo, hay una gran cantidad de acciones en el vídeo que no tienen el audio correspondiente. La descripción de audio específica de lo que sucede en un vídeo ayuda a estos usuarios a comprender mejor el contenido. Esta marca le permite habilitar o deshabilitar las descripciones de audio en los idiomas en los que se proporcionan.

 

 