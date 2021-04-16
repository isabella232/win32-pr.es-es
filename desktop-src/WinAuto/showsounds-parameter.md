---
title: Mostrar sonidos (y marca de descripción de audio)
description: En este tema se incluye información sobre un parámetro que indica si una aplicación debe proporcionar una alerta o una indicación visual cuando se utiliza un sonido para transmitir información importante.
ms.assetid: 7b316892-76ff-48b3-bf67-34dea2e63936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d01e3fda902c23c86279a9a4d75889ebfeff4d55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695678"
---
# <a name="show-sounds-and-audio-description-flag"></a>Mostrar sonidos (y marca de descripción de audio)

En este tema se incluye información sobre un parámetro que indica si una aplicación debe proporcionar una alerta o una indicación visual cuando se utiliza un sonido para transmitir información importante. También proporciona información sobre una marca que indica si una aplicación debe proporcionar una descripción de audio para los elementos visuales.

## <a name="show-sounds-parameter"></a>Mostrar parámetro de sonidos

El parámetro Mostrar sonidos indica si el usuario desea que las aplicaciones presenten toda la información importante en el formulario visual.

El usuario controla el valor del parámetro Mostrar sonidos mediante el centro de accesibilidad del panel de control u otra aplicación para personalizar el entorno. Las aplicaciones usan las marcas **SPI \_ GETSHOWSOUNDS** y **SPI \_ SETSHOWSOUNDS** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obtener y establecer el parámetro show Sounds. Como alternativa, las aplicaciones pueden usar la marca del **SM \_ SHOWSOUNDS** con la función [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) para determinar el estado del parámetro show Sounds.

La determinación del estado del parámetro show Sounds solo es necesaria para las aplicaciones que normalmente presentarían información importante solo por sonido. Las aplicaciones deben proporcionar compatibilidad para mostrar sonidos si utilizan sonidos de una de las siguientes maneras:

-   Transmitir información que es importante para el funcionamiento de la aplicación.
-   Para avisar al usuario de que la información importante se presenta visualmente. Si este es el caso, aunque la información se presente visualmente, el sonido tiene la función adicional de atraer la atención del usuario.

Los formularios de comentarios visuales adecuados pueden hacer que el software sea mucho más funcional para los usuarios que no pueden confiar solo en el sonido. El diseño de los comentarios visuales es específico de la aplicación y depende de la información que se presentará al usuario. Por ejemplo, para atraer la atención del usuario cuando llega un correo electrónico nuevo, es posible que la aplicación parpadee su ventana o incluso parpadee la pantalla completa. Si, por lo general, la aplicación hace sonar para indicar que el usuario está intentando realizar una operación no válida, también podría mostrar un mensaje apropiado en su línea de estado o utilizar la función [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) para mostrar un mensaje de error específico. Si, por lo general, la aplicación está diseñada para reproducir una pantalla de sonido que lleve significado, como la voz digitalizada, también podría mostrar una ventana de título con el mismo texto.

Se ha mostrado el uso redundante de alertas sonoras y visuales para aumentar la facilidad de uso de las aplicaciones de software. El parámetro show Sounds es una solicitud de comentarios visuales, pero su uso no impide que una aplicación presente la información visualmente. Los usuarios deben poder solicitar comentarios visuales independientemente de si también quieren recibir comentarios auditivos.

## <a name="audio-description-flag"></a>Marca de descripción de audio

Las aplicaciones usan las marcas **SPI \_ GETAUDIODESCRIPTION** y **SPI \_ SETAUDIODESCRIPTION** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para habilitar o deshabilitar las descripciones de audio. Aunque es posible que los usuarios con discapacidades visuales escuchen el audio en el contenido de vídeo, hay una gran cantidad de acciones en vídeo que no tienen el audio correspondiente. Una descripción de audio específica de lo que ocurre en un vídeo ayuda a estos usuarios a comprender mejor el contenido. Esta marca permite habilitar o deshabilitar las descripciones de audio en los idiomas en los que se proporcionan.

 

 