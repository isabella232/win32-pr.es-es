---
title: Interfaz de usuario de la ventana MCIWnd
description: Interfaz de usuario de la ventana MCIWnd
ms.assetid: 422c5acb-bce5-4be2-96ba-5ab7f9dcc826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98c0b11b6868828625c6c6e605f005fe842d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075338"
---
# <a name="mciwnd-window-user-interface"></a>Interfaz de usuario de la ventana MCIWnd

MCIWnd proporciona características adicionales para ajustar la apariencia de la ventana de MCIWnd, personalizar el comportamiento de la aplicación y optimizar el rendimiento de la reproducción. En la ventana de MCIWnd se incluyen las siguientes características:

-   Barra de herramientas con botones **reproducir**, **detener**, **grabar** y **menú**
-   Barra de control que controla el posicionamiento del contenido de reproducción.
-   Menú emergente que contiene comandos comunes
-   Un área de reproducción para vídeo y otros dispositivos que muestran imágenes

En la ilustración siguiente se muestra el estado inicial de la reproducción de vídeo controlada por el usuario. El archivo de ejemplo utilizado es CLOCK.AVI.

![Imagen de clock.avi](images/mciwnd1.gif)

La ventana MCIWnd incluye un área de reproducción para vídeo y otros dispositivos que muestran imágenes durante la reproducción. MCIWnd omite el área de reproducción de los dispositivos de audio de onda, secuenciadores MIDI y otros dispositivos que no escriben en la pantalla. En la ilustración siguiente se muestra el área de reproducción de audio de onda.

![imagen de la ventana de mciwnd](images/mciwnd4.gif)

El botón **reproducir** se encuentra en la esquina inferior izquierda de la ventana MCIWnd. Aparece cuando se detiene el contenido. El usuario puede reproducir el contenido de las maneras siguientes:

-   Para reproducir el contenido desde la posición de reproducción actual, seleccione el botón **reproducir** .
-   Para reproducir el contenido a pantalla completa desde la posición de reproducción actual, seleccione el botón **reproducir** mientras mantiene presionada la tecla Ctrl.
-   Para reproducir el contenido hacia atrás desde la posición de reproducción actual, seleccione el botón **reproducir** mientras mantiene presionada la tecla Mayús.

El botón de **menú** , situado junto al botón **reproducir** , activa un menú que permite al usuario abrir y cerrar archivos de audio y vídeo intercalados (AVI), y ajustar el tamaño de la imagen, la velocidad de reproducción y el volumen. (El usuario también puede activar el menú haciendo clic con el botón secundario del mouse siempre que el cursor se encuentra en el área cliente de la ventana). El menú también incluye comandos para cambiar la configuración del dispositivo actual, copiar el contenido de reproducción en el portapapeles y emitir comandos MCI.

La barra de menús a la derecha del botón de **menú** representa la duración del contenido de reproducción (o grabado). El control deslizante de la barra de desplazamiento representa la posición de reproducción actual dentro del contenido. Cuando el control deslizante se coloca en el extremo izquierdo de la barra de desplazamiento, la posición de reproducción actual es el principio del contenido. El usuario puede desplazarse a diferentes ubicaciones del contenido arrastrando el control deslizante a lo largo de la barra de desplazamiento. El botón **detener** se encuentra en la esquina inferior izquierda de la ventana MCIWnd. Aparece cuando se reproduce el contenido. En la ilustración siguiente se muestra la reproducción de vídeo en curso.

![imagen de reproducción de vídeo](images/mciwnd2.gif)

Los controles de MCIWnd también pueden incluir un botón de **registro** para los dispositivos que pueden grabar. El botón **grabar** está marcado con un círculo rojo y solo aparece cuando el dispositivo es capaz de grabar.

> [!Note]  
> La ventana de reproducción debe estar alineada en un límite de cuatro píxeles para obtener el mejor rendimiento de reproducción de vídeo. Normalmente, Windows alinea la ventana automáticamente cuando se crea. Si un usuario mueve o estira la ventana desde su posición inicial, la velocidad de reproducción de vídeo podría reducirse a la mitad.

 

 

 




